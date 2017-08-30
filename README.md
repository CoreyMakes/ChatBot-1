# Contextual Chatbot
The iPython Notebook "contextual_chatbot" inside the code folder creates a bot that can respond to a users greetings, questions, thanks and goodbyes.
In the intents.json file I have personally created tags withs patterns and their responses for typical conversations that could go on between a cars salesman and a customer.

A 2 layer neural net is trained on these conversations, which can then give probabilities of tags from new user inputs.
For example, if a user says "Hello, how are you today?", the bot will give the tag "greeting" a high probability and return a pre-made response.
I also allow for context settings, so if the bots response relies on understanding a previous response, it will be able to.
Also, I allow for sub-intents. For example, I have an tag called "hours", which has to do with when the car salesman is available.
The sub-intents have to do with whether the customer is referring to today, tomorrow or this week. The sub-intents are trained on their own just as the intents are.

At the bottom of contextual_chatbot.ipynb, I have given the bot several example sentences that it response well to.

## Future Considerations
I would like the bot to be able to take in multiple sentences and return a multiple sentence response. I have set the threshold at 60% so there is no response if all the probabilities are below that. I think this would work well in creating a multi-sentence response because there are some things the user says that do not need to be responded to and I could just combine all the responses together.

I also want to check for spelling errors made by the user.
