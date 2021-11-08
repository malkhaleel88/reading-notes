# **GraphQL @connection**

![GraphQL](https://d2908q01vomqb2.cloudfront.net/0a57cb53ba59c46fc4b692527a38a87c78d84028/2020/01/07/microservices.png)

## **What is Serverless Architecture? What are its Pros and Cons?**

* Serverless architecture is exciting, but it comes with a bunch of limitations.
* As the validity and success of architectures depend on the business requirements and by no means solely on technology.
* Serverless can shine when used in proper place.

## **AWS Amplify Kool-Aid**

**What is the advantage of AWS amplify?**

AWS Amplify makes it simple to develop, maintain and deploy applications by reducing the time and cost. The tool offers scalable and full-stack development options without having to worry about frontend or backend configurations. AWS Amplify Console is used to build, deploy, and host web apps.

### **AWS Amplify features**

* **Authentication**
 Create seamless on-boarding flows with a fully-managed user directory and pre-built sign-up, sign-in, forgot password, and multi-factor auth workflows.
* **DataStore**
Use a multi-platform (iOS/Android/React Native/Web) on-device persistent storage engine that automatically synchronizes data between mobile/web apps and the cloud, powered by GraphQL.
* **Analytics**
Understand the behavior of your web, iOS or Android users. Use auto tracking to track user sessions and web page metrics or create custom user attributes and in-app metrics.
* **API**
Make secure HTTP requests to GraphQL and REST endpoints to access, manipulate, and combine data from one or more data sources.
* **Functions**
Add a Lambda function to your project which you can use alongside a REST API or as a datasource in your GraphQL API using the @function directive in the Amplify CLI.
* **Geo**
Add location-aware features like maps and location search to your JavaScript-based web app in minutes.
* **Interactions**
Build interactive and engaging conversational bots with the same deep learning technologies that power Amazon Alexa with just a single line of code.
* **Predictions**
Enhance your app by adding AI/ML capabilities. You can easily achieve use cases like text translation, speech generation from text, entities recognition in image, interpretation of text, and transcribing text.
* **PubSub**
Pass messages between your app instances and your app's backend creating real-time interactive experiences. Amplify provides connectivity with cloud-based message-oriented middleware. Powered by AWS IoT services and Generic MQTT Over WebSocket Providers.
* **Push notifications**
Improve customer engagement by using marketing and analytics capabilities. Leverage customer insights to segment and target your customers more effectively.
* **Storage**
Store and manage user generated content such as photos, videos securely on device or in the cloud.

## **GraphQL `@connection`**

The `@connection` directive enables you to specify relationships between `@model` types,
Supports one-to-one, one-to-many, and many-to-one relationships.

### **Definition**

`directive @connection(keyName: String, fields: [String!]) on FIELD_DEFINITION`

### **Usage**

Relationships between types are specified by annotating fields on an `@model` object type with the `@connection` directive.

**Example of define a one-to-one connection:**

```
  type Project @model {
  id: ID!
  name: String
  team: Team @connection
  }

 type Team @model {
  id: ID!
  name: String!
 }
```

**Example of define a one-to-many connection:**

```
type Post @model {
  id: ID!
  title: String!
  comments: [Comment] @connection(keyName: "byPost", fields: ["id"])
}

type Comment @model
  @key(name: "byPost", fields: ["postID", "content"]) {
  id: ID!
  postID: ID!
  content: String!
}
```

**Example of define a one-to-many connection:**

```
type Post @model {
  id: ID!
  title: String!
  editors: [PostEditor] @connection(keyName: "byPost", fields: ["id"])
}

# Create a join model and disable queries as you don't need them
# and can query through Post.editors and User.posts
type PostEditor
  @model(queries: null)
  @key(name: "byPost", fields: ["postID", "editorID"])
  @key(name: "byEditor", fields: ["editorID", "postID"]) {
  id: ID!
  postID: ID!
  editorID: ID!
  post: Post! @connection(fields: ["postID"])
  editor: User! @connection(fields: ["editorID"])
}

type User @model {
  id: ID!
  username: String!
  posts: [PostEditor] @connection(keyName: "byEditor", fields: ["id"])
}
```

[HOME](https://malkhaleel88.github.io/reading-notes)