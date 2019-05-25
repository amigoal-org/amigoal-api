# amigoal api documentation
## user
### register
#### /user/register
##### post
body
```
{
    email: string,
    password: string,
    fname: string
}
```
### login
#### /user/login
##### post
body
```
{
    email: string,
    password: string
}
```
response
```
{
    token: string
}
```