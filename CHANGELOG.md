##### 7.0.0

- **ADDED** `~` *MspClient has 4 new Events `OnCommandError`, `OnLoggedIn`, `OnMessageSent`, `OnMessageReceived`*
- **ADDED** `~` *Some new methods for MovieStarPlanet*
- **ADDED** `~` *New Extension `ToType<T>` to convert a string to the enum*
- **CHANGED** `~` *Renamed `MspClientOption` to `MspClientConfig`*
- **CHANGED** `~` *Renamed all Methods for a better view*
- **CHANGED** `~` *We are no longer support the CreateAccount method*
- **FIXED** `~` *Checksum for valid Request*
- **FIXED** `~` *Many bug fixes and improvements*

##### 6.7.0.1

- Fixed authentication in CreateAccount method
- Bug fixes and improvments. 

##### 6.7.0

- Big changes have been made. everything has been improved and rewritten.
- Added Support to view Json response from a Request.
- Added better handling of classes and properties.
- Changed the access modifier for many classes.
- Changed `ServiceCommands` class to `MspClientCommands`
- Changed `ServiceHelper` class to `MspClientHelper`
- Fixed CheckSum where the `DateTime` was invalid.
- Fixed Nullreferenz issues while sending custom commands.
- Fixed issues while parsing the responses of requests.
- Fixed a issue where the server was incorrect after using multiple instances.
- many many more issues has been fixed and improved.

##### 6.5.0

- hotfix ~ invalid set property has been fixed.

##### 6.4.1

- hotfix ~ a invalid key in login result has been fixed.

##### 6.3.0

- Added new property Image in Login result to get the image of a actor
- Fixed a issue with Piggy and Nebula properties

###### example Image
```cs
Login Result = await mspClient.Login("Username", "Password");

if(!Result.LoggedIn)
   return;

PictureBox.Image = Result.Image.Thumbnail;
PictureBox.Load(Result.Image.ThumbnailUrl);
```

##### 6.2.0

- Added a new method to send custom commands
- Added more properties in login result
- Fixed a issue where some properties does not been used in login result
- Some Changes and Improvements

###### example custom commands
```cs
await mspClient.SendCommand("MovieStarPlanet.WebService....", TicketRequired: true, new object[] { "test" });
```

##### 6.1.1

- Added in ServerParser class a method to convert server string into type
- Added in ServerParser class a method to get all servers

###### example ServerParser
```cs
Server S = ServerParser.ParseToServer("Germany");
```
```cs
foreach (var server in ServerParser.GetAllServer())
        Console.WriteLine(server.ToString());

```
