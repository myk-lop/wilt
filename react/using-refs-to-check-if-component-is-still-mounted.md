# Using refs to check if a component is still mounted.

This is useful because if you try to update the state of a component that is already unmounted you will get the error.

```
//useMountedRef.js

import { useRef, useEffect } from 'react';

export default function useMountedRef() {
  const mounted = useRef(false);

  useEffect(() => {
    mounted.current = true;
    return () => (mounted.current = false);
  });

  return mounted;
}
```

### So why did we use a ref here instead of something like a state variable const [mounted, setMounted] = useState(false)?

The answer is pretty simple, updating a ref never causes a re-render, whereas updating the state(i.e. using setMounted()) obviously does which will cause the useEffect() to run again and again causing an infinite loop.

[Sourse](https://dev.to/tusharkashyap63/use-refs-to-check-if-a-component-is-still-mounted-2gk7)
