
<template>
    <div>
         {{title}}{{dataTime}}
        <button @click="changeTitle()">改变title</button>
        <button @click="destoryTitle()">销毁实例</button>
    </div>   
</template>

<script>
export default {
    name:'firstVue',
    data(){
        return{
            title:'ZHUANG YI LIANG FIRST VUE COMPONENTS'
        }
    },
    props:{
        dataTime:Date
    },
    methods:{
        changeTitle(){
            this.title=['zhuangyiliang','chenxi','chenyizhuang','zhuangchenliang'][Math.floor(Math.random()*2.999)]+'FIRST VUE COMPONENTS'
        },
        destoryTitle(){
            this.$destroy();
        },
        //实例初始化之后,数据观测和事件绑定之前
        beforeCreate(){
             /* eslint-disable */
            console.log('before create',this.dataTime);
        },
        //实例初始化完成，挂载尚未开始时
        created(){
            /* eslint-disable */
            console.log('created')
        },
        //挂载之前，render函数首次被调用时
        beforeMount(){
            console.log('before beforeMountMount')
        },
        //
        mounted (){
            console.log('mounted');
        },
        beforeUpdate(){
            console.log('before Update');
        },
        updated(){
             console.log('updated');
        },
        beforeDestory(){
             console.log('before Destory');
        },
        destroyed(){
             console.log('destroyed');
        },
    }
}
</script>