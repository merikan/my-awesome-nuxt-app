<template>
  <section class="single-sticker">
    <h1>{{ $route.params.id }}</h1>
    <div>
      <img src="" alt="">
    </div>
    <p>Sticker description</p>
  </section>
</template>

<style>
.single-sticker {
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 30px;
}
</style>
