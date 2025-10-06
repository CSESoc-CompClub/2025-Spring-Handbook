# IDOR

> [!INFO] What is IDOR?
> [IDOR](https://portswigger.net/web-security/access-control/idor) stands for _Insecure Direct Object Reference_ and it is a type of vulnerability that occurs when websites use user-provided input without first doing some checks.

## How IDOR Works

IDOR vulnerabilities typically occur when an application does not check the user has access to a certain thing before giving them access. This can be very dangerous.

> [!TIP] Examples
> For example, consider a url that you may have seen before in the past:
> `www.examplewebsite.com/orders/123`
>
> If the application doesn't verify that the current user is authorized to view order #123, an attacker could simply change the number to access other users' orders:
> Like this:
>
> - `www.examplewebsite.com/orders/124`
> - `www.examplewebsite.com/orders/125`
> - `www.examplewebsite.com/orders/1`
>
> ## IDOR vulnerabilities can be found in various contexts:
>
> - **User profiles**: `/user/profile?id=456`
> - **File downloads**: `/download?file=document123.pdf`
> - **API endpoints**: `/api/users/789/messages`
> - **Database records**: `/invoice?invoice_id=ABC123`
> - **Support tickets**: `/ticket/14`

> [!SUCCESS] Tasks
>
> 1. Find out what page could potentially lead to what we just mentioned.
> 2. After you discover the vulnerability, see what you can do with it. What additional information can you find out?

> [!INFO] Helpful links:
>
> - [IDOR](https://portswigger.net/web-security/access-control/lab-insecure-direct-object-references)
> - [More info](https://www.imperva.com/learn/application-security/insecure-direct-object-reference-idor/)
