<template>
  <div>
    <div v-for="item in items" :key="item.message" ref="c">
    {{ item.message }}
    </div>
  </div>
</template>

<script>
export default {
  data: () => {
    return {items: [
      { message: 'Foo' },
      { message: 'Bar' }
    ]}
  },
  created () {
    this.$nextTick(()=> {
      console.log(this.$refs.c)
    })

  }
}
</script>

<style>

</style>