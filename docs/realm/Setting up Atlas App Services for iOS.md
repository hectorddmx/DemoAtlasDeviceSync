The initial link for a newly created app would be something like this:
https://realm.mongodb.com/groups/63ac7aee96b6c7351edcda0f/apps

![](Pasted%20image%2020221228115127.png)
I chose the Realm-time Sync option and pressed Next.
![](../Pasted%20image%2020221228121512.png)
Then in the following screens I configured the four steps.
![](../Pasted%20image%2020221228121523.png)![](../Pasted%20image%2020221228121610.png)
Now we'll get redirected to another page to create the frontend code via templates.
We can chose multiple platforms which is nice.
![](../Pasted%20image%2020221228121657.png)I chose Swift, Flutter and React native, and downloaded the frontend code for each one them. Each links to a different tutorial, one per platform:
* https://www.mongodb.com/docs/atlas/app-services/tutorial/swiftui/
* https://www.mongodb.com/docs/atlas/app-services/tutorial/flutter/
* https://www.mongodb.com/docs/atlas/app-services/tutorial/react-native/

Note that there is an alternate way to setup the frontend code template, instead of downloading the zip's, there is a way to generated them with CLI commands:
![](../Pasted%20image%2020221228121918.png)
This one links to this articles:
- https://www.mongodb.com/docs/atlas/app-services/manage-apps/configure/export/export-with-cli/
- https://www.mongodb.com/docs/atlas/app-services/cli/
- https://cloud.mongodb.com/v2/63ac7aee96b6c7351edcda0f#access/apiKeys
- https://www.mongodb.com/docs/atlas/app-services/cli/
And gives these sample commands
```shell
npm install -g mongodb-realm-cli
realm-cli login --api-key <my-api-key> --private-api-key <my-private-api-key>
realm-cli pull --remote realtimesyncpoc-zbdkc --template swiftui.todo.flex
```

After we close that modal and have either downloaded ZIPs files or generated code via CLI, we'll see the following [dashboard screen](https://realm.mongodb.com/groups/63ac7aee96b6c7351edcda0f/apps/63ac87f01d1e91ce58733ac2/dashboard)
![](../Pasted%20image%2020221228122140.png)
We can still show that modal again with the Pull front-end code green button here.
It's nice that we already have some services created
![](../Pasted%20image%2020221228122451.png)
Before jumping to the code, explored a bit and went to setup the [environment](https://realm.mongodb.com/groups/63ac7aee96b6c7351edcda0f/apps/63ac87f01d1e91ce58733ac2/deployment/environment), changed it to Development in the drop down.
![](../Pasted%20image%2020221228122605.png)
When returning to the main screen we'll see that Development Mode is ON
![](../Pasted%20image%2020221228130018.png)
And this will enable Anonymous Authentication by default in this [screen](https://realm.mongodb.com/groups/63ac7aee96b6c7351edcda0f/apps/63ac87f01d1e91ce58733ac2/sync/config)
![](../Pasted%20image%2020221228130117.png)
Here I moved to 