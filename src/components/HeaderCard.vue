<template>
  <div class="container-card">
    <div class="discs">
      <img :src="components.poster" />
      <h5>{{ components.title }}</h5>
      <p>
        {{ components.author }}
        <br />
        {{ components.year }}
      </p>
    </div>
  </div>
</template>



<script>

export default {
  props: {
    components: Object,
  },
  
};
</script>


<style lang="scss" scoped>

</style>