Byte Units
==========

Utility classes for converting between granularities of SI and IEC byte units
and bit units.



Example Usage
-------------

What's the difference in hard drive space between perception and actual?
```java
long perception = DecimalByteUnit.TERABYTES.toBytes(2);
long usable = BinaryByteUnit.TEBIBYTES.toBytes(2);
long lost = BinaryByteUnit.BYTES.toGibibytes(perception - usable);
System.out.println(lost + " GiB lost on a 2TB drive.");
```

Method parameter for specifying a resource size.
```java
public void installDiskCache(long count, ByteUnit unit) {
  long size = unit.toBytes(count);
  // TODO Install disk cache of 'size' bytes.
}
```



License
-------

    Copyright 2014 Jake Wharton

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.



