####app.less and what it means for _you_

Your app.less file should not contain any explicit attribute definitions. Rather, it should serve as a home for imported component files (e.g. buttons, lists, forms, etc) and merely assigned pre-designed library styles to explicitly-named application usages.

Your LESS directory should be broken into three distinct parts: globals, components, and app.less itself. Globals should contain code written in the most abstract, reusable way possible and be written with language that denotes their visual appearance. Think of globals as your block level elements--buttons, forms, type, etc. Globals should be the only place where explicit CSS is written.

Components should integrate globals as mixins, and be written with language that denotes their "purpose" on the page. Think of components as "sections" or "parts" of a website.

App.less contains nothing but import statements that compile your components and globals.

(Also I should at some point mention we use LESS, not SASS. Deal with it.)

Here's an example of what a \_globals file named \_buttons.less might look like. Note that modifiers are as descriptive as possible. (Also note the parantheses with .btn, which prevents it from being output to the compiled CSS file. )

	.btn() {
		border-radius: 4px;
		padding: 1em 2em;
		background: @grey;

		&.green {
			background: @green;
		}
		&.red {
			background: @red;
		}
		&.square {
			border-radius: 0;
		}	
		&.extra-padding {
			padding: 1.5em 3em;
		}
	}

This would then be used as a mixin within our \_components files. Let's say we have a button associated with a person and a button associated with a product. The person button is green and square, the product button is red and has extra padding. This is our \_person.less file:

	.person .btn {
		.btn.green.square();
	}

and this is our \product.less file:

	.product .btn {
		.btn.red.extra-padding();
	}

Our app.less file then looks something like this: 

	@import("globals/buttons.less");
	@import("components/person.less");
	@import("components/product.less");

This system allows for an element's display characteristics to maintain a separation between *what* it is and *how* it looks on a page. This in turn allows for maximum reusability of code because form and function are distinct.

####Hyphenation

There shall be no instances of double-hyphenation in class names.


