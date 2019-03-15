<template>
    <div class="mylogin">
        <a href="#">你好，请登录
            <span>免</span>...
        </a>
    </div>
</template>

<style lang="scss">
.mylogin{
    display: inline-block;
    margin-right: 5px;
    a{
        text-decoration: none;
        line-height: 30px;
        &:hover{
            color:#e33333;
        }
        & > span {
            color:#f10215;
        }
    }
}
</style>

