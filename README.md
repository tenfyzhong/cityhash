# cityhash
[![Build Status](https://github.com/tenfyzhong/cityhash/actions/workflows/build-test.yml/badge.svg?branch=master)](https://github.com/tenfyzhong/cityhash/actions/workflows/build-test.yml)
[![GitHub tag](https://img.shields.io/github/tag/tenfyzhong/cityhash.svg)](https://github.com/tenfyzhong/cityhash/tags)
[![Go Reference](https://pkg.go.dev/badge/github.com/tenfyzhong/cityhash.svg)](https://pkg.go.dev/github.com/tenfyzhong/cityhash)

Google CityHash in Go. 

CityHash provides hash functions for strings. 

[cityhash homepage](https://github.com/google/cityhash)

# Example
```go
import github.com/tenfyzhong/cityhash

func ExampleCityHash32() {
	s := []byte("hello")
	hash32 := cityhash.CityHash32(s)
	fmt.Printf("the 32-bit hash of 'hello' is: 0x%x\n", hash32)

	// Output:
	// the 32-bit hash of 'hello' is: 0x79969366
}

func ExampleCityHash64() {
	s := []byte("hello")
	hash64 := cityhash.CityHash64(s)
	fmt.Printf("the 64-bit hash of 'hello' is: 0x%x\n", hash64)

	// Output:
	// the 64-bit hash of 'hello' is: 0xb48be5a931380ce8
}

func ExampleCityHash128() {
	s := []byte("hello")
	hash128 := cityhash.CityHash128(s)
	fmt.Printf("the 128-bit hash of 'hello' is: 0x%x%x\n", hash128.High64(), hash128.Low64())

	// Output:
	// the 128-bit hash of 'hello' is: 0x65148f580b45f3476f72e4abb491a74a
}
```
