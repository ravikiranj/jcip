## jcip - Java Concurrency in Practice
* Source - http://jcip.net/

## Setup
* Install [gradle](https://gradle.org/install/)
* Run `./gradlew clean && ./gradlew build && ./gradlew run` - This should print "Hello world!" if it succeeded
* In IntelliJ, create a new project - Import from existing sources and use `build.gradle`
* [JCIP Code Listings](http://jcip.net/listings.html)
    * Try opening the class `UnsafeSequence` (first program in the book) to check if your setup is correct

```java
package net.jcip.examples;

import net.jcip.annotations.*;

/**
 * UnsafeSequence
 *
 * @author Brian Goetz and Tim Peierls
 */

@NotThreadSafe
public class UnsafeSequence {
    private int value;

    /**
     * Returns a unique value.
     */
    public int getNext() {
        return value++;
    }
}
```
