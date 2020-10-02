<template>
  <div class="block">
    <div class="texts">
      <p>{{ title }} </p>
      <slot></slot>
    </div>
    <img class="full" :src="require(`@/assets/img/${filename}`)" alt="">
  </div>
</template>

<script>
export default {
  name: 'Title',
  props: {
    filename: String,
    title: String,
  }
}
</script>

<style lang="scss">
p {
  font-size: clamp(1.8rem, 10vw, 10rem);
  background-image: linear-gradient(45deg, #fafaf9, #f1e7ea);
  background-size: 100%;
  background-repeat: repeat;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-background-clip: text;
  -moz-text-fill-color: transparent;


}

.block {
  height: 100vh;
  width: 100vw;
  position: relative;
  display: grid;
  justify-content: center;
  align-content: center;

  &--bottom-left {
    align-content: end;
    justify-content: start;
    padding-bottom: 0;
    padding-left: 0;
  }

  &--top-left {
    align-content: start;
    justify-content: start;
    padding-top: 0;
    padding-left: 0;
  }
}

.texts {
  z-index: 1;
}

#app > div:nth-child(1) > img {
  clip-path: polygon(20% 0%, 100% 0, 100% 20%, 100% 100%, 80% 100%, 50% 100%, 0 70%, 0 0);


}

.full {
  position: absolute;
  left: 0;
  top: 0;
  width: 100vw;
  height: 100%;
  object-fit: cover;
  //mix-blend-mode: soft-light;
  clip-path: polygon(75% 0%, 100% 50%, 75% 100%, 0% 100%, 25% 50%, 0% 0%);
  pointer-events: none;
}

.subtitle {
  font-size: clamp(2.4rem, 7.5vw, 5rem);

}


</style>
