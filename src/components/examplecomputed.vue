<template>
    <div id="useComputed">
        <p class="data-label"><strong>A</strong><input type="text" v-model="avalue"></p>
        <p class="data-label"><strong>B</strong><input type="text" v-model="bvalue"></p>
        <p class="data-label"><strong>C=A*2+1=</strong>{{cvalue}}</p>
        <p class="data-label"><strong>D=A+B*2=</strong>{{dvalue}}</p>
        <p class="data-label"><strong>E=B/2+12=</strong>{{evalue}}</p>
        <p class="data-label"><strong>F=A+B=</strong>{{fvalue}}</p>
        <p class="data-label"><strong>G=C-D=</strong>{{gvalue}}</p>
    </div>
</template>
<script>
export default {
    name:"computed",
    data(){
        return{
            avalue:3,
            bvalue:4
        }
    },
    computed:{ //直接处理属性值 不接收参数,以一种值/属性方式调用
        cvalue(){
            return this.avalue*2+1
        },
        dvalue(){
            return this.avalue+this.bvalue*2
        },
        evalue(){
             return this.bvalue/2+12
        },
        fvalue(){
             return this.avalue+this.bvalue
        },
        gvalue(){
             return this.cvalue-this.dvalue
        }
    }
}
</script>
<style>
 #useComputed{
     font-family: Roboto,sans-serif;
     color: #363e4f;
 }
 .data-label{
     display:inline-block;
     width: 160px
 }
</style>