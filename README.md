# JSON parser
This project is a JSON parser built using the C++17 standard. It leverages std::variant to manage JSON data types, utilizes std::string_view to implement the proxy pattern with clear read-only semantics, and employs std::optional for non-intrusive exception handling.

The parser is implemented using recursive descent parsing, allowing JSON strings to be analyzed and dynamically modified after parsing. The parsed data can be re-serialized back into JSON format. The interface is designed to be intuitive and easy to use.
---
# Key Features Explained
Using ```std::variant``` to Manage JSON Data Types
JSON contains multiple data types, and traditionally, we would need a custom type system to track the current type. However, C++17's ```std::variant``` eliminates the need for manual type management, making code cleaner and safer.


## Using ```std::string_view``` for Read-Only Proxy Pattern
When emphasizing read-only semantics, we can use const, but C++ also provides ```std::string_view```, which ensures immutable access without unnecessary memory allocations.

## ⭐⭐This topic is also closely related to ownership management in C++.

## Using ```std::optional``` for Non-Intrusive Exception Handling
What happens if the JSON string is invalid? We could throw an exception and catch it, but C++17 introduces ```std::optional``` as a better alternative. Instead of forcing exception handling, std::optional allows us to gracefully handle errors without disrupting program flow.

In C++23, this concept is further improved with std::expected, which provides even better error-handling capabilities.
---

## Using Recursive Descent Parsing for JSON Strings
The parser is implemented using recursive descent parsing, a common technique for parsing structured text like JSON.
