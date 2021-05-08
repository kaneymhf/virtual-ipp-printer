<template>
  <div id="app">

    <div id="nav">
      <router-link to="/">Device</router-link>
      <router-link to="/jobs">Jobs</router-link>
      <router-link to="/settings">Settings</router-link>
      <router-link to="/counters">Counters</router-link>
    </div>

    <div id="post-nav"></div>

    <router-view />
  </div>
</template>
