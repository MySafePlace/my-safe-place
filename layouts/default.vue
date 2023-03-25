<template>
  <div>
    <PageHeader />
    <HeroSection/>
    <FeaturesSection/>
    <StatisticsSection/>
    <CtaSection/>
    <script>
      window.watsonAssistantChatOptions = {
        integrationID: '518a9043-05bb-4278-b728-c9663c147b35', // The ID of this integration.
        region: 'us-south', // The region your integration is hosted in.
        serviceInstanceID: '2966eee3-39a3-4360-b704-e49ca8ab7d53', // The ID of your service instance.
        onLoad: function (instance) {
          instance.writeableElements.beforeInputElement.innerHTML = '¿Estás en una emergencia? Accede a la línea de ayuda 24/7 en el menú desplegable del chat ubicado en la parte superior.';
          instance.updateCustomMenuOptions('bot', [
            { text: 'Linea de Ayuda SOS', handler: function() { 
              navigator.geolocation.getCurrentPosition(function(position) {
                console.log(position.coords.latitude, position.coords.longitude);
                const mapsLink = `https://www.google.es/maps?q=${position.coords.latitude},${position.coords.longitude}`;
                window.open(`https://wa.me/51970807304?text=Hola, estoy en una emergencia. Mi ubicación precisa: ${mapsLink}`, '_blank');
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
