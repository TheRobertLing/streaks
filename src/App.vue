<script setup lang="ts">
import {
  Accordion,
  AccordionContent,
  AccordionItem,
  AccordionTrigger,
} from "@/components/ui/accordion";

import GoToSleepStreak from "./components/streaks/go-to-sleep/GoToSleepStreak.vue";
import DrinkWaterStreak from "./components/streaks/drink-water/DrinkWaterStreak.vue";
import YeetCodeStreak from "./components/streaks/yeet-code/YeetCodeStreak.vue";
</script>

<template>
  <div class="max-w-3xl mx-auto p-8 min-w-[320px] overflow-x-auto">
    <h1
      class="scroll-m-20 text-center text-4xl tracking-tighter font-light mb-8"
    >
      TheRobertLing's Streaks
    </h1>

    <Accordion class="w-full space-y-2" type="multiple" collapsible>
      <AccordionItem
        value="go-to-sleep"
        class="rounded-lg border bg-background last:border-b"
      >
        <AccordionTrigger class="px-4 cursor-pointer">
          <span class="line-clamp-1">go-to-sleep</span>
        </AccordionTrigger>
        <AccordionContent class="overflow-x-auto border-t p-4">
          <GoToSleepStreak />
        </AccordionContent>
      </AccordionItem>
      <AccordionItem
        value="drink-water"
        class="rounded-lg border bg-background last:border-b"
      >
        <AccordionTrigger class="px-4 cursor-pointer">
          <span class="line-clamp-1">drink-water</span>
        </AccordionTrigger>
        <AccordionContent class="overflow-x-auto border-t p-4">
          <DrinkWaterStreak />
        </AccordionContent>
      </AccordionItem>
      <AccordionItem
        value="yeet-code"
        class="rounded-lg border bg-background last:border-b"
      >
        <AccordionTrigger class="px-4 cursor-pointer">
          <span class="line-clamp-1">yeet-code</span>
        </AccordionTrigger>
        <AccordionContent class="overflow-x-auto border-t p-4">
          <YeetCodeStreak />
        </AccordionContent>
      </AccordionItem>
    </Accordion>
  </div>
</template>
