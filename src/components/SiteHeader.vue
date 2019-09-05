<template>
  <header class="bg-gray-900 sm:flex sm:items-center sm:justify-between xl:bg-white">
    <div
      class="px-4 py-3 flex justify-between items-center sm:items-baseline xl:w-72 xl:py-5 xl:justify-center xl:bg-gray-900"
    >
      <!-- Logo -->
      <div>
        <svg
          class="h-8 w-auto"
          width="183"
          height="30"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M120.09 27.336c2.352 0 4.392-1.248 5.424-3.12l-2.688-1.536c-.48.984-1.512 1.584-2.76 1.584-1.848 0-3.216-1.368-3.216-3.264 0-1.92 1.368-3.288 3.216-3.288 1.224 0 2.256.624 2.736 1.608l2.664-1.56c-.984-1.848-3.024-3.096-5.376-3.096-3.648 0-6.336 2.76-6.336 6.336 0 3.576 2.688 6.336 6.336 6.336zM136.084 15v1.416c-.864-1.08-2.16-1.752-3.912-1.752-3.192 0-5.832 2.76-5.832 6.336 0 3.576 2.64 6.336 5.832 6.336 1.752 0 3.048-.672 3.912-1.752V27h3.096V15h-3.096zm-3.336 9.384c-1.896 0-3.312-1.368-3.312-3.384s1.416-3.384 3.312-3.384c1.92 0 3.336 1.368 3.336 3.384s-1.416 3.384-3.336 3.384zM148.851 17.976V15h-2.712v-3.36l-3.096.936V15h-2.088v2.976h2.088v4.992c0 3.24 1.464 4.512 5.808 4.032v-2.808c-1.776.096-2.712.072-2.712-1.224v-4.992h2.712zM152.57 13.56c1.056 0 1.92-.864 1.92-1.896s-.864-1.92-1.92-1.92c-1.032 0-1.896.888-1.896 1.92s.864 1.896 1.896 1.896zM151.034 27h3.096V15h-3.096v12zM162.676 27.336c3.528 0 6.36-2.76 6.36-6.336 0-3.576-2.832-6.336-6.36-6.336-3.528 0-6.336 2.76-6.336 6.336 0 3.576 2.808 6.336 6.336 6.336zm0-3.024c-1.824 0-3.24-1.368-3.24-3.312 0-1.944 1.416-3.312 3.24-3.312 1.848 0 3.264 1.368 3.264 3.312 0 1.944-1.416 3.312-3.264 3.312zM177.886 14.664c-1.608 0-2.856.6-3.576 1.68V15h-3.096v12h3.096v-6.48c0-2.088 1.128-2.976 2.64-2.976 1.392 0 2.376.84 2.376 2.472V27h3.096v-7.368c0-3.192-1.992-4.968-4.536-4.968z"
            fill="#A3BFFA"
          />
          <path
            d="M60.063 27h3.768l3.144-11.088L70.143 27h3.768l4.704-16.8h-3.48L71.92 22.656 68.391 10.2H65.56l-3.504 12.456L58.84 10.2h-3.48L60.063 27zM84.674 27.336c3.528 0 6.36-2.76 6.36-6.336 0-3.576-2.832-6.336-6.36-6.336-3.528 0-6.336 2.76-6.336 6.336 0 3.576 2.808 6.336 6.336 6.336zm0-3.024c-1.824 0-3.24-1.368-3.24-3.312 0-1.944 1.416-3.312 3.24-3.312 1.848 0 3.264 1.368 3.264 3.312 0 1.944-1.416 3.312-3.264 3.312zM96.308 17.064V15h-3.096v12h3.096v-5.736c0-2.52 2.04-3.24 3.648-3.048V14.76c-1.512 0-3.024.672-3.648 2.304zM112.831 27l-4.968-6.072L112.687 15h-3.696l-4.128 5.28V10.2h-3.096V27h3.096v-5.448L109.231 27h3.6z"
            fill="#fff"
          />
          <path
            fill-rule="evenodd"
            clip-rule="evenodd"
            d="M42.911 11.604L35.213 7.16v20.645h9v2h-44v-2h4v-12.72l-3.728.933L0 14.078l21.09-5.273h3.122a9.551 9.551 0 0 0-.68 2.559l-.483 3.975 5.164-2.982v15.448h5V7.161l-7.696 4.444a7.502 7.502 0 0 1 2.565-4.8h-4.12a7.489 7.489 0 0 1 6.646-2.972L25.017.603a7.488 7.488 0 0 1 6.696.403c1.039.6 1.88 1.41 2.5 2.347a7.461 7.461 0 0 1 2.5-2.347 7.49 7.49 0 0 1 6.698-.402l-5.593 3.229a7.488 7.488 0 0 1 6.646 2.973h-4.12a7.498 7.498 0 0 1 2.567 4.798zM24.213 27.805v-10h-6v10h6zm-11-8a2 2 0 1 1-4 0 2 2 0 0 1 4 0z"
            fill="#A3BFFA"
          />
        </svg>
      </div>
      <div class="flex sm:hidden">
        <button @click="toggle" type="button">
          <svg
            class="h-6 w-6 fill-current text-gray-500 hover:text-white focus:outline-none focus:text-white"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
          >
            <path d="M0 0h24v24H0z" fill="none" />
            <path
              v-if="isOpen"
              d="M19 6.41L17.59 5 12 10.59 6.41 5 5 6.41 10.59 12 5 17.59 6.41 19 12 13.41 17.59 19 19 17.59 13.41 12z"
            />
            <path v-else d="M3 18h18v-2H3v2zm0-5h18v-2H3v2zm0-7v2h18V6H3z" />
          </svg>
        </button>
      </div>
    </div>

    <nav
      :class="{ 'hidden': !isOpen, 'block': isOpen }"
      class="sm:block xl:px-4 sm:flex sm:items-center xl:flex-1 xl:justify-between"
    >
      <!-- Search -->
      <div class="hidden xl:block xl:relative xl:w-full xl:max-w-xs">
        <div class="absolute inset-y-0 left-0 flex items-center pl-3">
          <svg class="w-6 h-6 fill-current text-gray-500" xmlns="http://www.w3.org/2000/svg">
            <path
              d="M15.5 14h-.79l-.28-.27A6.471 6.471 0 0 0 16 9.5 6.5 6.5 0 1 0 9.5 16c1.61 0 3.09-.59 4.23-1.57l.27.28v.79l5 4.99L20.49 19l-4.99-5zm-6 0C7.01 14 5 11.99 5 9.5S7.01 5 9.5 5 14 7.01 14 9.5 11.99 14 9.5 14z"
            />
            <path d="M0 0h24v24H0z" fill="none" />
          </svg>
        </div>
        <input
          class="sm:block w-full pl-10 pr-4 py-2 border border-transparent bg-gray-200 text-gray-900 rounded-lg focus:outline-none focus:border-gray-200 focus:bg-white focus:text-gray-900"
          placeholder="Search by keywords"
        />
      </div>

      <div class="sm:block sm:flex sm:items-center">
        <div class="px-5 pt-3 pb-5 border-b border-gray-800 sm:py-0 sm:px-1 sm:flex sm:border-0">
          <a
            href="#"
            class="block text-gray-300 font-semibold sm:text-sm hover:text-white xl:text-gray-900 xl:hover:text-gray-700"
          >List your property</a>
          <a
            href="#"
            class="mt-3 block text-gray-300 font-semibold sm:mt-0 sm:ml-6 sm:text-sm hover:text-white xl:text-gray-900 xl:hover:text-gray-700"
          >Trips</a>
          <a
            href="#"
            class="mt-3 block text-gray-300 font-semibold sm:mt-0 sm:ml-6 sm:text-sm hover:text-white xl:text-gray-900 xl:hover:text-gray-700"
          >Messages</a>
        </div>

        <div class="px-5 py-5 sm:py-0 sm:relative">
          <div class="flex items-center sm:hidden">
            <img
              class="h-10 w-10 rounded-full object-cover border-2 border-gray-600 xl:border-gray-300"
              src="https://images.unsplash.com/photo-1487412720507-e7ab37603c6f?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=260&q=80"
              alt="Isla Schoger"
            />
            <span class="ml-4 font-semibold text-gray-200 sm:hidden">Isla Schoger</span>
          </div>

          <div class="sm:hidden mt-4">
            <a href="#" class="block text-gray-400 hover:text-white">Account settings</a>
            <a href="#" class="mt-3 block text-gray-400 hover:text-white">Support</a>
            <a href="#" class="mt-3 block text-gray-400 hover:text-white">Sign out</a>
          </div>

          <Dropdown class="hidden sm:block">
            <template #trigger="{ hasFocus }">
              <span
                class="block h-8 w-8 overflow-hidden rounded-full border-2"
                :class="[hasFocus ? 'border-indigo-400' : 'border-gray-600 xl:border-gray-300']"
              >
                <img
                  class="h-full w-full object-cover"
                  src="https://images.unsplash.com/photo-1487412720507-e7ab37603c6f?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=260&q=80"
                  alt="Isla Schoger"
                />
              </span>
            </template>
            <template #dropdown-items>
              <div class="mr-2 w-48 mt-3 py-2 bg-white rounded-lg shadow-xl xl:border">
                <a
                  href="#"
                  class="block text-gray-400 hover:text-white px-6 py-2 px-4 text-gray-800 hover:bg-indigo-500"
                >Account settings</a>
                <a
                  href="#"
                  class="block text-gray-400 hover:text-white px-6 mt-0 py-2 px-4 text-gray-800 hover:bg-indigo-500"
                >Support</a>
                <a
                  href="#"
                  class="block text-gray-400 hover:text-white px-6 mt-0 py-2 px-4 text-gray-800 hover:bg-indigo-500"
                >Sign out</a>
              </div>
            </template>
          </Dropdown>
        </div>
      </div>
    </nav>
  </header>
</template>

<script>
import Dropdown from "@/components/Dropdown.vue";

export default {
  props: [],
  components: {
    Dropdown
  },
  data() {
    return {
      isOpen: false
    };
  },
  methods: {
    toggle() {
      this.isOpen = !this.isOpen;
    }
  }
};
</script>