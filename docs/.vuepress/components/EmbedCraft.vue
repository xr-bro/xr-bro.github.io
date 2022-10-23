<template>
  <div>
    <div id="background">
      <img id="craft" src="/img/craft.webp" alt="">
    </div>
    <!-- 3.6rem 是 nav bar 的高度 -->
    <iframe :src="url"></iframe>
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
  position: fixed;
  background: white;
  top: 3.6rem;
  left: 0;
  right: 0;
  width: 100%;
  height: 100%;
  border: none;
  margin: 0;
  padding: 0;
  /* sidebar 的 z-index 是 13，所以这 bg 是 11 */
  z-index: 11;
  display: flex;
  justify-content: center;
  align-items: center;
}

iframe {
  position: fixed;
  top: 3.6rem;
  left: 0;
  right: 0;
  width: 100%;
  height: 100%;
  border: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  /* sidebar 的 z-index 是 13，所以这 iframe 是 12 */
  z-index: 12;
}

#craft {
  /* 直接看 craft loading icon 的效果写死的大小 */
  width: 27px;
  height: 27px;
}

@media (prefers-color-scheme: dark) {
  #background {
    background: var(--blurBg);
  }
}
</style>
