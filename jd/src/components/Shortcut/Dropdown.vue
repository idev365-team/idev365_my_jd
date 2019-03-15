<template>
    <div class="dropdown">

        <a class="menu-title" href="#">
            <i class="icon"></i>
            {{title}}
        </a>
        <div class="inner-panel">
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
        }
    }
}
</script>

<style lang="scss">
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
        }
    }

    .inner-panel{
        z-index: -1;
        padding:10px;
        position: absolute;
        top:30px;
        left:0;
        width:300px;
        height:200px;
        background-color: white;
        border:solid 1px #ccc;
        display: none;
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

