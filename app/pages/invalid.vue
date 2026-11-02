<template>
	<div>
		<header class="flex justify-between items-center mb-8">
			<h1 class="text-2xl font-semibold text-gray-800">
				Невалидные чеки
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
				<div class="grid grid-cols-2 gap-4">
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
							v-for="n in 3"
							:key="n"
							class="border-b border-gray-100 last:border-0"
						>
							<td class="py-3">---</td>
							<td class="py-3 text-red-500">Невалиден</td>
							<td class="py-3">---</td>
							<td class="py-3">---</td>
							<td class="py-3">
								<a href="#" class="text-accent">Подробнее</a>
							</td>
						</tr>
					</tbody>
				</table>
			</div>

			<div class="bg-white rounded-2xl shadow-sm p-6">
				<h3 class="font-semibold text-gray-800">Подробнее о чеке:</h3>
				<div class="mt-4">
					<p class="text-sm text-gray-500">
						Невалиден по причине путупу
					</p>
					<div class="mt-3 space-y-2">
						<div class="h-2.5 bg-slate-100 rounded w-4/5"></div>
						<div class="h-2.5 bg-slate-100 rounded w-3/5"></div>
						<div class="h-2.5 bg-slate-100 rounded w-11/12"></div>
						<div class="h-2.5 bg-slate-100 rounded w-3/4"></div>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>
