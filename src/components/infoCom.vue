<template>
    <div>
        <v-parallax
            src="https://images.pexels.com/photos/691668/pexels-photo-691668.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2">
            <v-container>
                <v-row>
                    <v-col col="12" md="4" sm="12">
                        <div class="left">
                            <div class="profile">
                                <div class="avatar-box">
                                    <img src="../assets/eddie.png" alt="avator img" class="avatar">
                                </div>
                                <p>Eddie Tsai</p>
                                <p>A chanlange-loving web developer</p>
                            </div>

                            <div class="info">
                                <p class="title">INFO</p>
                                <ul>
                                    <li>
                                        <div class="info-item">
                                            <v-icon class="mr-8 mt-1 icon">mdi-facebook</v-icon>
                                            <div class="desc">
                                                <p>Email</p>
                                                <span>Eddie055165@gmail.com</span>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="info-item">
                                            <v-icon class="mr-8 mt-1 icon">mdi-earth</v-icon>
                                            <div class="desc">
                                                <p>Website</p>
                                                <span>https://www.llt.com.tw</span>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="info-item">
                                            <v-icon class="mr-8 mt-1 icon">mdi-cake</v-icon>
                                            <div class="desc">
                                                <p>Birthdate</p>
                                                <span>1998/09/13</span>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="info-item">
                                            <v-icon class="mr-8 mt-1 icon">mdi-map-marker</v-icon>
                                            <div class="desc">
                                                <p>Location</p>
                                                <span>Taipei</span>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </div>


                            <div class="socials">
                                <p class="title">SOCAILS</p>
                                <ul>
                                    <li>
                                        <div class="social-item">
                                            <v-icon class="mr-8 mt-1 icon">mdi-github</v-icon>
                                            <a href="eddie055165@gmail.com">eddie055165@gmail.com</a>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="social-item">
                                            <v-icon class="mr-8 mt-1 icon">mdi-linkedin</v-icon>
                                            <a
                                                href="https://m055165.github.io/my-resume/#/">https://m055165.github.io/my-resume/#/</a>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="social-item">
                                            <v-icon class="mr-8 mt-1 icon">mdi-instagram</v-icon>
                                            <a
                                                href="https://m055165.github.io/my-resume/#/">https://m055165.github.io/my-resume/#/</a>
                                        </div>
                                    </li>
                                </ul>
                            </div>


                            <div class="hobbies">
                                <p class="title">HOBBIES</p>
                                <div class="hobbies-item">
                                    <span class="item">
                                        <v-icon class="icon mr-2">mdi-dumbbell</v-icon>
                                        <span>Workout</span>
                                    </span>
                                    <span class="item">
                                        <v-icon class="icon mr-2">mdi-youtube</v-icon>
                                        <span>Drama</span>
                                    </span>
                                    <span class="item">
                                        <v-icon class="icon mr-2">mdi-food</v-icon>
                                        <span>Food</span>
                                    </span>
                                    <span class="item">
                                        <v-icon class="icon mr-2">mdi-currency-usd</v-icon>
                                        <span>Investment</span>
                                    </span>
                                    <span class="item">
                                        <v-icon class="icon mr-2">mdi-campfire</v-icon>
                                        <span>Camping</span>
                                    </span>
                                </div>
                            </div>



                        </div>
                    </v-col>

                    <v-col col="12" md="8" sm="12" class='mlft'>
                        <div class="right">
                            <div class="about-box">
                                <v-container>
                                    <div class="autobiogrphy">
                                        <h3>Who am i?</h3>
                                        <p class="mt-10">I'm a developer born in Iran and founder of Delix.ir, Bytegate.ir
                                            and Bobet.ir
                                            and co-founder of Smo.li.
                                            I'm interested and skilled in different topics of Information Technology
                                            including programming, web development, and computer and network security.</p>
                                    </div>

                                    <div class="education">
                                        <h3>Education</h3>
                                        <div class="education-box d-flex">
                                            <span>2017-2021</span>
                                            <div class="education-info ml-10">
                                                <p>國立中正大學</p>
                                                <span>資訊管理學系、成人及繼續教育學系</span>
                                            </div>
                                        </div>
                                    </div>

                                    <div class="skills">
                                        <h3>Skills</h3>
                                        <div class="slills-box">
                                            <ul>
                                                <li>
                                                    <p class="mb-2">Vue.js</p>
                                                    <v-progress-linear model-value="75"></v-progress-linear>
                                                </li>
                                                <li>
                                                    <p>Flutter</p>
                                                    <v-progress-linear model-value="60"></v-progress-linear>
                                                </li>
                                                <li>
                                                    <p>Javascript</p>
                                                    <v-progress-linear model-value="65"></v-progress-linear>
                                                </li>
                                                <li>
                                                    <p>Nodej.js</p>
                                                    <v-progress-linear model-value="30"></v-progress-linear>
                                                </li>
                                                <li>
                                                    <p>Docker</p>
                                                    <v-progress-linear model-value="30"></v-progress-linear>
                                                </li>
                                            </ul>
                                        </div>

                                    </div>

                                </v-container>

                            </div>

                        </div>

                    </v-col>
                </v-row>
            </v-container>

        </v-parallax>


    </div>
</template>


<style lang="scss" scoped>
@media screen and (min-width: 768px) {
    .mlft {
        margin-left: -25px !important;
    }
}

@media screen and (max-width: 768px) {
    .mlft {
        margin-top: -25px !important;
    }
}

* {
    color: #fff;
}

ul {
    list-style: none;
}

li {
    padding: 10px;
}

.title {
    padding-bottom: 5px;
    border-bottom: 1px solid #fff;
    font-weight: bold;
}

.left {
    width: 100%;
    background-color: #424242;
}

.profile {
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: start;
    align-items: center;

    .avatar-box {
        width: 150px;
        height: 150px;
        margin: 20px 0px;
    }

    .avatar {
        width: 100%;
        height: 100%;
        border-radius: 50%;
    }
}

.info {
    margin-top: 10px;
    padding: 10px;

    .info-item {
        margin-top: 10px;
        display: flex;
        flex-direction: row;
        align-items: flex-start;
    }
}



.socials {
    margin-top: 10px;
    padding: 10px;

    .social-item {
        margin-top: 10px;
        display: flex;
        flex-direction: row;
        align-items: flex-start;
    }

    a {
        padding-top: 5px;
        text-decoration: none;
        font-size: 14px;

        &:hover {
            color: powderblue;
        }
    }
}

.hobbies {
    margin-top: 10px;
    padding: 10px;

    .hobbies-item {
        padding: 10px 0px;
    }

    .item {
        padding: 5px 10px;
        background-color: #555;
        border-radius: 20px;
        display: inline-block;
        margin: 10px 5px;
    }
}


.right {
    width: 100%;
    background-color: #f5f5f5;
    padding: 20px;
    margin-left: 0px !important;

    p {
        color: black;
    }
}

.about-box {
    width: 100%;
    background-color: #ECE6E6;

    h3 {
        color: black;
        font-size: 20px;
        border-bottom: 2px solid #424242;
        display: inline-block;

    }

    .autobiogrphy {
        margin-bottom: 30px;
    }

    .education {
        .education-box {
            padding: 20px 0px;

            span {
                color: black;
            }
        }
    }
}
</style>