I'm following this [tutorial](https://www.mongodb.com/docs/atlas/app-services/tutorial/swiftui/).

I will start configuring some things proper for my app for the AppID and API Key via this [page](https://realm.mongodb.com/groups/63ac7aee96b6c7351edcda0f/apps/63ac9c12a1f62d9f292956c0/deployment/export)
We will have to install a cli tool:

```shell
npm install -g mongodb-realm-cli
```

I will need to setup my public and private API keys in this command and run it
```shell
npx realm-cli login --api-key <API_KEY_HERE> --private-api-key <PRIVATE_KEY_HERE>
```

Then I'll create a new app wth the following information
```shell
npx realm-cli apps create -n RealTimeSyncPoCiOS --template swiftui.todo.flex \
   --deployment-model global --location us-va --environment development
```

After that I will get a new app generated with a [dashboard](https://realm.mongodb.com/groups/63ac7aee96b6c7351edcda0f/apps/63ac9c12a1f62d9f292956c0/dashboard)

And new code was added to my repo with the template generator
![](../../Pasted%20image%2020221228135350.png)
I'll end create a new file here Realm.plist.base and generate it with the example information and add the original Realm.plist to the project's root .gitignore

I would then open the project in Xcode that was generated located in the frontend folder:
```shell
xed ~/Developer/vivo/DemoAtlasDeviceSync/RealTimeSyncPoCiOS/frontend/swiftui.todo.flex
```

I can review new data in the [Data Services section](https://cloud.mongodb.com/v2/63ac7aee96b6c7351edcda0f#/metrics/replicaSet/63ac87f9da381b0beac7bf58/explorer/todo/Item/find)

And review new users [here](https://realm.mongodb.com/groups/63ac7aee96b6c7351edcda0f/apps/63ac9c12a1f62d9f292956c0/auth/users) in the authentication section within App Services.
