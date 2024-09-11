<template>
  <div class="w-5/6 mx-auto pt-4">
    <p class="text-2xl font-bold text-gray-500 dark:text-gray-300">
      Terms And Conditions
    </p>
    <div class="flex flex-col gap-2.5 text-gray-500 dark:text-gray-400">
      <p class="text-lg py-3">
        Please read these terms and conditions carefully before enrolling in our
        English course.
      </p>
      <ul class="list-disc flex flex-col gap-3 ml-4">
        <li>
          <strong class="dark:text-gray-300">Enrollment:</strong> By enrolling
          in our English course, you agree to abide by these terms and
          conditions as outlined below.
        </li>
        <li>
          <strong class="dark:text-gray-300">Course Content:</strong> The course
          content, including materials, lessons, and assessments, is the
          intellectual property of our organization. You may not distribute,
          reproduce, or share course content that belongs to the
          <em>Premium Section</em> without explicit permission, the rest of the
          content is made available for the community totally for free.
        </li>
        <li>
          <strong class="dark:text-gray-300">Payment:</strong> Payment for the
          course must be made in full before gaining access to course materials.
          We accept payment through our designated payment gateway or as
          otherwise specified.
        </li>
        <li>
          <strong class="dark:text-gray-300">Refunds:</strong> Refunds are
          available within a specified period, typically within the first week
          of the course. Refund requests must be made in writing and will be
          subject to review and approval by our administration.
        </li>
        <li>
          <strong class="dark:text-gray-300">Course Duration:</strong> The
          course duration is as specified on our website or in communication
          with our representatives. Extensions may be granted under certain
          circumstances, subject to availability and approval.
        </li>
        <li>
          <strong class="dark:text-gray-300"
            >Attendance and Participation:</strong
          >
          Regular attendance and active participation in course activities,
          discussions, and assessments are expected from all enrolled students.
        </li>
        <li>
          <strong class="dark:text-gray-300">Code of Conduct:</strong> Students
          are expected to conduct themselves professionally and respectfully
          towards instructors and fellow students. Any form of harassment,
          discrimination, or disruptive behavior will not be tolerated and may
          result in immediate dismissal from the course without refund.
        </li>
        <li>
          <strong class="dark:text-gray-300">Technical Requirements:</strong>
          Students are responsible for ensuring they have access to the
          necessary technology, including a computer, internet connection, and
          any required software, to participate in the course.
        </li>
        <li>
          <strong class="dark:text-gray-300">Privacy</strong>: We are committed
          to protecting your privacy and will only use your personal information
          for course-related purposes. We do not sell or share your information
          with third parties without your consent.
        </li>
        <li>
          <strong class="dark:text-gray-300">Intellectual Property:</strong> Any
          work produced by students during the course remains their intellectual
          property. However, by enrolling in the course, students grant us the
          right to use their work for promotional or educational purposes with
          appropriate attribution.
        </li>
        <li>
          <strong class="dark:text-gray-300">Changes to Terms:</strong> We
          reserve the right to update or modify these terms and conditions at
          any time. Changes will be communicated to enrolled students via email
          or through our website.
        </li>
        <li>
          <strong class="dark:text-gray-300">Termination:</strong> We reserve
          the right to terminate a student's enrollment in the course due to
          non-compliance with these terms and conditions or for any other valid
          reason determined by our administration.
        </li>
      </ul>
      <p class="pt-3">
        By enrolling in our English course, you acknowledge that you have read,
        understood, and agree to these terms and conditions.
      </p>
      <p>
        If you have any questions or concerns, please contact us before
        proceeding with enrollment.
      </p>
    </div>
    <div class="flex justify-center mt-6">
      <TheLink
        to="/"
        class="w-fit flex items-center gap-2 justify-center border border-gray-300 rounded-md px-4 h-10 text-gray-400 hover:text-gray-500 hover:border-gray-400 hover:bg-gray-100/50 hover:trasnsition-colors hover:duration-200 dark:hover:bg-gray-900/50 dark:border-gray-500/50 dark:text-gray-500 focus-visible:outline-2 focus-visible:outline-violet-violetMain"
      >
        Back To Home
        <Home :size="18" :stroke-width="1.5" />
      </TheLink>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { Home } from "lucide-vue-next";

useHead({
  title: "Terms",
});
</script>
