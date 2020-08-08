# VideoControls
React-native-media-controls without grey band
To make the code work run:
#  npm install

Changes done to remove the band:
go to the file ./react-native-media-controls/dist/react-native-media-controls.cjs.development.js 

there is a variable defined name as containerBackgroundColor,
 set it to "transparent".

var containerBackgroundColor = "transparent";

# optional slider

# step 1:
go to the file ./react-native-media-controls/dist/MediaControls.d.ts
```
export declare type Props = {
    duration: number;
    fadeOutDelay?: number;
    isFullScreen: boolean;
    isLoading: boolean;
    mainColor: string;
    onFullScreen?: (event: GestureResponderEvent) => void;
    onPaused: (playerState: PLAYER_STATES) => void;
    onReplay: () => void;
    onSeek: (value: number) => void;
    onSeeking: (value: number) => void;
    playerState: PLAYER_STATES;
    progress: number;
    showOnStart?: boolean;
    showSlider?: boolean; //=====> add this 
};

```
# Step 2: 
replace react-native-media-controls.cjs.development.js in react-native-media-controls with ./react-native-media-controls/dist/react-native-media-controls.cjs.development.js

# step 3: 
control slider with showSlider showSlider props
```
   <MediaControls
        {...props}
        showSlider={false}
       />
```


