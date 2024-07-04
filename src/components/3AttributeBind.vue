<template>
  <h2>3. Attribute Bindings :attr</h2>
  <a v-bind:href="tutorialChannel">Tutorial Link (Old Style v-bind:attr) </a>
  <a :href="tutorialChannel">Tutorial Link (New :attr)</a>
  <img :src="googlePhotosImage" :alt="altText" :height="imgHeight" :width="imgWidth">

</template>

<script setup>
  const tutorialChannel = 'https://www.youtube.com/watch?v=pgWZLS75Nmo&t=16s'
  const googlePhotosImage =  'https://lh3.googleusercontent.com/pw/AP1GczO4afjD3G7cLoweIYK64eVQ1P7AJJIKo5uV458e-_0preahkAcYktQ7jsA2v2py_JFtbf-iIyHPbW0yMrjwkSR52ge5bL3xXXks2OgEzGpdUS24qqkotaDZTuxDoP6J-o8pDzZ_MIH6NBf5qWu9HvawYIoDdp6Z0FXvtkzAessAhVFHNZGtlKNEOPDvfgsGoReuVwJ3r0yefV9uM-loT_3WCwGmUNTwW0vw2AloJ65gpee2Bwca3m6JZU_pGy_46T8tNulMFvPbBsIGMMQENbz10EemrJWuUV-GHzvDb6F-UIYUC42RmcPZ_fEAN94GTFg1suRksm7hv4fybuw8B1QNTLIbhe5N_4kbj00wxpn04uxVavblMVoaVH93lPXdeB43iUf93WPzLCS9qmHv2GCogn4Vd_SAGZ99W_H5hkn1U1oObbUAKVWsHM6KqVeDLxJGPCVGMXxR0sd3_1VbkHY6h2nvjPxew-nSZmcTOxWwQPNht-Vn5PUgZhQ6rOXaNuHJvMVUtiCPkhG8m2VuZ4EcEoNBvi9g1lSiKOZ_np4eeXAOvRhB4kqqWglaBHGtBsuvW1Xf68yVaLR-5bdRC3X7Gn1YZkLC8yMKDvXmmhdQJAFlj0kLqVTUsgQwFiPzSnJepRe-WUFyAvIkb_WN8issE8Psd4HJkqxD7tXQs4Nfe6DqRzN5tlSoOc05Q_0VpnhqDjGuPPzZ-Nynl2LFl_iPw1aNyi2INzpukuAFR0Tf9j8AHfSIb3SQMMuhIZLTQ7IfzoLS-LEOkMCsuxNeTgQ_l8CiqhvtEtn9Ef1Yv2UXaC-G4D8AlvRLOFqxcmx7DZF_3EeHuXuNAsn_ILv6hGhbX4xoz8jR1PxwAg--QecHZyJfNgO5b9hK7bFQThraeVhnb0M3G8RWxLSlXLkKKeD8IOi9z2-tG7xvxl71CgBSP05xDH4ppbzZJYAV=w1259-h680-s-no-gm?authuser=0'
  const altText = 'Sample alttext'
  const imgHeight = 100
  const imgWidth = 200
</script>

<style scoped>
a, img {
  display: block;
  text-align: left;
  margin: 0;
  padding-left: 20px;
}
</style>