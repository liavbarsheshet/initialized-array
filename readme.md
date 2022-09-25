# C++ Initialized Array

Implementation of a generic Initialized Array.

---

## Declaration

Supports >= c++11:

```c++
#include "initialized-array.hpp"

auto initialized_array = InitArr::InitializedArray<Value,Number>();
```

## Template

```c++
/**
 * Class: Represents an initialized array.
 * @tparam Value - The type/class of the value.
 * @tparam Number - Class/Primitive number type for index representation.
 */
template<typename Value, typename Number>
class InitArr::InitializedArray{...}
```

## Methods

Implementation of a Generic Initialized Array.

```cpp
/**
* Constructor: Creates an initialized array.
* @note Worst-Time Complexity: O(1).
* @note Worst-Space Complexity: O(3n).
* @param length - The length of the array.
* @param def - The default value which all values will be initialized to.
*/
InitializedArray(Number length, Value def);

/**
* Copy Constructor: Creates an initialized array from an existing one.
* @note Worst-Time Complexity: O(top) <= O(n).
* @note Worst-Space Complexity: O(3n).
* @param arr - The array reference.
*/
InitializedArray(const InitializedArray<Value, Number> &arr);

/**
* Destructor: Deallocates the entire array.
* @note Without responsibility of the content(items).
* @note Worst-Time Complexity: O(1).
*/
~InitializedArray();

/**
* Gets the element at a specific index.
* @note Worst-Time Complexity: O(1).
* @param index - Specific index of an element.
* @return {Value} Returns the element at specific index.
*/
Value Get(const Number &index) const;

/**
* Sets the element at a specific index.
* @note Worst-Time Complexity: O(1).
* @param index - Specific index of an element.
* @param value - Specific value.
*/
void Set(const Number &index, Value value);

/**
* Gets the default value.
* @note Worst-Time Complexity: O(1).
* @return {Value} Returns the default value.
*/
Value Default() const;

/**
* Gets the length of the array.
* @note Worst-Time Complexity: O(1).
* @return {Number} Returns the length of the array.
*/
Number Length() const;

/**
* Gets the element at a specific index.
* @note Worst-Time Complexity: O(1).
* @param index - Specific index of an element.
* @return {Value} Returns the element at specific index.
*/
Value operator[](const Number &index);
```

## Author

[Liav Barsheshet, LBDevelopments](https://github.com/liavbarsheshet)

## License

[MIT](LICENSE)
