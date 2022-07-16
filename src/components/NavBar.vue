<template>
  <nav class="bg-white shadow dark:bg-gray-800">
    <div class="flex justify-between items-center px-6 py-3 mx-auto">
      <h1
        class="text-2xl font-bold text-gray-800 transition-colors duration-200 transform dark:text-white lg:text-3xl hover:text-gray-700 dark:hover:text-gray-300"
        href="#"
      >
        Treco
      </h1>
      <div class="flex items-center gap-4">
        <div class="relative group">
          <button class="flex items-center text-orange-600 gap-1">
            <span class="material-symbols-rounded">diversity_3</span>
            Team
          </button>
          <div class="hidden absolute group-hover:flex">
            <ul class="flex flex-col mt-4 min-w-[6rem] bg-white shadow-md">
              <li class="p-2 hover:bg-gray-200">
                <a href="#">Team 1</a>
              </li>
              <li class="p-2 hover:bg-gray-200">
                <a href="#">Team 2</a>
              </li>
            </ul>
          </div>
        </div>
        <a
          class="px-3 py-2 mx-1 text-sm font-medium leading-5 text-center text-white transition-colors duration-200 transform bg-gray-500 rounded-md hover:bg-orange-600 md:mx-2 md:w-auto"
          href="#"
          >Logout</a
        >
      </div>
    </div>
  </nav>
</template>
