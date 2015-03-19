# Introduction

With all these new-found prowess of sass

the responsibility of code quality is even more paramount

leaving your code littered with unclear rule separation, randomly imported mixins and no clear use of selectors will quickly decrease readability, maintainability and scalability of your code.

This will also increase aggravation, snaring and disappointment from other developers on your team

leave your code as clean as or better than you found it



# About the compiler


## Visible and Invisible comments

```sass
// comment goes here <- these comments will not be output into your CSS
```

```sass
/* comment goes here */ <- these comments can be output into your css depending on settings
```

## Compiler Settings

**Default Sass**

```sass
// test comment
/* test comment */
$paddings: 30px;
$size: 4em;
.btn-lg {
	padding: $paddings;
	font-size: $size;
}
```

**Expanded**

```sass
/* test comment */
.btn-lg {
	padding: 30px;
	font-size: 4em;
}
```

**Nested**

```css
/* test comment */
.btn-lg {
  padding: 30px;
  font-size: 4em; }
```

**Compact**

```css
/* test comment */
.btn-lg { padding: 30px; font-size: 4em; }
```

**Compressed**

```css
.btn-lg{padding:30px;font-size:4em}
```

# Common Best Practices

## Nesting

```css
.block {
	color: orange;
	ul {
		width: 100%;
		li {
			width: 100%;
			p {
				font-weight: bold;
			}			
		}
	}
}
```

This is good, we are really following the OOP approach to Sass, is what you might think. But let's take a different look at this do we really need to be that specific especially for that last nested p selector?

This is really bad and you might end up writing that p selector style over and over again.

Which violates the rules of DRY

```sass
.block {
	color: orange;
}

ul {
	width: 100%;
}

li {
	width: 100%;
}

p {
	font-weight: bold;
}
```

this might not be the best example, but I hope you get the idea.

## Naming Conventions

camelCase

snake_case

hyphen-case

PascalCase

regardless of what ever floats your boat, the goal is to be consistent!

