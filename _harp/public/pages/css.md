####app.less and what it means for _you_

Your app.less file should not contain any explicit attribute definitions. Rather, it should serve as a home for imported component files (e.g. buttons, lists, forms, etc) and merely assigned pre-designed library styles to explicitly-named application usages.

Components should contain code written in the most abstract, reusable way possible. Mixins are a great way to abstract code that then gets used more explicitly.

Nesting in files should be avoided at anything more than one level.

(Also I should have mentioned we use LESS, not SASS. Deal with it.)

####Hyphenation

There shall be no instances of double-hyphenation in class names.


