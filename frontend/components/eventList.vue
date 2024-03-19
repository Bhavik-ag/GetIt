<template>
  <div
    class="w-96 bg-white shadow-md rounded-lg duration-500 hover:scale-[1.02] hover:shadow-xl"
  >
    <img class="w-96 h-60 object-cover rounded-t-lg" :src="img_url" />
    <div
      class="flex flex-col gap-3 px-4 py-3 w-96 border border-x-gray-500 border-b-gray-500 rounded-b-lg"
    >
      <h5 class="text-lg font-bold text-black truncate block capitalize">
        {{ title }}
      </h5>
      <p class="text-sm text-neutral-600">
        {{ description }}
      </p>
      <div class="flex flex-row justify-between">
        <div class="flex flex-col w-fit gap-5">
          <div class="flex gap-2 md:gap-3">
            <img src="../assets/calendar.svg" alt="calendar" class="w-6 h-6" />
            <div class="flex flex-wrap items-center">
              <p class="text-sm">{{ date }}</p>
            </div>
          </div>

          <div class="flex items-center gap-3">
            <img src="../assets/location.svg" alt="location" class="w-6 h-6" />
            <p class="text-sm">{{ location }}</p>
          </div>
        </div>
        <div class="flex items-center w-fit">
          <p
            class="text-lg bg-green-500/10 px-5 py-2 text-green-700 font-semibold cursor-auto my-3"
          >
            ₹{{ ticket_price }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    email: {
      type: String,
      required: true,
    },
    date: {
      type: String,
      required: true,
    },
    location: {
      type: String,
      required: true,
    },
    ticket_price: {
      type: String,
      required: true,
    },
    img_url: {
      type: String,
      required: true,
    },
  },
  name: "eventList",
};
</script>
