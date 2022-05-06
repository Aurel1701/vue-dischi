<template>
    <div class="box d-flex flex-wrap pt-5">
        <HeaderCard class="card-box" v-for="(component, index) in components"
        :key="index"
        :component="component"
        />
    </div>
</template>

<script>
import HeaderCard  from '@/components/HeaderCard.vue'
export default {
    components: {
    HeaderCard,
    },
    props:{
        components:Object,
    }
 
}
</script>


<style lang="scss" scoped>
.box{

    height: 100vh;
    background-color: #1E2D3B;

}
</style>