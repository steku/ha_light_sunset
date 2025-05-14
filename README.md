## Parabolic Sunset

This is a complementary blueprint to my [Parabolic Sunrise Alarm](https://community.home-assistant.io/t/simple-light-wake-up-alarm-with-parabolic-sunrise-effect/673747).

This package contains 2 components. The first component is a script that can be executed many times in series to change the rates of the 2 main settings, color temperature in kelvin and brightness. By running it many times in series you get get a more parabolic effect. It does not use parabolic equasions because I've found that I like having more control over how the light dims. I added this feature because I could visually detect changes in brightness more at lower values.

The second component is an automation that executes the script 3 times in series with different values for each execution. 

If you turn off the light at any point while the script/automation is running, the script and blueprint will end and the `Post Actions` will NOT be run.

The script also allows for defining how long to take to get from start to finish values and how many steps per minute to take to get there. The script will also turn off the light and run the `Post Actions` after the `Light Timeout` period. Setting this value to 0 will disable the timeout, and `Post Actions` will be run immediately.

I would use this script as I'm going to bed. This may vary from night to night so I've made the trigger a button or switch. I have a button that turns on my lamp beside my main switches and I actuall trigger this manually with that button, so not using the trigger at all. At a certain time of day, the button will run this automation instead of just turning on the lamp.

## Installation
1. Import the script blueprint
1. Create a script from the script blueprint (Only needs to be done once. Can be reused in many automations)
1. Import the automation blueprint
1. Create the automation from the automation blueprint and use the script created above in the automation