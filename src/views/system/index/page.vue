<template>
  <d2-container class="page">
    <d2-page-cover>
      <d2-icon-svg class="logo" name="d2-admin"/>
      <template slot="footer">
        <div class="btn-group">
          <span class="btn-group__btn" @click="$open('http://lindechao.work')">作者</span> |
          <span class="btn-group__btn" @click="$open('https://github.com/a479292487/ldc_hxzh_admin.git')">文档（整顿中）</span> |
          <el-popover :width="172" trigger="hover">
            <p class="d2-mt-0 d2-mb-10">作者联系</p>
            <img src="./image/qr@2x.png" style="width: 172px;">
            <span slot="reference" class="btn-group__btn btn-group__btn--link">
              <d2-icon name="weixin"/>
            </span>
            <p style="font-size: 12px; margin-top: 0px; margin-bottom: 0px;">
            </p>
          </el-popover>
        </div>
        <!-- <d2-badge/> -->
        <d2-help/>
      </template>
    </d2-page-cover>
  </d2-container>
</template>

<script>
// import D2Badge from './components/d2-badge'
import D2Help from './components/d2-help'
import D2PageCover from './components/d2-page-cover'
export default {
  components: {
    // D2Badge,
    D2Help,
    D2PageCover
  }
}
</script>

<style lang="scss" scoped>
.page {
  .logo {
    width: 120px;
  }
  .btn-group {
    color: $color-text-placehoder;
    font-size: 12px;
    line-height: 12px;
    margin-top: 0px;
    margin-bottom: 20px;
    .btn-group__btn {
      color: $color-text-sub;
      &:hover {
        color: $color-text-main;
      }
      &.btn-group__btn--link {
        color: $color-primary;
      }
    }
  }
}
</style>
