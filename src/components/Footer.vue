<template>
  <div class="wrapper">
    <footer class="bg-blue-300 text-black py-4 w-full">
      <div class="container mx-auto px-10 flex justify-between items-center">
        <!-- Left side with copyright info -->
        <div class="text-sm">
          <p>&copy; {{ currentYear }} Vanilla</p>
        </div>

        <!-- Middle section with developed by information -->
        <div class="text-sm">
          <p>
            Developed By
            <a href="https://chiraitori.lol" class="text-black hover:underline">Chiraitori</a>
          </p>
        </div>
        <div class="flex space-x-4">
          <a
            href="https://github.com/tathaha"
            target="_blank"
            rel="noopener noreferrer"
            class="text-black hover:text-white"
          >
            <ak-github-fill />
          </a>
          <a
            href="https://discord.com/"
            target="_blank"
            rel="noopener noreferrer"
            class="text-black hover:text-white"
          >
            <ak-discord-fill />
          </a>
          <a
            href="https://www.facebook.com/"
            target="_blank"
            rel="noopener noreferrer"
            class="text-black hover:text-white"
          >
            <ak-facebook-fill />
          </a>
          <a href="mailto:contact@example.com" class="text-black hover:text-white"><cl-mail /> </a>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
import { AkDiscordFill } from '@kalimahapps/vue-icons'
import { AkFacebookFill } from '@kalimahapps/vue-icons'
import { ClMail } from '@kalimahapps/vue-icons'
import { AkGithubFill } from '@kalimahapps/vue-icons'
export default {
  components: {
    AkDiscordFill,
    AkFacebookFill,
    ClMail,
    AkGithubFill
  },
  data() {
    return {
      currentYear: new Date().getFullYear()
    }
  }
}
</script>

<style scoped>
.wrapper {
  min-height: calc(100vh - 60px); /* Adjust 60px according to your header height */
  display: flex;
  flex-direction: column;
}

footer {
  margin-top: auto;
}
</style>
