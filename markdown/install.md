# Installing Dependencies

1. On Mac, run:
```bash
brew install portaudio ffmpeg
```
(on Linux, replace `brew` with `apt-get`)

2. _(Optional):_ create a new virtual environment

3. Clone the repository, either by downloading the files
from GitHub or by running:
```bash
git clone https://github.com/shakedzy/companion.git
```

4. From the main `companion` directory, run:
```bash
pip install -r requirments.txt
```


# Configuration
Rname the file `config.template` to `config.yml`, and fill in the details below:

* `title`: Will appear at the top of the application
* `model`:
  * `name`: The OpenAI chat model to be used. See [OpenAI API reference](https://platform.openai.com/docs/api-reference/chat) for list of options
  * `temperature`: What sampling temperature to use, between 0 and 2. Higher values like 0.8 will make the output more random, while lower values like 0.2 will make it more focused and deterministic
* `user`:
  * `name`: Your name
  * `image`: A URL to your profile image. Can be relative or full
* `bot`:
  * `name`: The bot name. You can refer to the tutor by this name
  * `image`: A URL which will function as the tutor's profile image. Can be relative or full
* `language`:
  * `native`: Your native language. ISO-639 format (i.e. "en", "fr", ...)
  * `learning`: The language you with the tutor to speak. ISO-639 format
  * `level`: Your level of the language you wish to learn. Can be specific (like "DELF A1.2" in French) or less specific, like "intermediate"
* `watson`:
  * `url`: your Watson URL
  * `voice`: the tutor's voice (see [Watson documentation](https://cloud.ibm.com/apidocs/text-to-speech?code=python#listvoices) for list of voices)
* `behavior`:
  * `auto_send_recording`: If `true`, text transcribed from your recordings will be sent directly to the bot. It is recommended
to use this option only when the chances for incorrect transcribing of your recordings are low. When set
to `false`, the transcribed text will be inserted to the text box, so it can be edited before submitted.