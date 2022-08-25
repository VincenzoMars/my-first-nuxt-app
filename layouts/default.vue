<template>
  <div>
    <header class="main-header">
      <ul class="nav">
        <li class="nav-link">
          <nuxt-link to="/admin">Admin</nuxt-link>
        </li>
        <li class="nav-link">
          <nuxt-link to="/posts">Posts</nuxt-link>
        </li>
        <li class="nav-link">
          <nuxt-link to="/about">About</nuxt-link>
        </li>
      </ul>
    </header>
    <Nuxt />
  </div>
</template>