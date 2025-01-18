<template>
    <nav>
        <label class="logo" @click="logoClick" />
        <input id="check" type="checkbox">
        <label for="check" class="checkbtn">
            <v-icon icon="$menu"></v-icon>
        </label>
        <ul class="navbar_item">
            <!-- <li><a href="/news" target="_self">NEWS</a></li>
            <li><a href="/software" target="_self">RESUME</a></li>
            <li><a href="/system" target="_self">WORKS</a></li>
            <li><a href="/sales" target="_self">TESTIMONIALS</a></li>
            <li><a href="/ctc" target="_self">CONTACT</a></li> -->
        </ul>
    </nav>
</template>


<script>

/*
頁面:navbar組件
邏輯:navbar組件，點擊item 可以跳轉到各個頁面
*/

export default {
    data() {
        return {
            navData: []
        }
    },
    methods: {
        // 點擊力麗科技logo 跳轉到公司首頁
        logoClick() {
            this.$router.push("/");
        },
        // Call Web api 獲得navbar list

    }
};
</script>

<style lang="scss" scoped>
* {
    padding: 0;
    margin: 0;
    text-decoration: none;
    list-style: none;
    box-sizing: border-box;
}

body {
    font-family: montserrat;
}

nav {
    position: fixed;
    top: 0;
    z-index: 9000000;
    background-color: transparent;
    height: 100px;
    width: 100%;
    white-space: nowrap;

    // border-bottom: 1px solid #dcdcdc;
    // margin-bottom: 100px;
}

label.logo {
    width: 200px;
    height: 100px;
    line-height: 100px;
    font-weight: bold;
    color: white;
    background-image: url("https://www.llt.com.tw/_nuxt/img/logo.552c770.svg") !important;
    background-size: contain;
    background-position: center center;
    background-repeat: no-repeat;
    cursor: pointer;
    margin-left: 10px;
}

nav ul {
    top: 100px;
    margin-right: 10px;
    float: right;
    white-space: nowrap;
    text-align: center;
}





nav ul li {
    display: inline-block;
    line-height: 100px;
    margin: 0 10px;
}

nav ul li a {
    text-transform: uppercase;
    font-size: 14px;
    letter-spacing: 2px;
    color: white;
    font-weight: bold;

    &:hover {
        color: #0095eb
    }
}

.checkbtn {
    font-size: 30px;
    color: black;
    float: right;
    line-height: 100px;
    margin-right: 40px;
    cursor: pointer;
}

#check {
    display: none;
}

.checkbtn {
    display: none;
}


@media screen and (min-width: 768px) {
    nav ul {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        text-align: center;
    }


}

@media screen and (max-width: 952px) {
    label.logo {
        font-size: 30px;
    }

    nav ul li a {
        font-size: 16px;
    }
}

@media screen and (max-width: 1100px) {
    .checkbtn {
        display: block;
    }

    .check1btn {
        display: block;
    }

    ul {
        position: fixed;
        width: 100%;
        background: #2c3e50;
        top: 0;
        left: -100%;
        height: calc(100vh - 100px);
        text-align: center;
        z-index: 999;
        transition: all 0.5s;
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
    }

    nav ul li {
        display: block;
        display: flex;
        justify-content: center;
        align-items: center;
        line-height: 0px;

    }

    nav ul li a {
        font-size: 20px;
        color: white;
    }

    a:hover {
        background: none;
        color: #0082e6;
    }

    #check:checked~ul {
        left: 0;
    }
}
</style>