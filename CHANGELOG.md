# Changelog

These entries describe fixes recorded in the repository’s [deployment patches](deployment-fixes/).

## 2026-11-22

### Fixed

- Long strings without spaces now wrap inside chat bubbles, so messages stay readable on small screens. [PR #5](https://github.com/rodneyg/AI-Safety-2/pull/5)

## 2026-11-21

### Fixed

- The browser tab now reads “Boundary Erosion | SafeLab,” and the page description explains how the simulator works.
- Reset Context now clears the boundary alert and prevents delayed replies and alert timers from the previous conversation from affecting the new one.
- The accessibility patch adds screen reader labels for Scenario Selection and Send message, and improves contrast for the empty chat prompt, sent messages, and context metrics. [PR #3](https://github.com/rodneyg/AI-Safety-2/pull/3)

The metadata and reset fixes are recorded in the deployment patch from [PR #1](https://github.com/rodneyg/AI-Safety-2/pull/1).
