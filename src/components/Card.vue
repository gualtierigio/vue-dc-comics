<template>
    <div class="thumb">
        <img :src="dcComic.thumb" :alt="dcComic.type">
        <h4>{{dcComic.series}}</h4>
    </div>
</template>

<script>
import buyComics from "../data/buy-comics.json";

export default {
    name: 'Main',
    data: function () {
      return {
         buyComics
      }
   }

}
</script>

<style lang="scss" scoped>

.thumb{
   // altezza provvisoria
   width: calc(100% / 6 - 20px);
   margin: 10px 10px 0 10px;
   img{
      width: 100%;
   }
}


</style>