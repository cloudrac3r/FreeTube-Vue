<template>
  <div
    class="topNav"
    :class="{ topNavBarColor: barColor }"
  >
    <font-awesome-icon
      class=" menuIcon navIcon"
      icon="bars"
      @click="toggleSideNav"
    />
    <font-awesome-icon
      class="navBackIcon navIcon"
      icon="arrow-left"
      @click="historyBack"
    />
    <font-awesome-icon
      class="navForwardIcon navIcon"
      icon="arrow-right"
      @click="historyForward"
    />
    <font-awesome-icon
      class="navSearchIcon navIcon"
      icon="search"
      @click="toggleSearchContainer"
    />
    <div
      class="logoIcon"
      :class="{ logoIconBarColor: barColor }"
    />
    <div
      class="logoText"
      :class="{ logoTextBarColor: barColor }"
    />
    <div class="searchContainer">
      <ft-input
        placeholder="Search / Go to URL"
        class="searchInput"
        :is-search="true"
        @click="goToSearch"
      />
      <font-awesome-icon
        class="navFilterIcon navIcon"
        icon="filter"
        @click="showFilters = !showFilters"
      />
    </div>
    <ft-search-filters
      v-show="showFilters"
      class="searchFilters"
      :class="{ expand: !isSideNavOpen }"
    />
  </div>
</template>

<script src="./top-nav.js" />
<style scoped src="./top-nav.css" />
