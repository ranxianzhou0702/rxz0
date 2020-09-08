<template>
  <div>
    <h1>Parent</h1>
    <h3>{{msg}}</h3>
    <m-child :msg="'from Parent msg'"
             @showMsg='showMsg'
             ref="child"></m-child>
  </div>
</template>

<script>
import MChild from './Child'
export default {
  data () {
    return {
      msg: ''
    }
  },
  methods: {
    showMsg (val) {
      this.msg = val
    }
  },
  components: {
    MChild,
  },
  mounted () {
    //console.log(this.$children[0].msg)
    console.log('ref', this.$refs.child)
  },
}
</script>

<style scoped>
</style>