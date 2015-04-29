# Suffuse and the JVM

--

## JVM demanding, unforgiving
- JVM allows no wiggle room in bytecode
- any unexpected difference is a linkage error
- JVM offers no link stage for reconciliation
- predictable result: brittle artifacts, upgrade aversion
- impact goes beyond bytecode, pervades culture
- binary compatibility remains huge issue in other jvm langs

--

## The missing link
- We can introduce an invisible link stage
- Classfiles to be stitched together when first read
- Linker logic can accommodate variation in interface
- An SFS is an interface implementation - bundle the logic!
- Jar contains metaclassfiles and linker logic
- Self-healing, self-adjusting binary artifacts
- Wrap asm/bytebuddy for on-demand classfile creation

--

## Scala
- Scala's trait encoding is a nightmare
- It can be thrown away in its entirety
- Traits to be composited declaratively
- A single constructor aggregates trait constructors
- Private fields can be local to the virtual class

--

## Specialization
- imagine specializing every class
- and every method
- across every primitive type
- with no bytecode size penalty and no custom loader
- all possible with virtual classfiles, created on demand

--

## The jvm you wanted
- Standard classloaders on a standard jvm
- opportunities abound for optimization, robustness
- instrumentation, profiling, tracing, jdk-patching
- de-duplicating bytecode in sane metabytecode
- Could supplant uses of JVMTI, java agents, custom loaders
- Analyze jars to produce virtual shell script runner

--

## Scala bytecode
- A typical scala method of the kind we don't need.

```java
public scala.collection.AbstractMap();
   0: aload_0
   1: invokespecial #410 // Method scala/collection/AbstractIterable."<init>":()V
   4: aload_0
   5: invokestatic  #414 // Method scala/collection/GenMapLike$class.$init$:(Lscala/collection/GenMapLike;)V
   8: aload_0
   9: invokestatic  #417 // Method scala/Function1$class.$init$:(Lscala/Function1;)V
  12: aload_0
  13: invokestatic  #420 // Method scala/PartialFunction$class.$init$:(Lscala/PartialFunction;)V
  16: aload_0
  17: invokestatic  #423 // Method scala/collection/generic/Subtractable$class.$init$:(Lscala/collection/generic/Subtractable;)V
  20: aload_0
  21: invokestatic  #426 // Method scala/collection/MapLike$class.$init$:(Lscala/collection/MapLike;)V
  24: aload_0
  25: invokestatic  #429 // Method scala/collection/Map$class.$init$:(Lscala/collection/Map;)V
  28: return
```

- TODO: more bytecode examples.
