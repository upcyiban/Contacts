<template>
  <div id="HelloWorld" class="whole">
   <dl>
        <dt v-for="message in messages " class ="hide">
          <span>{{ message.jobname }}</span>
          <hr>
          <dl class="show">
            
              <dt v-for="job in message.joblist">
                <div >
                  {{ job.name }}
                <br>
                  {{job.number}}
                <hr style="height:1px;border:none;border-top:1px dashed #06c">
                </div>
              </dt>
            
          </dl>
        </dt>
      </dl>
<!--       <dl>
        <dt v-for="option in options ">
          <span id="location">
            {{ option.name }}
          </span>
         </dt>
    </dl> -->
  </div>
</template>

<script>
import Vue from 'vue'
import axios from 'axios'
export default {
  name: 'HelloWorld',
  data () {
   return {
    messages: []
    }
  },
  created(){

  this.showunit()


  },
   methods:{
     showunit:function(){
       axios.get('http://yb.upc.edu.cn:8087/contacts/all').then(response=>{
       this.messages = response.data
        console.log('1')
      })
 
    },
/*test:function(){
    console.log(this)
}*/
  }

}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.show{
  display: none;
  background-color: #AFEEEE;
  opacity: 0.8;

}
.hide:hover .show{
  display: block;
}
.hide{
   padding-left: 3%;
   padding-right: 3%;
}
.whole{
  border-color: white;
  border:5px;
  background-color:#E6E6FA;
  margin-bottom: 0;
  padding-top: 2%;
  opacity: 0.8;
  margin-top: 2%;
}
</style>
