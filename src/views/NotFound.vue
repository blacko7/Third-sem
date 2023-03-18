<template>
    <div class="not-found">
      <h1>404</h1>
      <p>Page does not exist</p>
      <router-link :to="{name: 'CounterView'}">
        Counter page
      </router-link>
    </div>
  </template>
  