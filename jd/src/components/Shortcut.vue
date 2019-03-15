<template>
  <div class="shortcut">
    <div class="w">
      <div class="fl">
        <MyCityDropDown/>
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
import MyCityDropDown from '@/components/Shortcut/DropDownMyCity.vue';

export default {
  name: 'Shortcut',
  components:{
    MyLogin,
    Dropdown,
    MenuItem,
    Split,
    MyCityDropDown,
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
}
</style>
