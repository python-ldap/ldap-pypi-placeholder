# `ldap` on PyPI

This dummy project is not installable.
You probably want `python-ldap` instead.


### python-ldap

The widely used [python-ldap](https://python-ldap.org) project provides
an importable module named `ldap`.

This goes against the convention that PyPI distribution names should
match the module names.
But, python-ldap pre-dates wide use of that convention, and the issue
is hard to fix now.

Please install `python-ldap` to get the LDAP bindings.


### ldap 1.0

The `ldap` name on PyPI was used for an unrelated collection of
LDAP-related utilities, which is not as popular, and confused users who
install `ldap` to get the `ldap` module.

The project is no longer developed.
It is archived as `1.0.x` releases on PyPI, and on
[GitHub](https://github.com/andreif/ldap).


## Why we don't fix this transparently

This could have been a placeholder  package that depends on `python-ldap`,
saving you the trouble of reading this message.

However, `pip` [has trouble](https://github.com/pypa/pip/issues/4961)
with differently-named packages that provide the same module.


## Please: Don't install packages blindly

When you see the exception:

```
ModuleNotFoundError: No module named 'foo'
```

… please research the actual requirements instead of going directly for
`pip install foo`.
The project (distribution) name may differ from the module(s) it
provides.
