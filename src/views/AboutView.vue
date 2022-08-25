<template>
  <div class="about">
    <h1>This is an about page</h1>
    <button @click="checkRouteRouter">route and router</button>
    <button @click="gotoHome">Homeにもどる</button>
</div>
</template>

<script>
export default {
  methods: {
    checkRouteRouter() {
      console.log('---this.$route---');
      console.log(this.$route);
      console.log('---this.$router--');
      console.log(this.$router);
    },
    gotoHome() {
      this.$router.push('/');
    }
  }
}
</script>