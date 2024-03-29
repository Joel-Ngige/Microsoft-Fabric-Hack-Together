# Access Azure OpenAI for Hack Together, for Free!

**We've made it quick and easy to get access to Azure OpenAI models for the duration of Hack Together!**

By using our Azure OpenAI Proxy service you'll get access to keys and endpoints that work just like the real ones you get from using the Azure Portal and Azure OpenAI Studio to deploy your own models. 

When you get access to Azure OpenAI yourself, all you need to do is switch over your endpoints and keys to get up and running on your own resources.

Here you'll see how to **[get started](#get-started)** by gaining access to our proxy server. Then see how to **[get hacking](#get-hacking)** using the endpoint, key, and models. You will also find some examples here for each of the models and how to use them, for Python and .NET. 

**Got Stuck?** If you have any improvements for these instructions let us know in the [GitHub Issues](https://aka.ms/fabric-hack24-issues) so we can make them better for everyone.

## Get started
To gain access:

1. **Register for this event** at this URL: [https://aka.ms/Hacktogether-AI-register](https://aka.ms/Hacktogether-AI-register) 

2. **Login with GitHub** using the button in the top-right corner
![Screenshot of registration page with arrow pointing to top right corner.](images/proxy2.png  "Click login with GitHub")

3. Once logged in, you have access to your API key for this event, click the copy icon. **Keep your key handy, for the following steps and for your hacking!**  
![Screenshot of proxy site page with arrow pointing to the copy button next to API Key.](images/proxy3.png "Click the copy button to copy your key")

4. **Go to the AI Proxy Playground** at this URL: [https://aka.ms/Hacktogether-AI-playground](https://aka.ms/Hacktogether-AI-playground)


5. **Enter your API key** in the text box in the top-right corner and click ***Authorize***
![Screenshot of proxy playground page with arrow pointing to API text entry field and authorize button.](images/proxy5.png "Enter your key and hit 'Authorize'")

6. **You should now see the event name** "Hack Together Fabric AI" in the top-right corner!
![Screenshot of proxy playground page with a tick and an arrow pointing to the event name "Hack Together Fabric AI" that appears once you have succesfully entered a key for the event.](images/proxy6.png "When you see the event name you have succesfully entered your key")

7. **You're ready to test your set up**, first you need to **choose a model** in the pannel on the right-hand side. GTP models are used for running/testing in the chat, choose one to get started.<br>
![Screenshot of proxy playground page with an arrow pointing to the Model Deployment field](images/proxy7-1.png "Set the Model Deployment")
<br><br>
**We recomend one of the GTP-35 models** just for the purposes of testing the playground quickly.<br>
![Screenshot of proxy playground page with an arrow pointing to the Model Deployment drop down selecting gpt-35-turbo](images/proxy7-2.png "Set your model, GTP 3.5 options are fastest in this playground.")


8. You're ready to go, write a message in the **Chat Session**. You should receive a message back in a few seconds!
![Screenshot of proxy playground page with an arrow pointing to the input field, where the message /Hello" has been writen.](images/proxy8.png "Test the service using the Chat feature by writing a message")

9. **Once you receive a message you know you are ready to hack!**
![Screenshot of proxy playground where the AI has responded with a message that says "Hello! How can I assist you today?".](images/proxy9.png "When you receive a response you are ready to hack!")

***If you get an error** when trying out the chat feature try refreshing and if that fails, hard refreshing (CTRL + SHIFT + R) your browser. If it doesn't work after a few times take a screen shot of the error and leave us a message in the [GitHub Issues](https://aka.ms/fabric-hack24-issues).*


## Get Hacking 
### Using the Endpoint and Key
To get hacking with AI this event you'll need both the endpoint and key to put into your own code creations! 

> ### Key Event Info
> **Endpoint**: https://polite-ground-030dc3103.4.azurestaticapps.net/api/v1
>
> **Key:** Use the key you got in step 3 above.
> 
> **Never commit your keys to a Git repository or share them publicly.**


*If at any point your code runs and a request returns without content, run your code again (maybe a couple of times) and it should work. This is the expected behaviour of Azure OpenAI some of the time.*


### Model Details
For this event you have access to the four models below. You'll need to use the **model names from the table** below in your code. 
*You have up to 2000 requests per model per day.*

| Model  | Model Name  | Docs | Example (Python)*| Example (.NET)** |
|---|---|---|---|---|
| GTP-3.5  |  gtp-35-turbo | [GPT-3.5 Docs](https://aka.ms/fabric-hack24-python-docs-gtp35) | [Azure OpenAI Chat - Python ](https://aka.ms/fabric-hack24-python-eg-chat) | [Azure OpenAI Chat - .NET ](https://aka.ms/fabric-hack24-dotnet-eg-chat) | 
| GTP-3.5 (Turbo) |  gtp-35-turbo-16k | [GTP-3.5 Docs](https://aka.ms/fabric-hack24-python-docs-gtp35) | As above, change model name | As above, change model name | 
| GTP-4 |  gtp-4 | [GTP-4 Docs](https://aka.ms/fabric-hack24-python-docs-gtp4) | As above, change model name | As above, change model name |
| Embeddings |  text-embedding-ada-002 | [Embeddings Docs](https://aka.ms/fabric-hack24-python-docs-embeddings) | [Azure OpenAI Embeddings - Python ](https://aka.ms/fabric-hack24-python-eg-embeddings) | [Azure OpenAI Embeddings - .NET ](https://aka.ms/fabric-hack24-dotnet-eg-embeddings) |
| DALL-E 4 |  dall-e-3 | [DALL-E Docs](https://aka.ms/fabric-hack24-python-docs-dalle) | [Azure OpenAI DALL-E - Python ](https://aka.ms/fabric-hack24-python-eg-dalle) | [Azure OpenAI DALL-E - .NET ](https://aka.ms/fabric-hack24-dotnet-eg-dalle) |

*The models we are using are all hosted in the Sweden Central region. You won't need that information for your hacking purposes.*

#### More Python Info*
For more guidance on using Python with Azure OpenAI you can check out the [OpenAI Python API library](https://aka.ms/fabric-hack24-python) on PyPi for the docs, how to set up your environment variables, and for some simple examples. 

You'll need to add two environment variables to run the examples: ENDPOINT_URL and API_KEY. *The PyPi docs give a good example on how to set up a .env file to store your keys and endpoints and to use dot_env the library to access your keys and endpoints (dot_env is used in the Python examples listed in the table).*

#### More .NET Info**
For more guidance on using .NET with Azure OpenAI, check out the [Azure OpenAI client Library for .NET](https://aka.ms/fabric-hack24-dotnet). 

To run the examples from the table above you will need to add two environment variables:
YOUR_AZURE_OPENAI_PROXY_URL , set this to the endpoint provided above. 
YOUR_EVENT_AUTH_TOKEN , set this to your event key.
