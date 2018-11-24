<template>
  <section class="single-sticker">
    <h1>{{ sticker.title }}</h1>
    <div>
      <img class="sticker-image" :src="sticker.thumbnail" :alt="sticker.title">
    </div>
    <p>{{sticker.descriptionText}}</p>
  </section>
</template>

<script>
  export default {
    asyncData(context) {
      // return axios.get()   for a real request
      // hardcoded list of stickers
      // fake async request, add a 1.5s delay
      return new Promise((resolve, reject) => {
        setTimeout(() => {
          resolve({
            sticker: [
              {
                id: "1",
                title: "Gopher Boxer",
                previewText: "Keep on boxing!!",
                descriptionText: "fmt u all. I'm the master of boxing",
                thumbnail: "https://gopherswag.com/img/gophercises-box.png"
              },
              {
                id: "2",
                title: "Jump Rope Gopher",
                previewText: "Keep on jumping!!",
                descriptionText: "fmt u all. I'm the master of jumping",
                thumbnail: "https://gopherswag.com/img/gophercises-jump.png"

              }
            ].find(el => el.id === context.params.id)
          })
        }, 1500)
      })
    }
  }

</script>
<style>
.single-sticker {
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 30px;
}
.sticker-image {
  width: 100%;
}
</style>
