<script setup lang="ts">
import Card from '@/volt/Card.vue'
import RadioButton from '@/volt/RadioButton.vue'
import { ref } from 'vue'
import CrestHeading from '../ui/CrestHeading.vue'
import ToolkitNextButton from '../ui/ToolkitNextButton.vue'

const projectSize = ref<string>('Unknown')
const projectLocation = ref<string>('Unknown')
</script>

<template>
  <div class="w-full flex flex-col">
    <CrestHeading text="About Your Project"></CrestHeading>
    <p>
      Please select from the choices below. These choices will affect the content you see as you
      progress through the toolkit. Select &quot;unknown&quot; if you are unsure or want to see all
      content.
    </p>
    <div class="flex flex-wrap gap-2 mb-4">
      <Card class="w-full sm:w-auto">
        <template #title>Project Size</template>
        <template #content>
          <div class="flex justify-center">
            <div class="flex flex-wrap gap-4">
              <div class="flex items-center gap-2">
                <RadioButton
                  v-model="projectSize"
                  inputId="projectSizeSmall"
                  name="small"
                  value="Small"
                />
                <label for="projectSizeSmall">Small</label>
              </div>
              <div class="flex items-center gap-2">
                <RadioButton
                  v-model="projectSize"
                  inputId="projectSizeMedium"
                  name="medium"
                  value="Medium"
                />
                <label for="projectSizeMedium">Medium</label>
              </div>
              <div class="flex items-center gap-2">
                <RadioButton
                  v-model="projectSize"
                  inputId="projectSizeLarge"
                  name="large"
                  value="Large"
                />
                <label for="projectSizeLarge">Large</label>
              </div>
              <div class="flex items-center gap-2">
                <RadioButton
                  v-model="projectSize"
                  inputId="projectSizeUnknown"
                  name="unknown"
                  value="Unknown"
                />
                <label for="projectSizeUnknown">Unknown</label>
              </div>
            </div>
          </div>
        </template>
      </Card>
      <Card class="w-full sm:w-auto">
        <template #title>Location</template>
        <template #content>
          <div class="flex justify-center">
            <div class="flex flex-wrap gap-4">
              <div class="flex items-center gap-2">
                <RadioButton
                  v-model="projectLocation"
                  inputId="projectLocationOther"
                  name="other"
                  value="Other"
                />
                <label for="projectLocationOther">Non-UK</label>
              </div>
              <div class="flex items-center gap-2">
                <RadioButton
                  v-model="projectLocation"
                  inputId="projectLocationUk"
                  name="uk"
                  value="UK"
                />
                <label for="projectLocationUk">UK</label>
              </div>
              <div class="flex items-center gap-2">
                <RadioButton
                  v-model="projectLocation"
                  inputId="projectLocationUnknown"
                  name="locationUnkown"
                  value="Unknown"
                />
                <label for="projectLocationUnknown">Unkown</label>
              </div>
            </div>
          </div>
        </template>
      </Card>
    </div>
    <div>
      <ToolkitNextButton :phase="3" text="Get Started"></ToolkitNextButton>
    </div>
  </div>
</template>
