<template>
   <main>
      <section id="jumbotron">
         <button><a href="#">current series</a></button>
      </section>
      <!-- Fumetti -->
      <section>
         <div class="page-wrap">
            <div class="content-wrap d-flex">
               <Card />
            </div>
            <button><a href="#">Load more</a></button>
         </div>
      </section>
      <!-- Fumetti / -->

      <!-- buy comics -->
      <section class="buy-comics">
         <div class="page-wrap d-flex">
            <div v-for="(buyComic, index) in buyComics" :key="index" class="buy-comics__content">
               <a class="d-flex" href=""><img :src="buyComic.img" alt="">{{buyComic.text}}</a>
            </div>
         </div>
      </section>
      <!-- buy comics / -->
   </main>
</template>

<script>
import Card from "./Card.vue";
import buyComics from "../data/buy-comics.json";
import dcComics from "../data/dc-comics.json";

export default {
   name: 'Main',
   components: {
      Card
   },
   data: function () {
      return {
         dcComics,
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
   height: 400px;
   position: relative;
   button{
      padding: 15px 25px;
      font-size: 1.4rem;
      position: absolute;
      bottom: -28px;
      left: 14%;
      a{
         text-decoration: none;
         color: $white-color;
      }
   }
}

button{
   background-color: $main-blue-color;
   text-transform: uppercase;
   border: $main-blue-color;
   font-weight: bold;
}

.page-wrap{
   height: 100%;
   button{
      margin: 30px;
      padding: 8px 45px;
      a{
         text-decoration: none;
         color: $white-color;
      }
   }
}

.content-wrap{
   height: 700px;
   margin-top: 40px;
   flex-wrap: wrap;
}

.thumb{
   // altezza provvisoria
   width: calc(100% / 6 - 20px);
   margin: 10px 10px 0 10px;
   img{
      width: 100%;
   }
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