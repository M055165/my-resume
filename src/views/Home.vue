<template>
<div>
    <div v-if="navActive == 'contact'" class="bg_img2"></div>
    <div v-else class="bg_img1"></div>
  
    <!-- Nav區 -->
    <mynav @burgerClick="burgerClick"></mynav>
    <!-- Header區 -->
    <myheader :burgerFlag='burgerFlag'></myheader>
    <!-- About區 -->
    <about :aboutShow='aboutShow'></about>
    <!-- Skills區 -->
    <skills></skills>
    <!-- Projects區 -->
    <projects></projects>
    <!-- experience區 -->
    <experience></experience>
    <!-- contact區 -->
    <contact></contact>
    <!-- footer區 -->
    <myfooter></myfooter>
</div>
</template>

<style lang="scss">
body {
    font-family: 'Noto Sans TC', sans-serif;
}

.bg_img1 {
    background-image: url('../assets/top.jpg');
    background-size: cover;
    background-position: center center;
    width: 100vw;
    height: 100vh;
    position: fixed;
    z-index: -100;
    filter: blur(3px);
}
.bg_img2 {
   background-image: url('../assets/contact.jpeg');
    background-size: cover;
    background-position: center center;
    width: 100vw;
    height: 100vh;
    position: fixed;
    z-index: -100;
    filter: blur(3px);
}
</style>

<script>
import mynav from '../components/navbar'
import myheader from '../components/Header'
import about from '../components/About'
import skills from '../components/Skills'
import projects from '../components/Projects'
import experience from '../components/Experience'
import contact from '../components/Contact'
import myfooter from '../components/Footer'
export default {
    data() {
        return {
            burgerFlag: false,
            viewprotH: 0,
            viewprotW: 0,
            windowH: 0,
            skillDispaly: 'list',
            works_modal: {},
            navLinksH: {},
        }
    },
    components: {
        mynav,
        myheader,
        about,
        skills,
        projects,
        experience,
        contact,
        myfooter
    },
    methods: {
        burgerClick() {
            this.burgerFlag = !this.burgerFlag
        }
    },
    computed: {
        aboutShow() {
            const vm = this;
            if (vm.viewprotH > (vm.navLinksH.about - vm.windowH/3)) {
                return true;
            } else {
                return false;
            }
        },
         navActive() {
        const vm = this;
        let acitve = '';
        if (vm.viewprotH +1500 > vm.navLinksH.contact) {
          acitve = 'contact';
        } else if (vm.viewprotH + 605 > vm.navLinksH.experience) {
          acitve = 'experience';
        } else if (vm.viewprotH + 605 > vm.navLinksH.works) {
          acitve = 'works';
        } else if (vm.viewprotH + 605 > vm.navLinksH.skill) {
          acitve = 'skill';
        } else if (vm.viewprotH + 605 > vm.navLinksH.about) {
          acitve = 'about';
        } else {
          acitve = '';
        }
        return acitve;
      },
    },
    mounted() {
    const vm = this;
      const about = document.querySelector('#about');
      const skill = document.querySelector('#skills');
      const works = document.querySelector('#projects');
      const experience = document.querySelector('#experience');
      const contact = document.querySelector('#contact');
      vm.viewprotW = window.outerWidth;
      vm.windowH = window.outerHeight;
       //紀錄視窗寬度
      window.addEventListener("resize", function () {
        vm.viewprotW = window.outerWidth;
        vm.windowH = window.outerHeight;
      });

        window.addEventListener("scroll", function () {
        vm.viewprotH = window.pageYOffset;
        vm.navLinksH.about = about.offsetTop;
        vm.navLinksH.skill = skill.offsetTop;
        vm.navLinksH.works = works.offsetTop;
        vm.navLinksH.experience = experience.offsetTop;
        vm.navLinksH.contact = contact.offsetTop;
        console.log(vm.viewprotH)
        console.log(vm.navLinksH.contact) 

        });
    }
}
</script>
