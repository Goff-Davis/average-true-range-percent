# Average True Range Percent (ATRP)

A Pine Script v6 indicator for TradingView that expresses Average True Range (ATR) as a percentage of price instead of an absolute value.

Raw ATR is denominated in price, so it can't be used to compare volatility across instruments trading at different price levels — a $10 stock and a $400 stock can have very different ATR values even when they're moving by the same relative amount. Dividing ATR by close (×100) normalizes it into a percentage, making volatility comparable across any symbol, timeframe, or asset class.

## Settings

- **ATR Lookback Period** — number of bars used in the smoothing calculation (default 14).
- **ATR Smoothing** — RMA, SMA, EMA, or WMA (default RMA, the classic Wilder smoothing used by standard ATR).
- **Calculation**
  - **ATR Timeframe** — calculate ATR on the chart's own timeframe, or pin it to a fixed timeframe (ticks, seconds, minutes, hours, days, weeks, or months) regardless of the chart resolution you're viewing.
  - **Wait for Timeframe Closes** — only relevant when ATR Timeframe differs from the chart. Off: the value updates live with the still-forming higher-timeframe bar (can repaint on historical reloads). On: the value only updates once the selected timeframe's bar has closed (no repainting, one-bar lag).

The result is plotted as a thin red line in a separate pane below the chart.

## Installation

1. Open TradingView and create a new indicator in the Pine Editor.
2. Copy the contents of [`atrp.pine`](atrp.pine) into the editor.
3. Click **Add to Chart**.

## License

[MIT](LICENSE.md)
