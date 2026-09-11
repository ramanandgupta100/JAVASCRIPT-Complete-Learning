---
description: >-
  The main use of cookies is to let a website remember information about a user
  between requests and visits.
icon: cookie
---

# Cookies

used for:

* login sessions
* authentication and authorization
* user tracking (remember a user across visits)



`cookies()` in nextjs is a server-side API and cannot be used on client components.



get

{% code overflow="wrap" %}
```javascript
import { cookies } from "next/headers";

export default async function Page(){

    const cookies = await cookies();
    
    const myname = cookies.get("name");

.....
}
```
{% endcode %}



delete

{% code overflow="wrap" %}
```javascript
import { cookies } from "next/headers";

export default async function Page(){

    const cookies = await cookies();
    
    cookies.delete("name");

.....
}
```
{% endcode %}



set

{% code overflow="wrap" %}
```javascript
import { cookies } from "next/headers";

export default async function Page(){

    const cookies = await cookies();
    
    cookies.set("name", "john", {
        maxAge: 60 * 60 * 24 * 7,
        httpOnly: true,
        secure: true,
        sameSite: "lax"
    })

.....
}
```
{% endcode %}

> maxAge: cookie lasts 7 days  (its value is in SECONDS)> \
> httpOnly: JavaScript in the browser cannot access it> \
> secure: only sent over HTTPS> \
> sameSite: helps protect against CSRF (allow normal use, but be cautious when another website is involved)





check if a cookie exists or not

{% code overflow="wrap" %}
```javascript
import { cookies } from "next/headers";

export default async function Page(){

    const cookies = await cookies();
    
    if (cookies.has("name")){
        console.log("Cookie has been found");
    }

.....
}
```
{% endcode %}





### Where to see the Cookies ?

<figure><img src=".gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

### SOURCES:

[https://nextjs.org/docs/app/api-reference/functions/cookies](https://nextjs.org/docs/app/api-reference/functions/cookies)

{% embed url="https://nextjs.org/docs/app/api-reference/functions/cookies" %}

[https://www.youtube.com/watch?v=qTI7U4CAlVQ](https://www.youtube.com/watch?v=qTI7U4CAlVQ)

{% embed url="https://www.youtube.com/watch?v=qTI7U4CAlVQ" %}
