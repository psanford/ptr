# ptr

ptr is a Go package that provides a generic ptr.To function for getting a pointer to a value.

This can be used in place of things like the non-generic aws sdk helper functions:
```
str := aws.String("hello")
// vs
str := ptr.To("hello")

i := aws.Int(42)
//vs
i := ptr.To(42)
```

This package was pulled out of the [tailscale](https://github.com/tailscale/tailscale/blob/86f273d930df52440641ef2397f0f7ebca648d7c/types/ptr/ptr.go) repository into a stand alone module for ease of use.

## Usage

```go
import "github.com/psanford/ptr"

str := ptr.To("hello")    // *string
num := ptr.To(42)         // *int
val := ptr.To(MyStruct{}) // *MyStruct
```
