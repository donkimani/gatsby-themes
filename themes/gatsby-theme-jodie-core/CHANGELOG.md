# Change Log

## 2.0.0

### Major Changes

[#599](https://github.com/LekoArts/gatsby-themes/pull/599) [`1785dcf`](https://github.com/LekoArts/gatsby-themes/commit/1785dcfad131ab9270c401e6a3bb450f7cb01288) Thanks [@LekoArts](https://github.com/LekoArts)!

### Breaking Changes

1. Using `lessBabel` option for `gatsby-plugin-mdx`
1. Updating `theme-ui` from v0.3 to v0.9 and thus also `emotion` from v10 to v11
1. Updating all Gatsby related packages to latest
1. Migrated from `gatsby-image` to `gatsby-plugin-image`
1. Removed `fontsource-work-sans` npm package

#### Migrating

1. The `lessBabel` option might break your setup in some edge cases. If it doesn't work, turn on the `mdx` option and choose your own config for `gatsby-plugin-mdx`
1. The changelog/migration guide for `theme-ui` is here: https://theme-ui.com/migrating and for `emotion` here: https://emotion.sh/docs/emotion-11
1. Gatsby v3 migration guide: https://www.gatsbyjs.com/docs/reference/release-notes/migrating-from-v2-to-v3/
1. The theme itself is completely migrated to the new image plugin, but if you shadowed components and relied on the old structure, you'll need to migrate to `gatsby-plugin-image`: https://www.gatsbyjs.com/docs/reference/release-notes/image-migration-guide/
1. The starter now handles loading the font (via `gatsby-omni-font-loader`). This enables you to switch the primary font more easily (once you updated the Theme UI config). You can copy the configuration from there into your own `gatsby-config.js`

### Improvements

- You can use the `sharp` theme option to be able to configure `gatsby-plugin-sharp` on your own (helpful for defaults for `gatsby-plugin-image`)
- Performance improvements from `theme-ui` upgrade
- Eagerly load the first image in the grid (better lighthouse score)

### Updates to Starter

If you only cloned the starter (https://github.com/LekoArts/gatsby-starter-portfolio-jodie) and didn't change anything else this section will be more relevant to you.

- Conditionally add `gatsby-plugin-google-analytics`
- Conditionally add `gatsby-plugin-webpack-bundle-analyser-v2`
- Use `gatsby-omni-font-loader` to load the primary font ("Work Sans") instead of in the theme itself
- Add `FAST_DEV` flag
- Update to all latest Gatsby (+ plugins) versions
- Remove `gatsby-source-instagram` as Instagram locked down its API (and public scraping methods) even further. The page is now called `/art` and showcases the custom page in the same way

## 1.1.1

### Patch Changes

- [`47f747e`](https://github.com/LekoArts/gatsby-themes/commit/47f747e045962996503bf4043b0adc5a2527a855) [#559](https://github.com/LekoArts/gatsby-themes/pull/559) Thanks [@renovate](https://github.com/apps/renovate)! - Dependency updates for various packages, including theme-ui and gatsby related packages (includes improvements for `gatsby-plugin-image`)

## 1.1.0

### Minor Changes

- [`2e2b6de`](https://github.com/LekoArts/gatsby-themes/commit/2e2b6de1b4b35ca614143907a4366a91d1aa2b7e) [#557](https://github.com/LekoArts/gatsby-themes/pull/557) Thanks [@LekoArts](https://github.com/LekoArts)! - feat(gatsby-theme-jodie): Add customization options for homepage

  The PR https://github.com/LekoArts/gatsby-themes/pull/557 added some new possiblities to customize the homepage of `gatsby-theme-jodie`. This was requested in: https://github.com/LekoArts/gatsby-themes/issues/547

  More specifically, this adds two new theme options and one special file to shadow:

  1. `homepagePageLimit`
  2. `homepageProjectLimit`
  3. Shadowing [`modify-grid.ts`](https://github.com/LekoArts/gatsby-themes/blob/master/themes/gatsby-theme-jodie/src/utils/modify-grid.ts)

  The options 1) and 2) are explained in the theme options of the README -- they limit the number of projects and pages that will randomly be distributed on the page.

  Option 3) is a really powerful one! The `modifyGrid` function is wrapping the entire array of projects & pages before passing it to the `render` function of the React component. Or in other words: As the name suggests you can modify the items that are passed to the grid on the homepage.

  You don't need to update any code on your end, however, if you want to modify your homepage, see the instructions in the [README](https://github.com/LekoArts/gatsby-themes/blob/master/themes/gatsby-theme-jodie/README.md#customizing-the-homepage).

## 1.0.4

### Patch Changes

- [`9d25527`](https://github.com/LekoArts/gatsby-themes/commit/9d25527cf2372d24682d85c44ecca02675019774) [#551](https://github.com/LekoArts/gatsby-themes/pull/551) Thanks [@renovate](https://github.com/apps/renovate)! - chore(deps): update packages

  You can see the details of the update here: https://github.com/LekoArts/gatsby-themes/pull/551

All notable changes to this project will be documented in this file.
See [Conventional Commits](https://conventionalcommits.org) for commit guidelines.

## [1.0.3](https://github.com/LekoArts/gatsby-themes/compare/@lekoarts/gatsby-theme-jodie-core@1.0.2...@lekoarts/gatsby-theme-jodie-core@1.0.3) (2020-11-11)

**Note:** Version bump only for package @lekoarts/gatsby-theme-jodie-core

## [1.0.2](https://github.com/LekoArts/gatsby-themes/compare/@lekoarts/gatsby-theme-jodie-core@1.0.1...@lekoarts/gatsby-theme-jodie-core@1.0.2) (2020-11-02)

### Bug Fixes

- **deps:** update packages ([#530](https://github.com/LekoArts/gatsby-themes/issues/530)) ([2125d8e](https://github.com/LekoArts/gatsby-themes/commit/2125d8ec904388c66d821a7db7ebca6adc9ff73c))

## [1.0.1](https://github.com/LekoArts/gatsby-themes/compare/@lekoarts/gatsby-theme-jodie-core@1.0.0...@lekoarts/gatsby-theme-jodie-core@1.0.1) (2020-11-01)

### Bug Fixes

- **deps:** update packages ([#523](https://github.com/LekoArts/gatsby-themes/issues/523)) ([fb02217](https://github.com/LekoArts/gatsby-themes/commit/fb0221761af80e753990b5d2f2b410c98748ca02))
