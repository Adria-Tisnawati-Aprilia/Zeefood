<template>
  <div class="home">
    <NavItem/>
    <div class="container">
      <HeroF/>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import NavItem from '@/components/NavItem.vue'
import HeroF from '@/components/Hero.vue'

export default {
  name: 'HomeView',
  components: {
    NavItem,
    HeroF
  }
}
</script>
