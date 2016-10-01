# azure-meteor
__Azure Meteor__ is a sample project that can be used as a starting point for your MeteorJs apps on Azure web services. To get started just fork this repository and start developing (see [meteor.com](http://meteor.com) for more infos):

```
$ meteor
```

Create your App Service via the [Azure Management Portal](http://portal.azure.com) and set up your deployment credentials. In your application settings activate Web Sockets, then create a new entry _ROOT_URL_ with your apps URL (e.g. http://azure-meteor.azurewebsites.net). Optionally specify a _MONGO_URL_ to your MongoDB server. DocumentDB should be the easiest way to get you started here (the format should be like mongodb://username:passphrase@appname.documents.azure.com:10250/?ssl=true!

__Azure Meteor__ uses the free Travis CI service for optimizations and deployment. Visit [travis-ci.org](http://travis-ci.org), login with your GitHub credentials and activate your repository. Under _More options -> Settings_ set the following Environment variables: _AZURE_WA_SITE_, _AZURE_WA_USERNAME_ and _AZURE_WA_PASSWORD_ with your azure app service credentials.

Travis will listen for pushes to the master branch of your repository, optimize your app for production use (e.g. minify JavaScript, CSS, etc.) and automatically deploy it to azure within a few minutes.
