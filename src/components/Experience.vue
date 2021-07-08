<template>
<div id="experience">
    <div class="container">
        <div class="header">
            <h1>Experience</h1>
            <div class="hr mt-4">
                <i class="fas fa-user"></i>
            </div>
        </div>
        <div class="content">
            <div class="container">
                <div class="row">
                    <div class="col-md-3 content_img">
                        <div class="img_box">
                          <img class="img_pattern" src="../assets/experience/001-school.png" alt="">
                          <div class="line">

                          </div>
                        </div>

                    </div>
                    <div class="col-md-8 content_text">
                      <h4>成人及繼續教育學系｜國立中正大學｜<i class="far fa-clock mr-2"></i>2017/09/01</h4>
                      <p>透過高中的升學管道，進到國立中正大學就讀。</p>
                    </div>
                </div>
                 <div class="row">
                    <div class="col-md-3 content_img">
                        <div class="img_box">
                          <img class="img_pattern" src="../assets/experience/003-coding.png" alt="">
                          <div class="line">

                          </div>
                        </div>

                    </div>
                    <div class="col-md-8 content_text">
                      <h4>資訊管理學系｜國立中正大學｜<i class="far fa-clock mr-2"></i>2018/09/01</h4>
                      <p>透過這一年在學校、營隊的探索，決定要申請雙主修資管系，培養第二專長以及增加自己的競爭力</p>
                    </div>
                </div>
                 <div class="row">
                    <div class="col-md-3 content_img">
                        <div class="img_box">
                          <img class="img_pattern" src="../assets/experience/002-graduation-hat.png" alt="">
                          
                        </div>

                    </div>
                    <div class="col-md-8 content_text">
                       <h4>畢業｜國立中正大學｜<i class="far fa-clock mr-2"></i>2018/09/01</h4>
                      <p>經過四年的努力，終於如願在四年內拿到國立中正大學資管以及成人及繼續教育學系雙學位，邁入人生的下一個里程碑。</p>
                    </div>
                </div>
                
                  

            </div>
        </div>

    </div>
</div>
</template>

<style lang="scss" scoped>

#experience {
    padding-top: 60px;
    padding-bottom: 30px;
    min-height: 100vh;
    width: 100vw;
    background-image: url("https://images.pexels.com/photos/952670/pexels-photo-952670.jpeg?auto=compress&cs=tinysrgb&h=750&w=1260");
    background-size: cover;
    background-position: center center;
    color: white;
    font-size: 20px;
    font-weight: bold;
    text-shadow: 3px 3px 6px #000000;

    .header {
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        letter-spacing: 4px;

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

.row {
  height: 180px;

}

.content {
    padding-top: 60px;
}

.content_img {
  padding-right: 30px;
  display: flex;
  justify-content: flex-end;
}

.img_box {
  position: relative;
  width: 64px;
  height: 100%;
}
.img_pattern{
    position: absolute;
    background-image: linear-gradient(to bottom, rgb(24, 178, 192), rgb(71, 141, 189));
    border-radius: 50%;
    padding: 8px;
    z-index: 1;
    transition: all 0.5s;
    width: 64px;
}
.line{
    position: absolute;
    width: 20px;
    height: 120%;
    left: 50%;
    transform: translate(-50%, 5%);
    background-image: linear-gradient(to bottom, rgb(71, 141, 189), rgb(71, 141, 189), rgb(24, 178, 192), rgb(24, 178, 192));
    z-index: 0;
}

.row:hover img {
    transform: scale(1.3, 1.3);
}

#experience .row h4 {
    transition: all 0.5s;
}

#experience .row:hover h4 {
    color: rgb(68, 189, 219);
}

@media screen and (max-width: 767px){
  img,.line{
    display: none;
  }
  h4 {
    font-size: 22px;
  }
  p {
    font-size: 20px;
  }
  .row {
    margin-bottom: 30px;
  }
}

</style>
