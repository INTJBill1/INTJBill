---
title: "...this is the rhythm of the night..."
categories:
- "2023"
---

> Everybody's gone    
They left the television screaming   
that the radio's on  
Someone stole my shoes,   
but there's a couple of bananas    
And a bottle of booze  
>  
> -Counting Crows, *Holiday in Spain* 

*...and this begins my move toward something new...*

> An auto-save feature would be desastrous because it would take away the workflow from you.
>
> -LibreOffice forum user

My knee-jerk reaction to the above post was to think it was utter nonsense.  However, there was something about that which made me return to the idea.  My EFL poster is absolutely right:  taking the necessity to save my work takes away from me. Who doesn't remember *Wall-E*?  Do we *really* want that dystopia?

*...and perhaps, I spend too much time maintaining tools and another enough time using them?...*

I am convinced to go with Linux, USB drive backups and FLAC rips from old CDS for music.  I just have no interest in being part of the religion of *The Cool Kids Lunch Table*.  I just want to be completely disconnected from this new-fangled, "All your base are belong to us" world.  Make a big return to the computing I knew...the world I know... 

*...and yet?...* 

Do we need more than a pencil and a stack of paper snapped into order with a clipboard?  Far too often we are shaped by our tools—shouldn't it be the other way around?  Life becomes a disjointed text with all the semantics of a concrete brick. 

*...I'm torn because I want the conveniences of centralization?...*  

Have I been shaped by the mindset of centralization as opposed to any real need?  I don't want a life of a VAX terminal;  I want my space.  I have no interest in Big Tech's coding of demagogy.

*...can focus be unfocused?...*

After a Takeout, I lamented Google's wrecking of the organization of my uploaded music.  "Just throw every file into one big ol' directory."  What, is the sysadmin at Google a 5-year-old?  On a Windows box, I used to run mp3tag to sort this thing out.  But on Linux, well, I knew something might work out better.  And wholly thanks to ChatGPT, it generated (after some prodding) a script to rename songs with their track number followed by their title and move it into a folder with their album name:

```
#!/bin/bash

# Directory containing your FLAC files
input_directory="/media/intjbill/Quark/test"

# Iterate through the FLAC files in the directory
for flac_file in "$input_directory"/*.flac; do
    if [ -f "$flac_file" ]; then
        # Extract album name from FLAC tags (assuming it's the album field)
        album_name=$(metaflac --show-tag=ALBUM "$flac_file" | cut -d= -f2 | sed 's/^[ \t]*//;s/[ \t]*$//')
        
        # Extract track number and title from FLAC tags
        track_number=$(metaflac --show-tag=TRACKNUMBER "$flac_file" | cut -d= -f2 | sed 's/^[ \t]*//;s/[ \t]*$//')
        
        # Use awk to remove leading zeros if present and ensure it's a number
        track_number=$(echo "$track_number" | awk '{gsub(/^0+/,""); if ($0+0==$0) print $0; else print "01"}')

        song_title=$(metaflac --show-tag=TITLE "$flac_file" | cut -d= -f2 | sed 's/^[ \t]*//;s/[ \t]*$//')

        # Sanitize album name, track number, and song title
        album_name=$(echo "$album_name" | tr -cd '[:alnum:]()[]{} ')
        track_number=$(echo "$track_number" | tr -cd '[:alnum:]')
        song_title=$(echo "$song_title" | tr -cd '[:alnum:]()[]{} ')

        # Create a directory for the album
        album_directory="$input_directory/$album_name"
        mkdir -p "$album_directory"

        # Generate the new filename with track number and title
        new_filename="$album_directory/$track_number - $song_title.flac"

        # Move and rename the FLAC file to the album directory
        mv "$flac_file" "$new_filename"
    fi
done

```

*...just because I can install Linux on an M1 Macbook, should I?...*

