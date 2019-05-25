# amigoal api documentation
## users
### register
#### /users/register
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
#### /users/login
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