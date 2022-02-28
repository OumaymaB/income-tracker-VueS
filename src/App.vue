<template>
  <div>
    <Header :totalIncome="addIncomes"/>
    <Form @incomeMethode="add"/>
    <IncomeList :incomeList="incomes"/>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Form from './components/Form.vue'
import IncomeList from './components/IncomeList.vue'

export default {
  data() {
    return {
      incomes: [],
    };
  },
  computed: {
    addIncomes(){
      let sum =0;
      if(this.incomes.length > 0){
        for(let i=0; i<this.incomes.length; i++ ){
          sum = sum + this.incomes[i].value;
        }
      }
      return sum;
    }
  }
  ,
  components: {
    Header,
    Form,
    IncomeList
  },
  methods:{
    add(data){
      this.incomes = [...this.incomes,data];
    }
  },
  created(){
    this.incomes=[
      {
        id: "id01",
        desc : "train",
        value : 20,
        date : "2022/02/28"
      }
    ]
  }
};
</script>

<style lang="scss">
* {
  box-sizing: border-box;
  margin: 0%;
}

body {
  background-color: #DAD8DE;
}
</style>
