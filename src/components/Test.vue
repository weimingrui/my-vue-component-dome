<template>
  <div class="hello">
    <h2>Refund Reason</h2>
    <ul class="reason-box">
      <li class="level1" v-for="item1 in list" :key="item1.title">
        {{item1.title}}
        <ul class="level2" >
           <li v-for="item2 in item1.child_refund_reason" :key="item2.title">
             {{item2.title}}
            <ul class="level3" v-for="item3 in item2.child_refund_reason" :key="item3.title">
              <li>{{item3.title}}</li>
            </ul>
          </li>
        </ul>
      </li>
    </ul>
  </div>
</template>

<script>
import List from './refuned_reason.json'
export default {
  name: 'HelloWorld',
  data () {
    return {
      list: List
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.reason-box{

padding: 40px;
}
h1, h2 {
  font-weight: normal;
}
ul {
  /* list-style-type: none; */
  padding: 0;
  text-align: left;
  margin-top: 10px;
}
li {
  /* display: inline-block; */
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
