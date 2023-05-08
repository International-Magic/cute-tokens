# Design Tokens

> An opinionated design token structure, powering Magic as a Service’s [Design System](https://github.com/magicasaservice/design-system)

## Intention

This repository is intended to power our own design system as well as serving as a blueprint for all future design system project.

## Construction

Our design tokens are structured in three hierachical layers: `1. config`, `2. application`, `3. components`. The specificity of each layer topples the one prior. Tokens from each layer can either reference the layer below or include a finite value.

```
         __________
        /          \
       / Components \
      /______________\
     /                \
    /    Application   \
   /____________________\
  /                      \
 /         Config         \
/__________________________\
```

## Customization

To customize the design tokens, each of the layers’ tokens can be overwritten within a layer injected directly above it into the hierachical structure. This is intended for features such as adusted mobile styles or dark mode.

```
            __________
           /          \
          / Components \
         /______________\
        /                \
       /     Dark Mode    \
      /____________________\
     /                      \
    /       Application      \
   /__________________________\
  /                            \
 /            Config            \
/________________________________\
```

## Tooling

The design token structure is currently built with [Tokens Studio](https://tokens.studio/) in Figma. The tokens than act as a source for a custom compiler within our [Design System](https://github.com/magicasaservice/design-system), built with [Style Dictionary](https://github.com/amzn/style-dictionary).
