<!-- <script>
  import Router from "svelte-spa-router";
  import Home from "./pages/home.svelte";
  import Login from "./pages/login.svelte";
  import TeamMember from "./pages/teamMember.svelte";
  import MyForm from "./pages/myForm.svelte";

  const routes = {
    "/": Home,
    "/login": Login,
    "/team-member": TeamMember,
    "/my-form": MyForm,
  };
</script>

<main>
  <Router {routes} />
</main> -->

<script>
  import { Router, Route } from "svelte-routing";
  import Home from "./pages/home.svelte";
  import Login from "./pages/login.svelte";
  import TeamMember from "./pages/teamMember.svelte";
  import MyForm from "./pages/myForm.svelte";
  import DesignSystem from "./pages/DesignSystem.svelte";
</script>

<Router>
  <Route path="/" component={Home} />
  <Route path="/login" component={Login} />
  <Route path="/teammember" component={TeamMember} />
  <Route path="/myform" component={MyForm} />
  <Route path="/designsystem" component={DesignSystem} />
</Router>
