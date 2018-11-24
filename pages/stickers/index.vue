<template>
  <section class="stickers">
    <Sticker
      thumbnail= "https://gopherswag.com/img/gophercises-box.png"
      title="Gopher Boxer"
      id="1"
      previewText="Keep on boxing!!"/>
    <Sticker
      thumbnail= "https://gopherswag.com/img/gophercises-jump.png"
      title="Jump Rope Gopher"
      id="2"
      previewText="Keep on jumping!!"/>
  </section>
</template>

<script>
  import Sticker from '@/components/Sticker'

  export default {
    components: {
      Sticker
    }
  }
</script>

<style scoped>
  .stickers {
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    align-items: center;
  }
</style>
