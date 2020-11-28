<template>
  <section class="bg-purple-500">
    <form
      name="contact"
      method="post"
      data-netlify="true"
      data-netlify-honeypot="bot-field"
      class="text-center"
    >
      <input type="hidden" name="form-name" value="contact" />
      <p hidden>
        <label> Don’t fill this out: <input name="bot-field" /> </label>
      </p>
      <div class="sender-info">
        <div>
          <label for="name" class="label text-white">Your name</label>
          <input
            type="text"
            name="name"
            class="bg-purple-500 border-2 border-white border-solid"
            v-model="formData.name"
          />
        </div>
        <div>
          <label for="email" class="text-white">Your email</label>
          <input
            type="email"
            name="email"
            class="bg-purple-500 border-2 border-white border-solid"
            v-model="formData.email"
          />
        </div>
      </div>

      <div class="message-wrapper">
        <label for="message" class="text-white">Message</label>
        <textarea
          name="message"
          class="bg-purple-500 border-2 border-white border-solid"
          v-model="formData.message"
        ></textarea>
      </div>

      <button type="submit">Submit form</button>
    </form>
  </section>
</template>

<script>
export default {
  name: "Contact",
  data: function() {
    return {
      formData: {},
    };
  },
};
</script>

<style></style>
