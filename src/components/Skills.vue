<template>
<div id="skills">
    <div class="container">
        <div class="header">
            <h1>Skills</h1>
            <div class="hr mt-4">
                <i class="fas fa-tools"></i> </div>
        </div>
        <div class="type_list mt-5">
            <button class="btn btn-primary" @click.prevent='listFlag=true'>清單<i class="fas fa-list ml-2"></i></button>
            <button class="btn btn-danger" @click.prevent='listFlag=false'>圖示<i class="fas fa-shapes ml-2"></i></button>
        </div>
        <div class="skills_list mt-5" v-if='listFlag'>
            <ul>
                前端(Front-end)
                <li>Html、css</li>
                <li>Bootstrap</li>
                <li>Javascript</li>
                <li>Jquery</li>
                <li>Vue</li>
            </ul>
            <ul>
                後端(Front-end)
                <li>Node.js</li>
                <li>Python、Django</li>
                <li>Java</li>
                <li>C#</li>
            </ul>
            <ul>
                Database
                <li>Mysql</li>
                <li>Firebase</li>
            </ul>
            <ul>
                其他
                <li>Flutter</li>
                <li>Linux</li>
                <li>Git</li>
            </ul>
        </div>
        <div class="skills_pattern mt-5" v-else>
            <div class="row">
                <div class="col-6 col-sm-6 col-md-4 col-lg-3 d-flex justify-content-center">
                    <div class="flip-card">
                        <div class="flip-card-inner">
                            <div class="flip-card-front">
                                <img src="../assets/skill/html.png" alt="Avatar" style="width:150px;height:150px;">
                            </div>
                            <div class="flip-card-back">
                                <h2>HTML</h2>
                            </div>
                        </div>
                    </div>
                </div>
                <div class=" col-6 col-sm-6 col-md-4 col-lg-3 d-flex justify-content-center">
                    <div class="flip-card">
                        <div class="flip-card-inner">
                            <div class="flip-card-front">
                                <img src="../assets/skill/css.png" alt="Avatar" style="width:150px;height:150px;">
                            </div>
                            <div class="flip-card-back">
                                <h2>CSS</h2>
                            </div>
                        </div>
                    </div>
                </div>
                <div class=" col-6 col-sm-6 col-md-4 col-lg-3 d-flex justify-content-center">
                    <div class="flip-card">
                        <div class="flip-card-inner">
                            <div class="flip-card-front">
                                <img src="../assets/skill/javascript.png" alt="Avatar" style="width:150px;height:150px;">
                            </div>
                            <div class="flip-card-back">
                                <h2>JavaScript</h2>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-6 col-sm-6 col-md-4 col-lg-3 d-flex justify-content-center">
                    <div class="flip-card ">
                        <div class="flip-card-inner">
                            <div class="flip-card-front">
                                <img src="../assets/skill/jquery.png" alt="Avatar" style="width:150px;height:150px;">
                            </div>
                            <div class="flip-card-back">
                                <h2>jQuery</h2>
                            </div>
                        </div>
                    </div>
                </div>
                <div class=" col-6 col-sm-6 col-md-4 col-lg-3 d-flex justify-content-center">
                    <div class="flip-card">
                        <div class="flip-card-inner">
                            <div class="flip-card-front">
                                <img class="mt-3" src="../assets/skill/bootstrap.png" alt="Avatar" style="width:180px;height:180px;">
                            </div>
                            <div class="flip-card-back">
                                <h2>Bootstrap</h2>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-6 col-sm-6 col-md-4 col-lg-3 d-flex justify-content-center">
                    <div class="flip-card">
                        <div class="flip-card-inner">
                            <div class="flip-card-front">
                                <img class="mt-5" src="../assets/skill/vue.png" alt="Avatar" style="width:130px;height:130px;">
                            </div>
                            <div class="flip-card-back">
                                <h2>Vue</h2>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-6 col-sm-6 col-md-4 col-lg-3 d-flex justify-content-center">
                    <div class="flip-card">
                        <div class="flip-card-inner">
                            <div class="flip-card-front">
                                <img src="../assets/skill/mysql.png" alt="Avatar" style="width:150px;height:160px;">
                            </div>
                            <div class="flip-card-back">
                                <h2>Mysql</h2>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-6 col-sm-6 col-md-4 col-lg-3 d-flex justify-content-center">
                    <div class="flip-card">
                        <div class="flip-card-inner">
                            <div class="flip-card-front">
                                <img src="../assets/skill/nodejs.png" alt="Avatar" style="width:200px;height:200px;">
                            </div>
                            <div class="flip-card-back">
                                <h2>Node.js</h2>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="col-6 col-sm-6 col-md-4 col-lg-3 d-flex justify-content-center">
                    <div class="flip-card">
                        <div class="flip-card-inner">
                            <div class="flip-card-front">
                                <img src="../assets/skill/firebase.png" alt="Avatar" style="width:200px;height:200px;">
                            </div>
                            <div class="flip-card-back">
                                <h2>Firebase</h2>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-6 col-sm-6 col-md-4 col-lg-3 d-flex justify-content-center">
                    <div class="flip-card">
                        <div class="flip-card-inner">
                            <div class="flip-card-front">
                                <img class="mt-3" src="../assets/skill/python.png" alt="Avatar" style="width:160px;height:160px;">
                            </div>
                            <div class="flip-card-back">
                                <h2>Python</h2>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-6 col-sm-6 col-md-4 col-lg-3 d-flex justify-content-center">
                    <div class="flip-card">
                        <div class="flip-card-inner">
                            <div class="flip-card-front">
                                <img class="mt-3" src="../assets/skill/djnago.jpeg" alt="Avatar" style="width:180px;height:130px;">
                            </div>
                            <div class="flip-card-back">
                                <h2>Django</h2>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-6 col-sm-6 col-md-4 col-lg-3 d-flex justify-content-center">
                    <div class="flip-card">
                        <div class="flip-card-inner">
                            <div class="flip-card-front">
                                <img class="mt-3" src="../assets/skill/java.png" alt="Avatar" style="width:130px;height:130px;">
                            </div>
                            <div class="flip-card-back">
                                <h2>Java</h2>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-6 col-sm-6 col-md-4 col-lg-3 d-flex justify-content-center">
                    <div class="flip-card">
                        <div class="flip-card-inner">
                            <div class="flip-card-front">
                                <img class="mt-3" src="../assets/skill/flutter.png" alt="Avatar" style="width:130px;height:130px;">
                            </div>
                            <div class="flip-card-back">
                                <h2>Flutter</h2>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-6 col-sm-6 col-md-4 col-lg-3 d-flex justify-content-center">
                    <div class="flip-card">
                        <div class="flip-card-inner">
                            <div class="flip-card-front">
                                <img class="mt-3" src="../assets/skill/git.png" alt="Avatar" style="width:130px;height:130px;">
                            </div>
                            <div class="flip-card-back">
                                <h2>Git、Github</h2>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

        </div>
    </div>
</div>
</template>

<style lang="scss" scoped>
#skills {
    padding-top: 60px;
    padding-bottom: 30px;
    width: 100vw;
    background-image: url("https://cdn.pixabay.com/photo/2015/12/01/15/43/black-1072366_960_720.jpg");
    background-size: cover;
    background-position: center center;
    color: white;
    font-size: 20px;
    font-weight: bold;
    text-shadow: 3px 3px 6px #000000;
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

.type_list {
    width: 100%;
    display: flex;
    justify-content: center;
}

.skills_list {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    ul {
        font-size: 30px;
        width: 300px;
        text-align: left;
        padding: 0;
        display: flex;
        flex-direction: column;
        align-items: center;
        margin-bottom: 30px;

        li {
            letter-spacing: 3px;
        }
    }
}

.skills_pattern {
    padding: 15px;
    overflow: hidden;
    justify-content: flex-start;
    flex-wrap: wrap;
    display: flex;
}
img {
    width: 80%;
}
/* The flip card container - set the width and height to whatever you want. We have added the border property to demonstrate that the flip itself goes out of the box on hover (remove perspective if you don't want the 3D effect */
.flip-card {
    background-color: transparent;
    width: 300px;
    height: 200px;
    perspective: 1000px;
    /* Remove this if you don't want the 3D effect */
}

/* This container is needed to position the front and back side */
.flip-card-inner {
    position: relative;
    width: 100%;
    height: 100%;
    text-align: center;
    transition: transform 0.8s;
    transform-style: preserve-3d;
}

/* Do an horizontal flip when you move the mouse over the flip box container */
.flip-card:hover .flip-card-inner {
    transform: rotateY(180deg);
}

/* Position the front and back side */
.flip-card-front,
.flip-card-back {
    position: absolute;
    width: 100%;
    height: 100%;
    -webkit-backface-visibility: hidden;
    /* Safari */
    backface-visibility: hidden;
}

/* Style the front side (fallback if image is missing) */
.flip-card-front {
    color: black;
}

/* Style the back side */
.flip-card-back {
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    transform: rotateY(180deg);
}

@media screen and (max-width: 767px) {
    .skills_list ul {
        font-size: 20px;
    }
}
</style>

<script>
export default {
    data() {
        return {
            listFlag: false,
        }
    }
}
</script>
