<template>
  <div class="row justify-content-center p-3">
    <form action="">
      <div class="col-sm-12 col-sm-offset-12 col-xs-12 col-md-12 col-md-offset-6">
        <label for="">Quote</label>
        <textarea class="form-control" rows="2" cols="100" v-model="quote"></textarea>
      </div>
       <div class=" p-3 col-sm-12 col-sm-offset-12 col-xs-12 col-md-12 col-md-offset-6">
        <button class="btn btn-info" @click.prevent="createNew">Add Quote</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {

data(){
    return{
        quote:''
    }
},
methods:{
    createNew(){
        this.$emit('quoteAdded', this.quote);
        this.quote='';
    }
}

};
</script>

<style></style>
