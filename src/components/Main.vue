<template>
   <main>
      <section id="jumbotron"></section>
      <!-- Fumetti -->
      <section>
         <div class="page-wrap">
            <div class="content-wrap d-flex">
               <div class="thumb"></div>
            </div>
            <button>Load more</button>
         </div>
      </section>
      <!-- Fumetti / -->

      <!-- buy comics -->
      <section class="buy-comics">
         <div class="page-wrap d-flex">
            <div v-for="(buyComic, index) in buyComics" :key="index" class="buy-comics__content">
               <a class="d-flex" href=""><img :src="`${buyComic.img}`" alt="">{{buyComic.text}}</a>
            </div>
         </div>
      </section>
      <!-- buy comics / -->
   </main>
</template>

<script>
// import dcComics from "../data/dc-comics.jason";
import buyComics from "../data/buy-comics.json";

export default {
   name: 'Main',
   data: function () {
      return {
         // dcComics,
         buyComics,
      }
   }

}
</script>

<style scoped lang="scss">
@import "../style/variables.scss";

main{
   background-color: $nav-text-color;
   color: $white-color;
}

#jumbotron{
   background-image: url(../assets/img/jumbotron.jpg);
   background-position: top;
   background-size: cover;
   height: 200px;
}

div.page-wrap{
   height: 100%;
   button{
      margin: 30px;
      background-color: blue;
   }
}

div.content-wrap{
   height: 500px;
   border: 1px solid red;
}

.thumb{
   // altezza provvisoria
   height: 150px;
   width: calc(100% / 6);
   border: 1px solid red;
   flex-wrap: wrap;
}

// inizio parte blu

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