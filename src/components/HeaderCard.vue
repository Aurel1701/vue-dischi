<template>
  <div class="container-card">
    <div class=" discs">
      <img :src="component.poster" />
      <h5>{{ component.title }}</h5>
      <p>
        {{ component.author }}
        <br />
        {{ component.year }}
      </p>
    </div>
  </div>
</template>



<script>
export default {
  props: {
    component: Object,
  },
};
</script>


<style lang="scss" scoped>
.discs {
  color: white;
  text-align: center;
  img {
     padding: 10px;
    width: 200px;
    padding: 10px;
  }
  h5 {
    text-transform: uppercase;
    font-weight: bolder;
    font-size: 19px;
    margin-top: 6px;
  }
  p {
    color: grey;
    margin-top: 20px;
  }
}
</style>