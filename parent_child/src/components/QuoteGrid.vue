<template>
    <div class="row">
        <app-quote v-for="(quote,index) in quotes" v-bind:key="quote" @click.native="deleteQuote(index)" >
            {{quote}}
        </app-quote>
        <!-- <h2 v-for="quote in quotes" :key="quote">{{quote}}</h2> -->
    </div>
</template>
<script>
    import Quote from './Quote.vue'
export default {
    props:['quotes'],
    components:{
        'app-quote':Quote
    },
    methods:{
        deleteQuote(index){
            this.$emit('quoteDeleted',index);

        }
    }
    
}
</script>
<style>

</style>