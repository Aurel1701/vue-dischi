<template>
    
    <div class="select-box d-flex pt-4">
        <select v-model="selected" @change="$emit('selectedGenere', selected)" class="">
           <option disabled value="">Select genere</option>
           <option v-for="(genere, index) in values" :key="index" :value="genere">{{genere}}</option>
        </select>
    </div>
       
        
    
</template>

<script>
export default {
    props: {
        values: Array,
    },
    data(){
        return{
            selected: ''
        }
        
    }
    
}
</script>


<style lang="scss" scoped>
</style>