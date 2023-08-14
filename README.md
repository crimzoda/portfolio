# Ushan Dissanayake

A collection of my projects!

Table of contents:

[Software projects](#software-projects)

[Game developement projects](#game-development-projects)


# Software projects
---
![example_output](https://basedboard.net/favicon.png) [basedboard.net](https://basedboard.net/) - written in JavaScript, HTML/CSS using Node.js & Firebase:
---
A real-time live canvas in which people can submit and place 'tiles' (windows of media, text, links etc.), similar to r/place, except with media instead of pixels.

![Screenshot 2023-08-14 020754](https://github.com/crimzoda/portfolio/assets/46323591/4d471720-7e80-42bf-bc35-f066b4f421ba)

This is one of the projects I learnt the most from. I learned about client-side and server-side security, ranging from creating my own method to process media server-side, in order to increase security and working with the Firebase realtime databases from both the client and server-side of the project.

---

![example_output](https://i.imgur.com/ImUcjzC.gif) JiJi - written in C#, PHP and JavaScript:
---
JiJi allows you to view and create music playlists with queues and timestamps to scrollable web content. Users can upload their playlists and share the codes with anyone.

[Download](https://zodart.com/jiji/)

The client is built in C# under .NET 6.0 and WPF. 

For interfacing with the server I made a Web API that handles actions such as:
  - Uploading playlists
  - Fetching playlists
  - Favouriting playlists
  
![ezgif com-gif-maker (1)](https://user-images.githubusercontent.com/46323591/209410074-b00fc174-27ca-4af0-842e-f5e8b1149e29.gif)

The purpose of the API is security and for smoother SQL interactions with the database.

---
Ballast - written in C#
---

A library for retrieving data from the [Steam Store.](https://store.steampowered.com/)

[GitHub for Ballast](https://github.com/crimzoda/ballast)

I utilized a mix of the Steam Web API and scraping. 
For most of the functionality I used the Steam Web API, however, for parts where the API wasn't reliable I used scraping (HtmlAgilityPack) as a fallback.

Library functionality:
  - Retrieve name
  - Retrieve description
  - Retrieve developers
  - Retrieve rating
  - Retrieve price
  - Retrieve tags
  - Retrieve header image
  - Retrieve icon
  
Here's an example code snippet:
```cs
using Ballast;

/*205100 is the appid of the game in the steam store
you can put whatever you want*/
storeItem item = new storeItem("205100");

/*although you would already know the appid
it would be useful to just have it as property anyway*/
Console.WriteLine("AppId: " + item.appid);
Console.WriteLine("Name: " + item.name);
Console.WriteLine("Description: " + item.description);
Console.WriteLine("Developers: " + String.Join(',', item.developers.ToArray()));
Console.WriteLine("Rating: " + item.rating);
/*right now this returns the final discounted price
future versions will have both discounted and base price*/
Console.WriteLine("Price: " + item.price);
Console.WriteLine(item.imageURL);
Console.WriteLine(item.iconURL);
//the tags property in storeItem is a List<string>
Console.WriteLine("Tags: " + String.Join(',', item.tags.ToArray()));
```
Here is the output:

![example_output](https://user-images.githubusercontent.com/46323591/205365769-bd52895b-6c6e-4b38-887f-8a20d992bc91.PNG)

---
![zodi](https://user-images.githubusercontent.com/46323591/209404340-a8e8d4b9-1f6f-4d66-aecd-890f6a87c85a.png) [zodart.com](https://zodart.com/) - written in PHP using SQL ( + HTML/CSS)
---

A virtual gallery, people can submit art and everyday automatically, 3 will be chosen and displayed.

[GitHub for zodart](https://github.com/crimzoda/zodart)

![example_output](https://user-images.githubusercontent.com/46323591/204822159-607e6a76-804a-4e5e-a233-3ae68e06485d.png)

---

# Game development projects:
---

Purgatory - written in Godot
---

![LMwKKnK](https://github.com/crimzoda/portfolio/assets/46323591/f4c4bb1a-18ac-410e-a3ce-82d13cd7f30c)

Purgatory is a roguelike, 2.5d, procedural dungeon crawler. Taking place in my own interpretation of a limbo between heaven and hell. You will meet various characters and entities of varying backgrounds. Murderers, great Doctors, exiled angels. Survive or face eternal damnation to hell

Purgatory is a roguelike, procedural dungeon crawler. Taking place in my own interpretation of a limbo between heaven and hell. You will meet various characters and entities of varying backgrounds. Murderers, great Doctors, exiled angels. Survive or face eternal damnation to hell

Features:

 - Procedural dungeons:

   ![VDRkfwN](https://github.com/crimzoda/purgatory/assets/46323591/1bd77920-34a9-484e-9296-74a557d30985)

- Enemies:

  ![Ze1Pl11](https://github.com/crimzoda/purgatory/assets/46323591/e30c0aeb-baf0-40a3-8197-030897e0c6a5)

- Bosses:

  ![jFm7t5v](https://github.com/crimzoda/purgatory/assets/46323591/448e2d03-1132-482e-9f0f-33ce3256eb78)

- Combat/dual wielding:

  ![ezgif com-resize (10)](https://github.com/crimzoda/purgatory/assets/46323591/b3028691-3190-4c58-9667-2087c9ace10d)
  ![RXPnMlI](https://github.com/crimzoda/purgatory/assets/46323591/bc0e69b5-689d-488a-92bc-eafe4c8e05cf)

- Special rooms (trap and chest rooms):

  ![QOw8FpU](https://github.com/crimzoda/purgatory/assets/46323591/d05803cd-3034-491d-802c-eafd59e74225)
  ![cX3QyUt](https://github.com/crimzoda/purgatory/assets/46323591/45001200-b892-4b7b-ad47-e86fd43e46e2)
