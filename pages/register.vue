<template>
  <div>
    <TheHeader />

    <div class="flex">
      <div class="w-full justify-center flex items-center">
        <div class="max-w-[380px] flex flex-col">
          <p class="text-2xl font-extrabold mb-5">Join Alem community</p>
          <p class="text-base font-light mb-5">
            Get more features and priviliges by joining to the most helpful community
          </p>

          <form class="flex flex-col gap-4 w-full" novalidate @submit.prevent="onSubmit">
            <input
              v-model="username"
              type="text"
              placeholder="Username"
              class="input input-bordered h-[42px] text-sm rounded-md"
            />
            <span v-if="errors.username">{{ errors.username }}</span>
            <input
              v-model="email"
              type="email"
              placeholder="Email"
              class="input input-bordered h-[42px] text-sm rounded-md"
            />
            <span v-if="errors.email">{{ errors.email }}</span>
            <input
              v-model="password"
              type="password"
              placeholder="Password"
              class="input input-bordered h-[42px] text-sm rounded-md"
            />
            <span v-if="errors.password">{{ errors.password }}</span>
            <input
              v-model="passwordConfirm"
              type="password"
              placeholder="Repeat Password"
              class="input input-bordered h-[42px] text-sm rounded-md"
            />
            <span v-if="errors.passwordConfirm">{{ errors.passwordConfirm }}</span>

            <button class="btn bg-[#F48023] text-white rounded-md mt-3 py-3">REGISTER</button>
          </form>
        </div>
      </div>
      <img src="/images/banner.png" alt="banner register" class="min-h-screen" />
    </div>
  </div>
</template>

<script lang="ts" setup>
import { useField, useForm } from "vee-validate";
import { toTypedSchema } from "@vee-validate/zod";
import * as z from "zod";

const now = new Date();
const time = now.getTime();
const expireTime = time + 1000 * 36000;
now.setTime(expireTime);
const token = useCookie("token", { expires: now });

const { handleSubmit, errors } = useForm({
  validationSchema: toTypedSchema(
    z
      .object({
        username: z.string().optional().default(""),
        email: z
          .string({ required_error: "This is required" })
          .nonempty("This is required")
          .email({ message: "Must be a valid email" }),
        password: z.string({ required_error: "This is required" }).nonempty("This is required"),
        passwordConfirm: z
          .string({ required_error: "This is required" })
          .nonempty("This is required"),
      })
      .refine(data => data.password === data.passwordConfirm, {
        path: ["passwordConfirm"],
        message: "Password not match",
      })
  ),
});
const { value: username } = useField("username");
const { value: email } = useField("email");
const { value: password } = useField("password");
const { value: passwordConfirm } = useField("passwordConfirm");

const onSubmit = handleSubmit(() => {
  navigateTo("/questions");
  token.value = "erik";
});
</script>

<style></style>
