<template>
  <div id="wrapper">
    <nav>
        <a v-link="{path : '/hello',activeClass:'active',exact: true}">hello</a>
        <a v-link="{path : '/user',activeClass:'active',exact: true}">user</a>
        <a v-link="{path : '/world',activeClass:'active',exact: true}">world</a>
    </nav>
    <router-view
      class="view"
      keep-alive
      transition
      transition-mode="out-in">
    </router-view>
  </div>
</template>
<style lang="less">
.view {
  position: absolute;
  background-color: #eee;
  width: 100%;
  transition: opacity .2s ease;
  box-sizing: border-box;
  padding: 8px 20px;
  &.v-enter, &.v-leave {
    opacity: 0;
  }
}
</style>
