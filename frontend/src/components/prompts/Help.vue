<template>
  <div class="card floating help">
    <div class="card-title">
      <h2>{{ $t('help.help') }}</h2>
    </div>

    <div class="card-content">
      <p><strong>F1</strong> - {{ $t('help.f1') }}</p>
      <p><strong>F2</strong> - {{ $t('help.f2') }}</p>
      <p><strong>DEL</strong> - {{ $t('help.del') }}</p>
      <p><strong>ESC</strong> - {{ $t('help.esc') }}</p>
      <p><strong>CTRL + S</strong> - {{ $t('help.ctrl.s') }}</p>
      <p><strong>CTRL + F</strong> - {{ $t('help.ctrl.f') }}</p>
      <p><strong>CTRL + Click</strong> - {{ $t('help.ctrl.click') }}</p>
      <p><strong>Click</strong> - {{ $t('help.click') }}</p>
      <p><strong>Double click</strong> - {{ $t('help.doubleClick') }}</p>
    </div>

    <div class="card-action">
      <button type="submit"
        @click="$store.commit('closeHovers')"
        class="button button--flat"
        :aria-label="$t('buttons.ok')"
        :title="$t('buttons.ok')">{{ $t('buttons.ok') }}</button>
    </div>
  </div>
</template>

<script>
export default { name: 'help' }
</script>

