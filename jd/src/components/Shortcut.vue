<template>
  <div class="shortcut">
    <div class="w">
      <div class="fl">
        <DropDownMyCity/>
      </div>
      <div class="fr">
        <MyLogin/>
        <Split/>
        <MenuItem title="我的订单"/>
        <Split/>
        <DropDownMyJD/>
        <Split/>
        <MenuItem title="京东会员"/>
        <Split/>
        <DropDownEntityBuy/>
        <Split/>
        <DropDownCustomerService/>
        <Split/>
        <DropDownSiteNav/>
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
import DropDownMyCity from '@/components/Shortcut/DropDownMyCity.vue';
import DropDownMyJD from '@/components/Shortcut/DropDownMyJD.vue';
import DropDownEntityBuy from '@/components/Shortcut/DropDownEntityBuy.vue';
import DropDownCustomerService from '@/components/Shortcut/DropDownCustomerService.vue';
import DropDownSiteNav from '@/components/Shortcut/DropDownSiteNav.vue';

export default {
  name: 'Shortcut',
  components:{
    MyLogin,
    Dropdown,
    MenuItem,
    Split,
    DropDownMyCity,
    DropDownMyJD,
    DropDownEntityBuy,
    DropDownCustomerService,
    DropDownSiteNav
  }
}
</script>

<style lang="scss">
.shortcut{
  height:30px;
  background-color: #e3e4e5;
  .w{
    width:1190px;
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
