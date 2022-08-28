<template>
  <div>
    ItemVue
    <router-link to="1">Item1</router-link>
    <router-link to="2">Item2</router-link>
    {{ $route.params.id }}
  </div>
</template>

<script>
export default {
  name: 'ItemView',
  created() {
    console.log('created');
  },
  watch: {
    $route(to, from){
      console.log('to:',to)
      console.log('from:',from)

    }
  }
}
</script>

<style>

</style>