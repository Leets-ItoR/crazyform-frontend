<script>
  import Router from "svelte-spa-router";
  import Home from "./pages/Home.svelte";
  import Login from "./pages/Login.svelte";
  import TeamMember from "./pages/TeamMember.svelte";

  const routes = {
    "/": Home,
    "/login": Login,
    "/team-member": TeamMember,
  };
</script>

<main>
  <Router {routes} />
</main>
