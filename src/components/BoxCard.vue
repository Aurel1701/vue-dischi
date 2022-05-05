<template>
    <div class="box">
        <header-card v-for="(component, index) in components"
        :key="index"
        :disc="dischi"
        />
    </div>
</template>

<script>
import HeaderCard from './HeaderCard.vue'
export default {
    components: {
    HeaderCard,
    },
    props:{
        discs: Array,
    }
 
    
}
</script>


<style lang="scss" scoped>

</style>