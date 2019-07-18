<template>
  <view >
   <text class="text-color-secondary">{{homeMessage}}</text>  
     <button title="Go to HomeScreen" :on-press="() => navigate('homeScreen')"/>
  </view>
</template>

<script>
 export default {
     props: {
       navigate: {
         type: Function,
         required: true,
       }
     },
    data(){
        return{
            homeMessage:'This is Screen 1',
        }
    },
  }
</script>
 


