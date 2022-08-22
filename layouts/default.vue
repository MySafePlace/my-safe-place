<template>
  <div>
    <PageHeader />
    <Nuxt />
    <script>
      window.watsonAssistantChatOptions = {
        integrationID: 'bc3f38f3-f50f-499c-9f6c-fb813be47da2', // The ID of this integration.
        region: 'au-syd', // The region your integration is hosted in.
        serviceInstanceID: '7e0ce8b2-a61b-4f91-9120-26991bb0c21e', // The ID of your service instance.
        onLoad: function (instance) {
          instance.render()
        },
      }
      setTimeout(function () {
        const t = document.createElement('script')
        t.src =
          'https://web-chat.global.assistant.watson.appdomain.cloud/versions/' +
          (window.watsonAssistantChatOptions.clientVersion || 'latest') +
          '/WatsonAssistantChatEntry.js'
        document.head.appendChild(t)
      })
    </script>
    <PageFooter />
  </div>
</template>

<script>
export default {
  name: 'DefaultLayout',
}
