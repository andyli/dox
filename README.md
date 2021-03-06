A Haxe documentation generator.

> Note: Dox currently requires the development branch of Haxe due to some
minor changes in abstract rtti xml generation. You'll also need an up to date
haxelib (requires support for `classPath` in haxelib.json)

Install dependencies:

	haxelib git hxparse https://github.com/Simn/hxparse development src
	haxelib git hxtemplo https://github.com/Simn/hxtemplo master src
	haxelib install hxargs
	haxelib install markdown

To generate std documentation:

	haxelib install hxcpp
	haxelib install hxjava
	haxelib install hxcs

	haxelib dev dox .

	// Compile dox's run.n
	haxe run.hxml
	
	// Generate .xml files of Haxe standard library
	haxe gen.hxml
	
	// Generate documentation
	haxe std.hxml
	
To generate documentation of other library:
	
1. Compile all library code with haxe using `haxe -xml dir`.
2. Invoke `haxelib run dox -i dir`, where dir points to the .xml file(s)
	generated by step 1.