Bravia Remote Control
============

Control your Sony Bravia TV using nodejs.

### One time setup
* Turn on your TV 
* Find your TV's IP address
* Execute the `demo.js` file
* If you're running this script for the first time, you will be asked to enter a 4-digit code shown on your TV
* Done! 


### Usage
```
bravia('192.168.1.100', function(client) {

  // List available commands
  client.getCommandNames(function(list) {
    console.log(list);
  });

  // Call a command
  client.exec('Netflix');

});

```

### Authentication
This library handles the authentication process with the TV, saving the generated cookie as a file that can be accessed in later executions. If you need to refresh the credentials for some reason, just remove any content of the `cookies.json` file.


### Available commands
The available commands may vary from model to model. I'm getting the following ones with the Sony Bravia KDL-50W805:

```PowerOff, Input, GGuide, EPG, Favorites, Display, Home, Options, Return, Up, Down, Right, Left, Confirm, Red, Green, Yellow, Blue, Num1, Num2, Num3, Num4, Num5, Num6, Num7, Num8, Num9, Num0, Num11, Num12, VolumeUp, VolumeDown, Mute, ChannelUp, ChannelDown, SubTitle, ClosedCaption, Enter, DOT, Analog, Teletext, Exit, Analog2, *AD, Digital, Analog?, BS, CS, BSCS, Ddata, PicOff, Tv_Radio, Theater, SEN, InternetWidgets, InternetVideo, Netflix, SceneSelect, Mode3D, iManual, Audio, Wide, Jump, PAP, MyEPG, ProgramDescription, WriteChapter, TrackID, TenKey, AppliCast, acTVila, DeleteVideo, PhotoFrame, TvPause, KeyPad, Media, SyncMenu, Forward, Play, Rewind, Prev, Stop, Next, Rec, Pause, Eject, FlashPlus, FlashMinus, TopMenu, PopUpMenu, RakurakuStart, OneTouchTimeRec, OneTouchView, OneTouchRec, OneTouchStop, DUX, FootballMode, Social```

### Disclaimer
This is 5am code, it might work in misterious ways, sorry! :D. This is an experimental and non-official library developed just for fun, I'm not affiliated with Sony in any way. This software is distributed under the Apache 2.0 License: http://www.apache.org/licenses/LICENSE-2.0