<template>
	<nav class="bg-white shadow dark:bg-gray-700">
		<div class="mx-auto flex items-center justify-between px-6 py-3">
			<h1 class="text-2xl font-bold text-gray-800 dark:text-white lg:text-3xl" href="#">Treco</h1>
			<div class="flex items-center gap-4">
				<div class="group relative">
					<button class="flex items-center gap-1 text-orange-500">
						<span class="material-symbols-rounded">diversity_3</span>
						Team
					</button>
					<div class="absolute hidden group-hover:flex">
						<ul class="mt-4 flex min-w-[6rem] flex-col bg-white shadow-md dark:bg-gray-700 dark:text-white">
							<li class="p-2 hover:bg-gray-200 dark:hover:bg-gray-600">
								<a href="#">Team 1</a>
							</li>
							<li class="p-2 hover:bg-gray-200 dark:hover:bg-gray-600">
								<a href="#">Team 2</a>
							</li>
						</ul>
					</div>
				</div>
				<dark-mode-toggle></dark-mode-toggle>
				<button
					class="mx-1 rounded-md bg-gray-500 px-3 py-2 text-center text-sm font-medium leading-5 text-white hover:bg-orange-500 dark:bg-orange-500 dark:hover:bg-gray-500 md:mx-2 md:w-auto"
					href="#"
				>
					Logout
				</button>
			</div>
		</div>
	</nav>
</template>
