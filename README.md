# Ushan Dissanayake

A collection of my projects!

---
![example_output](https://i.imgur.com/ImUcjzC.gif) JiJi - written in C#, PHP and JavaScript:
---
JiJi allows you to view and create music playlists with queues and timestamps to scrollable web content. Users can upload their playlists and share the codes with anyone.

[Download](https://zodart.com/jiji/download/JiJi.zip)

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
