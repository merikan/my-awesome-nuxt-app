<template>
  <section class="stickers">
    <Sticker
      v-for="sticker in stickers"
      :key="sticker.id"
      :thumbnail= "sticker.thumbnail"
      :title="sticker.title"
      :id="sticker.id"
      :previewText="sticker.previewText"/>
  </section>
</template>

<script>
  import Sticker from '@/components/Sticker';

  export default {
    components: {
      Sticker
    },
    asyncData() {
      // return axios.get()   for a real request
      // hardcoded list of stickers
      // fake async request, add a 1.5s delay
      return new Promise((resolve, reject) => {
        setTimeout(() => {
          resolve({
            stickers: [
              {
                id: "1",
                title: "Gopher Boxer",
                previewText: "Keep on boxing!!",
                thumbnail: "https://gopherswag.com/img/gophercises-box.png"
              },
              {
                id: "2",
                title: "Jump Rope Gopher",
                previewText: "Keep on jumping!!",
                thumbnail: "https://gopherswag.com/img/gophercises-jump.png"

              }
            ]
          })
        }, 1500)
      })
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
