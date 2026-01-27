# vue-skills

Agent Skills for Vue.js development.

> [!IMPORTANT]
> (WIP) This project is under development. The skills provided here are experimental and may change in the future. Use them with caution and at your own risk, feedbacks are welcome!
>
> I started vue-skills to provide a reusable, community-friendly collection of Vue.js agent skills that lowers the barrier to adopting AI-assisted development in Vue projects.
> 
> (Unofficial) This project is not a official Vue.js project, if the project proves useful and aligns with the Vue community’s needs, I’m happy to transfer it to the Vue organization so it can be maintained collaboratively as a sustainable community asset.

## Installation

```bash
npx skills add serkodev/vue-skills
```

## Demo

### Todo App ([Source](./demo/todo-app))

Prompt

```
create a todo app
```

#### Changes after using skill
- [x] more readable [code](demo/todo-app/with-skills/App.vue)
- [x] [components](demo/todo-app/with-skills/components) splited
- [x] moved states into composables ([useTodos.ts](demo/todo-app/with-skills/composables/useTodos.ts))
- [x] use `shallowRef` for primitive reactive data (see [Reactivity Guide](skills/vue-best-prastice/references/reactivity-guide.md))

## Related Projects

- [vueuse/skills](https://github.com/vueuse/skills) - Agent skills for VueUse development
- [onmax/nuxt-skills](https://github.com/onmax/nuxt-skills) - Agent skills for Nuxt development
- [hyf0/vue-skills](https://github.com/hyf0/vue-skills/tree/master) - Agent skills for Vue 3 development

## License

MIT
