<template>
  <layout>
    <x-nav slot="header" back="/" title="Switch"></x-nav>
    <x-body slot="body">
      <group title="default">
        <cell :arrow="false">
          <div slot="title">开关（{{checked}}）</div>
          <x-switch slot="value" v-model="checked"/>
        </cell>
      </group>
      <group title="offValue:0,onValue:1">
        <cell :arrow="false">
          <div slot="title">开关（{{value}}）</div>
          <x-switch slot="value" v-model="value" on-value="1" off-value="0" />
        </cell>
      </group>
      <group title="small">
        <cell :arrow="false">
          <div slot="title">开关（{{checked}}）</div>
          <x-switch small slot="value" v-model="checked"/>
        </cell>
      </group>
    </x-body>
  </layout>
</template>

<script>
import { children } from 'utils/mixins/page'
export default {
  mixins: [children],
  data () {
    return {
      checked: true,
      value: '0'
    }
  }
}
</script>
