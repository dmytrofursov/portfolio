<script setup>
import Header from '../components/navbar/Header.vue';
import Section from '../components/ui/Section.vue';
import Container from '../components/ui/Container.vue';
import TextBlock from '../components/ui/TextBlock.vue';
import Heading from '../components/ui/Heading.vue';
import HeroCamera from '../components/hero-camera/HeroCamera.vue'
</script>

<template>
    <Header />
    <Section>
      <Container>
        <TextBlock text="welcome!" />
        <Heading headingText="I innovate your robotized projects." />
      </Container>
      <HeroCamera />
    </Section>
  </template>