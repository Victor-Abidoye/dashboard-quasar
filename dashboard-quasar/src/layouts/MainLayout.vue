<template>
  <q-layout view="hHh LpR fFf">

    <q-header
      elevated
      class="bg-primary text-secondary"
    >
      <q-toolbar>
        <q-btn
          dense
          flat
          round
          icon="menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title>
          <q-avatar>
            <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg">
          </q-avatar>
          Title
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-drawer
      show-if-above
      v-model="leftDrawerOpen"
      side="left"
      bordered
    >

      <!-- drawer content -->
      <div style="max-width: 350px">
        <q-list
          bordered
          class="rounded-borders"
        >
          <q-expansion-item
            expand-separator
            expand-icon="none"
            label="Menu"
            default-opened
          >
            <q-expansion-item
              :header-inset-level="1"
              :content-inset-level="3"
              expand-separator
              icon="rocket"
              label="Dashboard"
              default-opened
            >
              <q-list
              >
                <q-item
                  clickable
                  v-ripple
                >
                  <q-item-section>Analytics</q-item-section>
                </q-item>
                <q-item
                  clickable
                  v-ripple
                >
                  <q-item-section>Commerce</q-item-section>
                </q-item>
                <q-item
                  clickable
                  v-ripple
                >
                  <q-item-section>Sales</q-item-section>
                </q-item>



                    <q-expansion-item
              expand-separator
              label="Minimal"
            >



            </q-expansion-item>


                <q-item
                  clickable
                  v-ripple
                >
                  <q-item-section>CRM</q-item-section>
                </q-item>


              </q-list>
            </q-expansion-item>

            <q-expansion-item
              :header-inset-level="1"
              :content-inset-level="3"
              expand-separator
              icon="event"
              label="pages"
            >



            </q-expansion-item>
            <q-expansion-item
              :header-inset-level="1"
              :content-inset-level="3"
              expand-separator
              icon="castle"
              label="Applications"
            >



            </q-expansion-item>
          </q-expansion-item>


          <q-expansion-item
            expand-separator
            expand-icon="none"
            label="UI COMPONENTS"
            default-opened
          >
            <q-expansion-item
              :header-inset-level="1"
              :content-inset-level="3"
              expand-separator
              icon="diamond"
              label="Elments"
            >
            </q-expansion-item>

            <q-expansion-item
              :header-inset-level="1"
              :content-inset-level="3"
              expand-separator
              icon="local_taxi"
              label="components"
            >
            </q-expansion-item>
            <q-expansion-item
              :header-inset-level="1"
              :content-inset-level="3"
              expand-separator
              icon="dashboard"
              label="table"
            >
            </q-expansion-item>


          </q-expansion-item>




          <q-expansion-item
            expand-separator
            expand-icon="none"
            label="DASHBOARD WIDGETS"
            default-opened
          >
            <q-expansion-item
              :header-inset-level="1"
              :content-inset-level="3"
              expand-separator
              icon="watch_later"
              label="Chat Boxes 1"
            >
            </q-expansion-item>
            <q-expansion-item
              :header-inset-level="1"
              :content-inset-level="3"
              expand-separator
              icon="question_answer"
              label="Chat Boxes 2"
            >
            </q-expansion-item>

            <q-expansion-item
              :header-inset-level="1"
              :content-inset-level="3"
              expand-separator
              icon="sports_basketball"
              label="Chat Boxes 3"
            >
            </q-expansion-item>
            <q-expansion-item
              :header-inset-level="1"
              :content-inset-level="3"
              expand-separator
              icon="calendar_today"
              label="Chat Boxes 4"
            >
            </q-expansion-item>


          </q-expansion-item>



          <q-expansion-item
            expand-separator
            expand-icon="none"
            label="FORMS"
            default-opened
          >
            <q-expansion-item
              :header-inset-level="1"
              :content-inset-level="3"
              expand-separator
              icon="lightbulb"
              label="Elements"
            >
            </q-expansion-item>
            <q-expansion-item
              :header-inset-level="1"
              :content-inset-level="3"
              expand-separator
              icon="sports_esports"
              label="Widgets"
            >
            </q-expansion-item>




          </q-expansion-item>




          <q-expansion-item
            expand-separator
            expand-icon="none"
            label="CHATS"
            default-opened
          >
            <q-expansion-item
              :header-inset-level="1"
              :content-inset-level="3"
              expand-separator
              icon="insights"
              label="ChartsJS"
            >
            </q-expansion-item>
            <q-expansion-item
              :header-inset-level="1"
              :content-inset-level="3"
              expand-separator
              icon="schedule"
              label="Apex Charts"
            >
            </q-expansion-item>
            <q-expansion-item
              :header-inset-level="1"
              :content-inset-level="3"
              expand-separator
              icon="show_chart"
              label="Chart Sparklines"
            >
            </q-expansion-item>




          </q-expansion-item>


        </q-list>
      </div>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>

  </q-layout>
</template>

<script>
import { ref } from 'vue'

export default {
  setup () {
    const leftDrawerOpen = ref(false)

    return {
      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
}
</script>
