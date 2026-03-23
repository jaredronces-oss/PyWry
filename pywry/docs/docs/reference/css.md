# CSS Reference

PyWry provides a comprehensive CSS system with theme support, CSS variables, and utility classes.

## Theme Classes

Apply to root element or widget container:

| Class | Description |
|-------|-------------|
| `.pywry-theme-dark` | Dark theme (default) |
| `.pywry-theme-light` | Light theme |
| `.pywry-theme-system` | Follow OS preference |

```html
<div class="pywry-widget pywry-theme-dark">
  <!-- Dark themed content -->
</div>
```

## CSS Variables

### Typography

```css
:root {
    --pywry-font-family: Inter, -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    --pywry-font-size: 14px;
    --pywry-font-weight-normal: 400;
    --pywry-font-weight-medium: 500;
}
```

### Spacing & Layout

```css
:root {
    --pywry-radius: 4px;
    --pywry-radius-lg: 6px;
    --pywry-spacing-xs: 2px;
    --pywry-spacing-sm: 4px;
    --pywry-spacing-md: 6px;
    --pywry-spacing-lg: 8px;
}
```

### Widget Sizing

```css
:root {
    --pywry-widget-width: 100%;
    --pywry-widget-min-height: 200px;
    --pywry-widget-height: 500px;
    --pywry-grid-min-height: 200px;
}
```

### Transitions

```css
:root {
    --pywry-transition-fast: 0.1s ease;
    --pywry-transition-normal: 0.2s ease;
}
```

### Accent Colors (Shared)

```css
:root {
    --pywry-accent: #0078d4;
    --pywry-accent-hover: #106ebe;
    --pywry-text-accent: rgb(51, 187, 255);
    --pywry-btn-neutral-bg: rgb(0, 136, 204);
    --pywry-btn-neutral-text: #ffffff;
    --pywry-btn-neutral-hover: rgb(0, 115, 173);
}
```

### Dark Theme Colors

```css
.pywry-theme-dark {
    --pywry-bg-primary: #212124;
    --pywry-bg-secondary: rgba(21, 21, 24, 1);
    --pywry-bg-tertiary: rgba(31, 30, 35, 1);
    --pywry-bg-quartary: rgba(36, 36, 42, 1);
    --pywry-bg-hover: rgba(255, 255, 255, 0.08);
    --pywry-bg-overlay: rgba(30, 30, 30, 0.8);
    --pywry-text-primary: #ebebed;
    --pywry-text-secondary: #a0a0a0;
    --pywry-text-muted: #707070;
    --pywry-border-color: #333;
    --pywry-border-focus: #555;
    
    /* Tab Group */
    --pywry-tab-bg: #2a2a2e;
    --pywry-tab-active-bg: #3d3d42;
    --pywry-tab-hover-bg: #353538;
    
    /* Buttons */
    --pywry-btn-primary-bg: #e2e2e2;
    --pywry-btn-primary-text: #151518;
    --pywry-btn-primary-hover: #cccccc;
    --pywry-btn-secondary-bg: #3d3d42;
    --pywry-btn-secondary-text: #ebebed;
    --pywry-btn-secondary-hover: #4a4a50;
    --pywry-btn-secondary-border: rgba(90, 90, 100, 0.5);
}
```

### Light Theme Colors

```css
.pywry-theme-light {
    --pywry-bg-primary: #f5f5f5;
    --pywry-bg-secondary: #ffffff;
    --pywry-bg-hover: rgba(0, 0, 0, 0.06);
    --pywry-bg-overlay: rgba(255, 255, 255, 0.8);
    --pywry-text-primary: #000000;
    --pywry-text-secondary: #666666;
    --pywry-text-muted: #999999;
    --pywry-border-color: #ccc;
    --pywry-border-focus: #999;
    
    /* Tab Group */
    --pywry-tab-bg: #e8e8ec;
    --pywry-tab-active-bg: #ffffff;
    --pywry-tab-hover-bg: #f0f0f4;
    
    /* Buttons */
    --pywry-btn-primary-bg: #2c2c32;
    --pywry-btn-primary-text: #ffffff;
    --pywry-btn-primary-hover: #1a1a1e;
    --pywry-btn-secondary-bg: #d0d0d8;
    --pywry-btn-secondary-text: #2c2c32;
    --pywry-btn-secondary-hover: #c0c0c8;
    --pywry-btn-secondary-border: rgba(180, 180, 190, 1);
}
```

## Layout Classes

### Container

```css
.pywry-widget {
    /* Main widget container */
    width: var(--pywry-widget-width);
    min-height: var(--pywry-widget-min-height);
    height: var(--pywry-widget-height);
    display: flex;
    flex-direction: column;
}

.pywry-container {
    /* Content container */
    flex: 1 1 0%;
    min-height: 0;
    display: flex;
    flex-direction: column;
}
```

### Toolbar Positions

```css
.pywry-toolbar { /* Base toolbar */ }
.pywry-toolbar-top { /* Top position */ }
.pywry-toolbar-bottom { /* Bottom position */ }
.pywry-toolbar-left { /* Left sidebar */ }
.pywry-toolbar-right { /* Right sidebar */ }
.pywry-toolbar-header { /* Header with bottom border */ }
.pywry-toolbar-footer { /* Footer with top border */ }
.pywry-toolbar-inside { /* Floating overlay */ }
```

### Toolbar Content

```css
.pywry-toolbar-content {
    /* Flex container for toolbar items */
    display: flex;
    flex-wrap: wrap;
    gap: var(--pywry-spacing-md);
    align-items: center;
}
```

## Component Classes

### Buttons

```css
.pywry-btn { /* Base button */ }
.pywry-btn-primary { /* Primary style */ }
.pywry-btn-secondary { /* Secondary style */ }
.pywry-btn-neutral { /* Blue neutral style */ }
.pywry-btn-danger { /* Red danger style */ }
.pywry-btn-success { /* Green success style */ }
.pywry-btn-warning { /* Warning style */ }
.pywry-btn-ghost { /* Ghost/transparent style */ }
.pywry-btn-outline { /* Outline style */ }
.pywry-btn-icon { /* Icon-only button */ }
.pywry-btn-xs { /* Extra small size */ }
.pywry-btn-sm { /* Small size */ }
.pywry-btn-md { /* Medium size (default) */ }
.pywry-btn-lg { /* Large size */ }
.pywry-btn-xl { /* Extra large size */ }
```

### Inputs

```css
.pywry-input { /* Base input */ }
.pywry-input-group { /* Label + input wrapper */ }
.pywry-input-inline { /* Inline variant */ }
.pywry-input-label { /* Input label */ }
.pywry-input-text { /* Text input */ }
.pywry-input-number { /* Number input */ }
.pywry-input-date { /* Date input */ }
.pywry-input-range { /* Range input */ }
.pywry-input-secret { /* Password/secret input */ }
.pywry-number-wrapper { /* Number input wrapper */ }
.pywry-number-spinner { /* Spinner buttons container */ }
.pywry-date-wrapper { /* Date input wrapper */ }
```

### Select & Dropdown

```css
.pywry-select { /* Select dropdown */ }
.pywry-dropdown { /* Custom dropdown */ }
.pywry-dropdown-selected { /* Selected value display */ }
.pywry-dropdown-menu { /* Dropdown menu */ }
.pywry-dropdown-option { /* Individual option */ }
.pywry-dropdown-arrow { /* Arrow indicator */ }
.pywry-dropdown-text { /* Text label */ }
.pywry-dropdown-up { /* Opens upward */ }
.pywry-searchable { /* Searchable variant */ }
.pywry-select-header { /* Select header */ }
.pywry-select-options { /* Select options container */ }
```

### Multi-Select

```css
.pywry-multiselect { /* Multi-select variant */ }
.pywry-multiselect-header { /* Multi-select header */ }
.pywry-multiselect-search { /* Multi-select search */ }
.pywry-multiselect-options { /* Options list */ }
.pywry-multiselect-option { /* Option item */ }
.pywry-multiselect-checkbox { /* Checkbox in multi-select */ }
.pywry-multiselect-label { /* Label in multi-select */ }
.pywry-multiselect-actions { /* Action buttons */ }
.pywry-multiselect-action { /* Individual action button */ }
```

### Search

```css
.pywry-search-wrapper { /* Search input wrapper */ }
.pywry-search-icon { /* Search icon */ }
.pywry-search-input { /* Search input field */ }
.pywry-search-inline { /* Inline search variant */ }
```

### Textarea & Secret

```css
.pywry-textarea { /* Textarea element */ }
.pywry-textarea-group { /* Textarea + label wrapper */ }
.pywry-secret-wrapper { /* Secret input wrapper */ }
.pywry-secret-actions { /* Action buttons */ }
.pywry-secret-btn { /* Secret action button */ }
.pywry-secret-copy { /* Copy button */ }
.pywry-secret-confirm { /* Confirm button (green) */ }
.pywry-secret-cancel { /* Cancel button (red) */ }
.pywry-secret-edit-actions { /* Edit mode actions */ }
.pywry-secret-textarea { /* Secret textarea */ }
```

### Toggle & Checkbox

```css
.pywry-toggle { /* Toggle switch */ }
.pywry-toggle-input { /* Hidden toggle input */ }
.pywry-toggle-slider { /* Toggle background */ }
.pywry-toggle-track { /* Toggle track */ }
.pywry-toggle-thumb { /* Toggle thumb */ }
.pywry-checkbox { /* Checkbox wrapper */ }
.pywry-checkbox-input { /* Checkbox input */ }
.pywry-checkbox-box { /* Checkbox visual box */ }
.pywry-checkbox-label { /* Checkbox label */ }
```

### Radio Group

```css
.pywry-radio-group { /* Radio group container */ }
.pywry-radio-horizontal { /* Horizontal layout */ }
.pywry-radio-vertical { /* Vertical layout */ }
.pywry-radio-option { /* Individual radio option */ }
.pywry-radio-button { /* Radio visual element */ }
.pywry-radio-label { /* Radio label */ }
```

### Tabs

```css
.pywry-tab-group { /* Tab container */ }
.pywry-tab { /* Individual tab */ }
.pywry-tab-active { /* Active tab state */ }
.pywry-tab-sm { /* Small tab size */ }
.pywry-tab-lg { /* Large tab size */ }
```

### Slider & Range

```css
.pywry-slider { /* Slider wrapper */ }
.pywry-slider-input { /* Range input */ }
.pywry-slider-value { /* Value display */ }
.pywry-range-group { /* Dual-range group */ }
.pywry-range-track { /* Range track */ }
.pywry-range-track-bg { /* Track background */ }
.pywry-range-track-fill { /* Track fill */ }
.pywry-range-separator { /* Range value separator */ }
```

### Marquee & Ticker

```css
.pywry-marquee { /* Scrolling container */ }
.pywry-marquee-track { /* Animated track */ }
.pywry-marquee-content { /* Content wrapper */ }
.pywry-marquee-left { /* Scroll left */ }
.pywry-marquee-right { /* Scroll right */ }
.pywry-marquee-up { /* Scroll up */ }
.pywry-marquee-down { /* Scroll down */ }
.pywry-marquee-static { /* No animation */ }
.pywry-marquee-pause { /* Pause on hover */ }
.pywry-marquee-vertical { /* Vertical layout */ }
.pywry-marquee-alternate { /* Bounce back-and-forth */ }
.pywry-marquee-slide { /* Play once and stop */ }
.pywry-marquee-clickable { /* Clickable variant */ }
.pywry-marquee-separator { /* Separator element */ }
.pywry-ticker-item { /* Ticker item */ }
.pywry-ticker-item.stock-up { /* Price up indicator */ }
.pywry-ticker-item.stock-down { /* Price down indicator */ }
.pywry-ticker-item.ticker-neutral { /* Neutral state */ }
```

### Grid & Data Table

```css
.pywry-grid { /* Grid/table container */ }
.pywry-grid-wrapper { /* Grid wrapper */ }
.pywry-plotly { /* Plotly chart container */ }
.pywry-plotly-container { /* Chart wrapper */ }
```

### Divs

```css
.pywry-div { /* Div component */ }
```

### Tooltips

```css
.pywry-tooltip { /* Tooltip element */ }
.pywry-tooltip.visible { /* Visible tooltip */ }
.pywry-tooltip.arrow-bottom { /* Arrow points down */ }
.pywry-tooltip.arrow-top { /* Arrow points up */ }
```

## State Classes

```css
.pywry-disabled { /* Disabled state */ }
.pywry-collapsed { /* Collapsed toolbar */ }
.pywry-loading { /* Loading state */ }
.pywry-selected { /* Selected state */ }
.pywry-open { /* Open state */ }
```

## Modal Classes

```css
.pywry-modal-overlay { /* Backdrop overlay */ }
.pywry-modal-overlay.pywry-modal-open { /* Overlay visible */ }
.pywry-modal-container { /* Modal box */ }
.pywry-modal-sm { /* Small modal (400px) */ }
.pywry-modal-md { /* Medium modal (560px) */ }
.pywry-modal-lg { /* Large modal (720px) */ }
.pywry-modal-xl { /* Extra large modal (960px) */ }
.pywry-modal-full { /* Full width modal */ }
.pywry-modal-header { /* Modal header */ }
.pywry-modal-title { /* Modal title */ }
.pywry-modal-body { /* Modal body/content */ }
.pywry-modal-footer { /* Modal footer */ }
.pywry-modal-close { /* Close button */ }
.pywry-modal-body-locked { /* Body scroll lock (applied to body) */ }
```

## Toast Notification Classes

```css
/* Container (positioned fixed, holds all toasts) */
.pywry-toast-container { /* Toast container */ }
.pywry-toast-container--top-right { /* Top right (default) */ }
.pywry-toast-container--top-left { /* Top left */ }
.pywry-toast-container--bottom-right { /* Bottom right */ }
.pywry-toast-container--bottom-left { /* Bottom left */ }
.pywry-toast-container--blocking { /* Blocking variant */ }

/* Individual toast */
.pywry-toast { /* Toast notification */ }
.pywry-toast--info { /* Info type (blue) */ }
.pywry-toast--success { /* Success type (green) */ }
.pywry-toast--warning { /* Warning type (yellow) */ }
.pywry-toast--error { /* Error type (red) */ }
.pywry-toast--confirm { /* Confirmation type */ }
.pywry-toast--light { /* Light theme variant */ }

/* Toast inner elements */
.pywry-toast__icon { /* Icon element */ }
.pywry-toast__content { /* Content wrapper */ }
.pywry-toast__title { /* Title text */ }
.pywry-toast__message { /* Message text */ }
.pywry-toast__close { /* Close button */ }
.pywry-toast__buttons { /* Button group (confirm type) */ }
.pywry-toast__btn { /* Button element */ }
.pywry-toast__btn--cancel { /* Cancel button */ }
.pywry-toast__btn--confirm { /* Confirm button */ }
.pywry-toast-overlay { /* Overlay background (confirm type) */ }
.pywry-toast-overlay--visible { /* Overlay visible */ }
```

## Chat Classes

Used by the `show_chat()` / `ChatManager` component.

### Layout

```css
.pywry-chat { /* Chat container */ }
.pywry-chat-header { /* Header bar */ }
.pywry-chat-header-left { /* Left header content */ }
.pywry-chat-header-actions { /* Right header actions */ }
.pywry-chat-header-btn { /* Header button */ }
.pywry-chat-messages { /* Messages scroll area */ }
.pywry-chat-input-bar { /* Input bar container */ }
.pywry-chat-input-row { /* Input row */ }
.pywry-chat-input { /* Textarea input */ }
.pywry-chat-send-btn { /* Send button */ }
.pywry-chat-send-btn.pywry-chat-stop { /* Stop button (red) */ }
.pywry-chat-fullscreen { /* Fullscreen state */ }
.pywry-chat-fullscreen-expand { /* Expand icon */ }
.pywry-chat-fullscreen-collapse { /* Collapse icon */ }
```

### Messages

```css
.pywry-chat-msg { /* Message container */ }
.pywry-chat-msg-user { /* User message */ }
.pywry-chat-msg-assistant { /* Assistant message */ }
.pywry-chat-msg-system { /* System message */ }
.pywry-chat-msg-role { /* Role label */ }
.pywry-chat-msg-role-icon { /* Role icon */ }
.pywry-chat-msg-content { /* Message content */ }
.pywry-chat-msg-content.streaming { /* Streaming animation */ }
.pywry-chat-stopped { /* Stopped indicator */ }
.pywry-chat-typing { /* Typing indicator */ }
.pywry-chat-expand { /* Expand button */ }
.pywry-chat-new-msg-badge { /* New messages badge */ }
```

### Threads & Conversation Picker

```css
.pywry-chat-conv-picker { /* Conversation picker dropdown */ }
.pywry-chat-conv-picker.open { /* Open state */ }
.pywry-chat-conv-btn { /* Picker button */ }
.pywry-chat-conv-title { /* Current conversation title */ }
.pywry-chat-conv-dropdown { /* Dropdown menu */ }
.pywry-chat-chevron { /* Dropdown arrow */ }
.pywry-chat-thread-list { /* Thread list */ }
.pywry-chat-thread-item { /* Thread item */ }
.pywry-chat-thread-item.active { /* Active thread */ }
.pywry-chat-thread-info { /* Thread info container */ }
.pywry-chat-thread-title { /* Thread title text */ }
.pywry-chat-thread-title-input { /* Title edit input */ }
.pywry-chat-thread-id { /* Thread ID (monospace) */ }
.pywry-chat-thread-actions { /* Action buttons */ }
.pywry-chat-thread-rename { /* Rename button */ }
.pywry-chat-thread-delete { /* Delete button */ }
```

### Thinking & Todo

```css
.pywry-chat-thinking { /* Thinking block (<details>) */ }
.pywry-chat-thinking[open] { /* Expanded thinking */ }
.pywry-chat-thinking-summary { /* Thinking summary toggle */ }
.pywry-chat-thinking-icon { /* Thinking icon */ }
.pywry-chat-thinking-count { /* Token count */ }
.pywry-chat-thinking-spinner { /* Thinking animation */ }
.pywry-chat-thinking-content { /* Thinking content */ }
.pywry-chat-todo { /* Todo list container */ }
.pywry-chat-todo-details { /* Todo details element */ }
.pywry-chat-todo-summary { /* Todo summary toggle */ }
.pywry-chat-todo-label { /* Todo label */ }
.pywry-chat-todo-progress { /* Progress bar */ }
.pywry-chat-todo-progress-fill { /* Progress fill */ }
.pywry-chat-todo-list { /* Todo items list */ }
.pywry-chat-todo-item { /* Todo item */ }
.pywry-chat-todo-item-done { /* Completed item */ }
.pywry-chat-todo-item-active { /* Active item */ }
.pywry-chat-todo-clear { /* Clear button */ }
```

### Tool Calls & Artifacts

```css
.pywry-chat-tool-call { /* Tool call block */ }
.pywry-chat-tool-call[open] { /* Expanded tool call */ }
.pywry-chat-tool-summary { /* Tool summary toggle */ }
.pywry-chat-tool-icon { /* Tool icon */ }
.pywry-chat-tool-label { /* Tool label */ }
.pywry-chat-tool-name { /* Tool name (monospace) */ }
.pywry-chat-tool-spinner { /* Tool execution spinner */ }
.pywry-chat-tool-args { /* Tool arguments */ }
.pywry-chat-tool-result { /* Tool result */ }
.pywry-chat-tool-error { /* Error state */ }
.pywry-chat-tool-error-text { /* Error text */ }
.pywry-chat-artifact { /* Artifact container */ }
.pywry-chat-artifact[open] { /* Expanded artifact */ }
.pywry-chat-artifact-header { /* Artifact header */ }
.pywry-chat-artifact-chevron { /* Toggle arrow */ }
.pywry-chat-artifact-icon { /* Artifact icon */ }
.pywry-chat-artifact-title { /* Artifact title */ }
.pywry-chat-artifact-collapsed { /* Collapsed state */ }
.pywry-chat-artifact-body { /* Artifact body */ }
.pywry-chat-artifact-content { /* Artifact content */ }
.pywry-chat-artifact-code { /* Code artifact */ }
.pywry-chat-artifact-md { /* Markdown artifact */ }
.pywry-chat-artifact-iframe { /* HTML/iframe artifact */ }
.pywry-chat-artifact-image { /* Image artifact */ }
.pywry-chat-artifact-json { /* JSON artifact */ }
.pywry-chat-artifact-table { /* Table artifact */ }
.pywry-chat-artifact-plotly { /* Plotly artifact */ }
```

### Citations

```css
.pywry-chat-citation { /* Citation block */ }
.pywry-chat-citation-icon { /* Citation icon */ }
.pywry-chat-citation-snippet { /* Citation snippet */ }
```

### Interactive Input

```css
.pywry-chat-input-prompt { /* Question prompt */ }
.pywry-chat-input-prompt-icon { /* Prompt icon */ }
.pywry-chat-input-required { /* Required input indicator */ }
.pywry-chat-ir-controls { /* Inline controls container */ }
.pywry-chat-ir-buttons { /* Button group */ }
.pywry-chat-ir-btn { /* Inline button */ }
.pywry-chat-ir-radio-group { /* Radio group */ }
.pywry-chat-ir-radio-item { /* Radio item */ }
.pywry-chat-ir-radio-input { /* Radio input */ }
.pywry-chat-ir-radio-label { /* Radio label */ }
.pywry-chat-ir-radio-submit { /* Submit button */ }
```

### Command Palette & Mentions

```css
.pywry-chat-cmd-palette { /* Command palette */ }
.pywry-chat-cmd-item { /* Command item */ }
.pywry-chat-cmd-item.active { /* Active command */ }
.pywry-chat-mention-popup { /* Mention autocomplete */ }
.pywry-chat-mention-item { /* Mention item */ }
.pywry-chat-mention-icon { /* Mention icon */ }
```

### Settings & Attachments

```css
.pywry-chat-settings-menu { /* Settings menu */ }
.pywry-chat-settings-menu.open { /* Open state */ }
.pywry-chat-settings-dropdown { /* Dropdown menu */ }
.pywry-chat-settings-item { /* Settings item */ }
.pywry-chat-settings-item-label { /* Item label */ }
.pywry-chat-settings-sep { /* Separator */ }
.pywry-chat-settings-range-val { /* Range value display */ }
.pywry-chat-attach-btn { /* Attach button */ }
.pywry-chat-attachments-bar { /* Attachments display */ }
.pywry-chat-attachment-pill { /* Attachment badge */ }
.pywry-chat-attachment-pill-icon { /* Attachment icon */ }
.pywry-chat-attachment-pill-name { /* Attachment name */ }
.pywry-chat-attachment-pill-remove { /* Remove button */ }
.pywry-chat-drop-overlay { /* Drop zone overlay */ }
.pywry-chat-msg-attachments { /* Message attachments */ }
.pywry-chat-msg-attach-badge { /* Attachment badge */ }
```

### Syntax Highlighting

```css
.pywry-hl-kw { /* Keyword */ }
.pywry-hl-str { /* String */ }
.pywry-hl-cmt { /* Comment (italic) */ }
.pywry-hl-num { /* Number */ }
.pywry-hl-fn { /* Function */ }
.pywry-hl-type { /* Type/builtin */ }
.pywry-hl-dec { /* Decorator/attribute */ }
.pywry-hl-op { /* Operator */ }
.pywry-hl-punc { /* Punctuation */ }
.pywry-hl-prop { /* Property/key */ }
```

### Markdown Rendering

```css
.pywry-chat-md-table { /* Markdown table */ }
.pywry-chat-fmt-warn { /* Format timeout warning */ }
.pywry-chat-code-hidden { /* Hidden code block */ }
```

## Scrollbar Classes

Custom scrollbars for native windows:

```css
.pywry-scroll-wrapper { /* Scroll container wrapper */ }
.pywry-scroll-wrapper.has-scrollbar-v { /* Has vertical scrollbar */ }
.pywry-scroll-wrapper.has-scrollbar-h { /* Has horizontal scrollbar */ }
.pywry-scroll-wrapper.has-both-scrollbars { /* Both scrollbars */ }
.pywry-scroll-wrapper.is-scrolling { /* Currently scrolling */ }
.pywry-scroll-container { /* Scrollable content */ }
.pywry-scrollbar-track-v { /* Vertical scrollbar track */ }
.pywry-scrollbar-track-h { /* Horizontal scrollbar track */ }
.pywry-scrollbar-thumb-v { /* Vertical scrollbar thumb */ }
.pywry-scrollbar-thumb-h { /* Horizontal scrollbar thumb */ }
```

## Native Window Classes

Applied to `<html>` element in Tauri windows:

```css
html.pywry-native { /* Native window context */ }
html.dark { /* Dark mode on html */ }
html.light { /* Light mode on html */ }
```

## Custom CSS Injection

Inject CSS at runtime via Python:

```python
# In a callback (using app.emit with label)
def on_apply_styles(data, event_type, label):
    app.emit("pywry:inject-css", {
        "id": "my-custom-styles",
        "css": """
            .my-class {
                color: var(--pywry-text-accent);
                background: var(--pywry-bg-secondary);
            }
        """
    }, label)

# Or with a widget handle
widget = app.show("<h1>Demo</h1>")
widget.emit("pywry:inject-css", {
    "id": "my-custom-styles",
    "css": ".highlight { background: yellow; }"
})
```

Remove injected CSS:

```python
app.emit("pywry:remove-css", {"id": "my-custom-styles"}, label)
```

## Inline Styles

Set inline styles via Python:

```python
# By element ID
app.emit("pywry:set-style", {
    "id": "my-element",
    "styles": {
        "fontSize": "24px",
        "fontWeight": "bold",
        "color": "red"
    }
}, label)

# By CSS selector
app.emit("pywry:set-style", {
    "selector": ".my-class",
    "styles": {"display": "none"}
}, label)
```

## Override Examples

### Custom Widget Height

```python
from pywry import PyWry

app = PyWry(
    html="<h1>Tall Widget</h1>",
    head="""
    <style>
        :root {
            --pywry-widget-height: 800px;
        }
    </style>
    """
)
```

### Custom Theme

```python
custom_css = """
<style>
    .pywry-theme-custom {
        --pywry-bg-primary: #1a1a2e;
        --pywry-bg-secondary: #16213e;
        --pywry-text-primary: #e94560;
        --pywry-accent: #0f3460;
    }
</style>
"""

app = PyWry(html=content, head=custom_css)
```

### Custom Button Styles

```python
from pywry import PyWry, Toolbar, Button

app = PyWry()

def on_customize(data, event_type, label):
    app.emit("pywry:inject-css", {
        "id": "custom-buttons",
        "css": """
            .pywry-btn-primary {
                background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
                border: none;
            }
            .pywry-btn-primary:hover {
                background: linear-gradient(135deg, #764ba2 0%, #667eea 100%);
            }
        """
    }, label)

app.show(
    "<h1>Styled Buttons</h1>",
    toolbars=[Toolbar(position="top", items=[Button(label="Customize", event="ui:customize", variant="primary")])],
    callbacks={"ui:customize": on_customize},
)
```

## AG Grid Theme Integration

PyWry automatically syncs AG Grid themes:

```css
/* Dark mode */
.ag-theme-quartz-dark { /* Applied automatically */ }

/* Light mode */
.ag-theme-quartz { /* Applied automatically */ }
```

Update theme via event:

```python
# In a callback
app.emit("pywry:update-theme", {"theme": "light"}, label)
```

## Additional CSS Variables

Variables not listed in the main theme sections above:

### Monospace Font

```css
:root {
    --pywry-font-mono: 'Cascadia Code', 'Fira Code', Consolas, monospace;
}
```

### Scrollbar

```css
:root {
    --pywry-scrollbar-size: 10px;
    --pywry-scrollbar-thumb: rgba(155, 155, 155, 0.5);
    --pywry-scrollbar-thumb-hover: rgba(175, 175, 175, 0.7);
}
```

### Toast Notifications

```css
:root {
    --pywry-toast-bg: rgba(30, 30, 30, 0.95);
    --pywry-toast-color: #ffffff;
    --pywry-toast-accent: #0ea5e9;
    --pywry-modal-overlay-opacity: 0.5;
}
```

### Marquee Speed

```css
:root {
    --pywry-marquee-speed: 15s;
}
```

### AG Grid Overrides

```css
.ag-theme-quartz-dark,
.ag-theme-quartz {
    --ag-browser-color-scheme: dark; /* or light */
    --ag-wrapper-border-radius: 0;
    --ag-scrollbar-size: 10px;
    --ag-scrollbar-color: var(--pywry-scrollbar-thumb);
    --ag-scrollbar-track-color: transparent;
    --ag-input-focus-border-color: var(--pywry-accent);
    --ag-range-selection-border-color: var(--pywry-accent);
}
```

## Utility Classes

### Background Colors

```css
.pywry-bg-primary { /* var(--pywry-bg-primary) */ }
.pywry-bg-secondary { /* var(--pywry-bg-secondary) */ }
.pywry-bg-tertiary { /* var(--pywry-bg-tertiary) */ }
.pywry-bg-quartary { /* var(--pywry-bg-quartary) */ }
.pywry-bg-accent { /* var(--pywry-accent) */ }
.pywry-bg-hover { /* var(--pywry-bg-hover) */ }
```

### Text Colors

```css
.pywry-text-primary { /* var(--pywry-text-primary) */ }
.pywry-text-secondary { /* var(--pywry-text-secondary) */ }
.pywry-text-muted { /* var(--pywry-text-muted) */ }
.pywry-text-accent { /* var(--pywry-text-accent) */ }
```

### Borders

```css
.pywry-border-theme { /* var(--pywry-border-color) */ }
.pywry-border-outline { /* Outline border */ }
.pywry-border-modal { /* Modal border */ }
```

### Icons

```css
.pywry-ghost-icon { /* Ghost icon color */ }
.pywry-info-icon { /* Info icon color */ }
```

## Data Attributes

PyWry uses HTML data attributes for event wiring and component configuration:

| Attribute | Used On | Description |
|-----------|---------|-------------|
| `data-event` | Buttons, inputs | Event name to emit (e.g., `"app:save"`) |
| `data-component-id` | All components, modals | Unique component identifier |
| `data-data` | Buttons | JSON payload passed with the event |
| `data-tooltip` | Toolbar items | Tooltip text shown on hover |
| `data-value` | Dropdown options | Option value |
| `data-selected` | Dropdown options | Marks the selected option |
| `data-pywry-chart` | Plotly containers | Chart/Plotly instance identifier |
| `data-close-escape` | Modals | `"true"` to close on Escape key |
| `data-close-overlay` | Modals | `"true"` to close on overlay click |
| `data-reset-on-close` | Modals | `"true"` to reset form fields on close |
| `data-on-close-event` | Modals | Event emitted when modal closes |
| `data-collapsible` | Toolbars | `"true"` for collapsible toolbar |
| `data-resizable` | Toolbars | `"true"` for resizable toolbar |
| `data-accept-types` | Chat input | Accepted file types for upload |
