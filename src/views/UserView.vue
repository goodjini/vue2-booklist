<template>
  <div class="red-b">
    ユーザー情報<br>
    <router-link to="profile">プロフィル</router-link> |
    <router-link to="post">記事</router-link>
    <div class="purple-b">
      <router-view/>
    </div>
  </div>
  </template>

<script>
export default {
  created() {
    console.log('created: UserView')
  }
}
</script>

<style>
.red-b {
  border: 1px solid red;
}
.purple-b {
  border: 1px solid purple;
}
</style>