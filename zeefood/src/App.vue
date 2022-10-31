<template>
  <div id="app"> 
    <router-view/>
    <FootEr/>
  </div>
</template>

<script>
import FootEr from "@/components/Footer.vue"

export default {
  components : {
    FootEr
  }
}
</script>