<template>
  <view class="container">
   <text class="text-color-secondary">{{homeMessage}}</text>  
    <text class="text-color-primary">{{test}}</text> 
      <text class="text-color-secondary">{{testingData}} </text>  
      <button
        :on-press="hello"
        title="Excuite"
        color="#841584"
        accessibility-label="Test the sample"
      /> 
    <Hello/>
    <button title="Go to Screen 1" :on-press="() => navigate('Screen1')"/>
  </view>
</template>

<script>
import Hello from '@/components/Hello'
export default {
  components:{
    Hello
  },
  props: {
      testingData: {
          type: String,
          required: true,
      },
      navigate: {
          type: Function,
          required: true,
      }
  },
  data(){
    return{
        test:45565656,
        homeMessage:'This is home message screen on click',
      }
    },

  methods: {
   hello(){
      if(this.test > 44){
      this.test +=1;
       }
      }
    },

    mounted() {
      
    },
}
</script>
 

