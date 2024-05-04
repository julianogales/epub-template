# Book ePub Template
This is a basic template to start a new electronic book project.

> [!NOTE]
> I used **[Sigil](https://github.com/Sigil-Ebook/Sigil)**, a multi-platform EPUB ebook editor, to create my own ePubs.

> [!TIP]
> I recommend installing **Sigil** (and its xhtml editor, **PageEdit**, if it's your first time writing in xhtml)
> to get started with your first ebook project. If you need some help with your first steps in Sigil (and you speak
> spanish), you could visit [**Tutorial de Sigil en español**](https://youtube.com/playlist?list=PLMdoCO6yLSw7iIxQu0v_TDx4AMUm-TP6g&si=6jlAakQwetgZkU90)
> in YouTube.

## How to use this template
### Add font families
#### 1. Add font files (.ttf) to Fonts

To add a new font family in your epub, go to the fonts folder of your computer (``C:\Windows\Fonts`` for Windows),
copy all the **.ttf** files of the family you wish to use (e.g. Sitka Small: _SitkaSmall.ttf_, _SitkaSmall-Bold.ttf_,
_SitkaSmall-Italic.ttf_, ...) or download new ones (e.g. [Google Fonts](https://fonts.google.com/)), and paste them inside
the folder [**Fonts**](Fonts).

#### 2. Link the new font to the document style

In [**styles.css**](Styles/styles.css) file, where you can modify and create new text styles for your ePub, modify the
following methods with the name of your new font:

```css
/* Font family: Sitka Small */

@font-face {
  font-family: 'sitka-small';
  font-style: normal;
  font-weight: normal;
  src: url(Fonts/SitkaSmall.ttf);
}

@font-face {
  font-family: 'sitka-small';
  font-style: italic;
  font-weight: normal;
  src: url(Fonts/SitkaSmall-Italic.ttf);
}

@font-face {
  font-family: 'sitka-small';
  font-style: normal;
  font-weight: bold;
  src: url(Fonts/SitkaSmall-Bold.ttf);
}
```
- **font-family**: the name you want to give to your font family
- **font-style**: normal or _italic_
- **font-weight**: normal or **bold**
- **src**: the location of the font file

#### 3. Define the body

Also in [**styles.css**](Styles/styles.css), modify the following method with the name of your new font:

```css
/* Body of the text */

body {
  font-family: sitka-small, serif;
  margin: 1em;
  padding: 0;
  border: 0;
}
```
- **font-family**: the name you previously gave to your font family (should also be accompanied by a generic font family
like _serif_, _monospace_, ...)
- **margin**: space outside the border of an element
- **padding**: space between the content of an element and its border
- **border**: line that surrounds the content and padding of an element

### Add images

#### 1. Add image files (.png, .jpg, ...) to Images
Upload all the images you wish to put in your ebook inside the folder [**Images**](Images). If your ePub has many
pictures, you could organize them by creating new folders inside Images (e.g. _Covers_, _Chapter1_, _Chapter2_, ...).

#### 2. Link the images to the document
In the file (e.g. [_chapter1.xhtml_](Text/chapter1.xhtml)) where you wish to put your image
[img001.png](Images/Chapter1) write down the following line:

```xhtml
<br/> <p class="ilustra"> <img alt="" src="../Images/img004.png"/> </p> <br/>
```
- **\<br/>**: 
- **\<p>...\</p>**:
- **class=" "**:
- **"ilustra"**:
- **\<img>**:
- **alt=" "**:
- **src=" "**: