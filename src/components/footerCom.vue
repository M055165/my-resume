<template>
    <footer>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Eius dolorem minima quis sit unde magni deleniti odio,
        fugit perspiciatis quia excepturi? Non perspiciatis distinctio rerum nihil ducimus culpa a illum.
        <v-icon class="mr-8 mt-1 icon" @click="scrollToTop">mdi-arrow-up-bold-circle-outline</v-icon>
    </footer>
</template>


<script setup>

const scrollToTop = () => {
    window.scrollTo({
        top: 0,
        behavior: "smooth" // 滑動行為，平滑滾動
    });
}


</script>

<style scoped>
footer {
    min-height: 300px;
    background-color: rgba(0, 0, 0, 0.7);
    position: relative;
}

.icon {
    color: white;
    font-size: 50px;
    position: absolute;
    top: -25px;
    left: calc(50% - 25px);
}
</style>