<script setup lang="ts">
import {
  Tooltip,
  TooltipContent,
  TooltipProvider,
  TooltipTrigger,
} from "@/components/ui/tooltip";
import { logs } from "./drink-water";
</script>

<template>
  <TooltipProvider>
    <div class="flex flex-wrap gap-2">
      <Tooltip v-for="(day, index) in logs" :key="day.date">
        <TooltipTrigger
          :data-complete="day.completed ? '' : undefined"
          :data-incomplete="!day.completed ? '' : undefined"
          class="size-10 rounded-full inline-flex items-center justify-center text-sm font-medium cursor-default outline-none transition-all data-complete:bg-green-500/30 data-complete:text-green-400 data-complete:focus-visible:ring-[3px] data-complete:focus-visible:ring-green-500/40 data-incomplete:bg-red-500/30 data-incomplete:text-red-400 data-incomplete:focus-visible:ring-[3px] data-incomplete:focus-visible:ring-red-500/40"
        >
          {{ index + 1 }}
        </TooltipTrigger>
        <TooltipContent>
          <p class="font-semibold">{{ day.date }}</p>
        </TooltipContent>
      </Tooltip>
    </div>
  </TooltipProvider>
</template>
