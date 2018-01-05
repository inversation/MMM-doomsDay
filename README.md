# MMM-doomsDay

This module for the [MagicMirror](https://github.com/MichMich/MagicMirror) shows the number of days left to a specific date.

## Installation

  1\. Execute the following commands to install the module:

```bash
cd ~/MagicMirror/modules # navigate to module folder
git clone https://github.com/brobergp/MMM-doomsDay.git # clone this repository
```

  2\. Then, add the following into the `modules` section of your `config/config.js` file:

````javascript
{
    module: 'MMM-doomsDay',
    position: 'top_center', // This can be any of the regions, best results in center regions
    config: {
        doomsDay: "2018-02-23 24:00:00", // YYYY-MM-DD HH:MM:SS, Do not alter the time, just the date
        toWhat: "Leaving for Paris!",
        
        // See 'Configuration options' for more information.
    }
},
````


## customization

  Copy the code from the MMM-doomsDay.css to your own custom.css and change whatever you like about the font, color etc.
  Using the configuration options singular and plural you can change the language of day/days left.
  Using the configuration options showWeeks, singularW and pluralW you can change whether weeks are displayed, and if so the language of week/weeks left.

## Configuration options

The following properties can be configured:

| option | description |
| ------------- | ------------- |
| `doomsDay` | date and time as a string, the end day of the countdown, format is `YYYY-MM-DD HH:MM:SS`, default is `"2018-02-23 24:00:00"`, don't alter the hour, keep it at `24:00:00` |
| `updateInterval` | time between updates in ms, default is `60 * 60 * 1000` (1 hour) |
| `toWhat` | the title of your countdown event |
| `singular` | what it should say when it's only one day left, default is `Day Left` |
| `plural` | what it should say when it's more days left, default is `Days Left` |
| `singularW` | what it should say when there's only one week left, default is `Week` |
| `pluralW` | what it should say when it's more weeks left, default is `Weeks` |
| `present` | What it says when the day is finally here! |
| `timesUp`| What it says when the day has went and gone, default is `death and despair, your time is up.` |
| `showWeeks`| Determines whether weeks will also be shown. Set to `true` to display weeks, set to `false` to hide. Default is `false` |
