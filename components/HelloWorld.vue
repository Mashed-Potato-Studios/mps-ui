<script setup lang="ts">
const router = useRouter();

const asideLinks = [
  {text: "Documentation", to: "/"},
  {text: "MPS", to: "/mps"},
  {text: "Releases", to: "/changelog"},
];

// const navigate = (route: string) => {
//   console.log(route);
//   router.push(route);
// };
</script>

<template>
  <div>
    <!--    <v-app-bar :elevation="2"></v-app-bar>-->
    <MPSHeader headerTitle="MPS UI Layer" :links="asideLinks"/>
    <v-main>
      <v-breadcrumbs bg-color="green" :items="['Documentation', 'Components', 'MPSMain']"></v-breadcrumbs>
      <v-container fluid>
        <v-row>
          <!-- Aside Feature 1 -->
          <v-col xs="12" sm="4" md="3">
            <!-- Add content for the first aside feature here -->
            <v-navigation-drawer
              v-model="drawer"
              :rail="rail"
              permanent
              @click="rail = false"
            >
              <v-list-item
                prepend-avatar="https://images.unsplash.com/photo-1559275117-d096eb5d85b2?auto=format&fit=crop&q=80&w=1365&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
                title="Cookies and Milk"
                nav
              >
                <template v-slot:append>
                  <v-btn
                    variant="text"
                    icon="mdi-chevron-left"
                    @click.stop="rail = !rail"
                  ></v-btn>
                </template>
              </v-list-item>

              <v-divider></v-divider>

              <v-list density="compact" nav>
                <v-list-item title="Home" value="home"></v-list-item>
                <v-list-item title="My Account" value="account"></v-list-item>
                <v-list-item title="Users" value="users"></v-list-item>
              </v-list>
              <v-divider></v-divider>
              <v-list-item
                prepend-avatar="https://images.unsplash.com/photo-1559275117-d096eb5d85b2?auto=format&fit=crop&q=80&w=1365&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
                title="Page"
                nav
              >
                <template v-slot:append>
                  <v-btn
                    variant="text"
                    icon="mdi-chevron-left"
                  ></v-btn>
                </template>
              </v-list-item>
              <v-divider></v-divider>
              <v-list density="compact" nav>
                <v-list-item title="MPSPageHero" value="home"></v-list-item>
                <v-list-item title="MPSPageBody" value="account"></v-list-item>
                <v-list-item title="MPSPageCard" value="users"></v-list-item>
              </v-list>
            </v-navigation-drawer>

          </v-col>

          <!-- Content Layer in the Middle -->
          <v-col xs="12" sm="8" md="6">
            <!-- Add your main content here -->
            <v-sheet
              class="d-flex align-center pb-16"
            >
              <v-container class="text-center">
                <v-responsive class="mx-auto">

                  <h3 class="text-h1">
                    Try the new MPS UI Layer
                  </h3>

                  <p class="mt-4 text-medium-emphasis">
                    loriem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore
                    et dolore magna aliqua.
                  </p>
                  <v-img
                    src="https://images.unsplash.com/photo-1623659945109-a0ab8cee7762?auto=format&fit=crop&q=80&w=1287&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
                    height="700"
                  />

                </v-responsive>
              </v-container>
            </v-sheet>
            <v-divider class="border-opacity-50"></v-divider>
            <MPSLandingHero title="Supercharged MPS" description="This is a hero">
              <v-img
                :width="500"
                max-height="1000"
                aspect-ratio="16/9"
                src="https://images.unsplash.com/photo-1623659945109-a0ab8cee7762"
              ></v-img>
            </MPSLandingHero>
            <v-sheet
              class="py-16"
              color="#181818"
            >
              <section id="grid">
                <v-container>
                  <v-row justify="space-between">
                    <v-col cols="auto">
                      <v-responsive
                        class="overflow-visible"
                        width="350"
                      >
                        <h2 class="text-h4">
                          Shape the future of Vuetify
                        </h2>

                        <p class="text-success mt-3">
                          Support Development
                        </p>

                        <strong>Become a sponsor</strong>

                        <p class="mt-8">
                          Vuetify is free to use software under the <a href="https://opensource.org/licenses/MIT"
                                                                       target="_blank" rel="noopener noreferrer">MIT</a>
                          License and requires an extensive amount of time to maintain. Supporting development ensures
                          Vuetify will be actively maintained.
                        </p>

                        <v-btn-alt
                          class="mt-6 "
                          href="https://github.com/sponsors/johnleider"
                          target="_blank"
                          rel="noopener noreferrer"
                          text="Support now"
                          prepend-icon="$vuetify"
                        />
                      </v-responsive>
                    </v-col>

                    <v-img
                      max-width="400"
                      src="https://cdn.vuetifyjs.com/store/themes/vite-free/vuetify.png"
                    />
                  </v-row>
                </v-container>
              </section>
            </v-sheet>
            <v-divider class="border-opacity-50"></v-divider>
            <v-sheet
              class="py-16"

            >
              <section id="grid">
                <v-container>
                  <v-row justify="space-between">
                    <v-col cols="auto">
                      <v-responsive
                        class="overflow-visible"
                        width="350"
                      >
                        <h2 class="text-h4">
                          Shape the future of Vuetify
                        </h2>

                        <p class="text-success mt-3">
                          Support Development
                        </p>

                        <strong>Become a sponsor</strong>

                        <p class="mt-8">
                          Vuetify is free to use software under the <a href="https://opensource.org/licenses/MIT"
                                                                       target="_blank" rel="noopener noreferrer">MIT</a>
                          License and requires an extensive amount of time to maintain. Supporting development ensures
                          Vuetify will be actively maintained.
                        </p>

                        <v-btn-alt
                          class="mt-6 "
                          href="https://github.com/sponsors/johnleider"
                          target="_blank"
                          rel="noopener noreferrer"
                          text="Support now"
                          prepend-icon="$vuetify"
                        />
                      </v-responsive>
                    </v-col>

                    <v-img
                      max-width="400"
                      src="https://cdn.vuetifyjs.com/store/themes/vite-free/vuetify.png"
                    />
                  </v-row>
                </v-container>
              </section>
            </v-sheet>

            <v-card title="Card title" subtitle="Subtitle" text="...">
              <v-card-actions>
                <v-btn>Click me</v-btn>
              </v-card-actions>
            </v-card>
          </v-col>
          <!-- Aside Feature 2 -->
          <!--          <v-col xs="12" sm="4" md="3">-->
          <!--            &lt;!&ndash; Add content for the first aside feature here &ndash;&gt;-->
          <!--            <v-naviagtion-drawer location="right">-->
          <!--              <v-list>-->
          <!--                <v-list-item v-for="link in asideLinks" :key="link.text">-->
          <!--                  <v-list-item-title>{{ link.text }}</v-list-item-title>-->
          <!--                </v-list-item>-->
          <!--              </v-list>-->
          <!--            </v-naviagtion-drawer>-->
          <!--          </v-col>-->
        </v-row>
      </v-container>

    </v-main>
    <MPSFooter/>
  </div>
</template>
