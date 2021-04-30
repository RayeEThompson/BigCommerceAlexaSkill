
# Alexa, Where Will Ecommerce Be In 2022?

I have been interested in the development of Internet of Things (IOT) applications for a while now. It amazes, confounds, and excites me. I like to think about how people 100 years ago would marvel at such technological advancements and how people 500 years ago would prosecute us for witchcraft.

If you think about it, we all look like modern wizards. We walk around talking to objects that make things happen. Instead of wands, they are various types of hardware; instead of spells, they’re invocations to illicit scripts.

>“Alexa, order my fav from Pizza Hut.” 
>Alexa responds, “I have ordered my fav from Pizza Hut.

Twenty minutes to an hour later you have a pizza, that is your favorite, on your doorstep. You can’t tell me that is not magic. IOT is magical. 

![Magic Gif](https://media.giphy.com/media/12NUbkX6p4xOO4/giphy.gif)

Throughout this post, I will explain the magic that is IOT and we will answer, 
“Alexa, where will ecommerce be in 2022?”.

## The Five W’s of IOT
I don’t want to ruin the magic that is IOT, but at the end of the day - it’s technology. Let’s review the Five W’s: What, Why, Who, Where, and When. 

### 1. What is IOT?
After StackOverflow, my favorite site as a developer is Wikipedia. Wikipedia defines the [Internet of Things (IOT)](https://en.wikipedia.org/wiki/Internet_of_things) as, “A network of physical objects -- “things” that are embedded with sensors, software and other technologies for the purpose of connecting and exchanging data with other devices and systems over the internet”. 

For our purposes at BigCommerce, these are devices that can take in a verbal input (speech) and relay that information to a server containing a script that can be invoked to call an action or relay data from BigCommerce stores. Since BigCommerce is Open SaaS and API driven, nearly every action that you can accomplish via storefront can be accomplished via a voice assistant. Therefore, using IOT you can build applications that surface products, allow orders and relay shipping information to users. 

### 2. Why should I build IOT applications?
As mentioned above, this technology allows people to access BigCommerce stores using their voice. This means that you can offer a valuable add to a BigCommerce merchant, the ability to be even more accessible. If you can architect your decision tree well, you can enhance the shopper experience for people who are differently abled and make the lives of busy people wanting to make a quick purchase even easier.

As the omnichannel evolution in commerce continues to grow, developers need to understand how to enable these experiences in order to keep up with what will be rising demand.

### 3. Who are the big IOT influencers?
There are three big IOT influencers in the voice assistant space. 
They are:
* Alexa by Amazon.
* Google Assistant by Netflix. Just kidding. It’s by Google.
* Siri by Apple. 

### 4. Where can I learn about these platforms?
Here are the main learning spaces for the above platforms:
* Learn the [Alexa Skills Kit](https://developer.amazon.com/en-US/alexa/alexa-skills-kit/start?sc_category=paid&sc_channel=SEM&sc_campaign=SEM-GO^Brand^All^LD^Professional_Developer^Evergreen^US^English^Tex&sc_publisher=GO&sc_content=content&sc_detail=379690615386&sc_funnel=convert&sc_country=US&sc_keyword=alexa%20skills%20kit%20tutorial&sc_place=&sc_trackingcode=e&sc_segment=&sc_medium=paid%7CSEM%7CSEM-GO^Brand^All^LD^Professional_Developer^Evergreen^US^English^Tex%7CGO%7Ccontent%7C379690615386%7Cconvert%7CUS%7Calexa%20skills%20kit%20tutorial%7C%7Ce%7C&gclid=Cj0KCQjwpdqDBhCSARIsAEUJ0hP-NseIhGYEvOP8ehY23n61mIKBG1AlXmXmiLOLPxYAJcQUVUVB1QQaAqooEALw_wcB).
* Take [Actions on Google](https://developers.google.com/assistant).
* Enable [SiriKit](https://developer.apple.com/documentation/sirikit).

### 5. When should IOT be part of your omnichannel strategy?
Personally, always… However, this level of custom development might not be the right fit, budget wise, for some merchants. That’s where creating an app like [Blu.AI](https://blu.ai/) could make IOT more accessible to the greater BC ecosystem. 

**Developers unite! Democratize IOT for SMB merchants!** 

Now that I have set forth the rally cry, let’s dive into how you can actually develop an Alexa Skill. 

## How to create an Alexa Skill

Alexa Skills are very easy to develop. Their SDK supports both JavaScript and Python. Additionally, most configuration is done in a JSON file, which is a very developer-friendly feature.

![Impressive, Very Nice](https://media.giphy.com/media/eKNrUbDJuFuaQ1A37p/giphy.gif)

Another developer-friendly feature is the Amazon Developer Console for Alexa Skills. This allows you to avoid some of the initial development steps in code. You can opt to use the slick UI. This will also allow you to create a project that is “Alexa Hosted” which means that you do not have to go into AWS and standup services. 

This tutorial will use that console. At the end, I will suggest some extensions for VS code to enable development locally. 

### 1. Become an Amazon Developer.
First, you need to have a developer account through Amazon. After checking out [“Getting Started with Alexa Skills Kit”](https://developer.amazon.com/en-US/alexa/alexa-skills-kit/start?sc_category=paid&sc_channel=SEM&sc_campaign=SEM-GO^Brand^All^LD^Professional_Developer^Evergreen^US^English^Tex&sc_publisher=GO&sc_content=content&sc_detail=379690615386&sc_funnel=convert&sc_country=US&sc_keyword=alexa%20skills%20kit%20tutorial&sc_place=&sc_trackingcode=e&sc_segment=&sc_medium=paid%7CSEM%7CSEM-GO^Brand^All^LD^Professional_Developer^Evergreen^US^English^Tex%7CGO%7Ccontent%7C379690615386%7Cconvert%7CUS%7Calexa%20skills%20kit%20tutorial%7C%7Ce%7C&gclid=Cj0KCQjwpdqDBhCSARIsAEUJ0hP-NseIhGYEvOP8ehY23n61mIKBG1AlXmXmiLOLPxYAJcQUVUVB1QQaAqooEALw_wcB) you can click on the blue “Console” button. This will direct you to login or create an account. 


Follow the on screen instructions to create your account. The initial screens should look like the following gif.

[Gif of Sign Up](https://drive.google.com/file/d/1us4cjn8NFEWEVTbnu3iPUHaUX6RMDsSa/view?usp=sharing)

### 2. Build a Skill
![Slide Building a Skill](https://miro.medium.com/max/1400/0*7SXaAukKa42U1xEa)

To build a skill it requires understanding how Alexa constructs the frontend user interface. This auditory interface has four parts. 
They are:
* Invocation
* Intent
* Slots
* Utterances

An invocation is the app or skill that the user is requesting. The invocation or skill name is the only thing that cannot be changed post production. It is important to make sure that you are naming this well. Make sure that you are thinking about how the words are spelled as well as sound. I made the mistake of using “Raye’s Store”. However, Alexa could never find that skill because “Raye’s Store” in JSON was “rayes store” which when pronounced should be “ray-es”. I found that phonetic spelling for invocation names worked best. 

Intents are basically commands. Alexa Skills utilize an MVC architecture. Therefore, intents should align to a method in your controller with a similar name. This way when Alexa is running the skill the user feels like they are on a path. Whittling their way to an ultimate goal. 

You may be wondering, how does Alexa handle variables? 

This is where slots and utterances come into play. Slots are variables that that user might say to access specific functionality. For example: “Alexa, tell me the weather in Austin.” Austin is a slot because that could be represented as `{{city}}` or even more generally as `{{location}}`. 

Utterances are another type of variable; the variable of word choice. Users depending on region or preference could request a skill differently. Utterances allow you to teach Alexa the various ways your users may request the same intent. 

![Slide Utterances](https://miro.medium.com/max/1400/0*van8nOpO1sC7m8Bl)

As you can see, there are many ways to ask for the same thing. Utterances help your users avoid frustration. The more utterances you can feed into the model, the better. 

Now that you know the pieces, putting them together is a breeze in the Amazon Developer Console. Following the steps laid out in the UI, you set the invocation name by entering text in a text field. Then you can work on various intents. By default there are several required by Alexa for navigation and system purposes. You will want to have at least one intent that maps to custom functionality in the controller. That is all that is required. Slots and Utterances are optional. They are easily updated in a JSON file that is editable online.

![JSON Editor](https://miro.medium.com/max/1400/0*FSmubBPoZS6HID2j)

### 3. Code a Skill.
Alexa offers the ability to be low code for UX development, however,you still have to get your hands dirty when it comes to hooking up the frontend to your backend. They offer a nifty online editor that is directly linked to services in AWS. This is convenient so that you don’t have to navigate between AWS and Alexa Developer Console. This editor shows you your project and it’s dependencies. I chose to use a Node.js project. They also offer Python as an option. 

![Code Areas Alexa Console](https://miro.medium.com/max/1400/0*_05tmSWqBKLpP4gW)

Per usual, the Node.js project’s main file is index.js. This file is generated for you with all the required handlers and acts as the controller as previously noted this app utilizes an MVC architecture. You can add custom functions here directly, as I did for this proof of concept; you can also create classes and functions that are exported to be utilized in your index.js. For a larger scale application, I recommend the later option to give you the ability to scale. 

To quickly prove that I could connect to a BigCommerce store, I opted to call the BigCommerce catalog API directly from the index.js. As I go back and update this further, I will ensure to follow best coding practices and remove all keys and place them in key vaults  and .env files. I will also split all API calls into their own classes and export them. The following shows the API call I made to get featured products from a BigCommerce test store. 

```

function httpGet() {
  return new Promise((resolve, reject) => {
    var options = {
      host: "api.bigcommerce.com",
      path:
        "/stores/ltgn22trch/v3/catalog/products?include_fields=name&is_featured=1",
      method: "GET",
      headers: {
        "X-Auth-Token": "awj6qjj90rrt899pq5kff6n4ypagp5k",
      },
    };

    const request = https.request(options, (response) => {
      response.setEncoding("utf8");
      let returnData = "";

      response.on("data", (chunk) => {
        returnData += chunk;
      });

      response.on("end", () => {
        resolve(JSON.parse(returnData));
      });

      response.on("error", (error) => {
        reject(error);
      });
    });
    request.end();
  });
}
```
For those new to BigCommerce you have to use a storehash and authorization token that you generate in the stores control panel. The store hash looks like this, `/stores/ltgn22trch/v3/catalog/`. You will see that in the file that downloads when you generate your API keys. Using a simple httpGet() function was the easiest way to get started. This will send the request and return a response. You can then get the information you need from the response in your handler, or parse the response and hold what you need in a constant variable. 

>🤯  Quick Tip: In your httpGet() for the `host` don’t add the “https://” this will cause silly errors and several minutes of frustration while googling the error. Trust me and save yourself a trip to StackOverflow. 

Your handler function that utilizes the data returned from BigCommerce can look something like this: 
```
const FeaturedProductIntentHandler = {
  canHandle(handlerInput) {
    return (
      Alexa.getRequestType(handlerInput.requestEnvelope) === "IntentRequest" &&
      Alexa.getIntentName(handlerInput.requestEnvelope) ===
        "FeaturedProductIntent"
    );
  },

  async handle(handlerInput) {
    const response = await httpGet();
    console.log(response);

    return handlerInput.responseBuilder
      .speak(`Okay, here is what Raye has for you ${response.data[0].name}`)
      .reprompt("Would you like to hear the featured product?")
      .getResponse();
  },
};
```
In the above code, most of this is Alexa default code for creating a handler. I only added an async handlerInput for getting the data from BigCommerce. I then took the response from BigCommerce and asked for the first item name in the data array. If you wanted Alexa to say all featured products, you could loop over that data and have Alexa read all the names, just have the loop return a comma delimited string. 

> 🎉 This is all the code you need to create a simple Alexa Skill app that will read aloud the featured products from a BigCommerce Store. 

### 4. Test a Skill.
It is very easy to test these apps using either the Alexa Developer console or the VS Code Alexa Skills Kit extension. In the video below, you can see the Alexa Developer console in action. You can type commands or use voice commands. 

{% youtube Jr7a3yxyRgk %}

It is important to notice what happens when you speak. Are there words that Alexa can’t understand? Make sure to add these words and phrases to your utterances array. You should also review if you are finding yourself wanting to ask for more than one thing, this may be a good place to use a slot. You can then add scope for the next iteration to include the slot. I found many things that I would like to write up as user stories while testing. 

### 5. Deploy a Skill.
The last thing you need to do is deploy your skill. You do this in the console or via CLI. The code will be reviewed by automated tests. Should Amazon find an error - they will not deploy your application. 

As stated before, make sure your invocation name is correct. This is the only thing you cannot change after the skill is deployed. 

Just like that, you are now a BigCommerce and Amazon developer. 

![High Five](https://media.giphy.com/media/wrzf9P70YWLJK/giphy.gif)

## Want to see a sample app?
If you want to see the sample application source code from this tutorial, it is located on [my GitHub](https://github.com/RayeEThompson). You can view it in the repo [BigCommerceAlexaSkill](https://github.com/RayeEThompson/BigCommerceAlexaSkill). I have included a README.md that includes tips to get started as well as ideas for what you can build with it. Below I will discuss how I determined what to build, what I learned and how I plan to iterate on this concept. 

### Determining the POC
I had no idea what I wanted this app to do at first. I got into the role of the user. If I was going to ask Alexa anything about a favorite store, I would want to know what product they think is amazing. This led me to look at the BigCommerce catalog and the featured products list. This was small enough in scope to satisfy the requirements of my POC without taking up a whole sprint. There are many small apps that could come out of just using the BigCommerce catalog.  

If you are wanting to do your own, think small and scale up. This will help you get comfortable with this platform. You will iterate much faster each time as you learn the Alexa Skills Kit development patterns.

### What I Learned

I learned that IOT while magical is very accessible to developers. Companies want developers to expand the use of these platforms. Therefore, they make it easy to get started and iterate. I loved this project because it was just so fun to code and test. 

### How I Would Iterate
There are many things I can think of to make this app more robust. I would love to have all featured products read aloud but I would also want to make these items purchasable. This is completely doable as long as you use Amazon Pay. 

The last thing I would also like to do is convert this from using REST to using GraphQL. That way it would be easier to add more scope to the application in the future. Queries in GraphQL are my preferred method for gathering data from the BigCommerce storefront. I like how much control I have over the returned data. 

## Conclusion
This was a really fun project that I enjoyed creating. I truly believe that omnichannel commerce is going to take the lead in 2021 and on into 2022. One of those channels should definitely be the Alexa platform. 

So, Alexa...where will ecommerce be in 2022? 
The answer is everywhere. 
