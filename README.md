# Korean Dictionaries for Yomichan
Yomichan is a browser extension created for Japanese which enables its users to quickly and efficiently look up words on a webpage.

Using Yomichan for other languages is possible, but the crux of the challenge is deinflecting the notoriously arcane conjugations of Korean verbs.

Originally inspired by [Samuihasu's KRDICT for Yomichan](https://github.com/Samuihasu/krdict-yomichan), the trick is to duplicate each verb entry and change the header word to one of its conjugated forms.

There is no real and easy way to do this. I tackled this by using [Kyubyong's KoParadigm](https://github.com/Kyubyong/KoParadigm) that generates all the possible conjugations given a certain verb. It is the best conjugator we have at hand right now, but it is not perfect and probably makes some mistakes.

## Dictionaries

- [KRDICT](https://github.com/Samuihasu/krdict-yomichan/releases): This is a Korean-English dictionary.

- [Naver Korean-Japanese Dictionary](https://mega.nz/folder/Tcw1EDaI#BcXbB_pAw7Nn2qOIVeNXTw) (Updated 28 Jan 2023): This is helpful for anyone who knows Japanese. It is more natural to learn Korean using Japanese too. This dictionary is originally in StarDict format and I simply converted it into JSON using [PyGlossary](https://github.com/ilius/pyglossary) before converting into Yomichan format. Please comment or message me if you find any issues.

You should use both dictionaries to cover as much ground as possible because either dictionary might have missed some conjugations.

## Yomichan Setup

If you are already using Yomichan for Japanese/Chinese, I recommend creating a new profile or new browser to load the dictionaries.

You can follow [Xelieu's Mining Setup](https://rentry.co/mining) if this is your first time using Yomichan.

To use Forvo audio with Yomichan, download [Yomichan Forvo Server for Anki](https://ankiweb.net/shared/info/580654285) and change the language in the add-on configs to "ko".

![anki_7FSTTaP0ek](https://user-images.githubusercontent.com/33834537/215238526-d6740711-f2ed-45da-9c22-d2c461c90162.png)

Make sure that "Search text with non-Japanese characters" and "Allow scanning popup content" is enabled.

Under Audio->Configure audio playback sources, add Custom URL (JSON) with URL: `http://localhost:8770/?expression={expression}&term={term}&reading={reading}`

In order for the audio to work for conjugated verbs, you MUST look up the unconjugated verb.

![chrome_EBLTBGlayc](https://user-images.githubusercontent.com/33834537/215238481-2d3bf7a4-9b3a-4365-a73f-47f4c34f9b60.png)

Note that using `{sentence}` field in the card format will not show the original sentence if you mine within a pop-up. Using other sentence mining tools like [asbplayer](https://github.com/killergerbah/asbplayer) can help to update the sentence.

## Fonts

[Source Han Serif](https://source.typekit.com/source-han-serif/?scid=social71226596) has great fonts that support Korean and Chinese/Japanese characters.

## Future Plans

I would want to improve on the conjugator before making any other dictionaries, especially monolingual ones.

There are probably many mistakes in the Naver dictionary; please do tell me so that I can update them.

Discord: Lyroxi#5735