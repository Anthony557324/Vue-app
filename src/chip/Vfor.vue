<script>
import { ref } from 'vue'

export default {
    name: 'VforComp',
    setup() {
        const users = ref([
            {
                name: '小明',
                age: 18,
                height: 180
            },
            {
                name: '小红',
                age: 20,
                height: 165
            }
        ])

        const InputVal = ref(123)

        function handleClick(e, event) {
            console.log('哈哈哈')
            console.log(event)

            // e.target.disabled = true
        }

        

        return {
            users,
            InputVal,
            handleClick
        }
    }
}
</script>

<template>
    <div v-for="(user, index) in users" v-bind:key="user.age">
        <!-- v-bind:key可以简写成:key -->
        <div>序号{{ index + 1 }}</div>
        <div>{{ user.name }}</div>
        <div>{{ user.age }}</div>
        <div>{{ user.height }}</div>
    </div>
    <input />
    <button @click="handleClick('msg', $event)" @keyup.enter="handleClick('msg', $event)">点击</button>
    <!-- () => { handleClick('msg') } -->
</template>
