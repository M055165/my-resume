<template>
<header >
    <div class="container">
        <div class="row" >
            <div class="col-md-6 header_img" :class="{'mt300':burgerFlag}">
                <div class="header_bg"></div>
            </div>
            <div class="col-md-6 header_txt">
                <h1>Hello I'm Eddie</h1>
                <h1>Welcome to my website!</h1>
            </div>
        </div>
    </div>
</header>
</template>

<style lang="scss">
header {
    min-height:100vh ;
    width: 100vw;
    overflow: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
}

.header_img,
.header_txt {
    display: flex;
    align-items: center;
    justify-content: center;
}

.header_img {
    margin-top: 0px;
    transition: all .4s ease-in;
}

.header_txt {
    display: flex;
    flex-direction: column;

    h1 {
        text-shadow: 3px 3px 6px #000000;
        letter-spacing: 3px;
        color: white;
    }
}

.header_bg {
    width: 400px;
    height: 400px;
    border-radius: 100%;
    border: rgb(255, 255, 255) 10px solid;
    background-image: url("../assets/398081.jpg");
    background-size: cover;
    background-position: center center;
}

.mt300 {
    transition: all .4s ease-in;
    margin-top: 300px;
}

.h100 {
    min-height: 100vh;
}

@media screen and (max-width: 768px) {
    header {
        min-height: 85vh;
    }
    .header_txt {
        margin-top: 50px;

        h1 {
            font-size: 18px;
        }
    }

    .header_bg {
        width: 300px;
        height: 300px;
    }

}
</style>

<script>
export default {
    props: ['burgerFlag'],
    
}
</script>
