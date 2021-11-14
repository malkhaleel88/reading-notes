# **S3**

![S3](https://miro.medium.com/max/1160/1*DHe24MbDHtbkOeIJzxrfdA.png)

## **What is Amazon S3?**

- storage for the Internet.
- designed to make web-scale computing easier.

### **Why need Amazon S3?**

- it have a simple web services interface that you can use to store and retrieve data.
- It gives any developer access to the same highly scalable, reliable, fast, inexpensive data storage infrastructure that Amazon uses to run its own global network of web sites.

### **Advantages of using Amazon S3**

|Advantage|Explain|
|--------|-------|
|Creating buckets|Create and name a bucket that stores data. Buckets are the fundamental containers in Amazon S3 for data storage.|
|Storing data| Store an infinite amount of data in a bucket. Upload as many objects as you like into an Amazon S3 bucket. Each object can contain up to 5 TB of data. Each object is stored and retrieved using a unique developer-assigned key.|
|Downloading data|Download your data or enable others to do so. Download your data anytime you like, or allow others to do the same.|
|Permissions|Grant or deny access to others who want to upload or download data into your Amazon S3 bucket. Grant upload and download permissions to three types of users. Authentication mechanisms can help keep data secure from unauthorized access.|
|Standard interfaces|Use standards-based REST and SOAP interfaces designed to work with any internet-development toolkit.|

### **Amazon S3 concepts**

|Concept|Meaning|
|-------|-------|
|bucket|A  is a container for objects stored in Amazon S3. Every object is contained in a bucket.|
|Objects|Objects are the fundamental entities stored in Amazon S3. Objects consist of object data and metadata. The data portion is opaque to Amazon S3. The metadata is a set of name-value pairs that describe the object.|
|Keys|A key is the unique identifier for an object within a bucket. Every object in a bucket has exactly one key.|
|Regions|You can choose the geographical AWS Region where Amazon S3 will store the buckets that you create.|

### **Amazon S3 data consistency model**

- A process writes a new object to Amazon S3 and immediately lists keys within its bucket. The new object will appear in the list.

- A process replaces an existing object and immediately tries to read it. Amazon S3 will return the new data.

- A process deletes an existing object and immediately tries to read it. Amazon S3 will not return any data as the object has been deleted.

- A process deletes an existing object and immediately lists keys within its bucket. The object will not appear in the listing.

### **The REST interface**

- Using REST, you use standard HTTP requests to create, fetch, and delete buckets and objects.
- You can use any toolkit that supports HTTP to use the REST API.
- TIn some areas, we have added functionality to HTTP. In these cases, we have done our best to add the new functionality in a way that matched the style of standard HTTP usage.

## **S3 with Amplify**

- Install Amplify Libraries

```
dependencies {
    implementation 'com.amplifyframework:aws-storage-s3:1.17.4'
    implementation 'com.amplifyframework:aws-auth-cognito:1.17.4'
}
```

- Initialize Amplify Storage
To initialize the Amplify Auth and Storage categories you call `Amplify.addPlugin()`.
- Uploading data to your bucket

### **Why to use Amazon S3?**

By using  Amazon S3 we can easily create buckets, storing data and download data with permissions.

### **How to start using Amazon S3?**

**Step 1:**

Abb this command to commandLine: `amplify add storage`;
Then Enter the following:
```
? Please select from one of the below mentioned services:
    `Content (Images, audio, video, etc.)`
? You need to add auth (Amazon Cognito) to your project in order to add storage for user files. Do you want to add auth now?
    `Yes`
? Do you want to use the default authentication and security configuration?
    `Default configuration`
? How do you want users to be able to sign in?
    `Username`
? Do you want to configure advanced settings?
    `No, I am done.`
? Please provide a friendly name for your resource that will be used to label this category in the project:
    `S3friendlyName`
? Please provide bucket name:
    `storagebucketname`
? Who should have access:
    `Auth and guest users`
? What kind of access do you want for Authenticated users?
    `create/update, read, delete`
? What kind of access do you want for Guest users?
    `create/update, read, delete`
? Do you want to add a Lambda Trigger for your S3 Bucket?
    `No`
```

**Step 2:**

Push the changes to amplify: `amplify push`

**Step 3:**

Add the dependencies:
```
dependencies {
    implementation 'com.amplifyframework:aws-storage-s3:1.17.4'
    implementation 'com.amplifyframework:aws-auth-cognito:1.17.4'
}
```

**Step 4:**

Initialize Amplify Storage
```
Amplify.addPlugin(new AWSCognitoAuthPlugin());
Amplify.addPlugin(new AWSS3StoragePlugin());
```
Then the class should  look like this:
```
public class MyAmplifyApp extends Application {
    @Override
    public void onCreate() {
        super.onCreate();

        try {
            // Add these lines to add the AWSCognitoAuthPlugin and AWSS3StoragePlugin plugins
            Amplify.addPlugin(new AWSCognitoAuthPlugin());
            Amplify.addPlugin(new AWSS3StoragePlugin());
            Amplify.configure(getApplicationContext());

            Log.i("MyAmplifyApp", "Initialized Amplify");
        } catch (AmplifyException error) {
            Log.e("MyAmplifyApp", "Could not initialize Amplify", error);
        }
    }
}
```

**Step 5:**

Upload data to your bucket
```
private void uploadFile() {
    File exampleFile = new File(getApplicationContext().getFilesDir(), "ExampleKey");

    try {
        BufferedWriter writer = new BufferedWriter(new FileWriter(exampleFile));
        writer.append("Example file contents");
        writer.close();
    } catch (Exception exception) {
        Log.e("MyAmplifyApp", "Upload failed", exception);
    }

    Amplify.Storage.uploadFile(
            "ExampleKey",
            exampleFile,
            result -> Log.i("MyAmplifyApp", "Successfully uploaded: " + result.getKey()),
            storageFailure -> Log.e("MyAmplifyApp", "Upload failed", storageFailure)
    );
}
```

[HOME](https://malkhaleel88.github.io/reading-notes)