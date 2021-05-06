<template>
  <div class="about">
    <h1>This is an about page</h1>
    <div>{{ $t('main.logo') }}</div>
    <input type="text"
           :placeholer="$t('auth.username')" />
  </div>
</template>
