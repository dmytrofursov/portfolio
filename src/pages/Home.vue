<script setup>
import Header from '../components/navbar/Header.vue';
import Section from '../components/ui/Section.vue';
import Container from '../components/ui/Container.vue';
import TextBlock from '../components/ui/TextBlock.vue';
import Heading from '../components/ui/Heading.vue';
import HeroCamera from '../components/hero-camera/HeroCamera.vue'
import ExperienceList from '@/components/ui/ExperienceList.vue';
</script>

<template>
  <Header />

  <!--Hero Camera-->
  <Section>
    <Container>
      <TextBlock text="welcome!" />
      <Heading headingText="I innovate your robotized projects." />
    </Container>
    <HeroCamera />
  </Section>

  <!--Expreince Company Logos-->
  <Section>
    <Container>
      <h2 class="secondary-heading">Experience</h2>
      <Suspense>
        <!-- component with nested async dependencies -->
        <ExperienceList />

        <!-- loading state via #fallback slot -->
        <template #fallback>
          Loading...
        </template>
      </Suspense>
    </Container>
  </Section>
</template>
