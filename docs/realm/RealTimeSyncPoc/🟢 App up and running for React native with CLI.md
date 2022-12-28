Following this [tutorial](https://www.mongodb.com/docs/atlas/app-services/tutorial/react-native/) instead
```shell
# Generate from template the project
npx mongodb-realm-cli apps create \
--template react-native.todo.flex \
--name RealTimeSyncPoCRN

# change folders to the actual project
cd RealTimeSyncPoCRN/frontend/react-native.todo.flex

# Install RN dependencies
npm install

# Install iOS dependencies
npx pod-install

# Open Xcode project and run it
xed ios
```

Had to disable temporarily my Proxy from Proxyman

And then I was able to run the iOS application from Xcode
![](Pasted%20image%2020221228150527.png)
Created a sample user
![](Pasted%20image%2020221228150552.png)
And then some items
![](Pasted%20image%2020221228150618.png)