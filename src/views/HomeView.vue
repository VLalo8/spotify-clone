<template>
  <div class="home">
  </div>
</template>

<script>

export default {
  name: 'HomeView',
  components: {
    
  },
  data() {
    return{
    }
  },
  mounted() {
    this.$emit('HomeMount',true)
  },
  unmounted() {
    this.$emit('HomeMount',false)
  }
}
</script>
