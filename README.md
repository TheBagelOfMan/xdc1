# XDC1

4 key osu!mania difficulty algorithm. Tuned on LeoBlackMT's benchmark (0.169 MAE on the set it was tuned on and 0.168 MAE held out) and etterna scores to avoid overfitting. Part of a larger project.

Official Results for the benchmark are:
- RC, all rated rows: 0.180 MAE.
- RC, expected 10.5 to 18.5: 0.176 MAE.
- RC, expected 10.5 to 18.5, no marathon course: 0.173 MAE. (XDC1 consistently overrates marathons on average by +0.41 dan due to stamina)
- LN: 0.806 MAE. (XDC1 is not fitted correctly to the benchmarks LN scale as a deliberate design choice, other algorithms rate LNs too high imo)

```sh
g++ -O2 -std=c++17 xdc1.cpp -o xdc1
./xdc1 [--rate R] [--graph] chart.osu
```

[MIT](LICENSE). If you want to use this algorithm in your project please ask me first (discord: thebagelofman) as I'd like to know where it's used.

Algorithm design and equations by TheBagelOfMan, translated into C++ by Claude. Then further reviewed and tuned by TheBagelOfMan.
