<template>
    <div class="box">
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
    padding-top: 30px;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: space-evenly;
    
    
    background-color: #1E2D3B;
    .card-box{
        
        margin: 10px;
        width: 200px;
        height: 350px;
        background-color:rgba(30, 45, 59, 1) ;
        
    }
}
</style>