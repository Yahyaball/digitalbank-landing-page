<script setup lang="ts">
import { onMounted, onUnmounted, ref } from 'vue'
import hamburgerIcon from '@/assets/icons/icon-hamburger.svg'
import closeIcon from '@/assets/icons/icon-close.svg'

const isNavOpen = ref(false)
const isDesktop = ref(false)
const nav = ref<HTMLElement | null>(null)
const mediaQuery = window.matchMedia('(min-width: 64rem)')
const pageContent = ref<HTMLElement | null>(null)

function updateNavInert() {
    if (!nav.value || !pageContent.value) return

    if (isDesktop.value) {
        nav.value.removeAttribute('inert')
        nav.value.classList.add('show')
        pageContent.value.removeAttribute('inert')
        document.body.classList.remove('nav-open')
    } else {
        nav.value.toggleAttribute('inert', !isNavOpen.value)
        nav.value.classList.toggle('show', isNavOpen.value)
        pageContent.value.toggleAttribute('inert', isNavOpen.value)
        document.body.classList.toggle('nav-open', isNavOpen.value)
    }

    document.body.classList.toggle('nav-open', isNavOpen.value && !isDesktop.value)
}

function toggleNav() {
    if (isDesktop.value) return
    isNavOpen.value = !isNavOpen.value
    updateNavInert()
}

function closeNav() {
    if (isDesktop.value) return
    isNavOpen.value = false
    updateNavInert()
}

function handleKeydown(e: KeyboardEvent) {
    if (!isDesktop.value) return
    if (e.key === 'Escape' && isNavOpen.value && !isDesktop.value) closeNav()
}

function handleMediaChange(e: MediaQueryListEvent) {
    isDesktop.value = e.matches
    updateNavInert()
}

onMounted(() => {
    isDesktop.value = mediaQuery.matches
    pageContent.value = document.getElementById('page-content')
    updateNavInert()
    mediaQuery.addEventListener('change', handleMediaChange)
    window.addEventListener('keydown', handleKeydown)
})
onUnmounted(() => {
    mediaQuery.removeEventListener('change', handleMediaChange)
    window.removeEventListener('keydown', handleKeydown)
})
</script>

<template>
    <header>
        <div class="header-box">
            <div class="header-content">
                <img src="@/assets/logos/logo-dark.svg" alt="Digitalbank">
                <button v-show="!isDesktop" type="button" :aria-expanded="isNavOpen" @click="toggleNav"
                    :aria-label="isNavOpen ? 'Close menu' : 'Open menu'">
                    <img :src="isNavOpen ? closeIcon : hamburgerIcon" :alt="isNavOpen ? '' : 'Open menu'"
                        :class="isNavOpen ? 'close-icon' : 'open-icon'">
                </button>
            </div>
            <nav aria-label="Primary" :class="{ show: isNavOpen || isDesktop }" ref="nav">
                <ul>
                    <li><a href="#" @click="closeNav">Home</a></li>
                    <li><a href="#" @click="closeNav">About</a></li>
                    <li><a href="#" @click="closeNav">Contact</a></li>
                    <li><a href="#" @click="closeNav">Blog</a></li>
                    <li><a href="#" @click="closeNav">Careers</a></li>
                </ul>
            </nav>
            <button type="button" class="btn">Request Invite</button>
            <div class="overlay" @click="closeNav"></div>
        </div>
    </header>
    <div class="margin"></div>
</template>