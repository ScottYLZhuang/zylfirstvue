<template>
    <div id="mustacheSyntax" style="margin-left:300px;">
            <p><span class="profile">变量：</span>{{num}}</p>
            <p><span class="profile">表达式</span>{{5+10}}</p>
            <p><span class="profile">三元运算：</span>{{flag ? 15:10}}</p>
            <p><span class="profile">函数：</span>{{getNum()}}</p>
            <p><span class="profile">函数对象：</span>{{getNum}}</p>
            <p><span class="profile">html代码（表达式）：</span>{{'<span>15</span>'}}</p>
            <p><span class="profile">html代码（变量）：</span>{{num}}</p>
            <p><span class="profile">匿名函数：</span>{{(()=>5+10)()}}</p>
    </div>
</template>
<script>
export default {
    name:"fileMustaches",
    data(){
        return{
            num:15,
            flag:false,
            html:'<span>15</span>'
        }
    },
    methods:{
        getNum(){
            return this.num
        }
    }
}
</script>
<style>
.profile{
    display: inline-block;
    width: 300px;
}
</style>