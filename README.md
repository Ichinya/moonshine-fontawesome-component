# MoonShine FontAwesomeIcon Field for [MoonShine Laravel admin panel](https://moonshine-laravel.com)

![PHP](https://img.shields.io/badge/PHP-^8.2-blue.svg?style=flat)

### Requirements

- MoonShine v3.0+

| MoonShine | FontAwesomeIcon |
|-----------|-----------------|
| 2.0+      | 1.0+            |
| 3.0+      | 1.1+            |

## Installation

```bash
composer require ichinya/moonshine-fontawesome-field
```

## Usage

You can use `FontAwesome` field in your resources:

```php
<?php

declare(strict_types=1);

use Ichinya\FontAwesome\Components\FontAwesome;

use MoonShine\Laravel\Resources\ModelResource;

/**
 * @extends ModelResource<Custom>
 */
class CustomResource extends ModelResource
{
    public function fields(): array
    {
        return [
             Select::make('Тип', 'type')->options([
//                    TelegramBot::class => FontAwesome::make('<i class="fa-brands fa-telegram"></i>' , 'blue'),
                    TelegramBot::class =>  Badge::make(FontAwesome::make('<i class="fa-brands fa-telegram"></i>' , 'blue') . 'Telegram', 'blue'),

                ]),
        ];
    }
}
```

## Plans

* Macros to Fields.
* fa-brands fa-telegram => telegram
* Add more customization options for the FontAwesome field.

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.
