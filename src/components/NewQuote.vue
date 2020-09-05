<template>
  <div class="row">
    <form action="">
      <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3">
        <label for="">Quote</label>
        <textarea class="form-control" rows="3" v-model="quote"></textarea>
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
}

};
</script>

<style></style>
