# 07_vuecli3_instant_prototyping

1. vuecli3 comes with instant prototyping, if we have thought of an idea for a component, that we want to make with vuejs, but we dont want to set up a full project to get started on this component, configure the project, etc
2. with instant prototyping, we can mock up a component, anywhere on our computer and preview it straight away, on a local development server
3. in order to do this, we have a one time installation of a seperate vue package called cli-service-global,.. so what that does is basically take that cli-service, and installs that globally on our computer
4. so the way we do this is by : 
npm install -g @vue/cli-service-global
then enter to install that
5. we can now prototype any component anywhere on our computer, and we can do this because now that package has added this serve command and build command to the vue cli and we can access that anywhere on the computer
6. before if we wanted to preview the vue projects in a local development server, in the browser then -- npm run serve
7. if we have a simple component outside of those projects, online.vue, if we wanted to preview this in the browser, .. previously we couldnt do that, but now what we can do is :
vue serve mycomponent.vue
8. now, we do have to be in the correct directory here - vuecli3, 
9. but before we couldnt have said npm run serve here, because there is no package.json file, and there is no project set up to do that, so now we have got that other cli service global package installed,
10. it has added this command to the vue cli and we can use this now anywhere on our computer just to serve up single components, so thats what instant prototyping is all about
11. vue serve mycomponent.vue
this will now serve this up on a local development server
.. there is nothing inside this component at the minute, so it is not going to show anything in the browser
12. we can now build a component and instantly prototype this component independently of whether it is in a project or not, we can just develop single components, and preview them in the browser
13. creating a component based on an idea.. idea for a component : display the online status on a website of a staff member, now this status should show a green light when they are online, and a red one when they are not online
14. we can create a component which will do that now

---
mycomponent.vue
---
<template>
  <div class="online-status">
    <div v-if="online" class="online">
      <span class="light"></span>
      <p>A staff member is online and available</p>
    </div>
    <div v-if="!online" class="offline">
      <span class="light"></span>
      <p>A staff member is not currently online</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      online: true,
    };
  },
};
</script>

<style>
.online-status {
  background: #eee;
  border: 1px dashed #ddd;
  display: inline-block;
  padding: 10px;
}
p {
  display: inline-block;
  font-family: arial;
  margin: 0;
  color: #555;
}
.light {
  display: inline-block;
  width: 10px;
  height: 10px;
  border-radius: 50%;
  margin-right: 10px;
}
.online .light {
  background: limegreen;
}
.offline .light {
  background: crimson;
}
</style>
---
15. so we have rapidly prototyped this component right here, which is not inside any kind of project, its just in an independent file, standalone vue component, and we have previewed that using instant prototyping
16. so if we just want to preview a single component, and work on a single component, without having to set up a whole project, then what we do is install that package first of all, which was the cli-service-global, we installed that globally, on our computer 
17. then we say vue serve filename