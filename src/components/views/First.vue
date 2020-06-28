<template>
    <div class="first-app">
        {{msg}}
        <confirm text="注册" @message="getMessage"></confirm>
        <p><router-link to="/second">去第二个页面</router-link></p>
    </div>
</template>

<script>
import Confirm from "../sub/Confirm";
export default {
    name:"First",
    components:{
        Confirm
    },
    data () {
        return {
            msg:"welcome to FirstApp"
        }
    },
    methods: {
        getMessage(val) {
            console.log(val);
        }
    }
}
</script>
<style>

</style>