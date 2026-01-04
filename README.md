# AAC Row/Column Scanner

A microphone-controlled Augmentative and Alternative Communication (AAC) device designed for ALS patients and individuals with limited mobility. Uses sound-triggered scanning to enable communication without physical touch.

## Quick Start

### iPhone/iPad Setup (Recommended)

1. **Open in Safari**: Visit https://mbergmann.github.io/aac_scanner
2. **Allow Microphone**: Tap "Allow" when prompted for microphone access
3. **Add to Home Screen** (Important for full-screen app experience):
   - Tap the Share button (square with arrow)
   - Scroll down and tap "Add to Home Screen"
   - Tap "Add"
4. **Launch from Home Screen**: Open the app from your home screen (not Safari)
   - This removes the Safari URL bar and gives you full screen
   - Microphone works reliably in this mode

### Using the App

1. The scanner starts automatically
2. Make any sound to trigger selection:
   - First sound: Select a row (blue highlight)
   - Second sound: Select a cell (orange highlight)
3. Adjust settings using the ⚙️ button
4. **Use AirPods, headphones, or Bluetooth microphone** for best performance
   - Built-in iPhone speaker and mic can interfere with each other
   - Built-in mic is not sensitive enough for reliable triggering

## Features

- **Microphone Control**: Trigger selections using any sound (voice, clicking, tapping)
- **Row/Column Scanning**: Two-step selection process for accuracy
- **Multiple Boards**: Letters, Needs, and Food communication boards
- **Word Prediction**: Autocomplete suggestions automatically loaded from curated word list
- **Speech Synthesis**: Text-to-speech output for selected words
- **Visual Feedback**: Glow effects respond to microphone volume levels
- **Pause on Sound**: Scanning pauses when sound is detected for easier targeting
- **Settings Persistence**: Your preferences are automatically saved
- **Mobile Optimized**: Works on tablets and phones with touch support

## Settings

### Scan Speed
- **Row scan speed**: How fast rows are highlighted (600-2500ms)
- **Column scan speed**: How fast columns are highlighted (500-2000ms)

### Microphone Sensitivity
- **Pause threshold**: Volume level that pauses scanning (0.05-30)
- **Trigger threshold**: Volume level that triggers selection (0.05-30)
- Lower values = more sensitive

**Tip**: Set pause threshold lower than trigger threshold for best control

## Communication Boards

### Letters Board
- Frequency-optimized letter layout (E, T, A, O, I, N most accessible)
- Word autocomplete in top row
- Common shortcuts: YES, NO, CARETAKER

### Needs Board
- Essential needs: water, bathroom, phone, tired
- Emotions: thank you, sorry, sad, grateful, scared, love
- Commands: more, less, stop, go, wait, now, later

### Food Board
- Common foods organized by category
- Proteins, vegetables, fruits, beverages
- Texture options: straw, ice cream, pudding

## Browser Compatibility

**Recommended**: Chrome, Edge, Safari (iOS 14.5+)

**Known Issues**:
- Chrome may require `speechSynthesis.resume()` workaround (already implemented)
- iOS Safari requires user gesture to start microphone (tap mic button)
- Firefox has limited speech synthesis voice support

## Customization

### Adjusting Colors
Edit CSS variables in the `<style>` section:
```css
:root {
  --bg: #000;           /* Background color */
  --fg: #fff;           /* Text color */
  --hlBorder: rgba(0,150,255,1); /* Highlight color */
}
```

### Modifying Grids
Edit the `GRID_LETTERS`, `GRID_NEEDS`, or `GRID_FOOD` arrays in the JavaScript section.

## Technical Details

- **No server required**: Runs entirely in the browser
- **Privacy**: All processing happens locally, no data sent to servers
- **Storage**: Settings saved to browser localStorage
- **Audio**: Uses Web Audio API for microphone input
- **Speech**: Uses Web Speech API for text-to-speech

## Accessibility

- Touch-friendly interface with large targets
- High contrast design for visibility
- Visual feedback for all interactions
- Keyboard support (Space/Enter keys)
- Screen reader compatible (ARIA labels)

## Requirements

- Modern web browser with:
  - Web Audio API support
  - Web Speech API support
  - Microphone access
- Microphone (built-in or external)
- Optional: `words_freq.txt` for word prediction (see Customization section)

## Troubleshooting

### Microphone not working
- Check browser permissions (Settings → Privacy → Microphone)
- Try refreshing the page
- On iOS: Tap the mic button to activate

### Speech not working
- Check system volume
- Try a different browser (Chrome recommended)
- Some browsers require user interaction before speech works

### Scanning too fast/slow
- Adjust scan speed in settings
- Default: 1500ms for rows, 1500ms for columns

### Trigger too sensitive/insensitive
- Adjust trigger threshold in settings
- Lower = more sensitive
- Test with volume bar visualization

## Credits

Created for ALS patients and caregivers.

Built with AI assistance (Amazon Q Developer).

## License

MIT License - See LICENSE file for details

## Version

v0.1 - Initial release

## Contributing

Contributions welcome! Please feel free to submit issues or pull requests.

## Support

For questions or support, please open an issue on GitHub.
