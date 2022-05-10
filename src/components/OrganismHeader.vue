<template>
  <header
    class="absolute inset-x-0 text-gray-100 py-4 flex flex-wrap items-center"
  >
    <div
      class="
        w-full
        md:w-3/4
        px-4
        pb-4
        md:pb-0
        flex
        items-center
        justify-between
      "
    >
      <AtomLogo />
      <MoleculeLinks class="flex" :links="links" />
    </div>
    <div class="w-full md:w-1/4 px-4">
      <AtomButton :link="{ name: 'Button', url: '#' }" />
    </div>
  </header>
</template>

<script>
import AtomLogo from './AtomLogo.vue';
import AtomButton from './AtomButton.vue';
import MoleculeLinks from './MoleculeLinks.vue';

export default {
  name: 'OrganismHeader',
  props: ['links'],
  components: {
    AtomLogo,
    AtomButton,
    MoleculeLinks,
  },
};
</script>
