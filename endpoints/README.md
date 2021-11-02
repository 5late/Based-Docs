# Endpoints

### ``/api/basedbot/v1/get/users/``

Returns all created users.
- JSON

```
{
	"number_of_users": **int**,
	"users": [**list of strings**]
}
```

### ``/api/basedbot/v1/basedleaderboard``

Returns leaderboard for all users with a based score over 5.
- JSON

```
{
	"data": [**list of leaderboard user objects**](../objects/leaderboard-user.md)
}
```
