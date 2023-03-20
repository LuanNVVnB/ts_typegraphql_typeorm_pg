# graphql-typeorm-pg-nodejs

## Add your files

-   [ ] [Create](https://docs.gitlab.com/ee/user/project/repository/web_editor.html#create-a-file) or [upload](https://docs.gitlab.com/ee/user/project/repository/web_editor.html#upload-a-file) files
-   [ ] [Add files using the command line](https://docs.gitlab.com/ee/gitlab-basics/add-file.html#add-a-file-using-the-command-line) or push an existing Git repository with the following command:

```
cd existing_repo
git remote add origin https://gitlab.com/luannvvIT/graphql-typeorm-pg-nodejs.git
git branch -M main
git push -uf origin main
```

## Integrate with your tools

-   [ ] [Set up project integrations](https://gitlab.com/luannvvIT/graphql-typeorm-pg-nodejs/-/settings/integrations)

## test graphql with registerUser muntation

```
mutation {
registerUser(
input:{
username: "nvvluands",
password:"123",
age: 23,
email:"uanlvvn@gmail.com"
}
){
status
message
user{
username
email
id
}
}
}
```

```
mutation {
refeshToken(input:"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjo2LCJ1c2VybmFtZSI6Im52dmx1YW5kIiwiZW1haWwiOiJ1YW5sdnZuQGdtYWlsLmNvbSJ9LCJpYXQiOjE2Nzc3NDEzNzAsImV4cCI6MTY3NzgyNzc3MH0.uuvYoDxn3V*I_MXt1D*-M9zsBmxTZe_MuGCJvuzzkaw"){
status
token{
accessToken
refeshToken
}
}
}
```

```
mutation{
createVoucher(
input:{
event:"dfb24c0a-99d2-46da-a29a-740843ebbc8e"
quantity:10
}
){
status
message

}
}
```

```
mutation {
createEvent(
input:{
name_event: "sale 60% macbook",
max_quantity:10
}
){
status
event{
id
vouchers{
id
}

    }

}
}
```

```
mutation{
loginUser(input:{
username: "nvvluands",
password: "123"})
{
status
message
token{
accessToken
}

}
}
```

```
mutation{
sendVoucher(input:"4e396e7c-1802-45f9-9d34-dbbc149742d4"){
status
message
}
}
```

```
{
"Authorization": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXlsb2FkIjp7ImlkIjoiMWUxYTYzYjctMDg0Ni00YzVkLWJhODUtOWMwNGNkOGE5NTVmIiwidXNlcm5hbWUiOiJudnZsdWFuZHMiLCJlbWFpbCI6InVhbmx2dm5AZ21haWwuY29tIn0sImlhdCI6MTY3ODI0MDM1NiwiZXhwIjoxNjc4MzI2NzU2fQ.V1SLf4fNELgYUi5OYe-l9oZTLkAQquNS9MyTv0FVY2Y"
}
```

## test graphql with query

```
{
getAllUser{
username
email
vouchers{
id
}
}
}
```
