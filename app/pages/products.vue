<template>
	<div>
		<header class="flex justify-between items-center mb-8">
			<h1 class="text-2xl font-semibold text-gray-800">Товары</h1>
			<NuxtLink
				to="/"
				class="flex items-center font-bold text-lg text-gray-800 no-underline"
			>
				<span
					class="w-8 h-8 rounded-lg bg-accent text-white flex items-center justify-center mr-2.5"
				>
					<i class="fa-solid fa-cube"></i>
				</span>
				<span>Nazvanie</span>
			</NuxtLink>
		</header>

		<!-- Stat cards -->
		<div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-6">
			<div
				class="bg-white rounded-2xl shadow-sm p-6 flex flex-col gap-1"
			>
				<div
					class="w-11 h-11 rounded-xl bg-green-50 text-green-600 flex items-center justify-center mb-2"
				>
					<i class="fa-solid fa-dollar-sign"></i>
				</div>
				<div class="text-2xl font-bold text-gray-800">50 000</div>
				<div class="text-sm text-gray-500">Общая выручка</div>
				<div class="text-xs text-emerald-500">+8% за сутки</div>
			</div>

			<div
				class="bg-white rounded-2xl shadow-sm p-6 flex flex-col gap-1"
			>
				<div
					class="w-11 h-11 rounded-xl bg-blue-50 text-blue-600 flex items-center justify-center mb-2"
				>
					<i class="fa-solid fa-box"></i>
				</div>
				<div class="text-2xl font-bold text-gray-800">7000</div>
				<div class="text-sm text-gray-500">Продано товаров</div>
				<div class="text-xs text-emerald-500">+5% за сутки</div>
			</div>

			<div
				class="bg-white rounded-2xl shadow-sm p-6 flex flex-col gap-1"
			>
				<div
					class="w-11 h-11 rounded-xl bg-blue-50 text-blue-600 flex items-center justify-center mb-2"
				>
					<i class="fa-solid fa-triangle-exclamation"></i>
				</div>
				<div class="text-2xl font-bold text-gray-800">4</div>
				<div class="text-sm text-gray-500">Нет в наличии</div>
				<div class="text-xs text-red-500">-1.2% за сутки</div>
			</div>
		</div>

		<!-- Top tables -->
		<div class="grid grid-cols-1 lg:grid-cols-2 gap-6 mb-6">
			<div class="bg-white rounded-2xl shadow-sm p-6">
				<h3 class="font-semibold text-gray-800 mb-4">
					Популярные типы товаров
				</h3>
				<table class="w-full text-sm">
					<thead>
						<tr class="text-gray-400 text-left">
							<th class="pb-3 font-medium">#</th>
							<th class="pb-3 font-medium">Тип</th>
							<th class="pb-3 font-medium">Популярность</th>
						</tr>
					</thead>
					<tbody>
						<tr class="border-b border-gray-100 last:border-0">
							<td class="py-3">01</td>
							<td class="py-3">Продукты питания</td>
							<td class="py-3">
								<span
									class="text-emerald-600 bg-emerald-50 px-1.5 py-0.5 rounded text-xs"
									>50%</span
								>
							</td>
						</tr>
						<tr class="border-b border-gray-100 last:border-0">
							<td class="py-3">02</td>
							<td class="py-3">Табак</td>
							<td class="py-3">
								<span
									class="text-blue-600 bg-blue-50 px-1.5 py-0.5 rounded text-xs"
									>20%</span
								>
							</td>
						</tr>
						<tr class="border-b border-gray-100 last:border-0">
							<td class="py-3">03</td>
							<td class="py-3">Лекарства</td>
							<td class="py-3">
								<span
									class="text-violet-600 bg-violet-50 px-1.5 py-0.5 rounded text-xs"
									>18%</span
								>
							</td>
						</tr>
						<tr>
							<td class="py-3">04</td>
							<td class="py-3">Электроника</td>
							<td class="py-3">
								<span
									class="text-amber-600 bg-amber-50 px-1.5 py-0.5 rounded text-xs"
									>8%</span
								>
							</td>
						</tr>
					</tbody>
				</table>
			</div>

			<div class="bg-white rounded-2xl shadow-sm p-6">
				<h3 class="font-semibold text-gray-800 mb-4">
					Популярные товары
				</h3>
				<table class="w-full text-sm">
					<thead>
						<tr class="text-gray-400 text-left">
							<th class="pb-3 font-medium">#</th>
							<th class="pb-3 font-medium">Товар</th>
							<th class="pb-3 font-medium">Популярность</th>
						</tr>
					</thead>
					<tbody>
						<tr class="border-b border-gray-100 last:border-0">
							<td class="py-3">01</td>
							<td class="py-3">Хлеб</td>
							<td class="py-3">
								<span
									class="text-emerald-600 bg-emerald-50 px-1.5 py-0.5 rounded text-xs"
									>50%</span
								>
							</td>
						</tr>
						<tr class="border-b border-gray-100 last:border-0">
							<td class="py-3">02</td>
							<td class="py-3">Молоко</td>
							<td class="py-3">
								<span
									class="text-blue-600 bg-blue-50 px-1.5 py-0.5 rounded text-xs"
									>20%</span
								>
							</td>
						</tr>
						<tr class="border-b border-gray-100 last:border-0">
							<td class="py-3">03</td>
							<td class="py-3">Аспирин</td>
							<td class="py-3">
								<span
									class="text-violet-600 bg-violet-50 px-1.5 py-0.5 rounded text-xs"
									>18%</span
								>
							</td>
						</tr>
						<tr>
							<td class="py-3">04</td>
							<td class="py-3">Сигареты</td>
							<td class="py-3">
								<span
									class="text-amber-600 bg-amber-50 px-1.5 py-0.5 rounded text-xs"
									>8%</span
								>
							</td>
						</tr>
					</tbody>
				</table>
			</div>
		</div>

		<!-- Charts -->
		<div class="grid grid-cols-1 lg:grid-cols-3 gap-6">
			<div class="bg-white rounded-2xl shadow-sm p-6 lg:col-span-2">
				<div class="flex justify-between items-center mb-4">
					<h3 class="font-semibold text-gray-800">
						Товаров в чеке по дням
					</h3>
					<select
						class="border border-gray-200 px-2.5 py-1 rounded-md bg-white outline-none text-xs"
					>
						<option>За месяц</option>
					</select>
				</div>
				<div class="relative h-[280px]">
					<canvas id="itemsPerReceiptChart"></canvas>
				</div>
			</div>

			<div class="bg-white rounded-2xl shadow-sm p-6">
				<h3 class="font-semibold text-gray-800 mb-4">
					Популярные категории
				</h3>
				<div class="relative h-[280px]">
					<canvas id="categoriesChart"></canvas>
				</div>
			</div>
		</div>
	</div>
</template>

<script setup lang="ts">
	import { onBeforeUnmount, onMounted } from "vue";
	import type { Chart } from "chart.js";

	let itemsChart: Chart | null = null;
	let categoriesChart: Chart | null = null;

	onMounted(async () => {
		const { default: ChartCtor } = await import("chart.js/auto");

		const ctx1 = document.getElementById(
			"itemsPerReceiptChart",
		) as HTMLCanvasElement | null;
		const ctx2 = document.getElementById(
			"categoriesChart",
		) as HTMLCanvasElement | null;

		if (ctx1) {
			itemsChart = new ChartCtor(ctx1, {
				type: "line",
				data: {
					labels: ["Пн", "Вт", "Ср", "Чт", "Пт", "Сб", "Вс"],
					datasets: [
						{
							label: "Товаров в чеке",
							data: [3, 4, 2, 5, 4, 6, 3],
							borderColor: "#5b6bf0",
							backgroundColor: "rgba(91,107,240,0.1)",
							tension: 0.35,
							fill: true,
							pointRadius: 3,
						},
					],
				},
				options: {
					responsive: true,
					maintainAspectRatio: false,
					plugins: { legend: { display: false } },
					scales: { y: { beginAtZero: true } },
				},
			});
		}

		if (ctx2) {
			categoriesChart = new ChartCtor(ctx2, {
				type: "doughnut",
				data: {
					labels: ["Продукты", "Табак", "Лекарства", "Электроника"],
					datasets: [
						{
							data: [50, 20, 18, 8],
							backgroundColor: [
								"#10b981",
								"#3b82f6",
								"#8b5cf6",
								"#f59e0b",
							],
							borderWidth: 0,
						},
					],
				},
				options: {
					responsive: true,
					maintainAspectRatio: false,
					cutout: "65%",
					plugins: { legend: { position: "bottom" } },
				},
			});
		}
	});

	onBeforeUnmount(() => {
		itemsChart?.destroy();
		categoriesChart?.destroy();
	});
</script>
