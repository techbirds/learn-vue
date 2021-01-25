<template>
  <label>
    {{ label }}
    <input
      id="2"
      v-bind="$attrs"
      v-bind:value="value"
      v-on:input="$emit('input', $event.target.value)"
    >
  </label>
</template>

<script>
export default {
  inheritAttrs: false, // 要不要将组件的非prop属性透传到组件根节点上
  props: ['label', 'value'],
  created () {
    console.log(this.$attrs) // 自定义指定父组件的非prop属性透传目标
  }
}
</script>

<style>

</style>