# Endpoints

## Users

### ``/api/basedbot/v1/get/users/``

Returns all created users.
- JSON

```
{
	"number_of_users": **int**,
	"users": [...]
}
```

- ``users`` will return a list of strings with discord id's

### ``/api/basedbot/v1/user/{USER-ID}``

Returns all data for specified user.
- JSON

```
{
	"discord_id": 00000000000000 //int
	"created_at": 000000000 //int
	"data": {
		"based": {...},
		"cringe": {...}
	},
	"settings": {
		"public_profile": false, //bool
		"show_badges": false //bool
	},
	"badges": {
		"alpha_tester": false, //bool
		"early_adopter:" false, //bool
		"developer": false, //bool
		"owner": false, //bool
		"donator": false, //bool
		"50_based_count": false,
    		"100_based_count": false,
    		"200_based_count": false,
    		"50_cringe_count": false,
    		"100_cringe_count": false,
    		"200_cringe_count": false
	},
	"server_id": 0000000000000 //int
	"discord_name": "Example" //string
	"avatar_url": "test123" //string
	"sapply": "https://sapplyvalues.github.io/results.html" //string
}
```
- ``based`` returns a [user based object](../objects/user-based.md)
- ``cringe`` returns a [user cringe object](../objects/user-cringe.md)

### ``/api/basedbot/v1/basedleaderboard``

Returns leaderboard for all users with a based score over 5.
- JSON

```
{
	"data": []
}
```

- ``data`` will return a list of [leaderboard user objects](../objects/leaderboard-user.md)
