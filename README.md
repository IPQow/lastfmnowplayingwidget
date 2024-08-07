![Last.fm Now Playing Widget](https://github.com/IPQow/lastfmnowplayingwidget/blob/main/GitAssets/githubbannernp.png?raw=true)

# Last.fm Now Playing Widget

## Overview

The Last.fm Now Playing Widget is a dynamic widget built that displays your currently playing track from Last.fm in a visually engaging format for live stream viewers that changes size dynamically depending on the width of the song name to make sure that it shows the full song name. It fetches real-time data using the Last.fm API, allowing you to display the song that is currently playing in a nice and concise way.

> *This project is heavily inspired by Aiden Wallis and his original Spotify widget [aidenwallis/nowplaying](https://github.com/aidenwallis/nowplaying) but since he didn't release the Spotify portion of the code, I was stuck sharing his spotify api key with everyone else that was using the widget, and such the updates sometimes took a while as requests were being rate limited. This project was built on his principles that were used in his widget but the lastfm api integration was all developed by me and the rest of the widget. Side note: I didn't like the design of his widget, it got the work done but I didn't like the green and I wanted to customise it a bit to make it look more appealing*

*If anyone does decide to use this widget, please let me know by messaging me on discord @ipq or open an issue and let me know your stream link.*
*No particular reason, it would just be cool to know that someone is using this widget! :D*

## Built with

- **JavaScript**: The core functionality is written in vanilla JavaScript.
- **Last.fm API**: Fetches recent tracks from your Last.fm profile.

## Features

- **Multiple music providers**: As it uses lastfm, this means that it can track many platforms, like Spotify, YouTube Music, Tidal, Soundcloud, Deezer, and more.
- **Real-Time Updates**: Automatically updates to show the current track you're listening to on stream.
- **Smooth Transitions**: Animates the update of the song name and album cover when a new track starts playing.
- **Dynamic container**: Adjusts to make sure that the song name is always on the container (3rd screenshot below).
- **Easy Configuration**: Customize the username and API key via a separate `config.js` file.

## Setup

1. **Clone the repository:**

    ```bash
    git clone https://github.com/IPQow/lastfmnowplayingwidget
    cd lastfmnowplayingwidget
    ```

2. **Configure the widget:**

    Open the `config.js` file and update the following parameters:

    ```javascript
    export const config = {
    username: 'USERNAME',
    apikeylfm: 'APIKEY',
    };
    ```

    > To get a lastfm api key, create an api key on the [lastfm api key creation page](https://www.last.fm/api/account/create), or you can see your API keys at the [lastfm api accounts page](https://www.last.fm/api/accounts)

3. **Include the widget in your streaming software:**

    - Add a new browser source in OBS (or any streaming software).
    - Set the URL to the path where the `nowplaying.html` file is hosted or saved locally, like `file:///path/to/your/widget/nowplaying.html` *(e.g. file:///C:/Users/IPQow/Downloads/lastfmnowplayingwidget/nowplaying.html).*
    - Set the dimensions to a `Height: 70px` and `Width: 500px` *(260px is the default width but as the widget dynamically adjusts the size of the container to the width of the song, you should leave some room, I have it at 500 and it hasn't reached there but you can set it to whatever number you want)* .

## Screenshots

### Widget displaying currently playing song.
![Widget Open](https://github.com/IPQow/lastfmnowplayingwidget/blob/main/GitAssets/Widget.png?raw=true)


### Opening animation.
![Widget Opening](https://github.com/IPQow/lastfmnowplayingwidget/blob/main/GitAssets/Open.gif?raw=true)


### Dynamic container showcase to fit large song names.
![Dynamic container showcase](https://github.com/IPQow/lastfmnowplayingwidget/blob/main/GitAssets/Dynamic%20Container.gif?raw=true)


### Song changing.
![Song changing](https://github.com/IPQow/lastfmnowplayingwidget/blob/main/GitAssets/Song%20Change.gif?raw=true)


### Closing animation.
![Widget Closing](https://github.com/IPQow/lastfmnowplayingwidget/blob/main/GitAssets/Close.gif?raw=true)

## Usage

Once set up, the widget will automatically start displaying the current track from your Last.fm profile (Spotify). Your viewers will see the song title and album cover on your stream, keeping them in the loop with what you're listening to.

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests to enhance the widget's functionality or fix any bugs.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
