<template>
	<div>
		<!-- Header -->
		<header class="flex justify-between items-center mb-8">
			<h1 class="text-2xl font-semibold text-gray-800">
				Главная страница
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

		<!-- Top row -->
		<div class="grid grid-cols-1 lg:grid-cols-2 gap-6 mb-6">
			<!-- Stats -->
			<div class="bg-white rounded-2xl shadow-sm p-6">
				<div class="mb-4">
					<h3 class="font-semibold text-gray-800">
						Ежедневная статистика
					</h3>
					<p class="text-sm text-gray-400">Сводка продаж</p>
				</div>

				<div class="grid grid-cols-2 md:grid-cols-4 gap-4">
					<div class="rounded-xl p-4 bg-green-50 text-green-800">
						<div
							class="w-8 h-8 rounded-full bg-white/60 flex items-center justify-center mb-2.5"
						>
							<i class="fa-solid fa-arrow-trend-up"></i>
						</div>
						<div class="text-2xl font-bold">50 000</div>
						<div class="text-xs opacity-80">Общая выручка</div>
						<div class="text-[10px] mt-1">+8% за сутки</div>
					</div>

					<div class="rounded-xl p-4 bg-blue-50 text-blue-800">
						<div
							class="w-8 h-8 rounded-full bg-white/60 flex items-center justify-center mb-2.5"
						>
							<i class="fa-solid fa-wallet"></i>
						</div>
						<div class="text-2xl font-bold">300</div>
						<div class="text-xs opacity-80">Средний чек</div>
						<div class="text-[10px] mt-1">+5% за сутки</div>
					</div>

					<div class="rounded-xl p-4 bg-sky-50 text-sky-800">
						<div
							class="w-8 h-8 rounded-full bg-white/60 flex items-center justify-center mb-2.5"
						>
							<i class="fa-solid fa-receipt"></i>
						</div>
						<div class="text-2xl font-bold">5000</div>
						<div class="text-xs opacity-80">Всего чеков</div>
						<div class="text-[10px] mt-1">+1.2% за сутки</div>
					</div>

					<div class="rounded-xl p-4 bg-purple-50 text-purple-800">
						<div
							class="w-8 h-8 rounded-full bg-white/60 flex items-center justify-center mb-2.5"
						>
							<i class="fa-solid fa-user"></i>
						</div>
						<div class="text-2xl font-bold">80</div>
						<div class="text-xs opacity-80">Клиенты</div>
						<div class="text-[10px] mt-1">+0.5% за сутки</div>
					</div>
				</div>
			</div>

			<!-- Chart placeholder -->
			<div class="bg-white rounded-2xl shadow-sm p-6">
				<div class="flex justify-between items-center">
					<h3 class="font-semibold text-gray-800">
						Динамика продаж по годам
					</h3>
				</div>
				<div
					class="mt-4 h-[200px] rounded-lg bg-slate-100 border border-dashed border-slate-200 flex items-center justify-center text-slate-400 text-sm"
				>
					График
				</div>
				<div class="flex gap-4 mt-4 text-xs items-center">
					<span class="flex items-center">
						<span
							class="w-2 h-2 rounded-full bg-green-500 mr-1.5"
						></span>
						Текущий год
					</span>
					<select
						class="border border-gray-200 px-2.5 py-1 rounded-md bg-white outline-none text-xs"
					>
						<option>2024</option>
						<option>2023</option>
					</select>
				</div>
			</div>
		</div>

		<!-- Monthly sales -->
		<div class="bg-white rounded-2xl shadow-sm p-6 mb-6">
			<div class="flex justify-between items-center">
				<h3 class="font-semibold text-gray-800">Продажи за месяц</h3>
				<select
					class="border border-gray-200 px-2.5 py-1 rounded-md bg-white outline-none text-xs"
				>
					<option>Август</option>
				</select>
			</div>
			<div
				class="mt-4 h-[300px] rounded-lg bg-slate-100 border border-dashed border-slate-200 flex items-center justify-center text-slate-400 text-sm"
			>
				Линейный график
			</div>
		</div>

		<!-- Bottom row -->
		<div class="grid grid-cols-1 lg:grid-cols-3 gap-6">
			<div class="bg-white rounded-2xl shadow-sm p-6">
				<div class="flex justify-between items-center">
					<h3 class="font-semibold text-gray-800">Тип оплаты</h3>
					<select
						class="border border-gray-200 px-2.5 py-1 rounded-md bg-white outline-none text-xs"
					>
						<option>Август</option>
					</select>
				</div>
				<div
					class="mt-4 h-[150px] rounded-lg bg-slate-100 border border-dashed border-slate-200 flex items-end justify-around p-2.5"
				>
					<div class="w-1/4 h-[60%] bg-blue-300 rounded-t"></div>
					<div class="w-1/4 h-[90%] bg-blue-400 rounded-t"></div>
				</div>
				<div class="flex gap-4 mt-4 text-xs">
					<span class="flex items-center">
						<span
							class="w-2 h-2 rounded-full bg-blue-300 mr-1.5"
						></span
						>Наличные
					</span>
					<span class="flex items-center">
						<span
							class="w-2 h-2 rounded-full bg-blue-400 mr-1.5"
						></span
						>Оплата картой
					</span>
				</div>
			</div>

			<div class="bg-white rounded-2xl shadow-sm p-6">
				<div class="flex justify-between items-center">
					<h3 class="font-semibold text-gray-800">Средний чек</h3>
					<select
						class="border border-gray-200 px-2.5 py-1 rounded-md bg-white outline-none text-xs"
					>
						<option>Август</option>
					</select>
				</div>
				<div
					class="mt-4 h-[150px] rounded-lg bg-slate-100 border border-dashed border-slate-200 flex items-center justify-center text-slate-400 text-sm"
				>
					График
				</div>
			</div>

			<div class="bg-white rounded-2xl shadow-sm p-6">
				<div class="flex justify-between items-center">
					<h3 class="font-semibold text-gray-800">
						Количество чеков
					</h3>
					<select
						class="border border-gray-200 px-2.5 py-1 rounded-md bg-white outline-none text-xs"
					>
						<option>Август</option>
					</select>
				</div>
				<div
					class="mt-4 h-[150px] rounded-lg bg-slate-100 border border-dashed border-slate-200 flex items-center justify-center text-slate-400 text-sm"
				>
					График
				</div>
			</div>
		</div>
	</div>
</template>
