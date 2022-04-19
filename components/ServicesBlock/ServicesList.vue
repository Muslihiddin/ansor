<template>
    <ul class="servicesList">
        <li v-for="item in services" :key="item.id" class="border rounded-2xl">
            <service :item="item" />
        </li>
    </ul>
</template>

<script>
import Service from './Service.vue'
export default {
  components: { Service },
    name: 'ServicesList',
        data() {
            return {
                services: [
                    { id: 1, icon: 'hand', title: 'Dedicated team', description: 'We can make awesome websites and Apps.We can make awesome websites ....'},
                    { id: 2, icon: 'mobile', title: 'Development of mobile applications', description: 'We can make awesome websites and Apps.We can make awesome websites ....'},
                    { id: 3, icon: 'link', title: 'Development and implementation of ERP systems', description: 'We can make awesome websites and Apps.We can make awesome websites ....'},
                    { id: 4, icon: 'stack', title: 'UX/UI design', description: 'We can make awesome websites and Apps.We can make awesome websites ....'},
                    { id: 5, icon: 'settings', title: 'Infrastructure optimization', description: 'We can make awesome websites and Apps.We can make awesome websites ....'},
                    { id: 6, icon: 'desktop', title: 'IT consulting', description: 'We can make awesome websites and Apps.We can make awesome websites ....'},
            ]
            }
        }
}
</script>

<style lang="scss" scoped>
    .servicesList {
        display: grid;
        justify-items: center;
        gap: 24px;
        grid-template-columns: repeat(auto-fit,minmax(320px, 1fr));
        grid-auto-rows: 1fr;
    }
</style>