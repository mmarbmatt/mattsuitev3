# MattSuite V3 - TradingView Indicator Suite

A comprehensive Pine Script indicator suite for TradingView that combines multiple advanced trading tools and analysis features in a single overlay indicator.

## 🚀 Features

### Core Indicators
- **Fair Value Gaps (FVG)** - Identifies bullish and bearish fair value gaps with strength analysis
- **Break of Structure (BOS)** - Detects structural breaks in price action
- **Change of Character (CHoCH)** - Identifies character changes in market structure
- **Order Blocks** - Bullish and bearish order block detection
- **Bollinger Bands** - Traditional and extended bands with multiple standard deviations
- **EMA 100** - 100-period Exponential Moving Average
- **High/Low Levels** - Daily, weekly, and monthly high/low tracking
- **Liquidation Levels** - Volume-based liquidation level detection
- **Session Highlighting** - Multi-market session visualization

### Visual Elements
- **Color Themes** - 6 pre-built color schemes for customization
- **Dynamic Candle Coloring** - Candles colored based on Bollinger Band distance
- **Session Background Highlighting** - Visual session start/end markers
- **Real-time Statistics** - Live session and volume data display

## 📊 Installation

1. Open TradingView and go to the Pine Editor
2. Copy the entire code from `oldms.txt`
3. Paste it into a new Pine Script
4. Click "Add to Chart"
5. Configure your preferred settings in the indicator settings panel

## ⚙️ Configuration Options

### Display Settings
| Setting | Default | Description |
|---------|---------|-------------|
| Display FVG | `true` | Show/hide Fair Value Gap detection |
| FVG Extension Length | `30` | Length of FVG lines in bars |
| Display timelines | `true` | Show/hide timeline elements |
| Display Lines | `true` | Show/hide order block lines |

### Technical Analysis Settings
| Setting | Default | Description |
|---------|---------|-------------|
| EMA Length | `100` | Period for Exponential Moving Average |
| BB Length | `20` | Period for Bollinger Bands calculation |
| BB Standard Deviation | `2.0` | Standard deviation multiplier for Bollinger Bands |
| Lookback Period | `50` | Bars to look back for high/low breaks |
| Line Length | `30` | Length of indicator lines in bars |

### Volume Analysis
| Setting | Default | Description |
|---------|---------|-------------|
| Volume Multiplier | `3.0` | Threshold for high volume detection |
| Lookback Period | `20` | Period for average volume calculation |
| Max Levels | `5` | Maximum liquidation levels to display |

### Color Customization
| Setting | Default | Description |
|---------|---------|-------------|
| Color Theme | `Default` | Pre-built color schemes |
| Bullish Order Block Color | `Green` | Color for bullish order blocks |
| Bearish Order Block Color | `Red` | Color for bearish order blocks |

## 🎨 Color Themes

Choose from 6 professionally designed color themes:

1. **Default** - Classic white/yellow theme
2. **Purple/Teal** - Purple and teal combination
3. **Ocean Blue** - Blue and navy maritime theme
4. **Forest Green** - Green and lime nature theme
5. **Sunset Orange** - Orange and yellow warm theme
6. **Monochrome** - Black, white, and gray minimal theme

## 📈 Indicator Explanations

### Fair Value Gaps (FVG)
- **Purpose**: Identify price inefficiencies in the market
- **Logic**: Detects 3-candle patterns where middle candle creates a gap
- **Strength Levels**:
  - Strong FVG: Strength > 0.5
  - Regular FVG: Strength between 0.2-0.5
  - Weak FVG: Filtered out (< 0.2)

### Break of Structure (BOS)
- **Purpose**: Identify significant structural breaks in price movement
- **Detection**: Compares current highs/lows with previous swing points
- **Display**: Horizontal lines at break levels

### Change of Character (CHoCH)
- **Purpose**: Detect shifts in market character and trend changes
- **Logic**: Uses ATR-based threshold to confirm significant character changes
- **Threshold**: 1.5x ATR for validation

### Order Blocks
- **Bullish Order Block**: Triggered when price breaks above recent highs
- **Bearish Order Block**: Triggered when price breaks below recent lows
- **Management**: Automatically removes old blocks when new ones form

### Liquidation Levels
- **Detection**: Based on high volume candles (3x average volume)
- **Management**: Keeps top 5 levels by volume
- **Removal**: Levels removed when price crosses through them

## 🕐 Session Analysis

The indicator tracks and highlights four major trading sessions:

### Session Times (UTC)
- **USA Session**: 13:30 - 20:00 (9:30 AM - 4:00 PM EST)
- **Euro Session**: 08:00 - 16:00 (9:00 AM - 5:00 PM CET)
- **Asia Session**: 00:00 - 08:00 (New daily session)
- **China Session**: 05:00 - 09:00 (1:00 PM - 5:00 PM CST)

### Session Features
- **Background Highlighting**: Different colors for session starts
- **Real-time Stats**: Volume delta and price change tracking
- **Alerts**: Optional alerts for session starts and ends

## 📊 Live Statistics Display

The indicator shows real-time information including:
- Current candle volume
- Session volume delta
- Session price change percentage
- Active trading sessions

## 🔔 Alerts

Built-in alert conditions for:
- USA Session start/end
- Euro Session start/end
- Asia Session start/end
- China Session start/end

## 💡 Usage Tips

### For Day Traders
1. Use FVG detection for entry/exit points
2. Monitor session starts for volatility
3. Watch order blocks for support/resistance

### For Swing Traders
1. Focus on BOS and CHoCH signals
2. Use daily/weekly high/low levels
3. Monitor liquidation levels for major moves

### For Scalpers
1. Enable all visual elements for maximum information
2. Use shorter timeframes (1m, 5m)
3. Focus on volume delta and session changes

## ⚠️ Important Notes

### Performance Considerations
- Some plots are disabled to stay under TradingView's 64-plot limit
- Code includes commented sections for additional features
- Optimize settings based on your timeframe and trading style

### Limitations
- Works best on liquid markets (Forex, major indices, crypto)
- Some features may be less effective on low-volume assets
- Session times are in UTC - adjust mentally for your timezone

## 🛠️ Troubleshooting

### Common Issues
1. **Too many plots error**: Some features are commented out to prevent this
2. **Slow performance**: Reduce lookback periods and max levels
3. **Lines not showing**: Check if "Display Lines" is enabled

### Optimization Tips
- Start with default settings and adjust gradually
- Use appropriate timeframes (works best on 1H and below)
- Consider disabling features you don't actively use

## 📝 Version History

**V3 Features:**
- Multi-session analysis
- Enhanced color theming
- Liquidation level detection
- Real-time statistics display
- Improved performance optimization

## 🤝 Support

For questions or suggestions regarding this indicator suite, please refer to the Pine Script documentation or TradingView's community forums.

---

*Disclaimer: This indicator is for educational and analysis purposes only. Always conduct your own research and risk management before making trading decisions.*
