<template>
  <div>
    <svg-icon icon-class="question" @click="goto" />
  </div>
</template>

<script>
export default {
  name: 'SophieDoc',
  data() {
    return {
      url: 'https://github.com/user823/Sophie-ui'
    }
  },
  methods: {
    goto() {
      window.open(this.url)
    }
  }
}
</script>
