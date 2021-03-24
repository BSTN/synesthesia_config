# Synesthesia Tests Configuration Files

Here are some references/instructions for the configuration of the synesthesia tests.

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

See [tests/README.MD](tests/README.MD) for detailed reference.

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

Useful inside a test (pretest or posttest):

```
<nextbutton />
```

### The test repository:

[https://github.com/BSTN/synesthesia](https://github.com/BSTN/synesthesia) (please contact me for access)
