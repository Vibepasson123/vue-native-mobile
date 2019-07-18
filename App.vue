<template>
 <view class="container">
   <HomeScreen v-if="activeScreen ==='homeScreen'"
              :testingData="testingData" :navigate="navigate" />
   <Screen1 v-if="activeScreen === 'Screen1'"
             :navigate="navigate"  />
  </view>
</template>

<script>
  import HomeScreen from '@/screens/HomeScreen'
  import Screen1 from '@/screens/Screen1'
  export default {
    components:{
      HomeScreen,
      Screen1
    },
    data() {
      return {
        activeScreen: 'homeScreen',
        testingData: 'this is just for testing',
      }
    },
    methods: {
      navigate (screen) {
        this.activeScreen = screen
        	
       /*  BackHandler.addEventListener('hardwareBackPress', navigate()); */
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
    .text-color-secondary {
    color:#a947b0;
    font-size: 30px;
    padding-left:35px;
    }

</style>
