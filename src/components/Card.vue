<template>
    <div class="thumb">
        <img :src="fumettoSource" :alt="categories">
        <h4>{{title}}</h4>
    </div>
</template>

<script>

export default {
    name: 'Card',
    props: ['fumettoSource', 'title', 'hero' , 'categories']
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