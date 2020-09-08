<template>
  <div>
    <h2>Child</h2>
    <h5>{{msg}}</h5>
    <button @click="passMSg">发送</button>
  </div>
</template>

<script>
export default {
  data () {
    return {
      ChildMsg: 'child msg'
    }
  },
  props: {
    msg: {
      type: String,
      default: ''
    },
  },
  methods: {
    passMSg () {
      this.$emit('showMsg', '我是子组件传递来的值')
    }
  },
}
</script>

<style scoped>
</style>