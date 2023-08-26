# Vemto Plugin prepared for Filament V3

Changes:

- MultiSelectFilter -> SelectFilter->multiple()
- streamline use Statements to be fetched by Rectory (Filament V3 update)
- Add default edit, create, delete actions in pages and tables

Then do:

```bash
composer require filament/upgrade:"^3.0-stable" -W --dev
vendor/bin/filament-v3
```

Remove or update the Livewire dependency in your composer.json

```bash
composer require filament/filament:"^3.0-stable" -W
php artisan filament:install
composer remove filament/upgrade
```

and remove the `implements FilamentUser` from the user model.
