# Reference

Every file in this folder represents a test. The name of the file is the ID of the test, also used as the url https://locationofthetest.com/test/:ID. You can add as many files (tests) as you like in this folder.

To make them visible, **make sure you add the filename to "/texts/tests.md"**

#### name:

The (human readable) title of the test.

#### pretest:

A list of texts/pages to show before the test starts. The name is a reference to a file in the /texts/ folder. For example, if /texts/grapheme-intro.md exists:

```
pretest:
  - grapheme-intro
```

Otherwise use false as value for no extra text/page.

#### posttest:

Same as pretest, but for text/pages after the test is finished (before showing the results)

#### type:

Test type, currently available options are:

- grapheme
- audio
- imagesound

#### selector:

Color selection, options are:

- colorgrid
- colorpicker

#### cutoff:

Cutoff value for synesthetic range in results, for example: 1.43

#### likert:

Include extra questions, options are:

- true
- false

#### help:

Short text below the test for additional instructions with translations, example:

- nl: Probeer instinctief de kleur te kiezen die je associeert of het beste vindt passen bij de letter of het woord hierboven.
  en: Try to instinctively choose the color you associate, or feel fits best with the character/word above.

#### resulttext:

resulttext: Letter-kleur of cijfer-kleur synestheten zien altijd precies dezelfde kleur bij een letter of cijfer. Je score op de test geeft aan of jij elke keer dezelfde kleur hebt gekozen voor een letter of cijfer. Des te lager je score, des te preciezer je kleurkeuzes, en hoe meer synesthetisch je bent.

#### sets:

Here you can add a list of sets that will be picked randomly for each participant. There are 2 ways to define the list with options:

`set1: ["A", "B", "C]`

or

```
set1:
  - A
  - B
  - C
```

translations are available too, use the "t:" prefix:

`set1: ["t:wednesday","A","B","C"]`

Make sure you add the part behind the t: as a reference in the translations.yml (in the folder above).

```
wednesday:
  en: wednesday
  nl: woensdag
```
