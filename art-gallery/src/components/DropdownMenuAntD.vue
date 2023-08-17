<template>
    <div class="nav-site">
        <a-menu v-model:selectedMenuItems="selectedMenuItems" mode="horizontal" class="nav-menu" disabledOverflow={true}>
            <a-menu-item key="home" v-bind:class="{ 'active': selectedMenuItems.includes('home') }">
                <router-link to="/">
                    <span>Home</span>
                </router-link>
            </a-menu-item>
            <a-sub-menu>
                <template #title>
                    <router-link to="/artworks">
                        <span>Artworks</span>
                    </router-link>
                </template>
                <a-menu-item key="artwork-of-day" v-bind:class="{ 'active': selectedMenuItems.includes('artwork-of-day') }">
                    <router-link to="/artworkofday">
                        <span>Artwork of the Day</span>
                    </router-link>
                </a-menu-item>
                <a-menu-item key="artworks-list" v-bind:class="{ 'active': selectedMenuItems.includes('artworks-list') }">
                    <router-link to="/artworks">
                        <span>List of Artworks</span>
                    </router-link>
                </a-menu-item>
            </a-sub-menu>
            <a-sub-menu>
                <template #title>
                    <router-link to="/culture">
                        <span>Art & Culture</span>
                    </router-link>
                </template>
                <a-menu-item key="symbols" v-bind:class="{ 'active': selectedMenuItems.includes('symbols') }">
                    <span>Symbols</span>
                </a-menu-item>
                <a-menu-item key="artist-of-day" v-bind:class="{ 'active': selectedMenuItems.includes('artist-of-day') }">
                    <router-link to="/artistofday">
                        <span>Artist of the Day</span>
                    </router-link>
                </a-menu-item>
                <a-menu-item key="art-facts" v-bind:class="{ 'active': selectedMenuItems.includes('art-facts') }">
                    <span>Aboriginal Art Facts</span>
                </a-menu-item>
            </a-sub-menu>
            <a-sub-menu>
                <template #title>
                    <router-link to="/exhibition">
                        <span>Exhibitions</span>
                    </router-link>
                </template>
                <a-menu-item key="exhibition-currnt" v-bind:class="{ 'active': selectedMenuItems.includes('exhibition-currnt') }">
                    <router-link to="/exhibition">
                        <span>Current Exhibitions</span>
                    </router-link>
                </a-menu-item>
                <a-menu-item key="exhibition-past" v-bind:class="{ 'active': selectedMenuItems.includes('exhibition-past') }">
                    <span>Past Exhibitions</span>
                </a-menu-item>
            </a-sub-menu>
