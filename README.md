## Colemak Mod-DH (Bosnian, Croatian, Serbian)
A variant of [Colemak Mod-DH ISO](https://github.com/ColemakMods/mod-dh) for Bosnian/Croatian/Serbian. Available in Cyrillic and Latin.

<div align="center">
    <img src="https://github.com/K0stov/colemak-bs-hr-rs/assets/26684396/a98ddaf7-cecb-4a09-a556-b37a2833888a" width="500">
    </br>
    <img src="https://github.com/K0stov/colemak-bs-hr-rs/assets/26684396/f05de436-ccd4-492d-ad86-a1268eb30c07" width="500">
</div>

***

<p align="center"><em>Heatmap with an excerpt from </em>Na Drini ćuprija<em></em></p>

<div align="center">
    <img src="https://github.com/K0stov/colemak-bs-hr-rs/assets/26684396/b7d8cdbb-760e-4e2a-aaa4-786fca131ba5" width="500">
    </br>
    <img src="https://github.com/K0stov/colemak-bs-hr-rs/assets/26684396/9fed292c-c984-487c-993f-b5f4bf6a75ca" width="500">
</div>

### Description
Features a rearranged Colemak Mod-DH layout for more comfortable typing in these languages. Changes and features conform to Colemak’s philosophy:

- Characters have been moved in accordance with Bosnian/Croatian/Serbian letter patterns.
  - Common digraphs and trigraphs are now easier to type: *je*, *ra*, *da*, *sam*, *šta*, *ali*.
  - The first 4 home row characters have been changed from *ARST* to *RSTA*. The letter A is more common than the other three and therefore merits index finger use.
- Rare characters are placed further away. This includes letters from the English alphabet (Q, W, X).
- Punctuation marks are mostly positioned the same as in Colemak Mod-DH. (This placement is arguably more ergonomic compared to European QWERTY positions.)
- Third (AltGr) and fourth (Shift + AltGr) character layers are mostly preserved from the original QWERTY layout.

The Bosnian (Latin), Croatian and Serbian (Latin) layouts are the same functionally. The same applies to Bosnian (Cyrillic) and Serbian (Cyrillic).

### Download

#### Windows
1. Navigate to the [klc](klc) folder.
2. Download the .zip archive for your respective locale and script(s).</br>(Example: *colemak_dh_bs-cyrl.zip* for Bosnian Cyrillic.)
3. Extract the downloaded archive and run *setup.exe*.

#### Linux
1. Navigate to the [xkb](xkb) folder.
2. Download the file for your respective locale. (Example: *ba_colemak* for Bosnian.)

  ##### The following steps will require root access.

3. Move the downloaded file to ```/usr/share/X11/xkb/symbols/```.
4. Open ```/usr/share/X11/xkb/rules/evdev.lst``` in your text editor of choice.</br>*Back up the file in case something goes unexpectedly.*
5. At the end of the ```! model``` section, append the layout:
   ```
     ##_colemak      %%% (Colemak-DH)
   ```
   *Replace *##* with your file name and *%%%* with your language name (Bosnian/Croatian/Serbian).*
6. Save your text changes.
7. Open ```/usr/share/X11/xkb/rules/evdev.xml``` in your text editor of choice.</br>*Back up the file in case something goes unexpectedly.*
8. Find your language add make a new ```<layout>``` below it. Example:

    ```xml
    <layout>
      <configItem>
        <name>ba_colemak</name>
        <shortDescription>bs</shortDescription>
	      <description>Bosnian (Colemak-DH)</description>
        <languageList><iso639Id>bos</iso639Id></languageList>
      </configItem>
      <variantList>
        <variant>
          <configItem>
            <name>colemak_dh_cyr</name>
            <description>Bosnian (Cyrillic, Colemak-DH)</description>
          </configItem>
        </variant>
        <variant>
          <configItem>
            <name>colemak_dh_lat</name>
            <description>Bosnian (Latin, Colemak-DH)</description>
          </configItem>
        </variant>
      </variantList>
    </layout>
9. Save your text changes.
10. Set your newly added keyboard layout in your keyboard application.

### Known problems
- The digraph *nj* isn't very comfortable to type. *ije*, one of the most common trigraphs, could also be optimized; it currently requires the ring-index-middle fingers, in that order.
- [Cyrillic] Љ and Њ are positioned rather far away. A good solution would be to automatically turn the digraphs *лј*/*нј* into *љ*/*њ* respectively. This may be possible on Windows with [AutoHotkey](https://www.autohotkey.com/), but it is [**not yet possible**](https://github.com/autokey/autokey/issues/114) on Linux with [AutoKey](https://github.com/autokey/autokey).
- [Latin] The letter Y is not yet in the Latin layout, as a suitable position has not yet been found.

### Resources used when making
- [Online Tools - Calculate letter frequencies](https://onlinetoolz.net/letter-frequency)
- [Ortho Heat](https://oha-ohashi.github.io/2022_1/a_ortho/ortho_heat.html)

### External links
- [Topic on Colemak forum](https://forum.colemak.com/topic/2996-cyrilliclatin-colemak-for-boshrvmnesrb/)
- [Topic on Srpski jezički atelje](https://forum.srpskijezickiatelje.com/index.php?topic=6315.0)
