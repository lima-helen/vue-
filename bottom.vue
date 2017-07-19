<template>
    <div>{{showFlag}}</div>
</template>
<script>
    export default {
        props:['showFlag'],
        data(){
        return {
            isShow:false
        }
    },

    watch:{

        showFlag:function(){
            this.isShow=true;
        }
    }

    }
</script>


