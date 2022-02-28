<template>
  <header>
      <h1>Income Tracker</h1>
      <div class="totalincome">{{totalIncome}} DH</div>
  </header>
</template>

<script>
export default {
props:{
    totalIncome : Number
}
}
</script>

<style lang="scss" scoped>

header{
    display: flex;
    justify-content: space-between;
    background-color: crimson;
    padding: 20px;
    border-bottom: 5px solid black;

    h1{
        color: white;
    }

    .totalincome{
        color: black;
        background-color: darkgrey;
        border-radius: 8px;
        min-width: 100px;
        text-align: center;
        font-weight: bold;
        padding: 10px;
        font-size: 20px;
        font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
        border: 5px solid black;
    }

}

</style>