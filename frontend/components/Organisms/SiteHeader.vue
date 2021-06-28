<template>
  <div class="l_header">
    <atoms-button class="t_icon">
      <i class="xi-bars"></i>
      <span class="ir">메뉴</span>
    </atoms-button>
    <a href="#a">Chansoo's Web</a>
    <atoms-button class="t_icon">
      <i class="xi-search"></i>
      <span class="ir">검색</span>
    </atoms-button>
    <atoms-button class="t_icon">
      <i class="xi-ellipsis-v"></i>
      <span class="ir">기능 더보기</span>
    </atoms-button>
  </div>
</template>

<style lang="scss" scoped>
.l_header {
  position: fixed;
  top: 0;
  padding: 0 20px;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  height: 60px;
  & > a {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: trnaslate(-50%, -50%);
  }
}
</style>
