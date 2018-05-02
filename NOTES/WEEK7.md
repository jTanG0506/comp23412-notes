# Week 7: Using external APIs

##### Notice
The first section of this week's lecture was a quick guide on how to implement Google Maps API in our Spring application, which is not examinable hence omitted.

#### Geocoding
**Geocoding** is the process of converting addresses into longitude and latitudes and **reverse geocoding** (address lookup) is getting addresses from geographical coordinates.

## Finding the right API

- **Completeness of features**: does this API do everything I need it to? A general rule of thumb is to know what features are required for you and filter your selection based on that

- **Documentation**: is it well documented? Are the given examples clear and are parameters properly explained?

- **Limitations**: on most public APIs, there is a threshold per API key to prevent abuse or encourage you to upgrade your account. For developers, this adds complexity and overhead as you now need to manage request rate to ensure you stay within the API limits. You would need to consider whether all of this overhead worth it and are there competing APIs which offer more generous limits?

- **Community**: is there a helpful and active community which can help you out when things are going wrong? Is there a support forum for problems related to broken requests, timeouts, etc. What is the provider's reputation for answering support tickets in a timely and relevant manner?

- **Data format**: how does your API return data? Does it use the much lighter and easier-to-use alternative, JSON? Does it still use XML like we did 10 years ago? Or worse, does it return data in a URL encoded string? The data format is dependent on your needs and the developer's preferences.

