<template lang="html">
    <div :class="$style.home">
        <h1>Home</h1>
    </div>
</template>

<script>
export default {
}
</script>

<style lang="scss" module>
  @import '../../css/reset.scss';
  console.log('log')
  .home{
    color: red;
    font-size: 80px;
  }
</style>
