<template>
   <header class="d-flex">
       <div class="page-wrap d-flex">
            <img src="../assets/img/dc-logo.png" alt="">
            <nav>
                <ul class="d-flex">
                    <li v-for="(link, index) in links" :key="index">
                        <a href="{link.url}" :class="{active : link.current}">{{link.text}}</a>
                    </li>
                </ul>
            </nav>
       </div>
   </header>
</template>

<script>
export default {
    name: 'Header',
    data: function () {
        return {
            links: [
                {
                    text: "Characters",
                    url: "#character",
                    current: false,
                },
                {
                    text: "Comics",
                    url: "#comics",
                    current: true,
                },
                {
                    text: "Movies",
                    url: "#movies",
                    current: false,
                },
                {
                    text: "Tv",
                    url: "#tv",
                    current: false,
                },
                {
                    text: "Games",
                    url: "#games",
                    current: false,
                },
                {
                    text: "Collectibles",
                    url: "#collectibles",
                    current: false,
                },
                {
                    text: "Videos",
                    url: "#videos",
                    current: false,
                },
                {
                    text: "Fans",
                    url: "#fans",
                    current: false,
                },
                {
                    text: "News",
                    url: "#news",
                    current: false,
                },
                {
                    text: "Shop",
                    url: "#shop",
                    current: false,
                }
            ]
        }
    }

}
</script>

<style scoped lang="scss">

header{
    height: 120px;
    align-items: center;
    border: 1px solid red;
}

header img{
    height: 80px;

}

div.d-flex.page-wrap{
    align-items: center;
    justify-content: space-between;
}

ul{
    height: 100%;
    list-style-type: none;
    a{
        text-decoration: none;
    }
}

li{
    padding-right: 15px;
    :Hover{
        border-bottom: 3px solid blue;
    }
}


</style>