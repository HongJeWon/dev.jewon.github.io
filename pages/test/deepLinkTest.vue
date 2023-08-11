<script setup lang="ts">

onMounted(() => {
  redirect();
})
// let appURL = 'testapp://start';
// let appURL = 'intent://start/#Intent;scheme=testapp;package=com.example.mytestapp;end';
let appURL = 'intent://main?dest=/#Intent;scheme=fitamin;package=kr.fitamin;end';
const redirect = () => {

  // 앱이 설치되어 있지 않을 경우 Google Play Store URL
  let storeURL = 'https://play.google.com/store/apps/details?id=com.kakao.talk&hl=ko-KR';

  // 앱을 시도하여 열기
  window.location.href = appURL;

  // setTimeout(() => {
  //   if (!document.hasFocus()) {
  //     return;
  //   }
  //   window.location.href = storeURL;
  // }, 5000);

};
const startApp = () => {

  window.location.href = appURL;
};
</script>

<template>
  <div>
    <button @click="startApp">StartApp</button>
  </div>
</template>

<style scoped>

</style>