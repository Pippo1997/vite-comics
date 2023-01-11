<script>
export default {
    data() {
        return {
            menu: [
                {
                    label: 'Characters',
                    url: '#',
                    active: false
                },
                {
                    label: 'Comics',
                    url: '#',
                    active: true
                },
                {
                    label: 'Movies',
                    url: '#',
                    active: false
                },
                {
                    label: 'TV',
                    url: '#',
                    active: false
                },
                {
                    label: 'Games',
                    url: '#',
                    active: false
                },
                {
                    label: 'Video',
                    url: '#',
                    active: false
                },
                {
                    label: 'Fans',
                    url: '#',
                    active: false
                },
                {
                    label: 'News',
                    url: '#',
                    active: false
                },
                {
                    label: 'Shop',
                    url: '#',
                    active: false
                },
            ]
        }
    }
}
</script>

<template lang="">
  <header>
    <a href="/" class="logo">
        <img src="../assets/img/dc-logo.png" alt="logo-dc">
    </a>
    <nav>
        <ul>
            <li v-for="(item, index) in menu" :key="index">
                <a :href="item.url" :class="item.active ? 'active' : ''">
                {{item.label}}
                </a>
            </li>
        </ul>
       </nav>
  </header>
</template>

<style lang="scss">
  
</style>