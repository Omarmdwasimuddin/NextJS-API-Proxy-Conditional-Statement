## NextJS API---> Proxy Conditional Statement

### IF/ELSE condition
![](https://imgur.com/kLPz68a.png)

```bash
import { NextRequest, NextResponse } from "next/server";

export function proxy(request:NextRequest) {
    if (request.nextUrl.pathname.startsWith('/api')) {
        console.log('This is API route inside app dir')
        return NextResponse.next();
    } else if (request.nextUrl.pathname.startsWith('/about')) {
        console.log('This is page route inside app dir')
        return NextResponse.next();
    }

    return NextResponse.next();
}
```
---
