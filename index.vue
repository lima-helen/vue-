<template>
<div class="shuhe-content">
    <div class="nav-menu">
        <el-col :span="24">
            <el-menu default-active="2" class="el-menu-vertical-demo"  theme="dark" v-on:click.native="linkShow">
                <el-submenu index="2">
                    <template slot="title">水果</template>
                    <li><router-link to="/index/map" v-on:click.native="warnShow">苹果</router-link></li>
                    <li><router-link to="/index/map">西瓜</router-link></li>
                </el-submenu>

            </el-menu>
        </el-col>
    </div>
    <router-view  v-bind:showFlag="showFlag" name="bottom"></router-view>
</div>
</template>
<script type="text/ecmascript-6">
    export default{
        data(){
            return {
                showFlag:0,
            }
        },
        methods: {
            warnShow:function(){
                if(this.showFlag>10){
                    this.showFlag=0
                }
                this.showFlag++;
            }
        }
    }
</script>

