![Vue Skills banner](./.github/assets/banner.png)

# Vue Skills

Agent Skills for Vue.js development.

> [!IMPORTANT]
> (WIP) This project is under development. The skills provided here are experimental and may change in the future. Use them with caution and at your own risk, feedbacks are welcome!

> [!NOTE]
> I started vue-skills to offer reusable, community-friendly Vue.js agent skills that make AI-assisted development easier to adopt in Vue projects.
> 
> (Unofficial) This project is not a official Vue.js project, if it proves useful and fits the community’s needs, I’m happy to transferring it to the Vue organization for collaborative and long-term maintenance.

- 🛡️ High Reliability: Optimized prompts for consistent results on lower-tier models.
- 📚 Comprehensive Best Practices: Combines official guidance with real-world production experience.
- ⚡ Modern Vue.js Stack: Built for Vue 3 and Nuxt 3 with TypeScript.
- 🔌 Offline-First Design: Works fully offline without extra permissions.

## Installation

```bash
npx skills add serkodev/vue-skills
```

## Skills

#### [`vue-best-practices`](#-vue-best-practices)  
  This skill enforces best practices when developing Vue.js or Nuxt applications.

#### [`create-agnostic-composable`](#-create-agnostic-composable)  
  This skill help to create a reusable composable (VueUse-like) for controlling hidden for an element.

## Demos

### 🪄 `vue-best-practices`

#### Demo - Todo App

Prompt

```
create a todo app
```

🔎 See demo [full output](./demo/todo-app).

#### Changes after using skill

- More readable [code](demo/todo-app/with-skills/App.vue)
- [Components](demo/todo-app/with-skills/components) splited
- Moved states into composables ([useTodos.ts](demo/todo-app/with-skills/composables/useTodos.ts))
- Use `shallowRef` for primitive reactive data (see [Reactivity Guide](skills/vue-best-prastice/references/reactivity-guide.md))

---

### 🪄 `create-agnostic-composable`

#### Demo - useHidden

Prompt

```
create a reusable composable for controling hidden for a element
```

🔎 See demo [full output](./demo/hidden-composable).

#### Changes after using skill

- Used `MaybeRef` and `MaybeRefOrGetter` for input parameters for reactivity flexibility.

```ts
export interface UseHiddenOptions {
  hidden?: MaybeRef<boolean>
  initialHidden?: MaybeRefOrGetter<boolean>
  syncAria?: boolean
}

export function useHidden(
  target?: MaybeRefOrGetter<HTMLElement | null | undefined>,
  options: UseHiddenOptions = {},
)
```

## Related Projects

- [vueuse/skills](https://github.com/vueuse/skills) - Agent skills for VueUse development
- [onmax/nuxt-skills](https://github.com/onmax/nuxt-skills) - Agent skills for Nuxt development
- [hyf0/vue-skills](https://github.com/hyf0/vue-skills/tree/master) - Agent skills for Vue 3 development

## License

MIT
