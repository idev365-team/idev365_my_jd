<template>
    <Dropdown 
                class="my-jd" 
                title="企业采购" 
                titleFontColor="red"
                :showRightDownIcon="true" 
                :panelWidth="157"
            >
          <ul class="site-list">
              <li class="item">
                  <span>企业购</span>
              </li>
              <li class="item">
                  <span>商用场景馆</span>
              </li>
              <li class="item">
                  <span>工业品</span>
              </li>
              <li class="item">
                  <span>礼品卡</span>
              </li>
          </ul>
        </Dropdown>
</template>

<script>
import Dropdown from '@/components/Shortcut/Dropdown.vue';
export default {
    name: "DropDownMyCity",
    components:{
        Dropdown,
    }
}
</script>


<style lang="scss">
.my-jd{
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
      &::after{
          display: block;
          content: "";
          clear: both;
      }
    }

    .split{
        height:1px;
        background-color: #eee;
        margin:5px 0;
    }
    .row-title{
        margin: 9px 0;
        color: #8f8f8f;
    }

    .site-list{
        margin:0;
        padding:0;
        &::after{
            display: block;
            content: "";
            clear: both;
        }
        .item{
            list-style: none;
            width:50%;
            float: left;
            line-height: 26px;
            color: #8f8f8f;
            .flag-icon{
                display: inline-block;
                height: 12px;
                width: 15px;
                background-repeat: no-repeat;
                background-image: url(data:image/png;base64,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);
                margin-right:5px;
                &.global{
                    background-size: 50px 24.5px;
                    background-position: 0 0;
                }
                &.russia{
                    background-size: 50px 24.5px;
                    background-position: -17.5px 0;
                }
                &.indonesia{
                    background-size: 50px 24.5px;
                    background-position: 0 -14.5px;
                }
                &.spain{
                    background-size: 50px 24.5px;
                    background-position: -35px 0;
                }
                &.thailand{
                    background-size: 50px 24.5px;
                    background-position: -17.5px -14.5px;
                }

            }
        }
    }
  }
</style>


