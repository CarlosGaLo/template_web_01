<template>
  <div class="center">
    <section id="content">
      <!-- Aquí va el article Wiki -->
      <ArticleWiki></ArticleWiki>
    </section>
    <aside id="sidebar">
      <div id="nav-blog" class="sidebar-item">
        <h3>Artículos creados</h3>
        <a href="#" class="btn btn-success">Mirar catálogo</a>
      </div>

      <div id="search" class="sidebar-item">
        <h3>Buscador</h3>
        <p>¿Qué andas buscando?</p>
        <form action="">
          <input type="text" name="search" />
          <input type="submit" name="submit" value="Buscar" class="btn" />
        </form>
      </div>
    </aside>

    <div class="clearfix"></div>
  </div>
</template>

<script>
import ArticleWiki from "./ArticleWiki.vue";

export default {
  components: {
    ArticleWiki: ArticleWiki,
  },
};
</script>
