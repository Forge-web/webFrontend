<template>
	<div>
		<header class="flex justify-between items-center mb-8">
			<h1 class="text-2xl font-semibold text-gray-800">
				Валидные чеки
			</h1>
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

		<div class="grid grid-cols-1 lg:grid-cols-2 gap-6 mb-6">
			<div class="bg-white rounded-2xl shadow-sm p-6">
				<h3 class="font-semibold text-gray-800 mb-4">
					Ежедневная статистика
				</h3>
				<div class="grid grid-cols-3 gap-4">
					<div class="rounded-xl p-4 bg-green-50 text-green-800">
						<div
							class="w-8 h-8 rounded-full bg-white/60 flex items-center justify-center mb-2.5"
						>
							<i class="fa-solid fa-check"></i>
						</div>
						<div class="text-2xl font-bold">50 000</div>
						<div class="text-xs opacity-80">Валидный чек</div>
					</div>
					<div class="rounded-xl p-4 bg-red-50 text-red-800">
						<div
							class="w-8 h-8 rounded-full bg-white/60 flex items-center justify-center mb-2.5"
						>
							<i class="fa-solid fa-xmark"></i>
						</div>
						<div class="text-2xl font-bold">300</div>
						<div class="text-xs opacity-80">Невалидный чек</div>
					</div>
					<div class="rounded-xl p-4 bg-blue-50 text-blue-800">
						<div
							class="w-8 h-8 rounded-full bg-white/60 flex items-center justify-center mb-2.5"
						>
							<i class="fa-solid fa-receipt"></i>
						</div>
						<div class="text-2xl font-bold">5000</div>
						<div class="text-xs opacity-80">Всего чеков</div>
					</div>
				</div>
			</div>

			<div class="bg-white rounded-2xl shadow-sm p-6">
				<h3 class="font-semibold text-gray-800">Валидность чеков</h3>
				<div
					class="mt-4 h-[200px] rounded-lg bg-slate-100 border border-dashed border-slate-200 flex items-center justify-center text-slate-400 text-sm"
				>
					График
				</div>
			</div>
		</div>

		<div class="grid grid-cols-1 lg:grid-cols-2 gap-6">
			<div class="bg-white rounded-2xl shadow-sm p-6">
				<h3 class="font-semibold text-gray-800">Список чеков</h3>
				<table class="w-full text-sm mt-4">
					<thead>
						<tr class="text-gray-400 text-left">
							<th class="pb-3 font-medium">ID клиента</th>
							<th class="pb-3 font-medium">Статус</th>
							<th class="pb-3 font-medium">Дата</th>
							<th class="pb-3 font-medium">Сумма</th>
							<th class="pb-3 font-medium">О чеке</th>
						</tr>
					</thead>
					<tbody>
						<tr
							v-for="r in receipts"
							:key="r.id"
							class="border-b border-gray-100 last:border-0"
						>
							<td class="py-3">{{ r.id }}</td>
							<td class="py-3 text-green-600">Валиден</td>
							<td class="py-3">{{ r.date }}</td>
							<td class="py-3">{{ r.sum }}</td>
							<td class="py-3">
								<a href="#" class="text-accent">Подробнее</a>
							</td>
						</tr>
					</tbody>
				</table>
			</div>

			<div class="bg-white rounded-2xl shadow-sm p-6">
				<h3 class="font-semibold text-gray-800">Подробнее о чеке:</h3>
				<p class="text-sm text-gray-400 mt-1">
					№ 123456789 <br />
					14.02.2025 12:30:45
				</p>
				<table class="w-full text-sm mt-4">
					<thead>
						<tr class="text-gray-400 text-left">
							<th class="pb-3 font-medium">Товар</th>
							<th class="pb-3 font-medium">Кол-во</th>
							<th class="pb-3 font-medium">Цена</th>
							<th class="pb-3 font-medium">Сумма</th>
						</tr>
					</thead>
					<tbody>
						<tr class="border-b border-gray-100">
							<td class="py-3">Молоко</td>
							<td class="py-3">3</td>
							<td class="py-3">100.00</td>
							<td class="py-3">300.00</td>
						</tr>
						<tr class="border-b border-gray-100">
							<td class="py-3">Хлеб</td>
							<td class="py-3">1</td>
							<td class="py-3">50.00</td>
							<td class="py-3">50.00</td>
						</tr>
						<tr>
							<td class="py-3">Корм</td>
							<td class="py-3">15</td>
							<td class="py-3">70.00</td>
							<td class="py-3">3500.00</td>
						</tr>
					</tbody>
				</table>
				<div class="mt-4 text-right text-base font-semibold">
					<strong>Итого:</strong> 4501.00
				</div>
				<div class="mt-4">
					<p class="text-sm text-gray-500">Оплата по карте</p>
					<div class="mt-2 space-y-2">
						<div class="h-2 bg-slate-100 rounded w-4/5"></div>
						<div class="h-2 bg-slate-100 rounded w-3/5"></div>
						<div class="h-2 bg-slate-100 rounded w-9/12"></div>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script setup lang="ts">
	const receipts = [
		{ id: "123456789", date: "14.02.2025 12:30:45", sum: "1200.00" },
		{ id: "425741234", date: "14.02.2025 12:30:45", sum: "12.45" },
		{ id: "4145841351", date: "14.02.2025 12:30:45", sum: "254.35" },
	];
</script>
