<template>
    <v-parallax
        src="https://images.pexels.com/photos/593158/pexels-photo-593158.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2">
        <v-container>
            <v-row>
                <div class="timeline">
                    <v-timeline align="start">
                        <v-timeline-item v-for="(item, i) in items" :key="i" :dot-color="item.color" :icon="item.icon"
                            fill-dot>
                            <v-card>
                                <v-card-title :class="['text-h6', `bg-${item.color}`]">
                                    {{ item.title }}
                                </v-card-title>
                                <v-card-text class="bg-white text--primary card-box">
                                    <pre>{{ item.content }}</pre>
                                </v-card-text>
                            </v-card>
                        </v-timeline-item>
                    </v-timeline>
                </div>
            </v-row>
        </v-container>

    </v-parallax>
</template>


<script>
export default {
    data: () => ({
        items: [
            {
                color: 'red-lighten-2',
                icon: 'mdi-domain',
                title: '力麗科技前端工程師',
                content: `在公司擔任的是前端工程師的職務，完成的專案有
                
1. 科技設備監控系統App( 使用Flutter)

2. 科技設備安裝系統App( 使用Flutter)

3. 科技設備安裝系統儀表板（使用Vue.js)

4. 財團法人臺灣更生保護會全球網站(使用Vue.js)

`
            },
            {
                color: 'purple-lighten-2',
                icon: 'mdi-pistol',
                title: "服兵役",
                content: `在湖口的五八四旅擔任4個月的義務役`
            },
            {
                color: 'green-lighten-1',
                icon: 'mdi-book',
                title: '力麗科技前端工程師',
                content: `1. 力麗科技官方網站的前後台設計與撰寫，
此網站是透過Vue.js撰寫，此專案的前端部分從0到完成皆是由我獨立完成 (https://www.llt.com.tw/)

2. 採購系統雛型(使用Vue.js配合後端工程師，完成力麗科技採購系統的雛形)

3. 專案的修改密碼、重設密碼(使用Vue.js)

4. 報表生成系統( 使用Node.js)`
            },
        ],
    }),
}
</script>

<style lang="scss" scoped>
.timeline {
    padding-top: 50px;
}

.card-box {
    padding: 15px;

    pre {
        margin-top: 10px;
    }
}
</style>