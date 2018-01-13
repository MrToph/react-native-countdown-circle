[![license](https://img.shields.io/github/license/mashape/apistatus.svg)]()
[![Version](https://img.shields.io/npm/v/react-native-countdown-circle.svg)](https://www.npmjs.com/package/react-native-countdown-circle)
[![npm](https://img.shields.io/npm/dt/react-native-countdown-circle.svg)](https://www.npmjs.com/package/react-native-countdown-circle)
[![Twitter Follow](https://img.shields.io/twitter/follow/cmichelio.svg?style=social&label=Follow)](https://twitter.com/cmichelio)

# React Native Countdown Circle

![React Native Countdown Circles](/README/featured.gif?raw=true "React Native Countdown Circles")

## Features

* Custom colors
* Custom size and border radius
* Light-weight: No other dependencies besides `react-native`
* Performant and Smooth: Uses React Native's [`Animated`](https://facebook.github.io/react-native/docs/animations.html) library

## Installation

`yarn add react-native-countdown-circle`

or

`npm install --save react-native-countdown-circle`

## Usage

```javascript
import CountdownCircle from 'react-native-countdown-circle'

render() {
    return (
        <CountdownCircle
            seconds={10}
            radius={30}
            borderWidth={8}
            color="#ff003f"
            bgColor="#fff"
            textStyle={{ fontSize: 20 }}
            onTimeElapsed={() => console.log('Elapsed!')}
        />
    )
}
```

## Props
| Name | Description | Type | Required | Default Value |
| :--- | :----- | :--- | :---: | :---: |
| seconds | The seconds to count down from | Number | ✓ |  |
| radius | The radius in `px` of the component (including border) | Number | ✓ |  |
| borderWidth | The border width in `px` | Number | ✓ |  |
| color | The border color | String |  | ![#f00](https://placehold.it/15/f00/000000?text=+) `'#f00'` |
| shadowColor | The background color of the border | String |  | ![#999](https://placehold.it/15/999/000000?text=+) `'#999'` |
| bgColor | The inner background color of the component  | String |  | ![#e9e9ef](https://placehold.it/15/e9e9ef/000000?text=+) `'#e9e9ef'` |
| containerStyle | The custom styling which will be applied to the container of the Text component | Style |  | `null` |
| textStyle | The custom styling which will be applied to the Text component | Style |  | `null` |
| updateText | A function used to display a different text inside this component. Is called after every second, with the number of _elapsed_ seconds, and the _total_ seconds | func | | ` (elapsedSecs, totalSecs) => (totalSecs - elapsedSecs).toString()` |
| onTimeElapsed | A function being called when the countdown is over | func |  | ` () => null` |

> Note: Setting the `seconds` prop to a different value restarts the timer with that new value.

## Author

[Christoph Michel](http://cmichel.io)

## Implementation Details

[React Native Progress Circle](http://cmichel.io/react-native-progress-circle)

## License

MIT
