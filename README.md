# Compound Interest Calculator

An interactive compound-interest visualizer in a single self-contained HTML file.
No build step, no dependencies, no tracking.
Open `index.html` in any browser, or use the live page linked below.

**[Live demo](https://jay37mack37.github.io/compound-interest-calculator/)**

## Features

- **Rate basis toggle** - interpret the rate as either a nominal annual rate (split across periods) or a per-period rate (the full rate every compounding step).
- **Compounding frequency** - annually, semi-annually, quarterly, monthly, 252 trading days, daily, or continuous.
- **Reinvested vs withdrawn** - the growth curve is plotted against a simple-interest twin, so the gap shows exactly what reinvesting the interest buys you.
- **Live effective APY** - shown next to the frequency control, so you always see what the frequency is actually worth.
- **Optional monthly contributions.**
- **Interactive chart** - hover or tap any point to read the balance, interest earned, and the reinvestment gap.
- Light and dark themes, following your system preference.

## Why the two rate bases matter

At a fixed nominal 3% annual rate, compounding daily instead of annually is a tiny difference:
it only lifts the effective yield from 3.0000% to 3.0453%, about +$24 over 20 years on $1,500.

If instead 3% is a per-period rate, frequency dominates:
3% every trading day over 252 days is `1.03^252`, roughly a 1,718x multiple.
That per-period mode is a sensitivity tool, not a forecast.
No real strategy sustains an edge like that indefinitely.

## Math

- Per year (nominal), discrete: `A = P(1 + r/n)^(nt)`
- Per year (nominal), continuous: `A = Pe^(rt)`
- Per period: `A = P(1 + r)^(nt)`

Figures are nominal and not inflation-adjusted, and assume the rate holds every period.

## License

MIT
