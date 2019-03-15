<template>
  <div class="shortcut">
    <div class="w">
      <div class="fl">
        <Dropdown class="my-city" title="上海">
          <ul class="city-menus">
            <li><a>北京</a></li>
            <li class="active"><a>上海</a></li>
            <li><a>天津</a></li>
            <li><a>重庆</a></li>
            <li><a>河北</a></li>
            <li><a>山西</a></li>
            <li><a>河南</a></li>
            <li><a>辽宁</a></li>
            <li><a>吉林</a></li>
            <li><a>黑龙江</a></li>
            <li><a>内蒙古</a></li>
            <li><a>江苏</a></li>
            <li><a>山东</a></li>
            <li><a>安徽</a></li>
            <li><a>浙江</a></li>
            <li><a>福建</a></li>
            <li><a>湖北</a></li>
            <li><a>湖南</a></li>
            <li><a>广东</a></li>
            <li><a>广西</a></li>
            <li><a>江西</a></li>
            <li><a>四川</a></li>
            <li><a>海南</a></li>
            <li><a>贵州</a></li>
            <li><a>云南</a></li>
            <li><a>西藏</a></li>
            <li><a>陕西</a></li>
            <li><a>甘肃</a></li>
            <li><a>青海</a></li>
            <li><a>宁夏</a></li>
            <li><a>新疆</a></li>
            <li><a>港澳</a></li>
            <li><a>台湾</a></li>
            <li><a>钓鱼岛</a></li>
            <li><a>海外</a></li>
          </ul>
        </Dropdown>
      </div>
      <div class="fr">
        <MyLogin/>
        <Split/>
        <MenuItem title="我的订单"/>
        <Dropdown title="我的京东"/>
        <Split/>
        <MenuItem title="京东会员"/>
        <Split/>
        <Dropdown title="企业采购"/>
        <Split/>
        <Dropdown title="客户服务"/>
        <Split/>
        <Dropdown title="网站导航"/>
        <MenuItem title="手机京东"/>
      </div>
    </div>
  </div>
</template>

<script>
import MyLogin from '@/components/Shortcut/MyLogin.vue';
import Dropdown from '@/components/Shortcut/Dropdown.vue';
import MenuItem from '@/components/Shortcut/MenuItem.vue';
import Split from '@/components/Shortcut/Split.vue';

export default {
  name: 'Shortcut',
  components:{
    MyLogin,
    Dropdown,
    MenuItem,
    Split,
  }
}
</script>

<style lang="scss">
.shortcut{
  height:30px;
  background-color: #e3e4e5;
  .w{
    width:1190px;
    border: solid 1px red;
    height:30px;
    margin:auto;
  }
  .fl{
    float:left;
  }
  .fr{
    float:right;
  }
  .my-city{
    margin-left: 200px;
    .city-menus{
      margin:0;
      padding: 0;
      li{
        float: left;
        width:60px;
        list-style: none;
        a{
          display:inline-block;
          width:40px;
          line-height: 24px;
          text-align: center;
          &:hover{
              color: #e33333;
              background-color: #f4f4f4;
          }
        }
        &.active{
          a{
            background-color: #f10215;
            color: #fff;   
          }
        }
      }
    }
  }
}
</style>
