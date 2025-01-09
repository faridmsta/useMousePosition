# useMousePosition Custom Hook for TypeScript

Welcome! 👋🏻 Today, we'll explore the **useMousePosition** custom hook. This hook is designed to simplify the process of tracking mouse positions within a window or specific elements.

---

## 🚀 What Does This Hook Do?

Sometimes, you need to get the mouse's **X** and **Y** positions relative to the window or a specific element. Writing code for this can be time-consuming. Instead, you can use this hook to save time and effort!

---

## 🔍 What Does It Return?

The hook returns an object with the following properties:

```typescript
{
  x: 0,        // X position of the mouse
  y: 0,        // Y position of the mouse
  visible: false // Whether the mouse is inside the reference element
}
```

### Explanation:
- **x**: The X-coordinate relative to the reference element (or window if no reference is provided).
- **y**: The Y-coordinate relative to the reference element (or window if no reference is provided).
- **visible**: A boolean indicating whether the mouse is inside the reference element.

---

## 🛠 How to Use

Follow these steps to use the **useMousePosition** hook:

### 1. Import the Hook

```typescript
import useMousePosition from '../../../../hooks/useMousePosition';
```

### 2. Create a Reference for the Target Element (Optional)

Use `useRef` to create a reference for the element you want to track. If you want to track the mouse position relative to the **window**, skip this step.

```typescript
import { useRef } from 'react';

function Projects() {
  const myRef = useRef<HTMLDivElement | null>(null); // Adjust the type of ref based on your element
  // Rest of the code...

```

### 3. Attach the Reference to the Element

Assign the reference to the target element:

```typescript
<div ref={myRef}>
  {/* Rest of the code... */}
</div>
```

### 4. Retrieve the Values

Call the hook with the reference to get the mouse position and visibility status. To track the mouse relative to the **window**, leave the reference blank.

```typescript
// Get mouse position relative to a specific element
const { x, y, visible } = useMousePosition(myRef);

// Get mouse position relative to the window
const { x, y, visible } = useMousePosition();
```

---

## ✨ Example Output

Here’s an example of the returned object:

```typescript
{
  x: 120,       // Mouse X position
  y: 250,       // Mouse Y position
  visible: true // Mouse is inside the element
}
```

---

## 🎉 That's It!

Now you can easily track mouse positions and visibility with this custom hook. I hope this guide was helpful! Feel free to share your feedback or contributions.

See you later! 👋🏻

