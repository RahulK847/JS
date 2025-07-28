# Tailwind CSS Complete Syntax Guide

## 1. Basic Syntax

Tailwind uses utility-first classes to apply styles directly in HTML.

```html
<div class="bg-blue-500 text-white p-4 rounded-lg shadow-lg">
  Hello, Tailwind!
</div>
```

### Breakdown:

- `bg-blue-500` → Background color (blue, shade 500)
- `text-white` → White text color
- `p-4` → Padding of `1rem` (16px)
- `rounded-lg` → Large border radius
- `shadow-lg` → Large box shadow

## 2. Responsive Design

Use responsive prefixes to apply styles at different breakpoints:

```html
<div class="text-sm sm:text-base md:text-lg lg:text-xl xl:text-2xl">
  Responsive Text
</div>
```

### Breakpoints:

- `sm:` → `640px`
- `md:` → `768px`
- `lg:` → `1024px`
- `xl:` → `1280px`
- `2xl:` → `1536px`

## 3. State Modifiers

Apply styles conditionally based on states:

```html
<button
  class="bg-blue-500 hover:bg-blue-700 active:bg-blue-900 focus:ring-2 focus:ring-blue-300 disabled:opacity-50"
>
  Click Me
</button>
```

### States:

- `hover:` → On hover
- `active:` → When active/clicked
- `focus:` → When focused
- `disabled:` → When disabled
- `group-hover:` → When parent has `hover`
- `peer-focus:` → When sibling has `focus`

## 4. Dark Mode

Enable dark mode using `dark:` modifier:

```html
<div class="bg-white dark:bg-gray-800 text-black dark:text-white">
  Dark Mode Enabled
</div>
```

## 5. Flexbox & Grid

### Flexbox Example:

```html
<div class="flex items-center justify-between p-4">
  <div>Left</div>
  <div>Right</div>
</div>
```

### Grid Example:

```html
<div class="grid grid-cols-3 gap-4">
  <div class="bg-gray-200 p-4">1</div>
  <div class="bg-gray-300 p-4">2</div>
  <div class="bg-gray-400 p-4">3</div>
</div>
```

## 6. Spacing & Sizing

### Margin & Padding

```html
<div class="m-4 p-6">Spacing</div>
```

- `m-4` → Margin `1rem`
- `p-6` → Padding `1.5rem`

### Width & Height

```html
<div class="w-1/2 h-32">Half Width</div>
```

- `w-1/2` → 50% width
- `h-32` → Height `8rem`

## 7. Typography

```html
<p class="text-lg font-bold italic underline uppercase tracking-wide">
  Tailwind Typography
</p>
```

- `text-lg` → Large text
- `font-bold` → Bold text
- `italic` → Italic text
- `underline` → Underlined text
- `uppercase` → Uppercase letters
- `tracking-wide` → Wider letter spacing

## 8. Borders & Shadows

```html
<div class="border-4 border-red-500 rounded-lg shadow-xl">Border & Shadow</div>
```

- `border-4` → 4px border
- `border-red-500` → Red border
- `rounded-lg` → Large border radius
- `shadow-xl` → Extra-large shadow

## 9. Customization

Modify Tailwind via `tailwind.config.js`:

```js
module.exports = {
  theme: {
    extend: {
      colors: {
        primary: "#1E40AF",
      },
    },
  },
  plugins: [],
};
```

Now you can use `bg-primary` in your HTML!

## 10. Applying Custom Styles

Use `@apply` to combine classes in CSS:

```css
.btn {
  @apply bg-blue-500 text-white font-bold py-2 px-4 rounded;
}
```

Then use it in HTML:

```html
<button class="btn">Click Me</button>
```

## 11. Animations & Transitions

### Transitions

```html
<button
  class="bg-green-500 transition duration-500 ease-in-out transform hover:scale-110"
>
  Hover Me
</button>
```

- `transition` → Enables animation
- `duration-500` → 500ms duration
- `ease-in-out` → Smooth start & end
- `transform hover:scale-110` → Scales on hover

### Keyframe Animations

```css
@keyframes bounce {
  0%,
  100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-10px);
  }
}

.bounce {
  animation: bounce 1s infinite;
}
```

```html
<div class="bounce bg-yellow-500 p-4">Bouncing Box</div>
```

## Conclusion

more:- [Advance but most usefull](https://umeshmk.github.io/Tailwindcss-cheatsheet/)
more simple one: - [Good for you](https://flowbite.com/tools/tailwind-cheat-sheet/)
Tailwind CSS simplifies styling with utility classes, making development faster and more consistent. Explore more at [tailwindcss.com](https://tailwindcss.com).
