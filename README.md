# Rube Goldberg Machine / Telephone Game

A rube-goldberg machine / telephone game thing, where you give it a message (like "banana") and it passes it to each part of the chain and then that part of the chain passes it on to the next part, and it will be glorious. I can implement each part in a different language and connect them all with webhooks.

## Basic Design

Each part of the contraption has an http server where it listens for a post request, and then upon recieving it, sends another post request. If I do this in a uniform way, then i can plug/play thing into different orders

Need to decide how purist imma be about apps having access to data, like can the esp32 send the thing to the printer and then also be the one to read it?

Should we have a central control server that can be used for sending shit to all the parts so they can be configured to go in the order we want? (could also use this for testing, configure a thing to test that it works, just configure it to send back to me)

Gotta figure out how we wanna do the "simple" steps (send webhook to discord, send file to printer, write file to desktop)

## Transportation ideas
- minecraft/computercraft (complex system where it gets decoded to utf8, then that gets passed thru sand or something)
- website / animation (text gets drawn then fed thru something)
- Alexa (can have a machine talk to alexa or maybe this is how we start the chain)
- discord (a webhook calls a bot)
- tts => stt out loud (mebbe raspberry pi starts it, and computer running C# listens to it?)
- printer + text reading (any language thing (on some host computer?) sends it to printer, then esp32 reads it and passes it on)
- ahk opens up a notepad and a message.text file, and writes it out into the file, then saves and closes notepad, and then drag-drops the file onto an app that sends it???? (or just sends it itself)

### Half-Ideas
- home assistant/vaccum
- real-world rolling ball / classic rube goldberg thing? (not sure how we'd do this for text)


## devices to use
- raspberry pi
- esp32
- my computer
- my laptop

## Languages
- lua (minecraft/computercraft)
- C# (speech-to-text listener)
- python (raspberry pi tts)
- C++ (something on esp32, maybe image detection / reading?)
- ahk (opens file written to desktop and sends to next)
- anything (discord)

## Other languages to use
- powershell
- bash
- java?