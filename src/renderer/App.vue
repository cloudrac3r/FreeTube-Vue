<template>
  <div id="app">
    <top-nav ref="topNav" />
    <side-nav ref="sideNav" />
    <Transition
      mode="out-in"
      name="slide-up"
    >
      <!-- <keep-alive> -->
      <RouterView
        ref="router"
        class="routerView"
        :class="{ expand: !isOpen }"
      />
      <!-- </keep-alive> -->
    </Transition>
  </div>
</template>

<script src="./App.js" />

<style src="./themes.css" />
<style src="./videoJS.css" />
<style scoped src="./App.css" />
