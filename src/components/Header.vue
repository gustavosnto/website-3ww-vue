<script lang="ts">
export default {
    data() {
        return {
        showMobileMenu: false,
        };
    },
    methods: {
        showMenu() {
        this.showMobileMenu = !this.showMobileMenu;
        },
    },
};
</script>

<template>
    <header class="main">
        <div class="container flex">
            <div class="logo">
                <img src="https://3ww.com.br/wp-content/uploads/2022/07/logo-3ww-wp.png" />
            </div>

            <nav class="menu-js">
                <ul class="flex" :class="this.showMobileMenu ? 'open-menu' : 'closed-menu'">
                    <li><a href="">Home</a></li>
                    <li><a href="">Soluções</a></li>
                    <li><a href="">Projetos</a></li>
                    <li><a href="">Blog</a></li>
                    <li><a href="">Contato</a></li>

                    <i class="ri-close-fill close-menu" @click="showMenu()"></i>
                </ul>
                <a href="#" class="btn-contact">Entre em contato</a>

                <i class="ri-menu-4-fill menu-mobile" @click="showMenu()"></i>
            </nav>
        </div>
    </header>
</template>
