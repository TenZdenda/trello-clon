<template>
  <div class="p-2">
    <header class="w-full flex items-center">
      <div class="flex items-center space-x-5">
        <button class="bg-white bg-opacity-40 p-2 flex text-white rounded">
          <div class="m-auto flex items-center space-x-2">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-4 w-4"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M3 4h13M3 8h9m-9 4h9m5-4v12m0 0l-4-4m4 4l4-4"
              />
            </svg>
            <p class="font-medium">Nástěnka</p>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-4 w-4"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M19 9l-7 7-7-7"
              />
            </svg>
          </div>
        </button>
        <h2 class="text-xl font-bold text-white">Werxa - Changelog</h2>
        <button class="bg-white bg-opacity-40 p-2 rounded text-yellow-200 flex">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6 m-auto"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M11.049 2.927c.3-.921 1.603-.921 1.902 0l1.519 4.674a1 1 0 00.95.69h4.915c.969 0 1.371 1.24.588 1.81l-3.976 2.888a1 1 0 00-.363 1.118l1.518 4.674c.3.922-.755 1.688-1.538 1.118l-3.976-2.888a1 1 0 00-1.176 0l-3.976 2.888c-.783.57-1.838-.197-1.538-1.118l1.518-4.674a1 1 0 00-.363-1.118l-3.976-2.888c-.784-.57-.38-1.81.588-1.81h4.914a1 1 0 00.951-.69l1.519-4.674z"
            />
          </svg>
        </button>
      </div>
      <div class="border-r border-gray-100 opacity-40 w-1 h-5 mx-5"></div>
      <button class="p-2 bg-white bg-opacity-40 rounded font-bold text-white">
        Acme, Inc.
      </button>
      <div class="border-r border-gray-100 opacity-40 w-1 h-5 mx-5"></div>
      <div class="flex items-center space-x-5">
        <div class="flex items-center space-x-4">
          <div class="flex items-center">
            <img
              src="https://images.unsplash.com/photo-1535713875002-d1d0cf377fde?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=580&q=80"
              alt=""
              class="m-auto w-10 h-10 rounded-full"
            />
            <img
              src="https://i.redd.it/ypire7te8rc71.jpg"
              alt=""
              class="m-auto w-10 h-10 rounded-full transform -translate-x-2"
            />
            <img
              src="https://i.stack.imgur.com/frlIf.png"
              alt=""
              class="m-auto w-10 h-10 rounded-full transform -translate-x-4"
            />
            <button
              class="
                h-10
                p-2
                bg-white bg-opacity-40
                rounded-full
                text-sm text-white
                font-bold
              "
            >
              +10 more
            </button>
          </div>
          <button
            class="
              h-10
              py-2
              px-4
              bg-white bg-opacity-40
              rounded
              text-white
              font-bold
            "
          >
            Invite
          </button>
        </div>
      </div>
    </header>
    <main class="mt-4 flex flex-row space-x-4 overflow-auto relative">
      <div v-for="card in cards" :key="card.id">
        <Card :name="card.name" />
      </div>
      <button
        class="
          flex-shrink-0
          rounded
          bg-white bg-opacity-30
          h-10
          p-2
          w-72
          text-white
          font-bold
          flex
          space-x-2
        "
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-5 w-5"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M12 4v16m8-8H4"
          />
        </svg>
        <p>Přidej další sloupec</p>
      </button>
    </main>
  </div>
</template>

<script>
// @ is an alias to /src
import Card from "@/components/Card.vue";

export default {
  name: "Home",
  components: {
    Card,
  },
  data() {
    return {
      cards: [
        {
          id: 1,
          name: "Changelog",
        },
        {
          id: 2,
          name: "Issues from client",
        },
        {
          id: 3,
          name: "Issues from client",
        },
        {
          id: 4,
          name: "Issues from client",
        },
        {
          id: 5,
          name: "Issues from client",
        },
        {
          id: 6,
          name: "Issues from client",
        },
      ],
    };
  },
};
</script>
