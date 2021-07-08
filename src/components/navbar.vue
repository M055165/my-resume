<template>
<nav :class="{'hidden':!burgerFlag}">
    <div class="logo">
        <router-link to="/">
            <i class="far fa-folder-open mr-2"></i>Eddie's Resume
        </router-link>
    </div>
    <ul class="nav-links" :class="{'navactive':burgerFlag}">
        <li><a href="#about">About me</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#experience">Experience</a></li>
        <li><a href="#contact">Contact</a></li>
    </ul>
    <div class="burger" :class="{'toggle':burgerFlag}" @click="burgerClick">
        <div class="line1"></div>
        <div class="line2"></div>
        <div class="line3"></div>
    </div>
</nav>
</template>

<script>
export default {
    data() {
        return {
            modalFlag: false,
            burgerFlag: false,
            account: '',
            loginFlag: false
        };
    },
    methods: {
        burgerClick() {
            this.burgerFlag = !this.burgerFlag
            this.$emit('burgerClick')
        },

    },
    created() {
        this.account = sessionStorage.getItem('account')
        if (this.account) {
            this.loginFlag = true
        }
    },
};
</script>

<style lang="scss" scoped>
$white:rgb(226, 226, 226);

li,
a,
router-link {
    color:white;
    cursor: pointer;
    text-decoration: none;

}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-weight: bold;
}

img {
    width: 100px;
}

.app {
    // height: 60vh;
    // background-image: url("https://images8.alphacoders.com/553/thumb-1920-553032.jpg");
    // background-position: center center;
    // background-size: cover;
    // background-repeat: no-repeat;
}

.hidden {
    overflow: hidden !important;
}

nav {
    width: 100vw;
    display: flex;
    justify-content: space-around;
    align-items: center;
    min-height: 10vh;
    position: absolute;
}

.logo {
    text-transform: uppercase;
    letter-spacing: 3px;
    font-size: 22px;
}

.nav-links {
    display: flex;
    width: 30%;
    justify-content: space-around;
}

.nav-links li {
    list-style: none;
}

.nav-links a {
    color: $white;
    text-decoration: none;
    letter-spacing: 3px;
    font-weight: bold;
    font-size: 14px;
}

.burger {
    display: none;
    cursor: pointer;
}

.burger div {
    width: 25px;
    height: 3px;
    margin: 5px;
    background-color: $white;
}

@media screen and (max-width: 1024px) {
    .nav-links {
        width: 60%;
    }
}

@media screen and (max-width: 767px) {
    .nav-links {

        position: absolute;
        right: 0;
        height: 30vh;
        top: 10vh;
        display: flex;
        flex-direction: column;
        align-items: center;
        border: 0;
        width: 45%;
        transform: translateX(100%);
        transition: all .4s ease-in;
        z-index: 99;
    }

    .nav-links a {
        font-weight: bold;
        color: black;
    }

    .burger li {
        opacity: 0;
    }

    .burger {
        display: block;
    }
}

.navactive {
    transform: translateX(0);
}

.toggle .line1 {
    transform: rotate(-45deg) translate(-5px, 6px);
}

.toggle .line2 {
    opacity: 0;
}

.toggle .line3 {
    transform: rotate(45deg) translate(-5px, -6px);
}
</style>
