<template>
<div id="about">
    <div class="container">
        <div class="header">
            <h1>About me</h1>
            <div class="hr mt-4">
                <i class="fas fa-user"></i>
            </div>
        </div>
        <div class="container">
            <div class="row" :class="{'active':aboutShow}">
                <div class="col-md-6 content_img">
                </div>
                <div class="col-md-6 content_text">
                    <div class="text_box">
                        <p>您好！我叫做 蔡竣智</p>
                        <p>我畢業於國立中正大學資管系以及成人及繼續教育學系雙學位，隨著隨著台灣高齡化的現象越來越嚴重，
                            台灣也在2018年正式進入高齡社會，2020年超高齡(85歲以上)人口占老年人口10.3%，2070年預估增長至27.4%。
                            因此有關老年的產業也日漸發達，我曾經也以為我未來可能會就進入老年的產業，但是就在2018年的暑假我因緣際會的接觸到了程式，因而正式踏入軟體工程這個領域！</p>
                        <p>2018年決定申請雙主修資管系，在學校的課程中學會了JAVA、C言語、Mysql以及資料結構等等......</p>
                        <p>2018年也時因為課程的需要，正式踏入前端這令人又愛又恨的領域，透過學校的課程以及翻書、線上課程也學會了各式各樣的前端技能。</p>
                        <p>目前完成的專案有：</p>
                        <p>1.線上商購商城</p>
                        <p>2.電影訂票係統</p>
                        <p>3.草藥辨識App(學校專題）</p>
                    </div>
                </div>
            </div>
        </div>

    </div>
</div>
</template>

<style lang="scss" scoped>
#about {
    padding-top: 60px;
    padding-bottom: 60px;
    width: 100vw;
    background-image: url("https://cdn.pixabay.com/photo/2021/01/25/18/38/storm-5949243_960_720.jpg");
    background-size: cover;
    background-position: center center;
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
}

h1 {
    color: white;
    text-shadow: 3px 3px 6px #000000;
}

.row {
    padding-top: 50px;
}

.content_img {
    height: 400px;
    background-image: url('../assets/398085.jpg');
    background-position: center center;
    background-size: cover;
    box-shadow: 10px 12px 18px 0 rgba(0, 0, 0, 0.438),
        -10px 12px 18px 0 rgba(0, 0, 0, 0.411);
}

.content_text {
    .text_box {
        padding: 20px;
        border-radius: 10px;
        background-color:rgba($color:  #00AEAE, $alpha: 0.6);
        color:white;
        letter-spacing: 2.0px;
        text-shadow: 3px 3px 6px #000000;
        line-height: 1.5;
    }
}
.row {
    opacity: 0;
    transition: all 1s;
}
.active {
    opacity: 1;
    transform: translate(0, 0);
}

@media screen and (max-width: 767px) {
    .col-md-6 {
        padding: 0px !important;
    }

    .content_img {
        height: 270px;
    }

    .content_text {
        margin-top: 30px;
    }
}
</style>

<script>
export default {
    props:['aboutShow']
}
</script>