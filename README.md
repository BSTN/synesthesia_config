# Synesthesia Tests Configuration Files

The test repository:
[https://github.com/BSTN/synesthesia](https://github.com/BSTN/synesthesia)

## File structure:
```
/audio
  - audiofile.mp3
  - ...
/images
  - imagefile.jpg
  - ...
/tests
  - testname.yml
  - testname2.yml
  - ...
/texts
  - about.md
  - about.en.md
  - about.se.md
  - ...

/config.yml
/translations.yml
```

## config.yml example
```
languages:
  nl: Nederlands
  en: English
  se: Svenska
defaultLanguage: nl
animation: true
```

## translations.yml example
```
about:
  nl: Lees meer
  en: about
  se: handla om
```


## test.yml example
```
public: yes
name: 
  nl: grafeem-kleur
  en: graphemes
  se: graphemes
type: grapheme
selector: colorpicker
pretest:
  - grapheme.intro
posttest:
  - postquestions
cutoff: 1.43
help:
  nl: Probeer instinctief de kleur te kiezen die je associeert of het beste vindt passen bij de letter of het woord hierboven.
  en: Try to instinctively choose the color you associate, or feel fits best with the character/word above.
  se: Försök att så instinktivt som möjligt välja den färg du förknippar med, eller känner passar bäst ihop.
sets:
  set1: ["list","of","items"]
  set2: ...
  set3: ...

```

## text / markdown extra functionality

### List tests

```
<tests list="graphemes,graphemes-kids,vowels"></tests>
```

### Next page 
For inside a test: pretest or posttest
```
<nextbutton />
```

### Insert extra custom questions
**name:** unique name for database
**types:** 
  - likert
  - likert-reverse
```
<question type="likert" name="pq3">
  <slot>3. Altijd wanneer ik letters of cijfers zie of eraan denk (zwart tegen een witte achtergrond), ervaar ik automatisch een andere kleur voor de letter of het cijfer (bijv. rood).</slot>
</question>
```

