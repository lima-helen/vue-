# vue-click-link
解决此问题方法

想要获取点击之后不同状态

  <template>
<div class="content">
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
index.vue
在这添加一个warnShow
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
再将这个值传给bottom.vue，在bottom中watch这个数值，然后想干啥就干啥，哈哈

Contact GitHub API Training Shop Blog About
© 2017 GitHub, Inc. Terms Privacy Security Status Help
