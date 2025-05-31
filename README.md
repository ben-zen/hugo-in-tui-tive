# InTUItive (in-tui-tive)

**InTUItive** is the theme I assembled for my blog, starting from the already text-forward theme flat[^hugo-theme-flat]; in its first iterations here I'm spilling the innards of my personal blog's structure out, because I legitimately just copied the sources to flat into my repo and then just started paring down the structure to my preferred form.

## Minimalist site structure

I prefer legibility of sources above almost all else. Nested `<div>` elements often frustrate me, as they're opaque as to their meaning. I aspired with this theme―at this point it's truly its own theme―to produce HTML so clean it looked hand-written. I feel like I got there: at any point, it's relatively easy to orient yourself in the page layout from current tag or parent tags alone; the rare occasions where you _do_ encounter a `<div>` are almost uniquely there to structure elements that couldn't really be handled any other way.

## Accessibility-first design goals

I set out to ensure that the site was navigable and comprehensible with accessibility tools enabled; I've got Windows Narrator available to me right now, so that's my test-bench, and I aim for full keyboard accessibility of every element.

## Multi Section Supports (from flat)

> [!NOTE]
> This is from the previous repo and isn't exactly up to date, but it's mostly correct. I have not
> yet edited this to match current behavior.

If you use multi sections (with the concept from hugo), the RSS at bottom and *Recent* at side are ready for displaying those content. However, you will need to set up your menu at `config.toml` to point the hyperlink to proper destination.

If you want to re-order those sections, you need a `_index.md` at the directory of the section to set proper weight at front matter, just alike what was done at the exampleSite, see `/exampleSite/content/essays/_index.md`. See the predefined variable `weight` at [docs](https://gohugo.io/content-management/front-matter/#front-matter-variables).

**Note** that separating taxonomies according to different sections is not implemented yet. So better to only use taxonomies inside a specific section.

For a better understand, if you have to posts *A* and *B* in section *S1* and *S2*, both of the posts has the same tag *T1*, like the follow.

```
post A: section S1, tag T1, tag T2
post B: section S2, tag T2
```

When you open the index page of *T1*, there will be two posts, rathor than post *A* when you are in section *S1* and post *B* when you are in section *S2*.

```
tag T1: post A, post B
tag T2: post A
```

## Special Thanks

[leafee98](https://leafee98.com/) for the original inspiration with flat[^hugo-theme-flat]―I was looking for a very text-oriented theme to originally work from, but ideally would already be able to crib off someone's notes for the mode-shifting (light/dark). That theme fit the bill, and provided all the seed concepts I needed.

[^hugo-theme-flat]: leafee98's [flat theme on github](https://github.com/leafee98/hugo-theme-flat)