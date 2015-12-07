# Symfony Kernel Traits

Symfony 2.8 has that new [Microkernel trait](http://symfony.com/blog/new-in-symfony-2-8-symfony-as-a-microframework) and
this package contains some other simple traits that can support development of simple Symfony Kernel applications.

Using these traits effectively probably requires you to store configuration in the environment with [`SYMFONY__` prefixed
envrionment variables](http://symfony.com/doc/current/cookbook/configuration/external_parameters.html).

## `ClassBasedNameTrait`

Use this trait in your kernel to base the kernel's name on its class name instead of its directory.

## `VariableFilesystemTrait`

Use this trait in your kernel to store cache and logs in the Symfony 3 standard `var` location. If you have multiple
kernels in the same directory, you will need to use `ClassBasedNameTrait` to avoid conflicts.

## `YamlEnvironmentTrait`

Use this trait in your kernel to parse environment variables as YAML before populating the container parameters.

## `StandardConfigTrait` and `MinimalConfigTrait`

These two traits are probably not useful in any real sense, but they demonstrate how to sustain a Symfony Standard
configuration with the microkernel trait and the bare minimum required to instantiate the kernel and framework, respectively.
