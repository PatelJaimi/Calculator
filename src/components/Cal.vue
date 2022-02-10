<template>
  <div>
      <h1>Calculator</h1>
    <table>
      <tr>
        <td colspan="2">
          <label for='first'> Enter first number </label>
        </td>
        <td colspan="2"> 
          <input type="text" v-model='a' id='first' />
        </td>
      </tr>
      <tr>
        <td colspan="2">
          <label for='second'>Enter second number </label>
        </td>
        <td colspan="2">
          <input type="text" v-model='b' id='second' />
        </td>
      </tr>
      <tr>
        <td>
          <button v-on:click="addnum()">Add</button>
        </td>
        <td>
          <button v-on:click="subnum()">Subtract</button>
        </td>
        <td>
          <button v-on:click="mulnum()">Multiply </button>
        </td>
        <td>
          <button v-on:click="divnum()">Division</button>
        </td>
      </tr>
      <tr>
          <td colspan="4">
              <p>Result : {{result}}</p>
          </td>
      </tr>
    </table>
  </div>
</template>

<script>

export default{
    name:'Calculator',
    data(){
        return{
            result:0,
            a:'',
            b:''
        }
    },
    methods:{
        addnum(){
            this.result=parseInt(this.a)+parseInt(this.b);
        },
        subnum(){
            this.result=parseInt(this.a)-parseInt(this.b);
        },
        mulnum(){
            this.result=parseInt(this.a)*parseInt(this.b);
        },
        divnum(){
            this.result=parseInt(this.a)/parseInt(this.b);
        }
    }
}
</script>

<style scoped>
    div{
        width: 50%;
        margin: 10px auto;
        box-shadow: 1px 1px 10px 5px #ccc;
        padding: 30px;
    }
    table{
        margin: 10px auto;
        width: 80%;
    }
    td{
        padding: 10px 20px;
        font-size: 18px;
    }
    input{
        padding: 5px 10px;
        width: 90%;
    }
    button{
        padding: 10px 20px;
        font-size: 18px;
        margin-top: 20px;
    }
</style>