<template>
  <div class="flex flex-col">
    <div class="mb-8">
      <span class="w-full inline-flex rounded-md shadow-sm">
        <button
          type="button"
          class="flex w-full inline-flex justify-center py-2 px-4 border border-gray-300 rounded-md bg-white text-sm leading-5 font-medium text-gray-500 hover:text-gray-400 focus:outline-none focus:border-blue-300 focus:shadow-outline-blue transition duration-150 ease-in-out"
          aria-label="Sign in with Facebook"
          @click="loginHandler('Facebook')"
        >
          <svg class="h-5 h-5" fill="currentColor" viewBox="0 0 20 20">
            <path
              fill-rule="evenodd"
              d="M20 10c0-5.523-4.477-10-10-10S0 4.477 0 10c0 4.991 3.657 9.128 8.438 9.878v-6.987h-2.54V10h2.54V7.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V10h2.773l-.443 2.89h-2.33v6.988C16.343 19.128 20 14.991 20 10z"
              clip-rule="evenodd"
            />
          </svg>
          <p class="ml-4">Se connecter avec Facebook</p>
        </button>
      </span>
    </div>

    <div>
      <span class="w-full inline-flex rounded-md shadow-sm">
        <button
          type="button"
          class="flex w-full inline-flex justify-center py-2 px-4 border border-gray-300 rounded-md bg-white text-sm leading-5 font-medium text-gray-500 hover:text-gray-400 focus:outline-none focus:border-blue-300 focus:shadow-outline-blue transition duration-150 ease-in-out"
          aria-label="Sign in with Twitter"
          @click="loginHandler('Google')"
        >
          <svg
            aria-hidden="true"
            focusable="false"
            data-prefix="fab"
            data-icon="google"
            role="img"
            xmlns="http://www.w3.org/2000/svg"
            class="h-5 h-5"
            viewBox="0 0 488 512"
          >
            <path
              fill="currentColor"
              d="M488 261.8C488 403.3 391.1 504 248 504 110.8 504 0 393.2 0 256S110.8 8 248 8c66.8 0 123 24.5 166.3 64.9l-67.5 64.9C258.5 52.6 94.3 116.6 94.3 256c0 86.5 69.1 156.6 153.7 156.6 98.2 0 135-70.4 140.8-106.9H248v-85.3h236.1c2.3 12.7 3.9 24.9 3.9 41.4z"
            />
          </svg>
          <p class="ml-4">Se connecter avec Google</p>
        </button>
      </span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Login',
  layout: 'auth',
  methods: {
    loginHandler(provider) {
      this.$store.dispatch('authProvider', provider)
    }
  }
}
</script>