---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/data-management/how-to-load-data/load-voice-recordings
---

# Load Voice Recordings

No additional software or hardware is required on the part of the user to transcribe and code the voice recordings loaded into Ascribe. Any file that can be played by Windows Media Player can be loaded into Ascribe.

First, you'll find it valuable to have the [FTP](auto-ftp-setup.md) (file transfer protocol) process in place for your account. Voice recording files are large, and you may have difficulty loading them through the Ascribe interface. After confirming that you have the FTP process in place, we’ll need to set up a load file type for your needs.

Zip files will have a name corresponding to the study ID and the load file type. For example: 12345.wav.zip. This tells Ascribe which study the file is to be loaded to and the type of data files that are to be loaded. The recordings inside the zip file should be named similar to RID.QID.wav. Support can customize or tailor this component, but the important thing to remember is we need the two important bits of information, Respondent ID and Question ID. An example: 10001\_Q2.wav or 10002\_Q2.wav.

See [Translate/Transcribe Verbatims](../../verbatims/translate-transcribe-verbatims.md) to learn how to transcribe and code voice recorded verbatims.
