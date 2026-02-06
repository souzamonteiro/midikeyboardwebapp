# MIDI Keyboard Web App

A comprehensive browser-based MIDI keyboard application built with HTML5, CSS3, JavaScript, and the Tone.js library. This application provides a virtual piano keyboard with sound synthesis capabilities, MIDI device support, and various instrument options.

## Features

### 🎹 Core Functionality
- **Virtual Piano Keyboard**: Three-octave keyboard with touch/mouse support
- **Multiple Instrument Types**: 
  - Basic Synth
  - AM Synth
  - FM Synth
  - Duo Synth
  - Membrane Synth
  - Metal Synth
  - Pluck Synth
- **Real-time Audio Effects**: Adjustable reverb and volume controls
- **Note Sustain Control**: Customizable note duration
- **Octave Shifting**: Adjust keyboard octave range (Octaves 2-6)

### 🎛️ Controls & Interface
- **Audio Parameters**: Real-time adjustment of volume, reverb, and sustain
- **MIDI Device Support**: Connect and use external MIDI keyboards
- **Computer Keyboard Mapping**: Play using your computer keyboard (ASDFGHJ keys)
- **Touch Interface**: Fully responsive design for mobile devices
- **Visual Feedback**: Active notes are highlighted on the virtual keyboard

### 🔌 MIDI Integration
- Web MIDI API support for external MIDI devices
- Automatic device detection and connection
- Real-time MIDI message processing
- Visual indication of MIDI connection status

## Browser Compatibility

This application requires a modern browser with Web Audio API and (optionally) Web MIDI API support:

- **Chrome**: Full support (recommended)
- **Firefox**: Full support
- **Safari**: Limited MIDI support
- **Edge**: Full support

*Note: iOS devices have limitations with Web MIDI API*

## Quick Start

1. **Open the Application**: Load `midi_keyboard.html` in a modern web browser
2. **Initialize Audio**: Click "Start Audio Engine" to begin (required by browser security policies)
3. **Start Playing**: 
   - Click/tap on the virtual keyboard
   - Use computer keyboard keys (A-K for white keys, W-E-T-Y-U for black keys)
   - Connect an external MIDI keyboard via USB

## Usage Guide

### Virtual Keyboard
- **Mouse/Touch**: Click or tap keys to play notes
- **Mobile**: Touch and hold for sustained notes, swipe horizontally to navigate keyboard
- **Visual Feedback**: Active notes glow with orange/yellow highlights

### Computer Keyboard Mapping
```
White Keys: A S D F G H J K L
Black Keys: W E T Y U
```

### MIDI Device Connection
1. Click "Connect MIDI Device" button
2. Select your MIDI device from the list
3. Play your external MIDI keyboard - notes will trigger on the virtual keyboard

### Audio Controls
- **Instrument Type**: Select from 7 different synthesizer types
- **Volume**: Adjust output volume (-60dB to 0dB)
- **Reverb**: Control reverb effect intensity (0.0 to 1.0)
- **Sustain**: Set note duration (0.1 to 2.0 seconds)

## Technical Details

### Architecture
- Built with vanilla JavaScript (ES6+)
- Uses Tone.js for audio synthesis and processing
- Implements Web Audio API for sound generation
- Supports Web MIDI API for external device integration

### Audio Pipeline
```
Synth → Reverb → Volume → Output
```

### Polyphony
- Supports up to 8 simultaneous notes
- Automatic voice management
- Smooth note transitions

## File Structure
```
midi_keyboard.html      # Main application file
```

## Dependencies
- **Tone.js** (v14.8.49): Audio synthesis library
- **Font Awesome** (v6.4.0): UI icons
- Modern browser with Web Audio API support

## Development

### Customization
The application is structured for easy modification:
- Instrument parameters can be adjusted in the `initInstrument()` method
- Keyboard mapping is configurable in the `initComputerKeyboard()` method
- UI styling is contained in the `<style>` section

### Extending Functionality
- Add new instruments by extending the synth selection
- Implement additional effects by expanding the audio pipeline
- Customize MIDI handling for special use cases

## Troubleshooting

### Common Issues
- **No Sound**: Ensure you've clicked "Start Audio Engine" and allow browser audio permissions
- **MIDI Not Working**: Check browser compatibility and device drivers
- **Mobile Limitations**: Some mobile browsers have reduced MIDI support

### Performance Tips
- Close other audio-intensive applications
- Use fewer polyphonic voices if experiencing latency
- Disable effects for better performance on older devices

## License

This project is provided as-is under de Apache 2.0 license. Tone.js is licensed under MIT. Font Awesome is licensed under the Font Awesome Free License.
