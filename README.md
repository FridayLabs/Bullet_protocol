### Install
```
git submodule add --name protocol git@github.com:neronmoon/Bullet_protocol.git protocol
git submodule update --init
```

### For python
```
find protocol -type f -name "*.proto" -exec protoc --python_out=. {} \;
```

### Messages

```
###
> client->server
< server->client
###

> Hello <version>
< Hello <version>

> Goodbye

< Ping <time>
> Pong <time>

> Authenticate <user-id> <user-pass>
< Success <message>
< Failure <message>

> TransferPartyLeadership <user-id>
> InviteToParty <user-id>
> LeaveParty
< UserJoinsParty <user-id>
< UserLeavesParty <user-id>


> MakeMatch <party-id> <mode>
< AddedToQueue (to all party members)
< MatchFound <game-server-creds> (to all match members)
```
dkjahsdkjsdkjasdkjahsd





Parties:
id, users_list, party_leader


MatchmakingQueue

Mode, user-id, party-id=None
