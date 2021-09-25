<template>
   <main>
      <div class="page-wrap">
         <div class="content-wrap d-flex">
            <h2>--&gt; Content goes here &lt;-- </h2>
         </div>
      </div>
      <section class="buy-comics">
         <div class="page-wrap d-flex">
            <div v-for="(buyComic, index) in buyComics" :key="index" class="buy-comics__content">
               <a class="d-flex" href=""><img src="{buyComic.img}" alt="">{{buyComic.text}}</a>
            </div>
         </div>
      </section>
   </main>
</template>

<script>
export default {
   name: 'Main',
   data: function () {
      return {
         buyComics: [
            {
               text: "digital comics",
               img: "../assets/img/buy-comics-digital-comics.png",
            },
            {
               text: "dc merchandise",
               img: "../assets/img/buy-comics-merchandise.png",
            },
            {
               text: "subscription",
               img: "../assets/img/buy-comics-subscription.png",
            },
            {
               text: "comic shop locator",
               img: "../assets/img/buy-comics-shop-locator.png",
            },
            {
               text: "digital comics",
               img: "",
            },
         ]
      }
   }

}
</script>

<style scoped lang="scss">
@import "../style/variables.scss";

main{
   height: 120px;
   background-color: black;
   color: $white-color;
}

div.page-wrap{
   height: 100%;
}

div.content-wrap{
   height: 100%;
   align-items: center;
}

.buy-comics{
   height: 140px;
   background-color: $main-blue-color;
}

.buy-comics__content{
   height: 100%;
   padding: 20px;
   a{
      height: 100%;
      align-items: center;
      text-decoration: none;
      color: $white-color;
      text-transform: uppercase;
         img{
            height: 50px;
            padding-right: 20px;
         }
   }
}


</style>