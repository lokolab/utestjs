utestjs
=======
**This is development (master) version.<br> For production version (relase) see
<https://github.com/lokolab/utestjs/tree/v0.0.1>**
- Version: 0.0.1-dev
- Technologies:
  - JavaScript
- Compatibility:
  - Chrome
  - Firefox
  - Internet Explorer
  - Opera
- Dependencies:
  - null
- Copyright / Authors:
  - Krystian Pietruszka <kpietru@lokolab.net>
- Licenses:
  - MIT <http://opensource.org/licenses/MIT>
- Download: <https://github.com/lokolab/utestjs/releases>
- Homepage: <http://www.lokolab.net>

Utestjs JavaScript testing library.
___________________________________

Example usage
-------------

    <!doctype html>
    <html>
        <head>
            <title>Test page</title>
            <script src="utestjs-0.0.1.js"></script>
            <script src="somelib_for_test.js"></script>
        </head>
        <body>
            <h1>Test page</h1>
            <dl>
                <dt>All</dt>
                    <dd id="counter_all">0</dd>
                <dt>Ok</dt>
                    <dd id="counter_ok">0</dd>
                <dt>Error</dt>
                    <dd id="counter_error">0</dd>
            </dl>
            <dl id="results"></dl>

            <script>
                test('functionName description', function() {
                    assertType(somelib.upperCase('abc'), 'string');
                });

                test('functionName description', function() {
                    assertSame(somelib.upperCase('abc'), 'ABC');
                });

                test('functionName description', function() {
                    assertException('TypeError', function() {
                        somelib.someFunction(123);
                    });
                });
            </script>
        </body>
    </html>

API
---

- test ( string: __name__, function: __callback__ ): void
- assertSame ( *: __variable1__, *: __variable2__ ): void
- assertType ( *, *, ... ): void
- assertException ( string: __errorName__, function: __callback__ ): void

References
----------

1. [Google JavaScript Style Guide][1]

[1]: http://google.github.io/styleguide/javascriptguide.xml


