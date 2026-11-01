# XDC1

4 key osu!mania difficulty algorithm. Tuned on LeoBlackMT's benchmark (0.169 MAE) and etterna scores to avoid overfitting.

```sh
g++ -O2 -std=c++17 xdc1.cpp -o xdc1
./xdc1 [--rate R] [--graph] chart.osu
```

[MIT](LICENSE). If you want to use this algorithm in your project please ask me first (discord: thebagelofman) as I'd like to know where it's used.