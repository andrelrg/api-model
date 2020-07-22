# Requests examples

## Possible hosts
Here should be described the possible hosts that someone can hit, like:

### Running locally:
http://localhost:8000

### Testing ambient
http://mybeauty.test.env/

### Production
> :warning: ***You Should never create a fake user in production*** 
http://myproduction/


# Examples
> The `/user` prefix is not needed if you're running locally

## Heartbeat
<a name="heartbeat"></a>
```bash
curl {{HOST}}/user/heartbeat
```

## Create
<a name="craete"></a>
```bash
curl -X POST 
    -H "Authentication: Bearer {{TOKEN}}" 
    -H "Content-Type: application/json" 
    -d '{"username":"name", "password":"no"}' 
    {{HOST}}/user/create
```

## List
<a name="list"></a>
```bash
curl -X GET 
    -H "Authentication: Bearer {{TOKEN}}" 
    -H "Content-Type: application/json" 
    {{HOST}}/user/list
```

## Get user
<a name="getuser"></a>
```bash
curl -X GET 
    -H "Authentication: Bearer {{TOKEN}}" 
    -H "Content-Type: application/json" 
    {{HOST}}/user/get/{{userID}}
```
