# Git-Push-Deploy
Example of automated CI with git integration 

#### How to get private ssh key id (temporary workaround)

- Go to Dev Dashboard
- Add your **ptivate** key https://docs.jelastic.com/ssh-add-key
- Open Developer Tools -> Console 

<img src="https://raw.githubusercontent.com/siruslan/git-push-deploy/master/images/how-get-private-keyid.png" width="500">

- Execute the command below in the javascript console

```
JApp.Ajax.get("Management.Account.GetSSHKeys", {appid:GPlatform.APP_CLUSTER_APPID, isPrivate:true}, function(oResp) {console.log(Ext.each(oResp.keys, function(key) {console.log(key.title, key.id);} ))})
```

- Copy your keyId and past it in [manifest.jps](manifest.jps)


