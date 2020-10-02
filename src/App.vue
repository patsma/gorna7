<template>
  <Block class="block--bottom-left" title="Górna 7/4" filename="gorna0759.jpg">
    <p class="subtitle">Najlepsza lokalizacja w mieście</p>
  </Block>
  <Block title="Dostępne od zaraz" filename="gorna0769.jpg"/>
  <Block class="block--bottom-left" filename="gorna0760.jpg">
    <p class="subtitle">Napisz, zadzwoń 502 590 747</p>
    <a href="https://www.facebook.com/marketplace/item/980067239172834" class="subtitle">Więcej informacji</a>

  </Block>
  <Block  filename="gorna0788.jpg"/>

</template>

<script>
import gsap from 'gsap'
import Block from './components/Block.vue'

export default {
  name: 'App',
  components: {
    Block
  },
  mounted() {
    gsap.from('body', {autoAlpha: 0})

  }
}
</script>

<style lang="scss">
html {
  display: grid;
  width: 100vw;
  min-height: 100vh;
  overflow-x: hidden;
}


*, *:after, *:before {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

#app {
  display: grid;
  height: 100%;
  position: relative;
  justify-content: center;
  align-content: center;
  background: rgb(63, 94, 251);
  background: linear-gradient(90deg, rgba(63, 94, 251, 1) 0%, rgba(252, 70, 107, 1) 100%);
}

.wrapper {
  position: relative;
}

a {
  text-decoration: none;
  color: #fff;
}

</style>
