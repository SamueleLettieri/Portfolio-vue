<template>
  <section class="container">
    <div v-for="(immage, index) in immages" :key="index">
      <img :src="immage.img" alt="">
      <div>{{immage.title}}</div>
      <div>{{immage.description }}</div>
    </div>
  </section>
</template>

<script>
export default {

  data(){
    return{
      immages: [
        {
          img: require('@/assets/comics-img.png'),
          title: 'a',
          description:'a'
        },
        {
          img: require('@/assets/discord-img.png'),
          title: 'b',
          description:'b'
        },
        {
          img: require('@/assets/Immagine 2022-10-06 182244.png'),
          title: '',
          description:''
        },
        {
          img: require('@/assets/Immagine 2022-10-06 182651.png'),
          title: '',
          description:''
        },
        {
          img: require('@/assets/sony-img.png'),
          title: '',
          description:''
        },
        {
          img: require('@/assets/spotify-img.png'),
          title: '',
          description:''
        },
      ] 
    }
  }
}
</script>

<style lang="scss" scoped>
  img{
    width: 100%;
    height: 400px;
    object-fit: cover;
    object-position: top;
    
  }
</style>