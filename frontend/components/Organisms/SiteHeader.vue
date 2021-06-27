<template>
  <header class="l_header">
    <atoms-button class="t_icon">
      <i class="xi-search"></i>
      <span class="ir">검색</span>
    </atoms-button>
    <atoms-button class="t_icon">
      <i class="xi-ellipsis-v"></i>
      <span class="ir">기능 더보기</span>
    </atoms-button>
  </header>
</template>

<style scoped>
.l_header {
  position: sticky;
  top: 0;
  padding: 0 20px;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  height: 60px;
}
</style>
