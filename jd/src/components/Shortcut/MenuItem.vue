<template>
    <div class="menu-item">
        <a href="#">{{ title }}</a>
    </div>
</template>

<script>
export default {
    name: "MenuItem",
    componentName: "MenuItem",
    props:{
        "title":{
            default:"菜单名称"
        }
    }
}
</script>


<style lang="scss">
.menu-item{
    display: inline-block;
    margin:0 5px;
    a{
        text-decoration: none;
        line-height: 30px;
        &:hover{
            color:#e33333;
        }
    }
}
</style>

