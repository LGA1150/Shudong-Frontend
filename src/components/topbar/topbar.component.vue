<template lang='pug'>
  .topbar
    .left
      .btn(@click='toggleMenu')
        .pull-left(v-if='!hiddenMenu')
          v-icon(type='menu-fold')
        .pull-right(v-else)
          v-icon(type='menu-unfold')
      .brand Chun-Ge 树洞
      .current-page-content {{ topbarText }}
      v-input.search-box(style='width: 200px'
        icon='search' size='large'
        placeholder='搜索树洞帖子'
        @onPressIcon='onPressIcon')
    .right
      .logout-wrapper
        logoutComponent
      .notification
        .noMsg(v-if='!hasMsg')
          v-icon(type='notification')
        .hasMsg(v-else)
          v-badge(dot)
            v-icon(type='notification')
</template>

<script src='./topbar.component.ts' lang='ts'></script>
<style src='./topbar.component.styl' lang='stylus' scoped></style>
