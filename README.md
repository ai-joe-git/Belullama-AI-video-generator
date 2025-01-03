# Belullama AI Video Generator

An automated YouTube video generation tool that creates professional videos from text scripts using AI and open-source technologies.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)

## 🎥 Features

- **Interactive Configuration Wizard**
  - Easy-to-use CLI interface
  - Guided setup process
  - Configuration saving/loading

- **AI-Powered Script Analysis**
  - Automatic keyword extraction
  - Content segmentation
  - Smart image description generation

- **Advanced Media Management**
  - Automatic media search and download
  - Rights-compliant content usage
  - Integration with Storyblocks API

- **Professional Video Effects**
  - Multiple transition types
  - Dynamic video compositing
  - Automated timing adjustment

- **Text-to-Speech Integration**
  - Multiple language support
  - Voice style customization
  - Speech-video synchronization

## 🛠️ Requirements

- Python 3.8 or higher
- Linux/Unix environment (WSL supported for Windows users)
- FFmpeg installed on your system
- Active Storyblocks API key
- Ollama installed locally

## 📦 Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/autoyoutube-generator.git
cd autoyoutube-generator
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install required packages:
```bash
pip install -r requirements.txt
```

4. Install FFmpeg:
```bash
# Ubuntu/Debian
sudo apt-get update
sudo apt-get install ffmpeg

# macOS
brew install ffmpeg

# Windows
# Download from https://ffmpeg.org/download.html
```

5. Install Ollama:
```bash
# Follow instructions at https://ollama.ai/
```

## ⚙️ Configuration

1. Create a `.env` file in the project root:
```env
STORYBLOCKS_API_KEY=your_api_key_here
```

2. Run the configuration wizard:
```bash
python src/main.py --config
```

## 🚀 Usage

1. Basic video generation:
```bash
python src/main.py
```

2. Using a saved configuration:
```bash
python src/main.py --load config.json
```

3. Advanced options:
```bash
python src/main.py --help
```

## 📝 Input Format

The script expects a text file with the following format:

```text
Title: Your Video Title
Duration: 5:00
Language: English

[Section 1]
Your script content here...

[Section 2]
More content here...
```

## 🎬 Output

- Generated videos are saved in the `output` directory by default
- Supported formats: MP4 (1080p, 720p, 480p)
- Auto-generated metadata file for YouTube upload

## 🔧 Advanced Configuration

### Transition Types
- Fade
- Slide
- Zoom
- Blur
- Crossfade

### Voice Styles
- Gender: Male/Female/Neutral
- Age: Young/Adult/Senior
- Style: Professional/Casual/Dynamic

### Quality Settings
```json
{
  "1080p": {
    "width": 1920,
    "height": 1080,
    "bitrate": "8000k"
  },
  "720p": {
    "width": 1280,
    "height": 720,
    "bitrate": "4000k"
  }
}
```

## 📁 Project Structure

```
autoyoutube-generator/
├── src/
│   ├── __init__.py
│   ├── main.py
│   ├── config.py
│   ├── media_manager.py
│   ├── script_analyzer.py
│   ├── transition_manager.py
│   ├── video_editor.py
│   └── voice_generator.py
├── tests/
├── docs/
├── output/
├── requirements.txt
├── setup.py
└── README.md
```

## 🧪 Testing

Run the test suite:
```bash
pytest tests/
```

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [MoviePy](https://zulko.github.io/moviepy/)
- [Ollama](https://ollama.ai/)
- [gTTS](https://gtts.readthedocs.io/)
- [Storyblocks](https://www.storyblocks.com/)


## ⚠️ Disclaimer

This tool is for educational purposes only. Ensure you have the right to use any content generated with this tool.
