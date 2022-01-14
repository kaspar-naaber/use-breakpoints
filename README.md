# use-breakpoints
useMediaQuery based custom hook for spefic breakpoints

## Usage
Modify the breakpoint values:

```js
const gridBreakpoints = {
  xs: 0,
  sm: 576,
  md: 768,
  lg: 992,
  xl: 1200,
  xxl: 1400,
};
```

Use in a component
```tsx
export function MyComponent() {
  // Destructure only what you need in the current component
  const {
    // mediaBreakPointDownXs,
    // mediaBreakPointUpXs,
    // mediaBreakPointDownSm,
    // mediaBreakPointUpSm,
    mediaBreakPointDownMd,
    mediaBreakPointUpMd,
    // mediaBreakPointDownLg,
    // mediaBreakPointUpLg,
    // mediaBreakPointDownXl,
    // mediaBreakPointUpXl,
    // mediaBreakPointDownXxl,
    // mediaBreakPointUpXxl,
  } = useBreakpoints();
  
  return (
    <div>
     {mediaBreakPointDownMd && <div>Rendered only in less than 768px wide viewport</div>}
     {mediaBreakPointUpMd && <div>Rendered only in more than 768px wide viewport</div>}
    </div>
  )
}
```
