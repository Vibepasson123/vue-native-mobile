<template>
    <view>
        <text class="text-color-primary">{{message}}</text>
        <button :title="btnMessage" :on-press="handleClick"/>
        <text class="text-color-secondary">{{clickedCount}}</text>
        <text>{{clickFun}}</text>
    </view>
    
</template>
<script>
    export default {
        data() {
            return {
                message:'Welcome Vivek',
                btnMessage:'Click Me',
                clickedCount: 0,
            }
        },
        computed: {
           clickFun () {
               if (this.clickedCount < 5) {
                    return 'Please keep clicking';
               } else {
                   alert(`Wow you passed the test by clicking more than ${this.clickedCount} :-)`)
                    return 'Great Job!';
               }
           } 
        },
        methods: {
            handleClick () {
                this.btnMessage = 'Clicked';
                this.clickedCount++;
               /*  alert(`I am Clicked! by ${this.clickedCount} numbers`); */
                
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
  color:#1aff8c;
}
.text-color-secondary {
  color:#a947b0;
  font-size: 30px;
  padding-left:35px;
}

</style>


