<template>
  <div>
    <h3>{{ $t('settings.userCommands') }}</h3>
    <p class="small">{{ $t('settings.userCommandsHelp') }} <i>git svn hg</i>.</p>
    <input class="input input--block" type="text" v-model.trim="raw">

    <p><input type="checkbox" v-model="perm.executeAny"> {{ $t('settings.perm.executeAny') }}</p>
  </div>
</template>

<script>
export default {
  name: 'permissions',
  props: ['commands', 'perm'],
  computed: {
    raw: {
      get () {
        return this.commands.join(' ')
      },
      set (value) {
        this.$emit('update:commands', value.split(' '))
      }
    }
  }
}
</script>
