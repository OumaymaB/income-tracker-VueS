<template>
  <form @submit.prevent="formHandler" id="form">
    <input type="text" placeholder="Description" v-model="this.Data.desc"/>
    <input type="number" placeholder="DH" v-model="this.Data.value"/>
    <input type="date" v-model="this.Data.date"/>
    <input type="submit" value="Submit" id="submit" />
  </form>
</template>

<script>
export default {
    data(){
        return{
            Data : {
                desc : null,
                value: null,
                date: null
            },
            
        }
    },
    methods:{
formHandler(){
  const newIncom = {
        id: new Date().toString(),
        desc : this.Data.desc,
        value: this.Data.value,
        date : this.Data.date
    }
    this.$emit('incomeMethode',newIncom);
    this.Data.desc = null;
    this.Data.value = null;
    this.Data.date = null;
}
    }
};
</script>

<style lang="scss" scoped>

#form{

  display: flex;
    justify-content: center;
    margin-top: 30px; 
    
     input {
    color: #888;
    outline: none;
    font-size: 20px;
    display: flex;
    justify-content: space-between;
  }

    #submit {
display: block;
    color: #FFF;
    font-weight: 500;
    text-shadow: 0px 1px 3px rgba(0, 0, 0, 0.2);
    padding: 5px 15px;
    background-color: crimson;
    border-radius: 10px;
  }


}
</style>