<template>
   <main>
      <div class="page-wrap">
         <div class="content-wrap d-flex">
            <h2>--&gt; Content goes here &lt;-- </h2>
            <img src="" alt="">
         </div>
      </div>
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



</style>