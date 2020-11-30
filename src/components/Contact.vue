<template>
  <section class="bg-purple-500 break-container p-8">
    <h2 class="text-center text-5xl font-bold text-white">Contact Me</h2>
    <form
      name="contact"
      method="POST"
      action="/success/"
      data-netlify="true"
      data-netlify-honeypot="bot-field"
      class="text-center"
    >
      <input type="hidden" name="form-name" value="contact" />
      <p hidden>
        <label> Don’t fill this out: <input name="bot-field" /> </label>
      </p>
      <div class="sender-info">
        <div class="m-4">
          <label for="name" class="label text-white mr-2">Your name</label>
          <input
            type="text"
            name="name"
            class="border-2 border-white border-solid"
            v-model="formData.name"
          />
        </div>
        <div class="m-4">
          <label for="email" class="text-white mr-2">Your email</label>
          <input
            type="email"
            name="email"
            class="border-2 border-white border-solid"
            v-model="formData.email"
          />
        </div>
      </div>

      <div class="message-wrapper m-4">
        <label for="message" class="text-white mr-2">Message</label>
        <textarea
          name="message"
          class=" border-2 border-white border-solid"
          v-model="formData.message"
        ></textarea>
      </div>

      <button
        type="submit"
        class="text-white border border-white py-3 px-6 rounded-full hover:text-purple-500 hover:border-purple-500 hover:bg-white"
      >
        Submit
      </button>
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
  methods: {
    encode(data) {
      return Object.keys(data)
        .map(
          (key) => encodeURIComponent(key) + "=" + encodeURIComponent(data[key])
        )
        .join("&");
    },
    handleSubmit(e) {
      if (
        this.formData.name.length > 0 &&
        this.formData.email.length > 0 &&
        this.formData.message.length > 0
      ) {
        fetch("/", {
          method: "POST",
          headers: { "Content-Type": "application/x-www-form-urlencoded" },
          body: this.encode({
            "form-name": e.target.getAttribute("name"),
            ...this.formData,
          }),
        })
          .then(() => this.$router.push("/success"))
          .catch((error) => alert(error));
      }
    },
  },
};
</script>

<style></style>
