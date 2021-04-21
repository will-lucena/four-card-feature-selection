<template>
  <div class="content">
    <header>
      <sentence :pieces="headerTitle" />
    </header>
    <card
      v-for="(card, index) in cards"
      :key="index"
      :title="card.title"
      :description="card.description"
      :imageName="card.imageName"
    />
  </div>
</template>

<script>
import Card from "../components/Card.vue";
import Sentence from "../components/Sentence.vue";

export default {
  components: { Card, Sentence },
  data() {
    return {
      headerTitle: [
        { content: "Reliable, efficient delivery" },
        { content: "Powered by Technology", isBold: true },
        {
          content:
            "Our Artificial Intelligence powered tools use millions of project data points to ensure that your project is successful",
          isSmall: true,
        },
      ],
      cards: [
        {
          title: "Supervisor",
          description: "Monitors activity to identify project roadblocks",
          imageName: "icon-supervisor.svg",
        },
        {
          title: "Team Builder",
          description:
            "Scans our talent network to create the optimal team for your project",
          imageName: "icon-team-builder.svg",
        },
        {
          title: "Karma",
          description: "Regularly evaluates our talent to ensure quality",
          imageName: "icon-karma.svg",
        },
        {
          title: "Calculator",
          description:
            "Uses data from past projects to provide better delivery estimates",
          imageName: "icon-calculator.svg",
        },
      ],
    };
  },
};
</script>

<style></style>
