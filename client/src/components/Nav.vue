<script setup lang="ts">
    import { ref } from 'vue';
    import LoginBadge from './login-badge.vue';
    import { RouterLink } from 'vue-router';
    import Cart from './Cart.vue';
    import MessageList from './MessageList.vue';

    const isActive = ref(false);
    const isCartOpen = ref(false);
</script>

<template>
    <Cart :is-open="isCartOpen" />
    <nav class="navbar is-primary" role="navigation" aria-label="main navigation">
        <div class="navbar-brand">
            <a class="navbar-item" href="https://bulma.io">
                <img src="https://bulma.io/images/bulma-logo.png" width="112" height="28">
            </a>
        
            <a :class="{ 'is-active': isActive }" @click="isActive = !isActive" role="button" class="navbar-burger" aria-label="menu" aria-expanded="false">
                <span aria-hidden="true"></span>
                <span aria-hidden="true"></span>
                <span aria-hidden="true"></span>
            </a>
        </div>
        
        <div :class="{ 'is-active': isActive }" id="navbarBasicExample" class="navbar-menu">
            <div class="navbar-start">
                <router-link to="/" class="navbar-item">
                    Home
                </router-link>
        
                <router-link to="/products" class="navbar-item">
                    Store
                </router-link>
        
                <div class="navbar-item has-dropdown is-hoverable">
                    <a class="navbar-link">
                        More
                    </a>
        
                    <div class="navbar-dropdown">
                        <router-link to="/about" class="navbar-item">
                            About
                        </router-link>
                        <a class="navbar-item">
                            Jobs
                        </a>
                        <a class="navbar-item">
                            Contact
                        </a>
                        <hr class="navbar-divider">
                        <a class="navbar-item">
                            Report an issue
                        </a>
                    </div>
                </div>
            </div>
        
            <div class="navbar-end">
                <MessageList />
                <div class="navbar-item">
                    <button class="button is-primary" @click="isCartOpen = !isCartOpen">
                        <strong>Cart</strong>
                    </button>
                </div>
                <div class="navbar-item">
                    <login-badge />
                </div>
            </div>
        </div>
    </nav>
</template>