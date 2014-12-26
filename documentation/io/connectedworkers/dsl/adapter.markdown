
# Documentation for `io.connectedworkers.dsl.adapter`

This is a little DSL to simplify the Golo Adapters' use

sample: 

	let myDefinition = Adapter()
		: interfaces(["IHugable", "ICrazyable"])
		: extends("org.acme.Toon")
		: implements("hello", |this| -> "hello I'm " + this: name())
		: definition() # it's a getter (return the map definition)

	let ToonInstance = AdapterFabric()
		: maker(myDefinition)
		: newInstance("Babs")

	println(ToonInstance: hello())



## Structs

### `Adapter`

##### Members

- definition


The `definition` member of the `Adapter` structure contains the adapter configuration map




## Augmentations

### `Adapter`

Adapter augmentations: this DSL is fluent




#### `extends(this, className)`


`extends` method, parameter is a String (class name)



#### `implements(this, methodName, closure)`


`implements` method, parameter is a String (method name) and a closure



#### `interfaces(this, arrayInterfaces)`


`interface` method, parameter is an array of Strings (list of interfaces)



#### `overrides(this, methodName, closure)`


`overrides` method, parameter is a String (method name) and a closure



