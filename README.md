# MSRP & CPIM parser for Python

This is a companion project to my [SIP/SDP parser](https://github.com/alxgb/sip-parser) and, unlike that one, is not based off of any existing library in another language. Since the MSRP/CPIM formats are pretty simple, so are the parsers. They don't validate the contents of the headers, they just put them into a structure that can be easily consumed. The tests can be run from the project root by simply executing `pytest`. And anyone's free to fork this and use it as a starting point for their own parser/needs, the license is MIT (See LICENSE file).

## Examples

(For additional usage examples, you may check out the tests)

### MsrpMessage
```python
try:
    msrp_msg = MsrpMessage.from_string("<msg_str>")
except MsrpParseError as:
    print(f"Failed to parse message: {ex}")

# Use the parsed message (simply access the class properties, it's a pretty thin class)
```
