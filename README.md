# Simple Solitaire Collection - Modernized

[![License](https://img.shields.io/badge/license-GPLv3%2B-brightgreen.svg)](LICENSE.txt)
[![Platform](https://img.shields.io/badge/platform-Android-blue.svg)](https://developer.android.com)
[![API](https://img.shields.io/badge/API-16%2B-brightgreen.svg?style=flat)](https://android-arsenal.com/api?level=16)

A modernized fork of the Simple Solitaire Collection, updated to work with current Android development tools and practices.

## 🆕 What's New in This Fork

This is an **actively maintained fork** of the original Simple Solitaire project, which was archived in February 2024. This version includes:

- ✅ **AndroidX Migration** - Updated from deprecated Support Library to AndroidX
- ✅ **Modern Build Tools** - Gradle 8.4 and Android Gradle Plugin 8.1.4
- ✅ **Current Android Support** - Target SDK 34 (Android 14)
- ✅ **Build Compatibility** - Works with latest Android Studio
- ✅ **Maintained Dependencies** - Updated to current library versions
- 🔜 **New Games Coming** - Brisca (Spanish card game) and more planned

## 📱 About the Game

Simple Solitaire Collection is a lightweight, fully-featured solitaire game collection for Android with **no ads, no tracking, and completely free**.

### Currently Includes 17 Different Games:
- AcesUp
- Calculation
- Canfield
- Forty&Eight
- FreeCell
- Golf
- Grandfather's Clock
- Gypsy
- Klondike
- Mod3
- Napoleon's Tomb
- Pyramid
- SimpleSimon
- Spider
- TriPeaks
- Vegas
- Yukon

## ✨ Features

- **Highly Customizable**: 6 card sets, 12 card backgrounds, 6 background colors
- **Adjustable Difficulty**: Configure settings for Klondike, Spider, and Golf
- **Automatic Saving**: Game saves automatically when you pause or close
- **High Scores**: Track your best performances
- **Undo Function**: Take back up to 20 moves
- **Hint System**: Get up to 3 move suggestions
- **Left-Handed Mode**: Mirror card positions for left-handed play
- **Landscape Support**: Play in portrait or landscape mode
- **Tablet Optimized**: Great experience on larger screens

## 🚀 Getting Started

### For Users

#### Download & Install
1. Download the latest APK from [Releases](../../releases)
2. Enable "Install from Unknown Sources" on your Android device
3. Install the APK
4. Enjoy!

**Requirements:**
- Android 4.1 (API 16) or higher
- ~20MB storage space

### For Developers

#### Prerequisites
- Android Studio Hedgehog (2023.1.1) or newer
- JDK 17 or higher
- Android SDK with API 34

#### Building from Source

1. **Clone the repository:**
   ```bash
   git clone https://github.com/gjenkins20/Simple-Solitaire.git
   cd Simple-Solitaire
   ```

2. **Open in Android Studio:**
   - File → Open → Select the Simple-Solitaire folder
   - Wait for Gradle sync to complete

3. **Build and run:**
   ```bash
   # Build debug APK
   ./gradlew assembleDebug
   
   # Install on connected device
   ./gradlew installDebug
   
   # Or click the Run button (▶️) in Android Studio
   ```

4. **Build release APK:**
   ```bash
   ./gradlew assembleRelease
   # Output: app/build/outputs/apk/release/app-release.apk
   ```

## 🛠️ Technical Details

### Modernization Changes

This fork includes significant updates to bring the codebase up to modern Android standards:

#### Build System
- **Gradle**: Updated from 6.x to 8.4
- **Android Gradle Plugin**: Updated from 3.x to 8.1.4
- **Build Features**: Added modern namespace and buildConfig declarations

#### AndroidX Migration
- All `android.support.*` imports migrated to `androidx.*`
- Updated XML layouts to use AndroidX widget classes
- Migrated to Material Design Components
- Updated to AndroidX-compatible libraries

#### SDK Versions
- **Min SDK**: 16 (Android 4.1 Jelly Bean)
- **Target SDK**: 34 (Android 14)
- **Compile SDK**: 34

#### Key Dependencies
```gradle
androidx.appcompat:appcompat:1.6.1
com.google.android.material:material:1.9.0
androidx.legacy:legacy-support-v4:1.0.0
androidx.cardview:cardview:1.0.0
```

### Project Structure
```
app/src/main/
├── java/de/tobiasbielefeld/solitaire/
│   ├── classes/          # Core game classes
│   ├── games/            # Individual game implementations
│   ├── helper/           # Utility classes
│   └── ui/               # User interface activities
├── res/
│   ├── drawable/         # Vector drawables and backgrounds
│   ├── drawable-nodpi/   # Card graphics and assets
│   ├── layout/           # XML layouts
│   ├── values/           # Strings, colors, styles
│   └── xml/              # Preferences
└── AndroidManifest.xml
```

## 🎮 Adding New Games

Interested in adding a new solitaire game? Check out `DummyGame.java` in the `games/` directory - it's a well-commented template that shows you exactly what you need to implement.

### Upcoming: Brisca (Spanish Card Game)
We're currently working on adding Brisca, a popular Spanish trick-taking card game. Stay tuned!

## 🌍 Translations

Currently available in:
- English
- Esperanto
- Finnish
- French
- Italian
- Japanese
- Polish
- Portuguese
- Turkish
- Ukrainian

Want to add your language? Contributions welcome!

## 📄 License

This project is licensed under the **GPL-3.0 License** - see the [LICENSE.txt](LICENSE.txt) file for details.

```
Copyright (C) 2016-2024 Tobias Bielefeld (original)
Copyright (C) 2026 Greg Jenkins (modernization)

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.
```

### Asset Licenses

- **Poker card theme**: Vectorized Playing Cards 2.0 - LGPL 3.0
- **Other card themes**: CC0 License (from Pixabay)
- **Material Design icons**: Apache 2.0 License (Google)
- **Sounds**: CC0 License (from freesound.org)

## 🙏 Credits

### Original Author
**Tobias Bielefeld** - Original Simple Solitaire Collection
- Original Repository: [TobiasBielefeld/Simple-Solitaire](https://github.com/TobiasBielefeld/Simple-Solitaire) (archived)
- Contact: tobias.bielefeld@gmail.com

### Modernization
**Greg Jenkins** - AndroidX migration and ongoing maintenance
- Fork Repository: [gjenkins20/Simple-Solitaire](https://github.com/gjenkins20/Simple-Solitaire)

### Translation Contributors
- Esperanto & Polish: verdulo
- French: romainhk and cicithesquirrel
- Japanese: naofum
- Finnish: winjar
- Turkish: sekmenhuseyin
- Italian: imko92
- Portuguese: Alexandre Parente
- Ukrainian: olexn

### Libraries Used
- [AmbilWarna](https://github.com/yukuku/ambilwarna) - Color picker (Apache 2.0)
- [PagerSlidingTabStrip](https://github.com/astuetz/PagerSlidingTabStrip) - Tab navigation (Apache 2.0)

## 🤝 Contributing

Contributions are welcome! Whether it's:
- 🐛 Bug fixes
- ✨ New features
- 🎨 UI improvements
- 🌍 Translations
- 📖 Documentation

### How to Contribute

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Make your changes
4. Test thoroughly
5. Commit your changes (`git commit -m 'Add amazing feature'`)
6. Push to the branch (`git push origin feature/amazing-feature`)
7. Open a Pull Request

Please ensure:
- Code follows existing style conventions
- All games still work correctly
- New features are documented
- Commit messages are clear and descriptive

## 🐛 Bug Reports

Found a bug? Please [open an issue](../../issues) with:
- Android version
- Device model
- Steps to reproduce
- Expected vs actual behavior
- Screenshots if applicable

## 📮 Contact

- **Repository Issues**: [GitHub Issues](../../issues)
- **Original Author**: tobias.bielefeld@gmail.com
- **Fork Maintainer**: Available through GitHub

## 🗺️ Roadmap

### Completed
- ✅ AndroidX migration
- ✅ Gradle modernization
- ✅ Android 14 compatibility
- ✅ Build with latest tools

### In Progress
- 🔄 Adding Brisca (Spanish card game)
- 🔄 Code quality improvements
- 🔄 Enhanced documentation

### Planned
- 📋 Additional card games
- 📋 Custom card deck creator
- 📋 Statistics tracking improvements
- 📋 Achievement system
- 📋 Cloud save sync (optional)

## ⭐ Show Your Support

If you find this project useful, please consider:
- ⭐ Starring the repository
- 🐛 Reporting bugs
- 💡 Suggesting features
- 🤝 Contributing code
- 📢 Sharing with others

## 📊 Project Status

**Status**: Actively Maintained ✅

This is a maintained fork of the original archived project. We welcome contributions and are committed to keeping this working with modern Android development tools.

---

**Original Project**: [TobiasBielefeld/Simple-Solitaire](https://github.com/TobiasBielefeld/Simple-Solitaire) (archived February 2024)

**This Fork**: Modernized, maintained, and open to contributions!
