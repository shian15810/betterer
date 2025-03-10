---
id: filters-and-ignores
title: Filters & Ignores
sidebar_label: Filters & Ignores
slug: /filters-and-ignores
---

## Filters

If you want to be selective about which tests run, you can use the [`--filter`](./running-betterer#start-options) option, which can take mutliple values. Each filter should be a [regular expression](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions).

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

<!-- prettier-ignore -->
<Tabs
  groupId="package-manager"
  defaultValue="yarn"
  values={[
    { label: 'Yarn', value: 'yarn' },
    { label: 'npm', value: 'npm' },
  ]}>
  <TabItem
    value="yarn">

Run `yarn betterer --filter my-test` to run **Betterer** with a filter.

Run `yarn betterer --filter my-test --filter my-other-test` to run **Betterer** with multiple filters.

  </TabItem>
  <TabItem
    value="npm">

Run `npm run betterer --filter my-test` to run **Betterer** with a filter.

Run `npm run betterer --filter my-test --filter my-other-test` to run **Betterer** with multiple filters.

  </TabItem>
</Tabs>

When running in [Watch mode](./running-betterer#watch-mode-run-your-tests-when-files-change), filters can be updated on the fly by first pressing `f`, and then modifying the current filter.

## Ignores

If you want to be selective about which files are watched in [Watch mode](./running-betterer#watch-mode-run-your-tests-when-files-change), you can use the [`--ignore`](./running-betterer#watch-options) option, which can take mutliple values. Each ignore pattern should be a [glob](https://www.npmjs.com/package/glob#glob-primer).

<!-- prettier-ignore -->
<Tabs
  groupId="package-manager"
  defaultValue="yarn"
  values={[
    { label: 'Yarn', value: 'yarn' },
    { label: 'npm', value: 'npm' },
  ]}>
  <TabItem
    value="yarn">

Run `yarn betterer --ignore **/*.js` to run **Betterer** with an ignore.

Run `yarn betterer watch --ignore "**/*.js" --ignore "**/*.css"` to run **Betterer** with multiple ignores.

  </TabItem>
  <TabItem
    value="npm">

Run `npm run betterer --ignore **/*.js` to run **Betterer** with an ignore.

Run `npm run betterer watch --ignore "**/*.js" --ignore "**/*.css"` to run **Betterer** with multiple ignores.

  </TabItem>
</Tabs>

When running in [Watch mode](./running-betterer#watch-mode-run-your-tests-when-files-change), ignores can be updated on the fly by first pressing `i`, and then modifying the current ignore.
