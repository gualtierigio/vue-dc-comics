<template>
   <header>
       <div class="page-wrap d-flex">
            <img src="../assets/img/dc-logo.png" alt="">
            <ul>
                <li v-for="(link, index) in links" :key="index"><a href="{{}}"></a></li>
            </ul>
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
                    url: "#",
                    current: false,
                },
                {
                    text: "Comics",
                    url: "#",
                    current: true,
                },
                {
                    text: "Movies",
                    url: "#",
                    current: false,
                },
                {
                    text: "Tv",
                    url: "#",
                    current: false,
                },
                {
                    text: "Games",
                    url: "#",
                    current: false,
                },
                {
                    text: "Collectibles",
                    url: "#",
                    current: false,
                },
                {
                    text: "Videos",
                    url: "#",
                    current: false,
                },
                {
                    text: "Fans",
                    url: "#",
                    current: false,
                },
                {
                    text: "News",
                    url: "#",
                    current: false,
                },
                {
                    text: "Shop",
                    url: "#",
                    current: false,
                }
            ]
        }
    }

}
</script>

<style scoped lang="scss">

header img{
    height: 120px;
}


</style>