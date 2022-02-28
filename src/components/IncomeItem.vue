<template>
<div class="card">
  <div class="container">
    <h4><b>{{income.date}}</b></h4> 
    <p>{{income.desc}} | {{income.value}}dh </p> 
  </div>
</div>
  
</template>

<script>
export default {
props :{
    income : Object,
}
}
</script>

<style>
.card {
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
  width: 20%;
  background-color: white;
  margin-left: 40%;
  margin-top:30px;
}

.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}

.container {
  padding: 2px 16px;
}

.button1 {
  background-color: white; 
  color: black; 
  border: 2px solid red;
}
</style>