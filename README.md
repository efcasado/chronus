# chronus

The missing stopwatch for Erlang.

## Getting Started

`chronus` is a simple application that leverages on Erlang's metaprogramming
capabilities to provide Erlang developers with a tool to measure how long does
it take for a particular function to finish its work.

## TL;DR

```erlang
application:start(chronus).

Opts = [{file, "/tmp/chronus.output"}].

Pid  = chronus:start(Opts).

MFAs = [{proplists, get_value, 2}].
ok   = chronus:time(MFAs, Pid).

ok   = chronus:stop(Pid).
```


## Author(s)

- Enrique Fernandez `efcasado@gmail.com`


## License

> The MIT License (MIT)
>
> Copyright (c) 2015 Enrique Fernández
>
> Permission is hereby granted, free of charge, to any person obtaining
> a copy of this software and associated documentation files (the
> "Software"), to deal in the Software without restriction, including
> without limitation the rights to use, copy, modify, merge, publish,
> distribute, sublicense, and/or sell copies of the Software, and to
> permit persons to whom the Software is furnished to do so, subject to
> the following conditions:
>
> The above copyright notice and this permission notice shall be
> included in all copies or substantial portions of the Software.
>
> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
> EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
> MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
> NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
> LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
> OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
> WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
