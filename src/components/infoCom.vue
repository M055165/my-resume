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
                                    <img src="https://evryn.github.io/vue-modern-resume/img/avatar.jpg" alt="avator img"
                                        class="avatar">
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
                                            <v-icon class="mr-8 mt-1 icon">mdi-facebook</v-icon>
                                            <p>Email</p>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="social-item">
                                            <v-icon class="mr-8 mt-1 icon">mdi-earth</v-icon>
                                            <p>Website</p>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="social-item">
                                            <v-icon class="mr-8 mt-1 icon">mdi-cake</v-icon>
                                            <p>Birthdate</p>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="social-item">
                                            <v-icon class="mr-8 mt-1 icon">mdi-map-marker</v-icon>
                                            <p>Location</p>
                                        </div>
                                    </li>
                                </ul>
                            </div>

                        </div>
                    </v-col>
                    <v-col col="12" md="8" sm="12">
                        <h2>Eddie Tsai</h2>
                        <p>A chanlange-loving web developer</p>
                    </v-col>
                </v-row>
            </v-container>

        </v-parallax>


    </div>
</template>


<style lang="scss" scoped>
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
        width: 120px;
        height: 120px;
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
}
</style>