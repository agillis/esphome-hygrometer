I built this using SquareLine and the SquareLine to ESPHome converter. It was a fast build do the the simplicty of Squarline.

Install instructions

```
git clone https://github.com/gpambrozio/SquarelineToEsphome.git
git clone https://github.com/agillis/esphome-modular-lvgl-buttons.git
git clone https://github.com/agillis/esphome-hygrometer.git
uv run ./SquarelineToEsphome/squareline_to_esphome ./esphome-hygrometer/Squareline_files/hygrometer/hydro.spj -o ./squareline_generated.yaml 
cp esphome-hygrometer/SDL-SquarelineToEsphome-base.yaml .
esphome run SDL-SquarelineToEsphome-base.yaml
```
