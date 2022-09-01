<template>
  <div>
    <div id="background">
      <img id="craft" src="/img/craft.webp" alt="">
    </div>
    <!-- 3.6rem 是 nav bar 的高度 -->
    <iframe :src="url" style="position:fixed; top:3.6rem; left:0; right:0; width:100%; height:100%; border:none; margin:0; padding:0; overflow:hidden; z-index:18;"></iframe>
  </div>
</template>
<script>
export default {
  name: 'EmbedCraft',
  props: {
    url: {
      type: String,
      required: true
    }
  }
}
</script>
<style>
#background {
  position:fixed;
  background: white;
  top:3.6rem;
  left:0;
  right:0;
  width:100%;
  height:100%;
  border:none;
  margin:0;
  padding:0; z-index:17;

  display: flex;
  justify-content: center;
  align-items: center;
}
#craft {
  /* 直接看 craft loading icon 的效果写死的大小 */
  width: 27px;
  height: 27px;
}
</style>
