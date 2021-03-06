---
layout: post
title:  "Parsing SMILES using Razi"
date:   2014-02-15 20:28:13
tags: [Razi, SMILES, SMILES Parser, Chemistry Library, Chemistry Java Library]
categories: chemistry
---

Razi is a new scientific library for java.
By now this library is ready to parse SMILES and make an object-oriented model of a molecule.

1. [Download][1] The library, and import it into your project.
2. Make an instance of `com.razi.formats.smiles.Reader`.
3. Call the `set` method and set the input string.
4. Call the `process` method.
5. Done !

The code of above is :

{% highlight java %}
Reader sr = new Reader();
sr.set("C(=O)O");
sr.process();

Molecule mol = sr.get();
{% endhighlight %}

Now use descriptors to test it. By now `com.razi.descriptor.molecular.CountDescriptor` is available to get some basic countable informations of a molecule.

{% highlight java %}
cd.countAtoms(); // Number of all atoms
cd.countBonds(); // Number of all bonds
cd.countBondsByOrder(2); // Number of bonds with order 2
cd.countAtomsByElement(element); // Number of all atoms which are the same with given element
{% endhighlight %}

If you are interested in **cheminformatic** and you like to be contributor you should see [Razi on Github](https://github.com/mohebifar/Razi).


  [1]: https://github.com/mohebifar/Razi/tree/master/dist "Download"
