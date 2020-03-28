<template>
    <div class="row">
        <form>
       <div class="col-12 form-group  form-group">
           <label>Quote</label>
           <textarea class="form-control " rows="5"  width=" 40px" v-model="quote">
           </textarea>
       </div>
       <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
           <div class="btn btn-primary" @click.prevent="createNew">Add Quotes</div>
                
       </div>
       </form>
    </div>
</template>
<script>
 
export default {

    data:function(){
        return{
            quote:''
        }
    },
    methods:{
        createNew(){
            this.$emit('quoteAdded',this.quote);
            this.quote=''
        }
    }
}
</script>
<style>

</style>