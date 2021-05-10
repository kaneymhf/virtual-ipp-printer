<template>
  <div id="app">

    <div id="nav">
      <router-link to="/">Device</router-link>
      <router-link to="/jobs">Jobs</router-link>
      <router-link to="/settings">Settings</router-link>
      <router-link to="/counters">Counters</router-link>

      <div id="post-nav"></div>

    </div>

    <router-view />
  </div>
</template>
