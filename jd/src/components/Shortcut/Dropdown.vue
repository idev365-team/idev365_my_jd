<template>
    <div class="dropdown">

        <a class="menu-title" href="#">
            <i v-if="showIcon" class="icon"></i>
            <span :style="getTitleStyle">{{title}}</span>
            <i v-if="showRightDownIcon" class="icon downarrow"></i>
        </a>
        <div class="inner-panel" :style="getInnerPanelStyle">
            <slot></slot>
        </div>
    </div>
</template>


<script>
export default {
    name: "MenuItem",
    componentName: "MenuItem",
    props:{
        "title":{
            default:"下拉菜单"
        },
        "showIcon":{
            default:false,
        },
        "panelWidth":{
            default:300,
        },
        "titleFontColor":{},
        "showRightDownIcon":{
            default:false,
        },
        "isPanelDirectionLeft":{
            default:true, //left, right
        },
        "panelStyle":{

        }
    },
    computed:{
        getInnerPanelStyle(){
            return [{
                width:this.panelWidth+"px",
                left:this.isPanelDirectionLeft&&"0px",
                right:(!this.isPanelDirectionLeft)&&"5px",
            },this.panelStyle]
        },
        getTitleStyle(){
            return {
                color:this.titleFontColor,
            }
        }
    }
}
</script>

<style lang="scss" scoped>
.dropdown{
    display: inline-block;
    z-index: 10;
    position: relative;
    .menu-title{
        
        display: inline-block;
        margin-right: 5px;
        padding:0 10px;
        border:solid 1px transparent;
        border-bottom: 0;
        
        text-decoration: none;
        line-height: 30px;
        .icon{
            font-style: normal;
            font-family: iconfont;
            font-size: 14px;
            color: #f10215;
            margin-right: 4px; 
            &.downarrow{
                color:#999;
            }
        }
    }

    .inner-panel{
        z-index: -1;
        padding:10px;
        position: absolute;
        top:30px;
        width:300px;
        min-height:50px;
        background-color: white;
        border:solid 1px #ccc;
        display: none;
        box-shadow: 1px 2px 1px rgba(0,0,0,.1);
    }

    &:hover{
        .menu-title{
            background-color: white;
            border:solid 1px #ccc;
            border-bottom:none;
        }
        .inner-panel{
            display: block;
        }
    }
}
</style>

