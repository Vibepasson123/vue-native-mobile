<template>
  <view class="container">
    <text class="text-color-primary">{{test}}</text>
    
    <button
        :on-press="hello"
        title="Excuite"
        color="#841584"
        accessibility-label="Test the sample"
    />
    </view>
</template>
<script>
export default {
data:{
   test:45565656
 },

 mounted() {
   
 },

 methods: {
   hello(){
    if(this.test > 44){
     this.test +=1;
    }

   }
   
 },
}
</script>
 
<style>
.container {
  background-color: rgba(92, 88, 88, 0.438);
  align-items: center;
  justify-content: center;
  flex: 1;
}
.text-color-primary {
  color: blue;
}

</style>
