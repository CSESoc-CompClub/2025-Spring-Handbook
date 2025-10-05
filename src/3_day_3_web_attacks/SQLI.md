# SQL Injection

> [!INFO] What is SQL Injection?
> [SQL Injection](https://portswigger.net/web-security/sql-injection) is another form of vulnerability that attacks the database.

## What is SQL?

SQL stands for Structured Query Language, and you can think it of as another programming language that allows us to get information out of a 'database'.

Think of a database like a giant dictionary. You can look things up, and pull information. Say you wanted to look up 'all the words that began with the letter K'. This is something that you could do with SQL.

The issue begins when we perform queries like 'Give me all the users that ...' and the user is able to inject their custom phrases into that sentence. For example, the attacker might say 'have a username of 'bob''. Then, without checking, the computer would execute the query 'Give me all the users that have a username of bob'.

> [!TIP] Common SQL Injection Patterns
> Here are 3 of the most common SQL injection attack patterns:
>
> ```sql
> ' OR '1'='1' --
> ' DROP Users;--
> ' AND 1=1 --
> ```

> [!SUCCESS] Tasks
>
> 1. On the website, you are to find where you could possibly use SQL Injection. What are some common places that these vulnerabilities are found?

> [!INFO] Helpful sites
>
> - [OWASP SQL Injection Prevention Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/SQL_Injection_Prevention_Cheat_Sheet.html)
> - [SQLMap - Automated SQL Injection Tool](https://sqlmap.org/)
> - [PortSwigger SQL Injection Labs](https://portswigger.net/web-security/sql-injection)
> - [PayloadsAllTheThings - SQL Injection](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/SQL%20Injection)
> - [HackerOne SQL Injection Reports](https://hackerone.com/hacktivity?filter=type%3Aall%20weakness%3Asql_injection)
