<template>
    <ul class="flex flex-wrap justify-center gap-x-8 xm:gap-x-0 sm:justify-between items-center gap-y-4 my-12">
        <li v-for="member in members" :key="member.id">
            <team-member :member="member" />
        </li>
    </ul>
</template>

<script>
import TeamMember from './TeamMember.vue'
export default {
    name: 'TeamList',
    components: {
        TeamMember
    },
    data() {
        return {
            members: [
                {id: 1, name: 'Muhammad Xalil', position: 'CEO', img: 'MuhammadXalil.png'},
                {id: 1, name: 'Muhammad Xalil', position: 'CEO', img: 'MuhammadXalil.png'},
                {id: 1, name: 'Muhammad Xalil', position: 'CEO', img: 'MuhammadXalil.png'},
                {id: 1, name: 'Muhammad Xalil', position: 'CEO', img: 'MuhammadXalil.png'},
                {id: 1, name: 'Muhammad Xalil', position: 'CEO', img: 'MuhammadXalil.png'},
            ]
        }
    }
}
</script>