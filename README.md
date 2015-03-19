# Firestead

[Laravel Homestead](https://github.com/laravel/homestead) simplified and per-project based.

## Why Firestead?

Homestead is really awesome but recently they have changed direction and now it's a PHP/Composer Project, and works as a single VM for all your projects, which is great for some cases, but for other, not really.

If you are like me and likes to have separated VMs for each projects, **Firestead** is for you.

## Is it different from Homestead?

Not really, **Firestead** basicallly uses all generated files from Homestead and moves them all to a single folder, so it don't pollute your project repository.

## How to?

#### 1. Add Laravel Homestead Box

````bash
vagrant box add laravel/homestead
````

#### 2. Clone Firestead

````bash
git clone https://github.com/dbpolito/firestead.git
````

#### 3. Have Fun! :)

````bash
cd firestead
vagrant up
````
