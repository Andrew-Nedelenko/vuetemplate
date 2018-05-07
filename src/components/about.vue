<template>
  <div class="about">
      <p>{{ msg1 }}</p>
  </div>
</template>

<script>

export default {
  name: "about",
  data () {
      return {
          msg1: 'rendered from about'
      }
  }
}
</script>
