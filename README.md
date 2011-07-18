# Interface Tests for .NET

I've created this repository because I needed a default set of tests for the
implementation of _IDictionary<string, object>_ in [Simple.Data](http://github.com/markrendle/Simple.Data)'s SimpleRecord
type.

While the internal implementation of that type is specific to the requirements
of Simple.Data and its API, when it is used as an _IDictionary<string, object>_
its behaviour should be consistent and predictable according to the "contract"
represented by that interface.

This is true of a whole bunch of interfaces that are defined in the .NET Base
Class Library, and I hope that people will fork this repository and add more
standard tests for things like _IList<T>_, _ISet<T>_ and so on, or add more tests
to existing files, and send me pull requests.

My starting test is for NUnit; if you prefer a different test framework, please suffix the filename with, e.g., "\_XUnit" or "\_MSTest".

I originally tried to implement this first test as a base abstract class, but
the tooling support for running tests contained in a base class was so poor that
I switched to having a single-class implementation. Hopefully the tooling will
improve. :)
