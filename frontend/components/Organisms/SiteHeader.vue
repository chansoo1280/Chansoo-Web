<template>
  <div class="l_header" :class="{ s_hide: hide }">
    <nav>
      <a class="ir" href="#contents">본문 바로가기</a>

      <div>
        <atoms-button class="t_icon">
          <i class="xi-search"></i>
          <span class="ir">검색</span>
        </atoms-button>
        <atoms-button class="t_icon">
          <i class="xi-ellipsis-v"></i>
          <span class="ir">기능 더보기</span>
        </atoms-button>
      </div>
    </nav>
    <header>
      <atoms-button class="t_icon">
        <i class="xi-bars"></i>
        <span class="ir">메뉴</span>
      </atoms-button>
      <a href="#a">Chansoo's Web</a>
    </header>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  data() {
    return {
      hide: false,
      scrollTop: 0,
    }
  },
  mounted() {
    const wrap = document.querySelector('.l_wrap')
    wrap?.addEventListener('scroll', () => {
      this.hide = wrap.scrollTop > 260 && this.scrollTop < wrap.scrollTop
      this.scrollTop = wrap.scrollTop
    })
  },
})
</script>

<style lang="scss" scoped>
@mixin abs-center {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
.l_header {
  transition: top 0.3s ease;
  position: sticky;
  top: -200px;
  padding: 200px 0 0;
  background: #fff;
  &.s_hide {
    top: -260px;
    & > nav {
      top: -60px;
    }
  }
  & > nav {
    z-index: 9;
    transition: top 0.3s ease;
    position: fixed;
    top: 0;
    right: 0;
    display: flex;
    justify-content: flex-end;
    align-items: flex-start;
    height: 60px;
    & > div {
      padding: 0 20px;
      display: flex;
      justify-content: flex-end;
      align-items: center;
      height: 60px;
    }
  }
  & > header {
    position: relative;
    padding: 0 20px;
    display: flex;
    justify-content: flex-start;
    align-items: center;
    height: 60px;
    & > a {
      @include abs-center;
    }
  }
}
</style>
