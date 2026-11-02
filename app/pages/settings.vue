<template>
	<div>
		<header class="flex justify-between items-center mb-8">
			<h1 class="text-2xl font-semibold text-gray-800">Настройки</h1>
			<NuxtLink
				to="/"
				class="flex items-center font-bold text-lg text-gray-800 no-underline"
			>
				<span
					class="w-8 h-8 rounded-lg bg-accent text-white flex items-center justify-center mr-2.5"
				>
					<i class="fa-solid fa-bolt"></i>
				</span>
				<span>Nazvanie</span>
			</NuxtLink>
		</header>

		<div
			class="bg-white rounded-2xl shadow-sm p-6 max-w-lg mx-auto mt-12"
		>
			<h2 class="text-xl font-semibold text-gray-800 mb-4">
				Профиль и параметры
			</h2>
			<form class="flex flex-col gap-4" @submit.prevent="submit">
				<div>
					<label
						for="username"
						class="block font-medium text-gray-700 mb-1.5"
					>
						Имя профиля:
					</label>
					<input
						id="username"
						v-model="form.username"
						type="text"
						placeholder="Введите имя"
						class="w-full px-3 py-2.5 border border-gray-200 rounded-lg text-sm outline-none focus:ring-2 focus:ring-accent/30"
					/>
				</div>

				<div>
					<label
						for="theme"
						class="block font-medium text-gray-700 mb-1.5"
					>
						Тема:
					</label>
					<select
						id="theme"
						v-model="form.theme"
						class="w-full px-3 py-2.5 border border-gray-200 rounded-lg text-sm outline-none focus:ring-2 focus:ring-accent/30 bg-white"
					>
						<option value="light">Светлая</option>
						<option value="dark">Темная</option>
					</select>
				</div>

				<label
					class="flex items-center gap-2.5 cursor-pointer text-sm"
				>
					<input v-model="form.notifications" type="checkbox" />
					<span>Включить уведомления</span>
				</label>

				<button
					type="submit"
					class="bg-accent text-white py-3 rounded-lg font-bold hover:opacity-90 transition-opacity mt-2"
				>
					Сохранить и вернуться
				</button>
			</form>
		</div>
	</div>
</template>

<script setup lang="ts">
	import { reactive } from "vue";
	import { useRouter } from "vue-router";

	const router = useRouter();

	const form = reactive({
		username: "Admin",
		theme: "light",
		notifications: true,
	});

	const submit = () => {
		router.push("/");
	};
</script>
