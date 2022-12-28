https://realm.mongodb.com/groups/63ac7aee96b6c7351edcda0f/apps/63ac87f01d1e91ce58733ac2/deployment/export

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

After that I will get a new app generated with a dashboard:
https://realm.mongodb.com/groups/63ac7aee96b6c7351edcda0f/apps/63ac9c12a1f62d9f292956c0/dashboard

And new code added to my repo
![](../../Pasted%20image%2020221228135350.png)
I'll end create a new file here Realm.plist.base and generate it with the example information and add the original Realm.plist to the project's root .gitignore