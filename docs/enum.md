```php
namespace Akas\Enum\Enum;

class SampleEnum extends Enum
{
    const UNO = 1;
    const ONE = 1;
    const TWO = 2;
    const STR = "sth";
}
```

Now you are able to use this methods:

```php
SampleEnum::all(); // ['UNO' => 1, 'ONE' => 1, 'TWO' => 2, 'STR' => 'sth']

SampleEnum::keys(); // ['UNO', 'ONE', 'TWO', 'STR'];

SampleEnum::values(); // [1, 1, 2, 'sth']

SampleEnum::hasKey('ONE'); // true

SampleEnum::hasKey('xXx'); // false

SampleEnum::hasValue(2); // true

SampleEnum::hasValue('xXx'); // false

SampleEnum::valueOf('ONE'); // 1

SampleEnum::keysOf(1); // ['UNO', 'ONE']

SampleEnum::keyOf(1); // 'UNO'

SampleEnum::randomKey(); // One of 'UNO', 'ONE', 'TWO', 'STR'

SampleEnum::randomKeyExceptKeys(['ONE', 'TWO']); // One of 'UNO', 'STR'

SampleEnum::randomKeyExceptValues([SampleEnum::STR, SampleEnum::TWO]); // One of 'ONE', 'UNO'

SampleEnum::randomValue(); // One of 1, 2, 'sth'

SampleEnum::randomValueExceptValues([SampleEnum::STR, SampleEnum::TWO]); // One of SampleEnum::ONE, SampleEnum::UNO

SampleEnum::randomValueExceptKeys(['STR', 'TWO']); // One of SampleEnum::ONE, SampleEnum::UNO
``````php
namespace Akas\Enum\Enum;

class SampleEnum extends Enum
{
    const UNO = 1;
    const ONE = 1;
    const TWO = 2;
    const STR = "sth";
}
```

Now you are able to use this methods:

```php
SampleEnum::all(); // ['UNO' => 1, 'ONE' => 1, 'TWO' => 2, 'STR' => 'sth']

SampleEnum::keys(); // ['UNO', 'ONE', 'TWO', 'STR'];

SampleEnum::values(); // [1, 1, 2, 'sth']

SampleEnum::hasKey('ONE'); // true

SampleEnum::hasKey('xXx'); // false

SampleEnum::hasValue(2); // true

SampleEnum::hasValue('xXx'); // false

SampleEnum::valueOf('ONE'); // 1

SampleEnum::keysOf(1); // ['UNO', 'ONE']

SampleEnum::keyOf(1); // 'UNO'

SampleEnum::randomKey(); // One of 'UNO', 'ONE', 'TWO', 'STR'

SampleEnum::randomKeyExceptKeys(['ONE', 'TWO']); // One of 'UNO', 'STR'

SampleEnum::randomKeyExceptValues([SampleEnum::STR, SampleEnum::TWO]); // One of 'ONE', 'UNO'

SampleEnum::randomValue(); // One of 1, 2, 'sth'

SampleEnum::randomValueExceptValues([SampleEnum::STR, SampleEnum::TWO]); // One of SampleEnum::ONE, SampleEnum::UNO

SampleEnum::randomValueExceptKeys(['STR', 'TWO']); // One of SampleEnum::ONE, SampleEnum::UNO
```