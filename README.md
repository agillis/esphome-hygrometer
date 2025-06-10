I built this using SquareLine Studio and the SquareLine to ESPHome converter. It was a fast build due the the simplicty of Squarline Studio.

Step one is to create a secrets.yaml. This is what mine looks like 

```
wifi_ssid: "FBIvan05"
wifi_password: "VerySeceret!"
latitude: 38.897957
longitude: -77.036560
```

Next install the Squareline to ESPhome libary, the LVGL ESPhome libary and the libary for this screen.

```
git clone https://github.com/gpambrozio/SquarelineToEsphome.git
git clone https://github.com/agillis/esphome-modular-lvgl-buttons.git
git clone https://github.com/agillis/esphome-hygrometer.git
uv run ./SquarelineToEsphome/squareline_to_esphome ./esphome-hygrometer/Squareline_files/hygrometer/hydro.spj -o ./squareline_generated.yaml
```

You can test your code using SDL on a PC or mac. Lot of info in that here https://esphome.io/components/display/sdl.html

```
cp esphome-hygrometer/SDL-SquarelineToEsphome-base.yaml .
esphome run SDL-SquarelineToEsphome-base.yaml
```
