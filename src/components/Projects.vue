<template>
<div id="projects">
    <div class="container">
        <div class="header">
            <h1>Projects</h1>
            <div class="hr mt-4">
                <i class="fas fa-user"></i>
            </div>
        </div>
        <ul class="projects">
            <div class="row">
                <li class="projects_item  col-md-6 col-lg-6" v-for='(item,index) in projects' :key="index">
                    <div class="projects_item_pic" @click="modalClick(index)" :style="{ backgroundImage: `url(${item.imgUrl})`}">
                    </div>
                    <p class="projects_item_title">
                        {{item.title}}
                    </p>
                </li>

            </div>

        </ul>

        <div class="mymodal" v-if="modalFlag">
            <div class="container">
                <div class="modal_header">
                    <h2>{{projects[projectsIndex].title}}</h2>
                    <a @click.prevent="modalClick(index)"><i class="fas fa-times"></i></a>
                </div>
                <video src="../assets/demo.mp4" controls class="demo" v-if="projectsIndex==3"></video>
                <img class="modal_pic mt-3" :src="projects[projectsIndex].imgUrl" alt="" v-if="projectsIndex!=3">
                <ul class="modal_text">
                    <li v-for="(item,index) in projects[projectsIndex].content" :key="index">
                        {{item}}
                    </li>
                </ul>
                <div class="projects_links">
                    <a class="projects_button"  :href="projects[projectsIndex].href">點擊我進入專案</a>
                </div>
            </div>

        </div>
    </div>

</div>
</template>

<style lang="scss" scoped>
#projects {
    text-decoration: none;
    padding-top: 60px;
    padding-bottom: 30px;
    width: 100vw;
    background-image: url("https://images.pexels.com/photos/326311/pexels-photo-326311.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940");
    background-size: cover;
    background-position: center center;
    color: white;
    font-size: 20px;
    font-weight: bold;
    text-shadow: 3px 3px 6px #000000;
    position: relative;
}
a {
    text-decoration: none;
}
.header {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    letter-spacing: 3px;

    .hr {
        margin-top: 10px;
        width: 100%;
        height: 5px;
        background-color: #dcdcdc;
        display: flex;
        justify-content: center;
        align-items: center;
        color: #004B97;
        font-size: 40px;
        filter: blur(1px);

    }
}

.projects {
    padding: 100px 0 0px 0;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    list-style: none;
}
.row{
    width: 80%;
}

.projects_item {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-bottom: 20px;
    perspective: 1000px;

    .projects_item_pic {
        width: 90%;
        margin: 10px 3px;
        height: 200px;
        background-image: url("../assets/works/mymovie.png");
        background-size: cover;
        background-position: center;
        box-shadow: 0px 16px 14px 2px rgba(0, 0, 0, 0.438);
        transition: all 0.4s;
        transform-style: preserve-3d;
        transform: rotatex(30deg);
        &:hover {
            transform: scale(1.1, 1.1);
        }
    }
    .projects_item_title {
        letter-spacing: 1.2px;
        font-size: 24px;
        margin-top: 20px;
    }
}

.mymodal {
    margin-top: 100px;
    width: 50%;
    z-index: 999;
    background-color: rgba(#003060, 1);
    height: 500px;
    overflow: auto;
    position: fixed;
    left: 50%;
    top: 0%;
    transform: translateX(-50%);
    border-radius: 10px;
    border:10px solid #dcdcdc;
    .modal_header {
        margin: 15px 0;
        display: flex;
        justify-content: space-between;
        align-items: center;
        color: white;
        h2 {
            font-size: 25px;
        }
        a {
            font-size: 30px;
            color: #dcdcdc;
            cursor: pointer;
        }
    }
    img {
        width: 100%;
    }
    .modal_text {
        font-weight: normal;
        padding: 30px;
        font-size: 18px;
        li {
            margin-top: 15px;
        }
    }
}
.projects_links{
    width: 100%;
    display: flex;
    justify-content: center;
    margin-bottom: 30px;
    .projects_button{
        background-color: transparent;
        color: white;
        border:1px solid white;
        padding: 20px;
        border-radius: 30px;
        
    }
}
.demo{
    margin-left:30%;
    height: 450px;
}
@media screen and (max-width: 767px) {
    .mymodal {
        width: 95vw;
    }
    .demo{
    margin-left:20%;
    height: 450px;
}
}
</style>

<script>
export default {
    data() {
        return {
            modalFlag: false,
            projectsIndex:0,
             projects: [
             {
            title: 'Vue電商平台',
            imgUrl: 'https://firebasestorage.googleapis.com/v0/b/my-resume-f5266.appspot.com/o/vue-shopping.png?alt=media&token=928af636-181f-4b53-b7f2-4a9c7afac51d',
            href: 'https://m055165.github.io/vue-shopping/',
            content: [
              '前端框架使用Vue.js 搭配Vue router、Vue cli3 等技術',
              '使用 Axios 串接 Node.js 來達到前後端分離',
              '使用 Bootstrap4、SASS 製作 RWD 網頁',
              '配合成教系的專業來打造屬於高齡者的購物網站',
            ],
          },
          {
            title: 'Vue電影訂票系統',
            imgUrl: 'https://firebasestorage.googleapis.com/v0/b/my-resume-f5266.appspot.com/o/mymovie.png?alt=media&token=ea51cf5d-d0e9-482d-aa16-fc7993eed983',
            href: 'https://m055165.github.io/mymovie/',
            content: [
              '前端框架使用Vue.js 搭配Vue router、Vue cli3 等技術',
              '後端使用node.js 資料庫使用Mysql',
              '使用 Axios 串接 Node.js 來達到前後端分離',
              '使用 Bootstrap4、SASS 製作 RWD 網頁',
            ],
          },
          {
            title: '水庫即時雨量',
            imgUrl: 'https://firebasestorage.googleapis.com/v0/b/my-resume-f5266.appspot.com/o/vue-reservoir.png?alt=media&token=976f9749-3d2e-452e-bee5-d3c6d462c07c',
            href: 'https://m055165.github.io/vue-reservoir/',
            content: [
              '透過製作網頁來時時關心台灣的水庫',
              '使用 Bootstrap4、SASS 製作 RWD 網頁',
              '前端框架使用Vue.js 搭配Vue router、Vue cli3 等技術',
              '透過Axios來串結政府的公開Api',
            ],
          },
          {
            title: '阿里山草藥辨識App',
            imgUrl: 'https://firebasestorage.googleapis.com/v0/b/my-resume-f5266.appspot.com/o/ic_logo.png?alt=media&token=c3c55833-c716-4b3e-a02a-4c60236c4f34',
            href: 'https://github.com/M055165/identificationApp',
            content: [
              '中正大學畢業專題(系展第一名',
              '前端使用Flutter 後端使用Node.js 資料庫使用Mysql',
              '透過Pytorch來辨識草藥總類及其資訊'
            ],
          },
          
        ],
        }
    },
    methods: {
        modalClick(index) {
            this.modalFlag = !this.modalFlag;
            this.projectsIndex = index
        },
        toProjects(index){
            console.log(this.projects[index]['href'])
            this.$router.replace(`${this.projects[index]['href']}`)
            console.log('dksmk')
        }
    }
}
</script>
