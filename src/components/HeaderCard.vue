<template>
  <div class="container-card">
    <div class="discs">
      <img :src="disc.poster" />
      <h5>{{ dischi.title }}</h5>
      <p>
        {{ dischi.author }}
        <br />
        {{ dischi.year }}
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