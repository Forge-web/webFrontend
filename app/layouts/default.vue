<template>
	<div class="min-h-screen bg-[#f4f6f9] flex">
		<!-- Sidebar -->
		<aside
			class="fixed inset-y-0 left-0 w-20 bg-white shadow-[2px_0_10px_rgba(0,0,0,0.02)] flex flex-col items-center py-5 z-50 max-md:inset-x-0 max-md:inset-y-auto max-md:bottom-0 max-md:w-full max-md:h-auto max-md:flex-row max-md:justify-around max-md:py-2 max-md:border-t max-md:border-gray-200"
		>
			<div class="text-accent text-2xl mb-10 max-md:hidden">
				<i class="fa-solid fa-chart-simple"></i>
			</div>

			<nav
				class="flex flex-col items-center gap-3 max-md:flex-row max-md:justify-around max-md:gap-0 max-md:w-full"
			>
				<NuxtLink
					v-for="item in navItems"
					:key="item.to"
					:to="item.to"
					class="nav-btn"
					:class="{ 'nav-btn-active': isActive(item.to) }"
				>
					<i :class="item.icon"></i>
				</NuxtLink>
			</nav>

			<div class="mt-auto max-md:mt-0">
				<NuxtLink
					to="/settings"
					class="nav-btn"
					:class="{ 'nav-btn-active': isActive('/settings') }"
				>
					<i class="fa-solid fa-gear"></i>
				</NuxtLink>
			</div>
		</aside>

		<!-- Main -->
		<main
			class="ml-20 flex-1 p-8 max-md:ml-0 max-md:p-4 max-md:pb-24"
		>
			<slot />
		</main>
	</div>
</template>

<script setup lang="ts">
	import { useRoute } from "vue-router";

	const route = useRoute();

	const navItems = [
		{ to: "/", icon: "fa-solid fa-chart-pie" },
		{ to: "/valid", icon: "fa-solid fa-file-invoice" },
		{ to: "/invalid", icon: "fa-solid fa-file-excel" },
		{ to: "/products", icon: "fa-solid fa-chart-simple" },
	];

	const isActive = (path: string) =>
		path === "/" ? route.path === "/" : route.path.startsWith(path);
</script>

<style scoped>
	.nav-btn {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 3rem;
		height: 3rem;
		border-radius: 0.75rem;
		color: #aaa;
		font-size: 1.25rem;
		text-decoration: none;
		transition: all 0.3s;
	}
	.nav-btn:hover,
	.nav-btn-active {
		background-color: var(--color-accent);
		color: white;
	}
</style>
