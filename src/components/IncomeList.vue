<template>
  <div class="income-list">
    <IncomeItem v-for="data in incomeList" :key="data.id" :income="data"/>  
  </div>
</template>

<script>
import IncomeItem from './IncomeItem.vue'
export default {
  props:{
incomeList : [],
  },
components:{
  IncomeItem
}
}
</script>

<style>

</style>