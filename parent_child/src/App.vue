<template>
    <div class="container">
        <br>
        <br>
        <app-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-header>
        <app-new-quote @quoteAdded="NewQuote"></app-new-quote>
        <app-quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></app-quote-grid>
        <hr>
        <div class="row">
            <div class="col-sm-12 text-center">
                <div class="alert alert-info">
                    info:Click on Quote to delete
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue';
import newQuote from './components/NewQuote.vue';
import Header from './components/Header.vue';
export default{
    data:function(){
        return {
            quotes:["THIS IS MY FIRST QUOTE"],
            maxQuotes:10
        } 
          
},
components:{
    'app-quote-grid':QuoteGrid,
    'app-new-quote':newQuote,
    'app-header':Header
},
methods:{
    NewQuote(quote){
        if(this.quotes.length>=this.maxQuotes){
            return alert('please Delete quotes');
        }
        this.quotes.push(quote);

    },
    deleteQuote(index){
        this.quotes.splice(index,1);
    }

}
}
  
</script>

<style>
  
</style>
