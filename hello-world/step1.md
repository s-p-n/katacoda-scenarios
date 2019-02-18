## What does Arini look like?
In Arini, we have expressions, lists of expressions, identifiers, operators, and syntax used to craft those expressions. Control code (what you find in the root of an Arini program or in every scope) is a list of expressions seperated by semi-colons. Arini has a few basic types. [These basic types may be used to implement more abstract types.](https://github.com/s-p-n/arini/blob/master/docs/casting/custom.md).

### Primitive Types in Arini:
* A **boolean** is the token `true` or `false`.
<pre class="file" data-filename="project/program.ari" data-target="replace">
let foo = true or false; // true
let bar = true and false; // false
console.log(foo, bar);
</pre>
`arini program.ari`{{execute}}

* A **string** can be text surrounded by `""`, or `''`, or backticks.
<pre class="file" data-filename="project/program.ari" data-target="replace">
let foo = "I am a string.";
let bar = 'I am
    a multiline
    string';
let baz = \`
  I am a multiline string containing 2 variables:
  foo: ${foo}
  bar: ${bar}
  And that is that.
\`;
console.log(baz);
</pre>
`arini program.ari`{{execute}}

* A **number** is simply a number like JavaScript's Number.
<pre class="file" data-filename="project/program.ari" data-target="replace">
let a = 543;
let b = 1.25;

console.log(a + b);
</pre>
`arini program.ari`{{execute}}

* An **array** is a map of items. Arrays, if not named, use indices just like in most programming languages. Arini also supports named arrays. One big diference between Arini and JavaScript, is arrays. Arini takes JavaScript arrays and objects and consolidates their features. Interestingly, JavaScript already does this with the Array. So Arini builds on that.
<pre class="file" data-filename="project/program.ari" data-target="replace">
let foo = [
	question = "What is the answer to the universe and everything?",
	answer = 42
];
console.log(foo["question"]); // "What is the..."
console.log(foo.answer); // 42 

let bar = ["cow", "pig", "sheep"];
bar.forEach(#(val) {
	console.log(val);
});
</pre>
`arini program.ari`{{execute}}
