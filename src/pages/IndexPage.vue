<template>
  <q-page class="">
    <q-carousel swipeable animated v-model="slide" :autoplay="autoplay" ref="carousel" infinite>
      <q-carousel-slide :name="1" img-src="https://cdn.quasar.dev/img/mountains.jpg" />
      <q-carousel-slide :name="2" img-src="https://cdn.quasar.dev/img/parallax1.jpg" />
      <q-carousel-slide :name="3" img-src="https://cdn.quasar.dev/img/parallax2.jpg" />
      <q-carousel-slide :name="4" img-src="https://cdn.quasar.dev/img/quasar.jpg" />

      <template v-slot:control>
        <q-carousel-control
          position="top-right"
          :offset="[18, 18]"
          class="text-white rounded-borders"
          style="background: rgba(0, 0, 0, 0.3); padding: 4px 8px"
        >
          <q-toggle dense dark color="orange" v-model="autoplay" label="Auto Play" />
        </q-carousel-control>

        <q-carousel-control position="bottom-right" :offset="[18, 18]" class="q-gutter-xs">
          <q-btn
            push
            round
            dense
            color="orange"
            text-color="black"
            icon="arrow_left"
            @click="$refs.carousel.previous()"
          />
          <q-btn
            push
            round
            dense
            color="orange"
            text-color="black"
            icon="arrow_right"
            @click="$refs.carousel.next()"
          />
        </q-carousel-control>
      </template>
    </q-carousel>
    <div class="row">
      <div class="col">
        <div class="q-pa-md row items-start q-gutter-md">
          <q-card class="my-card" flat bordered>
            <q-img src="https://cdn.quasar.dev/img/parallax2.jpg" />

            <q-card-section>
              <div class="text-overline text-orange-9">Overline 1</div>
              <div class="text-h5 q-mt-sm q-mb-xs">Title</div>
              <div class="text-caption text-grey">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
                incididunt ut labore et dolore magna aliqua.
              </div>
            </q-card-section>

            <q-card-actions>
              <q-btn flat color="primary" label="Share" />
              <q-btn flat color="secondary" label="Book" />

              <q-space />

              <q-btn
                color="grey"
                round
                flat
                dense
                :icon="expanded ? 'keyboard_arrow_up' : 'keyboard_arrow_down'"
                @click="expanded = !expanded"
              />
            </q-card-actions>

            <q-slide-transition>
              <div v-show="expanded">
                <q-separator />
                <q-card-section class="text-subtitle2">
                  {{ lorem }}
                </q-card-section>
              </div>
            </q-slide-transition>
          </q-card>
        </div>
      </div>
      <div class="col">
        <div class="q-pa-md row items-start q-gutter-md">
          <q-card class="my-card" flat bordered>
            <q-img src="https://cdn.quasar.dev/img/parallax2.jpg" />

            <q-card-section>
              <div class="text-overline text-orange-9">Overline 2</div>
              <div class="text-h5 q-mt-sm q-mb-xs">Title</div>
              <div class="text-caption text-grey">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
                incididunt ut labore et dolore magna aliqua.
              </div>
            </q-card-section>

            <q-card-actions>
              <q-btn flat color="primary" label="Share" />
              <q-btn flat color="secondary" label="Book" />

              <q-space />

              <q-btn
                color="grey"
                round
                flat
                dense
                :icon="expanded ? 'keyboard_arrow_up' : 'keyboard_arrow_down'"
                @click="expanded1 = !expanded1"
              />
            </q-card-actions>

            <q-slide-transition>
              <div v-show="expanded1">
                <q-separator />
                <q-card-section class="text-subtitle2">
                  {{ lorem }}
                </q-card-section>
              </div>
            </q-slide-transition>
          </q-card>
        </div>
      </div>
      <div class="col">
        <div class="q-pa-md row items-start q-gutter-md">
          <q-card class="my-card" flat bordered>
            <q-img src="https://cdn.quasar.dev/img/parallax2.jpg" />

            <q-card-section>
              <div class="text-overline text-orange-9">Overline 3</div>
              <div class="text-h5 q-mt-sm q-mb-xs">Title</div>
              <div class="text-caption text-grey">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
                incididunt ut labore et dolore magna aliqua.
              </div>
            </q-card-section>

            <q-card-actions>
              <q-btn flat color="primary" label="Share" />
              <q-btn flat color="secondary" label="Book" />

              <q-space />

              <q-btn
                color="grey"
                round
                flat
                dense
                :icon="expanded ? 'keyboard_arrow_up' : 'keyboard_arrow_down'"
                @click="expanded2 = !expanded2"
              />
            </q-card-actions>

            <q-slide-transition>
              <div v-show="expanded2">
                <q-separator />
                <q-card-section class="text-subtitle2">
                  {{ lorem }}
                </q-card-section>
              </div>
            </q-slide-transition>
          </q-card>
        </div>
      </div>
      <div class="col">
        <div class="q-pa-md row items-start q-gutter-md">
          <q-card class="my-card" flat bordered>
            <q-img src="https://cdn.quasar.dev/img/parallax2.jpg" />

            <q-card-section>
              <div class="text-overline text-orange-9">Overline 4</div>
              <div class="text-h5 q-mt-sm q-mb-xs">Title</div>
              <div class="text-caption text-grey">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
                incididunt ut labore et dolore magna aliqua.
              </div>
            </q-card-section>

            <q-card-actions>
              <q-btn flat color="primary" label="Share" />
              <q-btn flat color="secondary" label="Book" />

              <q-space />

              <q-btn
                color="grey"
                round
                flat
                dense
                :icon="expanded ? 'keyboard_arrow_up' : 'keyboard_arrow_down'"
                @click="expanded3 = !expanded3"
              />
            </q-card-actions>

            <q-slide-transition>
              <div v-show="expanded3">
                <q-separator />
                <q-card-section class="text-subtitle2">
                  {{ lorem }}
                </q-card-section>
              </div>
            </q-slide-transition>
          </q-card>
        </div>
      </div>
      <div class="col">
        <div class="q-pa-md row items-start q-gutter-md">
          <q-card class="my-card" flat bordered>
            <q-img src="https://cdn.quasar.dev/img/parallax2.jpg" />

            <q-card-section>
              <div class="text-overline text-orange-9">Overline 5</div>
              <div class="text-h5 q-mt-sm q-mb-xs">Title</div>
              <div class="text-caption text-grey">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
                incididunt ut labore et dolore magna aliqua.
              </div>
            </q-card-section>

            <q-card-actions>
              <q-btn flat color="primary" label="Share" />
              <q-btn flat color="secondary" label="Book" />

              <q-space />

              <q-btn
                color="grey"
                round
                flat
                dense
                :icon="expanded ? 'keyboard_arrow_up' : 'keyboard_arrow_down'"
                @click="expanded4 = !expanded4"
              />
            </q-card-actions>

            <q-slide-transition>
              <div v-show="expanded4">
                <q-separator />
                <q-card-section class="text-subtitle2">
                  {{ lorem }}
                </q-card-section>
              </div>
            </q-slide-transition>
          </q-card>
        </div>
      </div>
      <div class="col">
        <div class="q-pa-md row items-start q-gutter-md">
          <q-card class="my-card" flat bordered>
            <q-img src="https://cdn.quasar.dev/img/parallax2.jpg" />

            <q-card-section>
              <div class="text-overline text-orange-9">Overline 6</div>
              <div class="text-h5 q-mt-sm q-mb-xs">Title</div>
              <div class="text-caption text-grey">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
                incididunt ut labore et dolore magna aliqua.
              </div>
            </q-card-section>

            <q-card-actions>
              <q-btn flat color="primary" label="Share" />
              <q-btn flat color="secondary" label="Book" />

              <q-space />

              <q-btn
                color="grey"
                round
                flat
                dense
                :icon="expanded ? 'keyboard_arrow_up' : 'keyboard_arrow_down'"
                @click="expanded5 = !expanded5"
              />
            </q-card-actions>

            <q-slide-transition>
              <div v-show="expanded5">
                <q-separator />
                <q-card-section class="text-subtitle2">
                  {{ lorem }}
                </q-card-section>
              </div>
            </q-slide-transition>
          </q-card>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script>
import { ref } from 'vue'

export default {
  setup() {
    return {
      slide: ref(1),
      autoplay: ref(false),
      expanded: ref(false),
      lorem:
        'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
      expanded1: ref(false),
      lorem1:
        'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
      expanded2: ref(false),
      lorem2:
        'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
      expanded3: ref(false),
      lorem3:
        'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
      expanded4: ref(false),
      lorem4:
        'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
      expanded5: ref(false),
      lorem5:
        'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
    }
  },
}
</script>
