<template>
    <div class="box">
        <HeaderCard v-for="(component, index) in components"
        :key="index"
        :component="components"
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
        components: Array,
    }
 
    
}
</script>


<style lang="scss" scoped>

</style>