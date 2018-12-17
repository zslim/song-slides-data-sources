# Lyrics data for the Sacral Slides

This is a subproject to my [Sacral Slide Factory](https://github.com/zslim/song-slides "Sacral Slide Factory repo"). 

Here I track the preparation of the source I work with in the main project.

## What source?

Project [Sacral Slide Factory](https://github.com/zslim/song-slides "Sacral Slide Factory repo") is about building an app through which slides are available for songs that are frequently sung in the holy mass in Hungary. So my source data consists of tons of lyrics. 

Fortunately I don't have to type them because nice people worked a lot doing it for the sake of the [Diatár Project](http://diatar.eu/ "Diatár") (which kind of tries to do something similar to my SSF). The lyrics are available in *dtx format, organized based on the song books that we use. One file contains all the lyrics of the song in one book, so my source files are huge. The lyrics file of the book "Kék könyv", which is the most important source for my project, contains more than 8000 lines.

## What preparation?

The source files contain separators that I use in my parser script to distinguish between songs and between slides within a song. However, the linebreaks are not always where they should be. The lyrics of some songs are only broken at the end of a slide. Some others contain lines that are too long to fit on a slide. 

Why are linebreaks so important to me? In most songs, lines are structural units and people can follow the song easier if they see the lyrics line by line. Besides, my slide maker script doesn't handle the case when a line is longer than the slide width, the extra words are just omitted. (Obviously this is the less important reason, because it'd probably take much less time to change this than reading through all the lyrics and fixing the linebreaks.)

So, the preparation of the source means mostly fixing line breaks. Other typos as well, sure, but there's not a lot of those.

## What is the desired output like?

When I'm ready, no line should be longer than 38 characters and no slide should have more than 13 lines. There should be nothing in the files except song separators (starting with >), slide separators (starting with #), the actual lyrics, and slide numbers (starting with /), which I don't need but don't mind either.

### Let's roll!
