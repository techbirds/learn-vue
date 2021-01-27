<template>
  <div>
    {{a}}
    <div v-for="item in items" :key="item.message" ref="c">
    {{ item.message }}
    </div>
  </div>
</template>

<script>
export default {
  props: {
    a: {
      type: String,
      default () {
        // console.log('----')
        // console.log(this)
        return "2"
      }
    }
  },
  data: () => {
    return {items: [
      { message: 'Foo' },
      { message: 'Bar' }
    ]}
  },
  created () {
    console.log('.....')
    this.$nextTick(()=> {
      console.log(this.$refs.c)
    })

  }
}
</script>

<style>

</style>