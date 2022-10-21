<template>
  <div>
    <PageHeader />
    <HeroSection/>
    <FeaturesSection/>
    <StatisticsSection/>
    <CtaSection/>
    <script>
      window.watsonAssistantChatOptions = {
        integrationID: 'bc3f38f3-f50f-499c-9f6c-fb813be47da2', // The ID of this integration.
        region: 'au-syd', // The region your integration is hosted in.
        serviceInstanceID: '7e0ce8b2-a61b-4f91-9120-26991bb0c21e', // The ID of your service instance.
        onLoad: function (instance) {
          instance.writeableElements.beforeInputElement.innerHTML = '¿Estás en una emergencia? Accede a la línea de ayuda 24/7 en el menú desplegable del chat ubicado en la parte superior.';
          instance.updateCustomMenuOptions('bot', [
            { text: 'Linea de Ayuda SOS', handler: function() { 
              navigator.geolocation.getCurrentPosition(function(position) {
                console.log(position.coords.latitude, position.coords.longitude);
                const mapsLink = `\nLatitud: ${position.coords.latitude}\nLongitud: ${position.coords.longitude}`;
                window.open(`https://wa.me/51924533055?text=Hola, estoy en una emergencia. Mi ubicación precisa: ${mapsLink}`, '_blank');
              })} },
            
          ]);
          instance.render();
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
import HeroSection from '~/components/HeroSection.vue';
import FeaturesSection from '~/components/FeaturesSection.vue';
import StatisticsSection from '~/components/StatisticsSection.vue';
import CtaSection from '~/components/CtaSection.vue';

export default {
    name: "DefaultLayout",
    components: { HeroSection, FeaturesSection, StatisticsSection, CtaSection }
}
