At first I started with Claude, but for the project I was looking for, I wanted to give some specific prompts and I'm more familiar with ChatGPT so I did most of the HW there on the browser. 


USER PROMPT: I have to develop an interactive application using the public API for my CMU 15-113 homework. Could you please suggest me some interesting project ideas that can be considered as creative and realistic in in a few hours?

CHATGPT PROMPT: Yes — here are some ideas that are more creative than a basic weather/search app but still realistic to build in a few hours:

📚 Judge a Book by Its Cover — Show a book cover but hide the title/author. The user guesses the genre, then your app reveals the book information and tracks their score using the Open Library API. Open Library can return titles, authors, publication years, cover IDs, and other book information.
🎮 Build Your Pokémon Team — Let the user choose preferences like speed, strength, or type and generate a Pokémon team. Show each Pokémon's image, type, abilities, and stats using PokéAPI. It requires no authentication, making it especially convenient for a short class project.
🍜 “What Should I Cook?” Challenge — The user chooses a cuisine or ingredient, and the app generates a meal with a picture, ingredients, and instructions. Add buttons like Another Meal and Surprise Me. TheMealDB provides meal searches, ingredient filters, categories, and random meals.
📖 Book Roulette — User chooses a mood such as adventurous, mysterious, romantic, or thought-provoking. Your app finds a matching book, displays its cover, author, and publication year, and lets them keep generating recommendations. Open Library's Search API supports query parameters and returns multiple books in one request.
🥘 Mystery Meal Game — Display only a meal picture and let the user guess its cuisine or category. After they guess, reveal the meal name, origin, ingredients, and recipe. Keep a score across five rounds. TheMealDB supplies images along with recipe and category information, so this could look quite polished without needing a huge amount of code.
⚔️ Pokémon Battle Predictor — simple version — User selects two Pokémon, your app retrieves their stats, compares things like HP, attack, defense, and speed, and shows the stat comparison. You could determine the result using a simple rule you design rather than trying to recreate the actual Pokémon battle system. PokéAPI exposes Pokémon resources through simple GET requests.
📕 Cover Color Book Explorer — User chooses something like “dark and mysterious,” “bright and cheerful,” or “classic,” and your app retrieves book covers matching a selected subject. They can flip through them like a mini gallery and reveal the book details. Open Library has both book-search and dedicated cover APIs.
🌎 Around the World in 5 Meals — Each round generates a meal from a different region. Show the picture first, let the user guess where it comes from, then reveal the country/region, meal name, ingredients, and recipe. TheMealDB supports filtering meals by area as well as retrieving full meal information.

For your assignment, I think the strongest combination of unique + visually interesting + doable quickly is Judge a Book by Its Cover. It naturally gives you user interaction, an API request, JSON processing, images, scoring, randomization, error handling, and a reason to make multiple API-driven rounds rather than simply displaying information. Open Library specifically supports low-volume, real-time book discovery projects like this.

USER PROMPT: I wanna  build a game where users can answer a bunch of questions about themnselves and then at the end it would give them a dog best suited to them. 

CHATGPT PROMPT:
🐶 “Find Your Perfect Dog Match”

The user answers questions about their lifestyle and preferences, and your app recommends a dog breed that fits them best.

You could ask questions like:

How active are you?
Very active
Moderately active
Not very active
How much space do you have?
Large house/yard
Apartment
Small living space
How much time can you spend exercising a dog?
2+ hours
About 1 hour
Less than 30 minutes
How social do you want your dog to be?
Very friendly
Balanced
More independent
How much grooming are you okay with?
A lot
Some
Very little
What size dog do you prefer?
Small
Medium
Large
No preference

At the end, your code calculates the best match and gives something like:

Your Best Match:

🐕 GOLDEN RETRIEVER

Why this dog fits you:
• Social and friendly
• Enjoys regular exercise
• Good for an active lifestyle
• Medium-to-large breed

[API-loaded Golden Retriever image]

Match Score: 88%

The API can then provide the actual dog image dynamically, so every result isn’t just hard-coded.

For your prompt log, this would also look good as one of your key prompts:

I want to build an interactive dog-matching game where users answer several questions about their lifestyle, activity level, living space, grooming preferences, and preferred dog size. At the end, I want the program to calculate which dog breed is best suited to them and use a public API to retrieve an image of that breed. Help me design a simple scoring system and choose a public API that would work for this project.

This is stronger than a basic personality quiz because you can explain that your app is combining user input + decision logic + API data into one interactive experience.

