<template>
  <div class="col-sm-6 col-md-4 col-lg-3 text-center">
    <div class="panel panel-default border">
      <div class="panel-body quote p-3">
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.panel-body {
  font-family: "Arizonia", cursive;
  font-size: 24px;
  color: rgb(89, 197, 131);
}

.quote {
  cursor: pointer;
}

.quote:hover {
  background-color: rgb(219, 200, 200);
}
</style>
