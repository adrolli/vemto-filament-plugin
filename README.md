# Vemto Plugin prepared for Filament V3

This is the Vemto Plugin for MOOX. We made few changes to be able to use the Filament V3 updater:

- MultiSelectFilter -> SelectFilter->multiple()
- Streamline use statements to be fetched by Rector (Filament V3 update)
- Add default edit, create, delete actions in pages and tables

After generating the App, you can update the resources like so:

```bash
composer require filament/upgrade:"^3.0-stable" -W --dev
vendor/bin/filament-v3
```

If you want to update the complete App, remove or update the Livewire dependency in your composer.json and do:

```bash
composer require filament/filament:"^3.0-stable" -W
php artisan filament:install
composer remove filament/upgrade
```

Last remove the `implements FilamentUser` from the user model.
