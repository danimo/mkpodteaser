# `mkpodteaser` - Create a visual teaser for your podcast

Promoting your podcast in social media either requires 
on either an expensive and laborsome audio/audio tools
or makes you dependend on propritary, paid-for online services.

`mkpodteaser` offers a relatively simple way to create
your own episode teasers. You provide a few static assets
and an audio file, and `mkpodteaser` will add a waveform
and render the result into an mp4 file that you can upload
to your favorite social media site.

## Preparation

### Dependencies

`mkpodteaser` is designed to require as few dependencies as possible.
It is provided as a bash shell script. As such, it will run on Linux,
MacOS and BSD-Derivates, provided that bash is installed. Windows 10
users might be able to run it using the Linux Subsystem for Windows.

You need to have ffmpeg installed on your machine. Only versions > 4.0 have
been successfully tested. Older versions are known to produce runtime
errors.

### One time setup for your podcast

1. Create a background PNG using your podcasts design
2. Adjust `mkpodteaser.conf` to make the design suit your needs

### Per episode effort

1. Extract an interesting, brief (<1min) audio snippet from your episode
2. Create a quotes file (see below) that transcribes what is being said.
3. Run mkpodteaser like this:

  ./mkdpodteaser examples/chaosradio/cr94\_t-hack.mp3 \
                 examples/chaosradio/cr94_quotes.txt \
                 "CR94: Computer-Telefonie" \
                 cr94-teaser.mp4

## Quotes file format

For the quotes, please create a text file with a content like this:
  
  0 7  Text transcription shown in seconds 0 to 7
  8 10 Text transcription shown in seconds 8 to 10

## Bugs

Please report any issues to the [issue tracker](http://github.com/danimo/mkpodteaser).
