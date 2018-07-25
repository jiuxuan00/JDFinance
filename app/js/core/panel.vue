<template>
  <div :class="[panelClass,cname]">
      <h4>-&nbsp;{{title}}&nbsp;-</h4>
      <slot></slot>
  </div>
</template>

<script>
export default {
    props:{
        cname:{
            type:String,
            default:''
        },
        title:{
            type:String,
            default:''
        }
    },
    data(){
        return {
            panelClass:'panel'
        }
    },
    components:{

    },
    methods:{

    },
    mounted(){

    }
}
</script>

<style lang="scss">
@import '../../css/element.scss';

.panel {
    @include panel;
    h4 {
        font-size: 26px;
    }
}
</style>
