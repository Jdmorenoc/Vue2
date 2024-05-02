<script setup>
import { ref } from 'vue'

const counter = ref(0)

function decrement() {
    if(counter.value > 0){
        counter.value--
    }
}
function increment() {
    counter.value++
}

</script>

<template>
<div class="bg-slate-300 rounded py-8 px-6 w-96 shadow-md flex-col flex items-center justify-center ">
			<div class="relative">
				<img class="size-32 rounded-full" src="https://static.vecteezy.com/system/resources/previews/002/204/278/non_2x/a-male-office-worker-is-signing-ok-hand-drawn-style-design-illustrations-vector.jpg" alt="">
				<div v-show="counter > 0" class="size-6 rounded-full bg-red-500 flex justify-center text-white absolute top-0 right-0 items-center">
					{{ counter }}
				</div>
			</div>
                <p v-if="counter>0">Tienes nuevos mensajes! 😊</p>
                <p v-else>Nadie te habla 😥</p>
                
			<div class="flex justify-around w-24 mt-6">
				<button @click="decrement" class="bg-blue-200 rounded w-6 flex justify-center items-center px-2">-</button>
				{{ counter }}
				<button @click="increment" class="bg-blue-200 rounded w-6 flex justify-center items-center px-2">+</button>
			</div>
		</div>
</template>