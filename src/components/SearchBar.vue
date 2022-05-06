<template>
    <div class="ricerca d-flex justify-content-center pt-2">
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
.ricerca{
    text-aling:center;
    background-color:rgba(46, 58, 70, 1);
}
</style>