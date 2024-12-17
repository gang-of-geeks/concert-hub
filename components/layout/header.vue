<template>
  <div class="header py-6">
    <div class="wrapper">
      <div class="align-items flex justify-between items-center">
        <div class="logo">
          <NuxtImg
            src="/logo.png"
            alt="logo"
            sizes="sm:192px md:192px lg:192px"
          />
        </div>
        <div class="menu">
          <ul class="flex justify-between items-center gap-6">
            <li class="contact-us">
              <NuxtImg src="/call.png" sizes="24px"/>
              <span class="text-base">Contact Us</span>
            </li>
            <li class="tikets">
              <NuxtImg src="/ticket.png" sizes="24px"/>
              <span class="text-base">Tickets</span>
            </li>
            <li class="blogs">
              <NuxtImg src="/document.png" sizes="24px"/>
              <span class="text-base">Blogs</span>
            </li>
            <li class="select-lan border border-gray-400 px-3 py-2.5 rounded-xl">
              <span class="text-sm">En</span>
              <NuxtImg src="/arrow-down.png" sizes="20px" />
            </li>
            <li class="login px-3 py-2 rounded-xl">
              <NuxtImg src="/user.png" sizes="18px" />
              <span class="text-base text-white ">Login</span>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
ul li {
  display: flex;
  align-items: center;
  gap: 8px;
}
.login {
  background:#4651C9;
}

</style>
