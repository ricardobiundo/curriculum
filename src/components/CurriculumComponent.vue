<template>
  <v-container>
    <v-row justify="center">
      <v-col cols="10">
        <v-timeline
          align-top
          :dense="$vuetify.breakpoint.smAndDown"
        >
          <v-timeline-item>
            <template v-slot:icon>
              <v-avatar>
                <img src="../assets/asml.png">
              </v-avatar>
            </template>
            <!-- <template v-slot:opposite>
              <div>ASML</div>
              <div>Feb 2021 - Present · 1 yr 7 mos</div>
            </template> -->
            <v-card
              color="indigo"
              dark
            >
              <v-card-title class="text-h6">
                Scrum master and fullstack developer
              </v-card-title>
              <v-img
                height="250"
                src="https://eindhovennews.com/wp-content/uploads/2020/01/ASML-Campus-in-Veldhoven-with-logo_43661-696x464.jpg"
              ></v-img>
              <v-card-text class="white text--primary">
                <div class="mb-4 text-subtitle-1 text--secondary">
                  <v-row>
                  <v-col cols="6">ASML • Veldhoven, Netherlands</v-col>
                  <v-col cols="6" class="text-right">Feb 2021 - Present · 1yr 7mos</v-col>
                  </v-row>
                </div>
                <div>
                  I'm currently helping ASML by modernizing and improving its testing tool set and workflow.
                  </div>
                  <v-divider light class="ma-4"></v-divider>
                <div class="mb-4 text-subtitle-1 text--secondary">
                  Achievements
                </div>
                  <div>
☆ Introduced four new members to the team and coached them to work in scrum.<br/>
☆ Developed a web application that the entire community uses to keep track of the severity of the regression introduced by their deliveries.<br/>
☆ Created a tool used to find the delivery responsible of breaking tests.<br/>
                </div>
                <v-col class="text-left">
                  <v-chip
                    v-for="(chip, i) in chips"
                    :key="i"
                    outlined
                    class="ma-1"
                    :color=chip.color
                  >
                  <v-icon left>
                    {{ chip.icon }}
                  </v-icon>
                    {{ chip.text }}
                  </v-chip>
                </v-col>
                <!-- <v-btn
                  color="indigo"
                  class="mx-0"
                  outlined
                >
                  Learn More
                </v-btn> -->
                <!-- <v-spacer></v-spacer>
                <v-btn
                  icon
                  @click="show = !show"
                  color="grey"
                >
                  <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
                </v-btn> -->
              </v-card-text>
              <v-expand-transition>
                <div v-show="show">
                  <v-divider></v-divider>
                  <v-card-text>
                    Pepe
                  </v-card-text>
                </div>
              </v-expand-transition>
            </v-card>
          </v-timeline-item>
          <v-timeline-item
            v-for="(item, i) in items"
            :key="i"
            :color="item.color"
            :icon="item.icon"
            fill-dot
          >
            <v-card
              :color="item.color"
              dark
            >
              <v-card-title class="text-h6">
                {{ item.title }}
              </v-card-title>
              <v-card-text class="white text--primary">
                <p>{{ item.text}}</p>
                <v-btn
                  :color="item.color"
                  class="mx-0"
                  outlined
                >
                  Button
                </v-btn>
              </v-card-text>
            </v-card>
          </v-timeline-item>
        </v-timeline>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: 'CurriculumComponent',
    data: () => ({
      show: false,
      items: [
        {
          title: 'Scrum master and fullstack developer',
          text: "I'm currently helping ASML by modernizing and improving its testing tool set and workflow.",
          color: 'red lighten-2',
          icon: 'mdi-star',
        },
        {
          title: 'Software engineer',
          text: 'I work as a software engineer freelancer in web development (full stack), embed systems and electronic engineering projects.',
          color: 'purple darken-1',
          icon: 'mdi-book-variant',
        },
        {
          title: 'Fullstack engineer',
          text: 'Worked per contract as a fullstack developer creating an in house system used to migrate from fleetbird, simplifying the workflow, smartphone support and enabling the team to expand with features nonexistent in the previous system.',
          color: 'green lighten-1',
          icon: 'mdi-airballoon',
        },
        {
          title: 'Fullstack developer',
          text: 'Worked at Microlab, a vibrant co-working space in Strijp-S.I work towards the development of smart buildings, integrating different technologies, designing and developing IOT devices that are customer oriented.',
          color: 'indigo',
          icon: 'mdi-buffer',
        },
      ],
      chips: [
        {
          color: 'grey',
          text: 'grafana',
          icon: 'mdi-chart-pie',
        },
        {
          color: 'red',
          text: 'Jenkins',
          icon: 'fa-brands fa-jenkins',
        },
        {
          color: 'primary',
          text: 'Kubernetes',
          icon: 'mdi-kubernetes',
        },
        {
          color: 'success lighten-2',
          text: 'Django',
          icon: 'mdi-language-python',
        },
        {
          color: 'success',
          text: 'Python',
          icon: 'mdi-language-python',
        },
        {
          color: 'primary',
          text: 'Vue.js',
          icon: 'mdi-vuejs',
        },
      ]
    }),
  }
</script>
<style>
p {
  padding-top: 16px;
}
.v-timeline--align-top .v-timeline-item__body > .v-card:not(.v-card--link)::before {
  top: calc(0% + 22px + 2px);
}
.v-timeline--align-top .v-timeline-item__body > .v-card::after {
  top: calc(0% + 22px);
}
.v-timeline-item__divider {
  top: 11px;
}
.v-timeline-item__opposite {
  align-self: normal;
  position: relative;
  top: 7px;
}
</style>