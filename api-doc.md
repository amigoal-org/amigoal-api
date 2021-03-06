# amigoal api documentation
__Table of Contents__
## user
### register
#### /user/register
##### post
body
```
{
    email: string,
    password: string,
    displayName: string
}
```
### login
#### /user/login
##### post
body
```
{
    displayName: string,
    password: string
}
```
response
```
{
    token: string
}
```
## goal
headers
```
    auth: user's token
```
### /goal
#### get
response
```
[
    {
       id: int,
       title: string,
       body: string,
       followers: [
            displayName: string,
            ...
       ],
       comments: [
            {
                author: string,
                text: string
            },
       ],
       tags: [string, ...]
    },
    ...
]
```
#### post
body
```
{
    title: string,
    body: string,
    tags: [string, ...]
    targetDate: string (mm-dd-yyyy)
}
```
### goal/<goalId>
#### get
```
{
    id: int,
    title: string,
    body: string,
    followers: [
        displayName: string,
        ...
    ],
    comments: [
        {
            author: string,
            text: string
        },
    ]
}
```
## comment
### /comment/<goalId>
headers
```
    auth: user's token
```
#### post
body
```
    text: string
```
## follow
### /follow/<goalId>
headers
```
    auth: user's token
```
#### post
## tags
```
    auth: user's token
```
### /tags
#### get
body
```
[string, ...]
```