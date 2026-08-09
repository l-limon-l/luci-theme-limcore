# Design rules

Checkable rules for the theme. Every one of them can be verified by measurement
in a browser, so "looks fine" is never the answer — a rule is either satisfied
or it is not.

LuCI markup is not ours: views ship their own tables, inline widths and widgets.
The theme has to survive that markup rather than assume it. When a rule and a
LuCI view disagree, fix the theme so it degrades gracefully; do not fight the
view with `!important` chains.

## Layout

1. **No page-level horizontal scroll.** `documentElement.scrollWidth` must not
   exceed `clientWidth` at any viewport from 320px up. Content wider than the
   viewport scrolls inside its own container, never by moving the page.
2. **Content uses the width it is given.** No fixed `max-width` on the content
   column beyond the `#maincontent` bound. Any gutter that holds nothing —
   an empty table of contents, a collapsed sidebar — reserves no space.
3. **Nothing overflows its container silently.** An element whose `scrollWidth`
   exceeds its parent's `clientWidth` either scrolls visibly or is reflowed.

## Typography

4. **Words never break mid-character.** `word-break: break-all` is banned in
   prose. Use `overflow-wrap: anywhere`, which breaks only words that genuinely
   do not fit. Cyrillic, German and long identifiers all depend on this.
5. **No clipped text.** `overflow: hidden` on a text container requires
   `text-overflow: ellipsis` and a title attribute, or it must not clip.

## Tables

6. **Tall rows align to the top.** When any cell in a row wraps to more than one
   line, every cell in that row aligns to the top edge. Middle alignment leaves
   short cells floating against a block of text.
7. **No column starves.** A column carrying prose gets enough width that its
   text does not wrap more than the row's tallest natural cell.

## Overlays

8. **Overlays are never clipped.** Dropdowns, popovers and tooltips render in
   the top layer, positioned in viewport coordinates, and stay on screen — a
   panel wider than its trigger is clamped to the viewport, not cut off.
9. **Opening an overlay shifts nothing.** No scrollbar appearing, no container
   resizing, no reflow of the page behind it.

## Stability

10. **No post-load jumps.** Elements do not move between columns or containers
    after first paint. Anything the theme relocates is relocated before the
    frame is shown, and for content inside modals too — LuCI mounts
    `#modal_overlay` on `document.body`, outside `#maincontent`.
11. **Same thing, same look.** A button, badge or status pill looks identical on
    every page. Page-specific overrides live in the patch layer and carry a
    comment saying what upstream breakage they work around.

## Interaction

12. **Interactive targets are at least 32px tall** (24px for inline icon
    buttons inside dense tables), and keyboard focus is always visible.
