<template>
  <header class="m_header">
    <span><slot /></span>
    <atoms-button class="t_icon">
      <i class="xi-bars"></i>
      <span class="ir">메뉴</span>
    </atoms-button>
  </header>
</template>

<style scoped>
.l_header {
  z-index: 0;
  position: sticky;
  top: 0;
  padding: 0 20px;
  display: flex;
  justify-content: flex-start;
  align-items: center;
  height: 60px;
}
</style>
