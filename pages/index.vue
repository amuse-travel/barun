<template>
<div>
  <v-container>
    <v-card elevation="0">
      <v-row>
        <v-col cols="6">
          <section>
            <v-container>
              <v-row>
                <v-col cols="12">
                  <v-card
                    elevation="0"
                    tile
                  >
                    <v-img src="/images/mascot1.png" data-aos="fade-right" />
                  </v-card>
                </v-col>
              </v-row>
            </v-container>
          </section>
        </v-col>
        <v-col cols="6" class="d-flex justify-start align-center">
          <section>
            <v-card
              class="mx-auto"
              elevation="0"
              tile
            >
              <v-card-title :class="largeFont" class="d-flex flex-column font-weight-bold">
                <div v-if="this.$vuetify.breakpoint.mdAndUp">
                  <div class="black--text mb-2">
                  바른연애생활은
                  </div>
                  <div class="light-blue--text">
                  낯선사람의 얼굴만보고 즉석 만남을 갖을 수는 없습니다...
                  </div>
                </div>
                <div v-else>
                  <span class="black--text mb-2">
                  바른연애생활은
                  </span>
                  <span class="light-blue--text">
                  낯선사람의 얼굴만보고 즉석 만남을 갖을 수는 없습니다...
                  </span>
                </div>
              </v-card-title>
            </v-card>
          </section>
        </v-col>
      </v-row>
      <v-row :style="padding">
        <v-col cols="6"  class="d-flex justify-end align-center">
          <section>
            <v-container>
              <v-row>
                <v-col cols="12">
                  <v-card
                    elevation="0"
                    tile
                  >
                    <v-card-title :class="largeFont" class="d-flex flex-column font-weight-bold">
                      <div v-if="this.$vuetify.breakpoint.mdAndUp">
                        <div class="black--text mb-2">
                        바른연애생활은
                        </div>
                        <div class="light-blue--text">
                        지인과 함께 모임을 개설하고 참가자들을 모집합니다.
                        </div>
                      </div>
                      <div v-else>
                        <span class="black--text mb-2">
                        바른연애생활은
                        </span>
                        <span class="light-blue--text">
                        지인과 함께 모임을 개설하고 참가자들을 모집합니다.
                        </span>
                      </div>
                    </v-card-title>
                  </v-card>
                </v-col>
              </v-row>
            </v-container>
          </section>
        </v-col>
        <v-col cols="6">
          <section>
            <v-container>
              <v-row>
                <v-col cols="12">
                  <v-card
                    elevation="0"
                    tile
                  >
                    <v-img src="/images/mascot2.png" data-aos="fade-left" />
                  </v-card>
                </v-col>
              </v-row>
            </v-container>
          </section>
        </v-col>
      </v-row>
    </v-card>
  </v-container>

  <v-card elevation="0" style="background: #fafafa;">
    <v-container>
      <v-row>
        <v-col cols="6">
          <section>
            <v-container>
              <v-row>
                <v-col cols="12">
                  <v-card
                    elevation="0"
                    color="transparent"
                    tile
                  >
                    <v-img src="/images/screenshot1.png" data-aos="flip-right" />
                  </v-card>
                </v-col>
              </v-row>
            </v-container>
          </section>
        </v-col>
        <v-col cols="6" class="d-flex justify-end align-center">
          <section>
            <v-container>
              <v-row>
                <v-col cols="12">
                  <v-card
                    elevation="0"
                    tile
                    color="transparent"
                  >
                    <v-card-title :class="largeFont" class="font-weight-black">
                      지인과 함께 2:2 모임
                    </v-card-title>
                    <v-card-text v-if="this.$vuetify.breakpoint.mdAndUp" :class="mediumFont" class="font-weight-bold grey--text">
                      지인에게 숨겨가면서 낯선 사람과 1:1 로 만나는 것이 부담스러웠다면 지인과 함께 2:2 로 만나는 모임에 참가해보세요.
                    </v-card-text>
                    <v-card-text v-else :class="mediumFont" class="font-weight-bold grey--text">
                      실제 친구를 바연생에 초대하여 안전하게 모임을 즐기세요.
                    </v-card-text>
                  </v-card>
                </v-col>
              </v-row>
            </v-container>
          </section>
        </v-col>
      </v-row>
    </v-container>
  </v-card>
  <v-card elevation="0">
    <v-container>
      <v-row>
        <v-col cols="6" class="d-flex justify-end align-center">
          <section>
            <v-container>
              <v-row>
                <v-col cols="12">
                  <v-card
                    elevation="0"
                    color="transparent"
                    tile
                  >
                    <v-card-title :class="largeFont" class="font-weight-black">
                      외모·스펙지상주의?!
                    </v-card-title>
                    <v-card-text v-if="this.$vuetify.breakpoint.mdAndUp" :class="mediumFont" class="font-weight-bold grey--text">
                      나를 평가의 대상으로 판단하는 사람들보다 나의 생각과 관심에 공감하는 사람들과 만나보세요.
                    </v-card-text>
                    <v-card-text v-else :class="mediumFont" class="font-weight-bold grey--text">
                      외모보다 나와 공감할 수 있는 사람들과 만나보세요.
                    </v-card-text>
                  </v-card>
                </v-col>
              </v-row>
            </v-container>
          </section>
        </v-col>
        <v-col cols="6">
          <section>
            <v-container>
              <v-row>
                <v-col cols="12">
                  <v-card
                    elevation="0"
                    color="transparent"
                    tile
                  >
                    <v-img src="/images/screenshot2.png" data-aos="flip-left" />
                  </v-card>
                </v-col>
              </v-row>
            </v-container>
          </section>
        </v-col>
      </v-row>
    </v-container>
  </v-card>
  <v-card elevation="0" style="background: #fafafa;">
    <v-container>
      <v-row>
        <v-col cols="6">
          <section>
            <v-container>
              <v-row>
                <v-col cols="12">
                  <v-card
                    elevation="0"
                    color="transparent"
                    tile
                  >
                    <v-img src="/images/screenshot3.png" data-aos="flip-right" />
                  </v-card>
                </v-col>
              </v-row>
            </v-container>
          </section>
        </v-col>
        <v-col cols="6"  class="d-flex justify-end align-center">
          <section>
            <v-container>
              <v-row>
                <v-col cols="12">
                  <v-card
                    elevation="0"
                    color="transparent"
                    tile
                  >
                    <v-card-title :class="largeFont" class="font-weight-black">
                      취미를 공유하는 의미있는 만남
                    </v-card-title>
                    <v-card-text v-if="this.$vuetify.breakpoint.mdAndUp" :class="mediumFont" class="font-weight-bold grey--text">
                      지역별, 관심사별, 또래별 모임들을 검색하고 지인과 함께 2:2 모임에 동참해 보세요.
                    </v-card-text>
                    <v-card-text v-else :class="mediumFont" class="font-weight-bold grey--text">
                      만나서 같이 즐기고 싶은 모임 유형을 선택하세요.
                    </v-card-text>
                  </v-card>
                </v-col>
              </v-row>
            </v-container>
          </section>
        </v-col>
      </v-row>
    </v-container>
  </v-card>

  <div :style="padding"></div>

  <marquee-text class="font-weight-bold grey--text" :duration="30">
    <v-chip class="mx-2" color="#53c6ff" text-color="white" label>바연생 10계명</v-chip>
    <span v-for="(label, i) in labels" :key="i">
      <span>{{ label }}</span>
    </span>
  </marquee-text>
  
  <div :style="padding"></div>

</div>
</template>

<script>
import AOS from 'aos'
import 'aos/dist/aos.css'
import MarqueeText from 'vue-marquee-text-component'

AOS.init({ once: true })

export default {
  components: {
    MarqueeText,
  },
  data() {
    return {
      labels: [
        '✋ 모태솔로라고 남의 애인을 탐하지 마라. ',
        '✋ 없다고 서러워말고 바연생으로 될 때까지 시도하라. ',
        '✋ 상대방이 내 스탈일수록 친구에게 무조건적 양보를 강요하지 마라. ',
        '✋ 프로파일 사진은 반드시 마스크 벗은 사진으로 올리시라. ',
        '✋ 업무시간에 숨어서 채팅하다 실실 쪼개지 마라. ',
        '✋ 채팅방에서 절대 음란대화 하지 마라. ',
        '✋ 생고기는 꼭 익혀드시라. ',
        '✋ 에스컬레이터에서 뛰거나 걷지 마라. ',
        '✋ 5년 전에 비트코인 샀다고 자랑하지 마라. ',
        '✋ 다시보니 박명수랑 닯았다고 말하지 마라. ',
      ]
    }
  },
  computed: {
    padding() {
      return this.$vuetify.breakpoint.mdAndUp ? { 'padding': '48px 0' } : { 'padding': '12px 0' }
    },
    largeFont() {
      return this.$vuetify.breakpoint.mdAndUp ? 'display-2' : 'h6'
    },
    mediumFont() {
      return this.$vuetify.breakpoint.mdAndUp ? 'display-1' : 'body-2'
    },
  },
}
</script>
