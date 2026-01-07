# nava-homework: Vue 3 + Vite

## Process

I began with a StackBlitz Vue template and implemented a rough version of the wireframe before breaking it into components that are easily digestible. Initially I worked in Firefox on desktop before switching to Chrome and running Lighthouse. I then tested in Safari on iPhone when finishing changes for mobile, and used Safari on my desktop during accessibility testing.

I chose VueJS for familiarity and single-file components that provide a scoped CSS approach without configuration. I opted for VueJS 3 to get access to `<script setup>` and reduced boilerplate. The design system I've been spending the most time with recently has been BootstrapVue, but without the styles. I chose to use native elements instead for improved accessibility out-of-the-box.

I deviated from the wireframe when adapting it for mobile, reducing the padding to conserve screen space and choosing to wrap the "tiles" of individual household members. I would have liked to discuss those decisions with the design team, and ask them about:

- the expected length of description text,
- plans to allow editing existing household members, and
- language support other than English
