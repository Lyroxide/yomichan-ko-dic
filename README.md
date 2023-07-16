# Korean Dictionaries for Yomichan
**UPDATE! [I have forked Yomichan to deinflect Korean verbs](https://github.com/Lyroxide/yomichan-korean). Please check out the fork.**


Yomichan is a browser extension created for Japanese which enables its users to quickly and efficiently look up words on a webpage.

Using Yomichan for other languages is possible, but the crux of the challenge is deinflecting the notoriously arcane conjugations of Korean verbs.

Originally inspired by [Samuihasu's KRDICT for Yomichan](https://github.com/Samuihasu/krdict-yomichan), the trick is to duplicate each verb entry and change the header word to one of its conjugated forms.

There is no real and easy way to do this. I tackled this by using [Kyubyong's KoParadigm](https://github.com/Kyubyong/KoParadigm) that generates all the possible conjugations given a certain verb. It is the best conjugator we have at hand right now, but it is not perfect and probably makes some mistakes.

There is also a lack of KR-JP dictionaries despite amazing glossaries like Naver. Therefore, the dictionaries in this repo should be useful for anyone coming from Japanese immersion/who are Japanese natives.

## Dictionaries

Download:

- [KRDICT](https://github.com/Samuihasu/krdict-yomichan/releases): This is a Korean-English dictionary.

- [Naver Korean-Japanese Dictionary](https://mega.nz/folder/Tcw1EDaI#BcXbB_pAw7Nn2qOIVeNXTw) (Updated 29 Jan 2023): This dictionary is originally in StarDict format and I simply converted it into JSON using [PyGlossary](https://github.com/ilius/pyglossary) before converting into Yomichan's JSON schema. Might be quite outdated as some words are not in this dictionary.

- [KRDICT Korean-Japanese](https://mega.nz/folder/Tcw1EDaI#BcXbB_pAw7Nn2qOIVeNXTw) (Updated 29 Jan 2023): A Japanese version of KRDICT. Highly recommended.

You should use all these dictionaries to cover as much ground as possible because one of them might have missing conjugations/words.

Github files are for pull requests purposes.

## Yomichan Setup

If you are already using Yomichan for Japanese/Chinese, I recommend creating a new profile or new browser to load the dictionaries.

You can follow [Xelieu's Mining Setup](https://rentry.co/mining) if this is your first time using Yomichan.

To use Forvo audio with Yomichan, download [Yomichan Forvo Server for Anki](https://ankiweb.net/shared/info/580654285) and change the language in the add-on configs to "ko".

![anki_7FSTTaP0ek](https://user-images.githubusercontent.com/33834537/215238526-d6740711-f2ed-45da-9c22-d2c461c90162.png)

Make sure that "Search text with non-Japanese characters" and "Allow scanning popup content" is enabled.

Under Audio->Configure audio playback sources, add Custom URL (JSON) with URL: `http://localhost:8770/?expression={expression}&term={term}`

In order for the audio to work for conjugated verbs, you MUST look up the unconjugated verb.

![chrome_Scsv24FTTD](https://user-images.githubusercontent.com/33834537/215333467-44b9c345-3fdd-4427-912b-22ff89ee2527.png)

Another feature of the dictionaries I made (Naver, KRDICT) is that it will show a reading/'furigana' to show how words are actually pronounced (as shown above). This is done through [g2pK](https://github.com/Kyubyong/g2pK). If the words and reading match, the reading field will be empty. Ensure that you have `{reading}` field in your card format.

Note that using `{sentence}` field in the card format will not show the original sentence if you mine within a pop-up. Using other sentence mining tools like [asbplayer](https://github.com/killergerbah/asbplayer) can help to update the sentence.

## Fonts

- [Source Han Serif](https://source.typekit.com/source-han-serif/?scid=social71226596) has great fonts that support Korean and Chinese/Japanese characters.

- [Nanum Myeongjo](https://github.com/Lyroxide/yomichan-ko-dic/files/10529996/Nanum_Myeongjo.zip)

## Dictionaries Changelog

- 29 Jan 2023: Fixed missing conjugations for Naver. Added reading/furigana for words with 'odd' pronunciation. KRDICT KR-JP First Release.

- 28 Jan 2023: Naver KR-JP First Release.

## Future Plans

I would want to improve on the conjugator or modify Yomichan for Korean before making any other dictionaries, especially monolingual and frequency dicts.

There are probably conjugation mistakes in the Naver/KRDICT; feel free to do a pull request or open an issue.

Discord: lyroxide
