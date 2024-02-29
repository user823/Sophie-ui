<template>
  <div>
    <svg-icon icon-class="github" @click="goto" />
  </div>
</template>

<script>
export default {
  name: 'SophieGit',
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
