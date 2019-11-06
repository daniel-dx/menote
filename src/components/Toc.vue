<template>
  <ul class="toc">
    <!-- level 1-->
    <li v-for="(a, idx) in list" :key="idx">
      <a :href="'#' + a.id" v-text="a.title"></a>
      <!-- level 2-->
      <ul v-if="a.children.length > 0">
        <li v-for="(b, idx) in a.children" :key="idx">
          <a :href="'#' + b.id" v-text="b.title"></a>
          <!-- level 3-->
          <ul v-if="b.children.length > 0">
            <li v-for="(c, idx) in b.children" :key="idx">
              <a :href="'#' + c.id" v-text="c.title"></a>
              <!-- level 4 -->
              <ul v-if="c.children.length > 0">
                <li v-for="(d, idx) in c.children" :key="idx">
                  <a :href="'#' + d.id" v-text="d.title"></a>
                  <!-- level 5 -->
                  <ul v-if="d.children.length > 0">
                    <li v-for="(e, idx) in d.children" :key="idx">
                      <a :href="'#' + e.id" v-text="e.title"></a>
                      <!-- level 6 -->
                      <ul v-if="e.children.length > 0">
                        <li v-for="(f, idx) in e.children" :key="idx">
                          <a :href="'#' + f.id" v-text="f.title"></a>
                        </li>
                      </ul>
                    </li>
                  </ul>
                </li>
              </ul>
            </li>
          </ul>
        </li>
      </ul>
    </li>
  </ul>
</template>


<script>
export default {
  props: {
    list: {
      type: Array
    }
  }
}
</script>

<style>
.toc li {
  text-decoration: none;
  list-style: none;
}

.toc a {
  text-decoration: none;
}

.toc {
  padding-left: 0;
}

.toc ul {
  padding-left: 25px;
}
</style>

