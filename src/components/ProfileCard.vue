<script>
export default {
   name: "ProfileCard",
};
</script>
<template>
   <!-- we display the user info here  -->
   <div class="flex items-center flex-1">
      <router-link to="/home"><slot name="userProfilePic"></slot></router-link>

      <div class="flex flex-col items-start ml-4 pt-2 text-ellipsis whitespace-nowrap overflow-hidden">
         <p class="xs:block hidden"><slot name="userFullName"></slot></p>
         <p class="xs:block hidden"><i class="far fa-building"></i><slot name="userWorkPlace"></slot></p>
         <router-link to="/Profile" class="text-xs pt-2 text-slate-600 xs:block hidden hover:underline">Modifier profil</router-link>
         <router-link to="/Profile" class="text-2xl pt-2 xs:hidden block active:text-slate-50"><i class="fas fa-cog"></i></router-link>
      </div>
   </div>
</template>
