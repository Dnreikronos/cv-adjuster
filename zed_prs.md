# Zed PRs — Author: Dnreikronos

Total: 56 PRs | 30 Merged | 12 Open | 14 Closed

---

## Merged (30)

| # | Title | Merged |
|---|-------|--------|
| [#52583](https://github.com/zed-industries/zed/pull/52583) | cli: Null stdio handles when spawning Zed on Windows | 2026-04-27 |
| [#52773](https://github.com/zed-industries/zed/pull/52773) | theme_selector: Revert theme when modal is dismissed by clicking outside | 2026-04-23 |
| [#50860](https://github.com/zed-industries/zed/pull/50860) | terminal_view: Show "Add to Agent Thread" on first right-click | 2026-04-23 |
| [#53571](https://github.com/zed-industries/zed/pull/53571) | Stop eagerly clearing available code actions on row change | 2026-04-22 |
| [#52948](https://github.com/zed-industries/zed/pull/52948) | vim: Preserve system clipboard when pasting over visual selection | 2026-04-21 |
| [#50403](https://github.com/zed-industries/zed/pull/50403) | editor: Fix edit predictions polluting completions menu | 2026-04-21 |
| [#53107](https://github.com/zed-industries/zed/pull/53107) | terminal: Send SIGTERM synchronously on terminal drop | 2026-04-21 |
| [#53713](https://github.com/zed-industries/zed/pull/53713) | terminal_view: Show hollow cursor when bar/underline is unfocused | 2026-04-21 |
| [#53195](https://github.com/zed-industries/zed/pull/53195) | editor: Hide run button in gutter for unsaved buffers | 2026-04-20 |
| [#52463](https://github.com/zed-industries/zed/pull/52463) | Add NewFile keybinding to Welcome context | 2026-04-20 |
| [#51308](https://github.com/zed-industries/zed/pull/51308) | Ensure language servers from extension properly start on workspace restoration | 2026-04-16 |
| [#53712](https://github.com/zed-industries/zed/pull/53712) | editor: Fix semantic tokens missing when opening buffer from multibuffer | 2026-04-12 |
| [#52461](https://github.com/zed-industries/zed/pull/52461) | theme_selector: Preserve selected theme after empty filter | 2026-04-07 |
| [#51623](https://github.com/zed-industries/zed/pull/51623) | gpui: Fix SVG renderer not rendering text when system fonts are unavailable | 2026-04-07 |
| [#53171](https://github.com/zed-industries/zed/pull/53171) | terminal_view: Reset cursor blink on `SendText` and `SendKeystroke` actions | 2026-04-07 |
| [#51766](https://github.com/zed-industries/zed/pull/51766) | markdown: Fix visible escape characters in LSP diagnostics | 2026-04-03 |
| [#52837](https://github.com/zed-industries/zed/pull/52837) | markdown: Show copy button on hover to prevent overlapping code block | 2026-04-01 |
| [#52545](https://github.com/zed-industries/zed/pull/52545) | agent_ui: Fix message editor not expanding after sending a message | 2026-03-27 |
| [#50090](https://github.com/zed-industries/zed/pull/50090) | editor: Include closing delimiter on same line when folding | 2026-03-24 |
| [#52217](https://github.com/zed-industries/zed/pull/52217) | Fix git panel context menu keybinding jitter | 2026-03-24 |
| [#52111](https://github.com/zed-industries/zed/pull/52111) | Fix terminal block missing first line via f32 tolerance | 2026-03-23 |
| [#50551](https://github.com/zed-industries/zed/pull/50551) | search: Fix deleted files persisting in project search results | 2026-03-19 |
| [#51890](https://github.com/zed-industries/zed/pull/51890) | rules_library: Register ActionSequence handler | 2026-03-19 |
| [#51035](https://github.com/zed-industries/zed/pull/51035) | gpui_macos: Fix deadlock during re-entrant key status changes | 2026-03-17 |
| [#50540](https://github.com/zed-industries/zed/pull/50540) | gpui: Hide XF86 keybindings from menus and keybinding hints | 2026-03-13 |
| [#51031](https://github.com/zed-industries/zed/pull/51031) | Truncate long diagnostic messages in the status bar | 2026-03-12 |
| [#50511](https://github.com/zed-industries/zed/pull/50511) | agent_ui: Fix agent panel focus stealing from modals | 2026-03-06 |
| [#50661](https://github.com/zed-industries/zed/pull/50661) | Fix `formatter: "auto"` to skip language servers that can't format | 2026-03-06 |
| [#50705](https://github.com/zed-industries/zed/pull/50705) | picker: Prevent clicking non-selectable entries from confirming selection | 2026-03-05 |
| [#49235](https://github.com/zed-industries/zed/pull/49235) | docs: Simplify Deno test task example | 2026-02-15 |

---

## Open (12)

| # | Title | Opened |
|---|-------|--------|
| [#55129](https://github.com/zed-industries/zed/pull/55129) | Fix JSDoc injection layers being duplicated | 2026-04-29 |
| [#54806](https://github.com/zed-industries/zed/pull/54806) | editor: Cache code actions per viewport instead of per selection | 2026-04-24 |
| [#52104](https://github.com/zed-industries/zed/pull/52104) | Focus buffer/multibuffer when clicking a file in the Git panel | 2026-03-21 |
| [#51626](https://github.com/zed-industries/zed/pull/51626) | gpui: Preserve font weight and style when falling back to alternate fonts | 2026-03-15 |
| [#51535](https://github.com/zed-industries/zed/pull/51535) | gpui: Suppress hover states and cursor changes during mouse drag | 2026-03-13 |
| [#51195](https://github.com/zed-industries/zed/pull/51195) | editor: Account for horizontal scrollbar height in `SizeByContent` layout | 2026-03-10 |
| [#51057](https://github.com/zed-industries/zed/pull/51057) | dap_adapters: Improve JavaScript debug adapter error on network failure | 2026-03-08 |
| [#50982](https://github.com/zed-industries/zed/pull/50982) | dap: Interpolate variables in DAP error response messages | 2026-03-07 |
| [#50769](https://github.com/zed-industries/zed/pull/50769) | Fix blame hover popover not showing on first trigger when inline blame is disabled | 2026-03-05 |
| [#50121](https://github.com/zed-industries/zed/pull/50121) | debugger: Fetch and display sources with sourceReference from DAP | 2026-02-25 |
| [#49843](https://github.com/zed-industries/zed/pull/49843) | editor: Add gutter checkboxes for split diff and restore hunk to context menu | 2026-02-22 |
| [#49393](https://github.com/zed-industries/zed/pull/49393) | html: Fix JavaScript completions in `<script>` tags | 2026-02-17 |

---

## Closed / Not Merged (14)

| # | Title | Opened |
|---|-------|--------|
| [#52666](https://github.com/zed-industries/zed/pull/52666) | Show failed servers in language server menu | 2026-03-29 |
| [#53314](https://github.com/zed-industries/zed/pull/53314) | Disable code actions button when buffer search bar is focused | 2026-04-07 |
| [#52377](https://github.com/zed-industries/zed/pull/52377) | editor: Fix inlay hints not showing on editor open | 2026-03-25 |
| [#52365](https://github.com/zed-industries/zed/pull/52365) | theme_selector: Fix theme preview not updating on filter changes | 2026-03-24 |
| [#52141](https://github.com/zed-industries/zed/pull/52141) | theme_selector: Fix theme preview not updating on filter changes | 2026-03-22 |
| [#52134](https://github.com/zed-industries/zed/pull/52134) | Normalize extension relative paths to use forward slashes for cross-platform remote compatibility | 2026-03-22 |
| [#51770](https://github.com/zed-industries/zed/pull/51770) | worktree: Canonicalize path in Worktree::local to ensure it is absolute | 2026-03-17 |
| [#51699](https://github.com/zed-industries/zed/pull/51699) | agent: Prevent fetch tool from overloading context window | 2026-03-16 |
| [#51558](https://github.com/zed-industries/zed/pull/51558) | acp_thread: Read current file content for write tool diffs | 2026-03-14 |
| [#51320](https://github.com/zed-industries/zed/pull/51320) | agent_ui: Fix context menu spawning at top of chat instead of cursor position | 2026-03-11 |
| [#50516](https://github.com/zed-industries/zed/pull/50516) | linux: Fix space key ignored on X11 due to update_key/update_mask conflict | 2026-03-02 |
| [#49857](https://github.com/zed-industries/zed/pull/49857) | editor: Add setting to hide edit predictions from completions menu | 2026-02-23 |
| [#49749](https://github.com/zed-industries/zed/pull/49749) | language: Fix JSDoc injection lost when editing deep inside block comment | 2026-02-20 |
| [#49630](https://github.com/zed-industries/zed/pull/49630) | agent_ui: Fix agent panel stealing focus from modals on workspace restore | 2026-02-19 |
