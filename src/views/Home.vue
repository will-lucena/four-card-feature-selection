<template>
  <div class="content">
    <header>
      <sentence :pieces="headerTitle" />
    </header>
    <div class="cards">
      <div>
        <card
          :title="cards[0].title"
          :description="cards[0].description"
          :imageName="cards[0].imageName"
          :color="cards[0].color"
        />
      </div>
      <div class="cards--center">
        <card
          :title="cards[1].title"
          :description="cards[1].description"
          :imageName="cards[1].imageName"
          :color="cards[1].color"
        />
        <card
          :title="cards[2].title"
          :description="cards[2].description"
          :imageName="cards[2].imageName"
          :color="cards[2].color"
        />
      </div>
      <div>
        <card
          :title="cards[3].title"
          :description="cards[3].description"
          :imageName="cards[3].imageName"
          :color="cards[3].color"
        />
      </div>
    </div>
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
          color: "cyan",
        },
        {
          title: "Team Builder",
          description:
            "Scans our talent network to create the optimal team for your project",
          imageName: "icon-team-builder.svg",
          color: "red",
        },
        {
          title: "Karma",
          description: "Regularly evaluates our talent to ensure quality",
          imageName: "icon-karma.svg",
          color: "orange",
        },
        {
          title: "Calculator",
          description:
            "Uses data from past projects to provide better delivery estimates",
          imageName: "icon-calculator.svg",
          color: "blue",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>
