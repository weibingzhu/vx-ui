<template>
  <layout>
    <x-nav slot="header" back="/" title="Flexbox"></x-nav>
    <x-body slot="body" class="flexbox-demos">
      <flexbox :gutter="10">
        <flexbox-item>
          <div class="flexbox-item">1</div>
        </flexbox-item>
        <flexbox-item>
          <div class="flexbox-item">2</div>
        </flexbox-item>
        <flexbox-item>
          <div class="flexbox-item">3</div>
        </flexbox-item>
      </flexbox>

      ### 跨度
      <flexbox :gutter="10">
        <flexbox-item>
          <div class="flexbox-item">1</div>
        </flexbox-item>
        <flexbox-item :flex="2">
          <div class="flexbox-item">2</div>
        </flexbox-item>
        <flexbox-item :flex="3">
          <div class="flexbox-item">3</div>
        </flexbox-item>
      </flexbox>

      ### 列布局
      <flexbox direction="column">
        <flexbox-item>
          <div class="flexbox-item">1</div>
        </flexbox-item>
        <flexbox-item style="margin:10px 0">
          <div class="flexbox-item">2</div>
        </flexbox-item>
        <flexbox-item>
          <div class="flexbox-item">3</div>
        </flexbox-item>
      </flexbox>
    </x-body>
  </layout>
</template>

<script>
import { children } from 'utils/mixins/page'
export default {
  mixins: [children]
}
</script>

<style lang="scss">
  .flexbox-demos{
    padding:10px;
    overflow:hidden;
    .flexbox-item{
      background:$color-primary;
      border-radius:6px;
      text-align:center;
      color:#fff;
      line-height:0.8rem;
    }
    .flex-wrap .flexbox-item{
      margin:5px 0;
    }
  }
</style>
