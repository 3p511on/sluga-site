<template>
  <section class="text-center">
    <v-layout column wrap class="my-5" align-center>
      <v-flex xs12 sm4 class="my-3">
        <div v-if="$vuetify.breakpoint.xsOnly" style="font-size: 30px">
          Программа партии
          <img src="@/assets/file.png" width="24px" />
        </div>
        <div v-else style="font-size: 45px">
          Программа партии
          <img src="@/assets/file.png" width="40px" />
        </div>
      </v-flex>
    </v-layout>

    <v-layout column wrap class="my-5" align-center>
      <v-flex xs12 sm4 class="my-3">
        <v-row justify="center">
          <v-expansion-panels popout hover style="max-width: 580px; margin: 10px;" focusable>
            <v-expansion-panel v-for="(message, i) in messages" :key="i" hide-actions>
              <v-expansion-panel-header class="white--text" color="rgb(52, 151, 77)">
                <v-row align="center" class="spacer" no-gutters>
                  <v-col cols="1" sm="1" md="1">
                    <v-avatar size="24px" tile>
                      <img v-if="message.img" alt="💼" :src="message.img" />
                    </v-avatar>
                  </v-col>
                  <strong v-html="message.name" style="padding-left: 15px"></strong>
                </v-row>
              </v-expansion-panel-header>

              <v-expansion-panel-content>
                <v-divider></v-divider>
                <v-card-text>
                  <span v-for="n in message.text" :key="n">
                    {{n}}
                    <br />
                  </span>
                </v-card-text>
              </v-expansion-panel-content>
            </v-expansion-panel>
          </v-expansion-panels>
        </v-row>
      </v-flex>
    </v-layout>
  </section>
</template>

<script>
export default {
  name: "Program",
  data: () => ({
    messages: [
      // Тебе сюда, милый человек
      {
        img:
          "https://emojipedia-us.s3.dualstack.us-west-1.amazonaws.com/thumbs/120/microsoft/209/briefcase_1f4bc.png",
        name: "Правительство",
        text: [
          "1. Введение импичмента Губернатору",
          "2. Более грамотное и рациональное распределение государственной казны между Министерствами, и органами власти",
          "3. Кабинет Министров не сможет самостоятельно отклонить решения Парламента без согласия Конституционного Суда",
          "4. Уменьшение пенсионного возраста Жителям Штата Ред-Рок",
          "5. Увеличение полномочий Судебной системе, и право на голос в Заседаниях Парламента (если он требуется)"
        ]
      },
      {
        img:
          "https://emojipedia-us.s3.dualstack.us-west-1.amazonaws.com/thumbs/120/microsoft/209/pistol_1f52b.png",
        name: "Министерство обороны",
        text: [
          "1. Введение военной (3-х дневной) академии для бойцов Армии.Академия представляет из себя ряд заданий, и обучающих упражнений. Со стороны правительства будет оказана материальная помощь бойцам в качестве премии за труды. ",
          '2. Введение Ордена "Герой Штата". Орден из себя являет наивысшую государственную заслугу. Боец, который больше всех проявил себя на ЧС, и обеспечивает максимальную защиту базы, и помогает своим коллегам получает данный орден. Министр обороны на заседании Кабинета министров выдвигает бойца на получение ордена, и путём голосования, он награждается данным орденом. Премия за получения ордена будет составлять - 250.000$.',
          "3. Введение боевых учений бойцам. 1-3 раза в неделю Министр Обороны совместно с Губернатором организовывает 2 военных Части, и они между собой проводят некоторые учения, где будут использованы тактические и физические умения бойцов.",
          "4. Часовой Отряд (ЧО). Отряд рядовых, которые занимаются охранной военного объекта на постах.",
          "5. Отдел Пешей Гвардии (ОПГ). Суть отряда состоит в пешем осмотре военного объекта, проверка Цехов, и порядка в Части.",
          "5. Отдел Пешей Гвардии (ОПГ). Суть отряда состоит в пешем осмотре военного объекта, проверка Цехов, и порядка в Части.",

          "5. Отдел Пешей Гвардии (ОПГ). Суть отряда состоит в пешем осмотре военного объекта, проверка Цехов, и порядка в Части.",

          "5. Отдел Пешей Гвардии (ОПГ). Суть отряда состоит в пешем осмотре военного объекта, проверка Цехов, и порядка в Части.",
          "5. Отдел Пешей Гвардии (ОПГ). Суть отряда состоит в пешем осмотре военного объекта, проверка Цехов, и порядка в Части."
        ]
      },
      {
        img:
          "https://emojipedia-us.s3.dualstack.us-west-1.amazonaws.com/thumbs/120/microsoft/209/police-officer_1f46e.png",
        name: "Министерство юстиции",
        text: "123"
        // excerpt: "Защита и оборона нашего штата",
      },
      {
        img:
          "https://emojipedia-us.s3.dualstack.us-west-1.amazonaws.com/thumbs/120/microsoft/209/hospital_1f3e5.png",
        name: "Министерство здравоохранения",
        text: "123"
        // excerpt: "Защита и оборона нашего штата",
      },
      {
        img:
          "https://emojipedia-us.s3.dualstack.us-west-1.amazonaws.com/thumbs/120/microsoft/209/camera-with-flash_1f4f8.png",
        name: "СМИ",
        text: "123"
        // excerpt: "Защита и оборона нашего штата",
      },
      {
        img:
          "https://emojipedia-us.s3.dualstack.us-west-1.amazonaws.com/thumbs/120/microsoft/209/money-with-wings_1f4b8.png",
        name: "Банк",
        text: "123"
        // excerpt: "Защита и оборона нашего штата",
      },
      {
        img:
          "https://emojipedia-us.s3.dualstack.us-west-1.amazonaws.com/thumbs/120/microsoft/209/oncoming-automobile_1f698.png",
        name: "Автошкола",
        text: "123"
        // excerpt: "Защита и оборона нашего штата",
      }
    ]
  })
};
</script>

<style>
</style>