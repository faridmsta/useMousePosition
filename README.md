# useMousePosition Custom Hook for TypeScript

Hello everyone 👋🏻
Today we will talk about **useMousePosition** Custom Hook.

## What does This code for.
  - Sometimes We need to get the mouse **X** , **Y** position of the window object even some Elements. Writeing Code For this small thing can Taketime enought time. Or you can just Use This hook.

## What does it returns
  - it retuns object with 3 element: X,Y,Visiable
'''
{
  x: 0,
  y: 0,
  visible: false
}
'''

*x - returns the x position of Referance 
*y - returns the y position of Referance 
*visiable - returns the boolean if the mouse is in inside of referance element

## How to use
  1. Fist import the Custom Hook
'''
import useMousePosition from '../../../../hooks/useMousePosition'
'''
  2. Create a Refecance by UseRef for the Element that you wabt to get positions of mouse inside it (If you want to get *Window* mouse position skip this part)
'''
import { useRef } from 'react'

function Projects() {
  const myref = useRef<HTMLDivElement | null>(null); // Thetype of Ref Should change based on element
  // rest of code...
'''

  3. Set The ref for element
'''
<div ref={myref} >
  // rest of code...
</div>
'''

  4. get the values by pasteing Ref inside the bracets (to get *Window* mouse position leave it blank)
'''
const { x, y, visible } = useMousePosition(myref);

// For geting Window mouse position
const { x, y, visible } = useMousePosition();  
'''


## That's all. I hope you enjoyed it. See you later


