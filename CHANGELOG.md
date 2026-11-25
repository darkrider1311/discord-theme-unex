# Patch Notes

## v0.4

- Reduced the readable CSS from 3,278 to 1,209 lines (63% fewer) and from 102,584 to 46,310 characters (55% smaller) compared with the full v0.3.1 stylesheet. Consolidated shared surface rules, removed redundant overrides and comments, and kept the rules focused on the Discord components they style.
- Unified the title bar, navigation, chat, and member list on a shared `r1` backdrop. Removed overlapping fills and gradients from the message composer and member list.
- Added separate blur controls for fixed interface surfaces, floating surfaces, and the wallpaper. Profile windows, activity cards, tooltips, and menus use the floating-surface setting.
- Restored targeted styling for event details, voice occupancy, Friends, Quests, Shop, and Nitro. Removed promotional hover fills from composer shortcuts.
- **Vesktop benchmark:** Median style recalculation was **95 ms** when opening Server Settings and **104 ms** when opening User Settings. The trace covers three openings per area and sums `UpdateLayoutTree` time in the first 500 ms after each click. The local test used 3 px static blur, 10 px hover blur, 0 px wallpaper blur, and 50% opacity for `r1`.

## v0.3.1

- Expanded the shared palette to eight RGB colors and linked more surfaces, frames, dividers, and interaction states to it.
- Matched channel icons to the corresponding read, unread, selected, and connected channel colors. Applied the shared hover fill to messages and posts in the active-posts popout.
- Standardized button fills and hover borders, including the active-posts action and server icon upload. Updated switch styling, event tabs, RSVP badges, and event icons.
- Updated the chat composer and mention styling, including hover borders and support for plugin-provided mention text colors.
- Reduced style recalculation during settings navigation by targeting profile activity cards directly and removing a global SVG override that matched icons by their inline color. Continued performance tuning is in progress.

## v0.3

- Reorganized the stylesheet into theme variables, shared components, and page layouts. Removed older selectors that had no matching classes in the local Discord cache.
- Consolidated the custom palette to seven red and pink base shades. Standardized CSS color declarations on RGB and replaced the old saturation-dependent colors with references to the current palette.
- Mapped Discord's semantic colors to the shared palette so pages and component variants can inherit a consistent look.
- Unified dropdown surfaces and item states. Extended the shared popup styling to dropdowns, context menus, submenus, and floating action bars using 12 px backdrop blur and 80% content opacity.
- Reduced the use of `!important` to two shared overrides for control backgrounds and the **Event Details** border. The button retains its background on hover and changes only its border color.

## v0.2.1

- Continued the theme as a standalone project under the filename `UNEX.theme.css`. Removed the previous project name from CSS variables, comments, metadata, and on-screen branding.
- Integrated the base stylesheet into the theme file and removed the old logo. Retained credit for the original authors and contributors.
- Renamed the local background image to `wallpaper.png` and reused it in profile popups. Replaced the close icon with a simple cross.
- Updated the local Vesktop configuration to use the renamed theme file.

## v0.2

- Styled unread-message banners and compact indicators in burgundy with brighter, bolder text and matching hover colors.
- Applied a shared palette to context menus, submenus, server menus, action bars, and tooltips, including their surfaces, dividers, and hover and focus states.
- Redesigned voice-channel occupancy badges with two equal-width, subtly contrasting segments and centered numbers. Removed the vertical and diagonal dividers.
- Themed Spotify hover cards, game activity cards, and other activity cards that share the same popup frame. These cards use 80% content opacity and a 12 px backdrop blur.
- Set the live stream preview background to dark burgundy (`#1d0d12`). Styled the **Request Stream** button with a muted red background, a slightly brighter label, and a more prominent hover border.
- Added a short project description to the README.

## v0.1

- Started with przemec's **Novum** stylesheet and adapted it to the Vesktop interface.
- Added a local wallpaper with a subtle blur. Styled the main window, direct messages, Friends list, chat, and member areas with translucent surfaces, coordinated text colors, and thin dividers.
- Extended the palette to user and server settings, including the role editor, member management, permissions, audit log, stickers, onboarding, Server Guide, access rules, safety features, AutoMod, and server tags.
- Styled the backgrounds of Quests, Shop, Nitro, and message embeds.
- Unified interaction colors for buttons, text fields, switches, radio options, and dropdowns. Gave destructive actions a distinct treatment within the red palette.
- Added initial styles for settings popups, server hover cards, new-message indicators, Rich Presence cards, and stream previews.
