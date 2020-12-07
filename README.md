
![msplib](https://files.catbox.moe/lq201t.jpg)


[![Discord Server](https://img.shields.io/discord/708318629112053841?color=darkcyan&label=Discord&logo=Discord&logoColor=white&style=flat-square)](https://discord.gg/dolo) 
[![Nuget](https://img.shields.io/nuget/v/Dolo.msplib?logo=nuget&style=flat-square)](https://www.nuget.org/packages/Dolo.msplib/)

![Info](https://placehold.it/15/F09B9D/000000?text=+) `This is a library for developing MovieStarPlanet tools. and no hack or cheat.`   
![Info](https://placehold.it/15/F09B9D/000000?text=+) `We do not offer ready-made programs.`    
![Info](https://placehold.it/15/F09B9D/000000?text=+) `Learn the basics of c#.`  

> *the most powerful and best library for moviestarplanet.*   
> *with msplib you can easily create tools or other things for moviestarplanet.*   

 
# Installation

Use [Nuget](https://www.nuget.org/profiles/cydolo) to install the [mspLib](https://msplib.cbkdz.eu/installation). 
```
Install-Package Dolo.msplib
```

# Start

> A Simple way to login with KeepAlive.

```cs
MspClient mspClient = new MspClient(new MspClientConfig {
	KeepAlive = true,
	Server = Server.Germany
	// Server = "Germany".ToType<Server>()
});

Login mspLogin = await mspClient.LoginAsync("Username", "Password");

if (!mspLogin.LoggedIn) {
	Console.WriteLine("Error > {0}", mspLogin.Status);
	return;
}

ActorImage Img = await mspLogin.Actor.GetActorImageAsync();

Console.WriteLine("Hello {0}\n\nStarCoins {1}\n\nImage {3}", 
                  mspLogin.Actor.Username, 
                  mspLogin.Actor.StarCoins.ToString("N0"), 
                  Img.AvatarUrl);
```

for more examples [click here](https://github.com/cydolo/mspLib/tree/master/msp)

# Documentation

documentation coming soon.
 
for any help join our [discord server](https://discord.gg/dolo) or [create a new issue](https://github.com/cydolo/mspLib/issues)

# Changelog

for release notes or changelog examples [click here](https://github.com/cydolo/mspLib/blob/master/CHANGELOG.md)
