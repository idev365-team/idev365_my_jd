<template>
    <div class="dropdown">
        <a href="#">{{title}}</a>
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
    margin-right: 5px;
    a{
        text-decoration: none;
        line-height: 30px;
    }
}
</style>

