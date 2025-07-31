### Normalisasi Data

#### a. Min-max normalization
Min-max normalization mengubah data sehingga nilainya berada di antara 0 dan 1 berdasarkan rumus:
\[ x' = \frac{x - x_{\text{min}}}{x_{\text{max}} - x_{\text{min}}} \]

Diberikan data: \(20, 20, 24, 25, 25, 30, 32, 34, 40\)
- \(x_{\text{min}} = 20\)
- \(x_{\text{max}} = 40\)

Mari kita hitung nilai normalisasi untuk setiap data:

\[
\begin{array}{|c|c|}
\hline
x & x' = \frac{x - 20}{40 - 20} \\
\hline
20 & \frac{20 - 20}{40 - 20} = 0 \\
20 & \frac{20 - 20}{40 - 20} = 0 \\
24 & \frac{24 - 20}{40 - 20} = \frac{4}{20} = 0.2 \\
25 & \frac{25 - 20}{40 - 20} = \frac{5}{20} = 0.25 \\
25 & \frac{25 - 20}{40 - 20} = \frac{5}{20} = 0.25 \\
30 & \frac{30 - 20}{40 - 20} = \frac{10}{20} = 0.5 \\
32 & \frac{32 - 20}{40 - 20} = \frac{12}{20} = 0.6 \\
34 & \frac{34 - 20}{40 - 20} = \frac{14}{20} = 0.7 \\
40 & \frac{40 - 20}{40 - 20} = 1 \\
\hline
\end{array}
\]

#### b. Z-score normalization
Z-score normalization mengubah data berdasarkan mean (\(\mu\)) dan standar deviasi (\(\sigma\)) dengan rumus:
\[ z = \frac{x - \mu}{\sigma} \]

Langkah pertama adalah menghitung mean dan standar deviasi dari data:
- Mean (\(\mu\)): \(\mu = \frac{20 + 20 + 24 + 25 + 25 + 30 + 32 + 34 + 40}{9} = \frac{250}{9} \approx 27.78\)

- Standar deviasi (\(\sigma\)):
\[
\sigma = \sqrt{\frac{(20 - 27.78)^2 + (20 - 27.78)^2 + (24 - 27.78)^2 + (25 - 27.78)^2 + (25 - 27.78)^2 + (30 - 27.78)^2 + (32 - 27.78)^2 + (34 - 27.78)^2 + (40 - 27.78)^2}{9}}
\]
\[
\sigma \approx \sqrt{\frac{60.77 + 60.77 + 14.29 + 7.74 + 7.74 + 4.94 + 18.05 + 37.75 + 149.38}{9}} \approx \sqrt{\frac{361.43}{9}} \approx \sqrt{40.16} \approx 6.34
\]

Mari kita hitung nilai Z-score untuk setiap data:

\[
\begin{array}{|c|c|}
\hline
x & z = \frac{x - 27.78}{6.34} \\
\hline
20 & \frac{20 - 27.78}{6.34} \approx -1.23 \\
20 & \frac{20 - 27.78}{6.34} \approx -1.23 \\
24 & \frac{24 - 27.78}{6.34} \approx -0.60 \\
25 & \frac{25 - 27.78}{6.34} \approx -0.44 \\
25 & \frac{25 - 27.78}{6.34} \approx -0.44 \\
30 & \frac{30 - 27.78}{6.34} \approx 0.35 \\
32 & \frac{32 - 27.78}{6.34} \approx 0.67 \\
34 & \frac{34 - 27.78}{6.34} \approx 0.98 \\
40 & \frac{40 - 27.78}{6.34} \approx 1.93 \\
\hline
\end{array}
\]

### Tabel Hasil Normalisasi

\[
\begin{array}{|c|c|c|}
\hline
x & \text{Min-max normalization (x')} & \text{Z-score normalization (z)} \\
\hline
20 & 0 & -1.23 \\
20 & 0 & -1.23 \\
24 & 0.2 & -0.60 \\
25 & 0.25 & -0.44 \\
25 & 0.25 & -0.44 \\
30 & 0.5 & 0.35 \\
32 & 0.6 & 0.67 \\
34 & 0.7 & 0.98 \\
40 & 1 & 1.93 \\
\hline
\end{array}
\]
