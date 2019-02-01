# `ldap` on PyPI

This dummy project is not installable.
You want `python-ldap` or `ldap-utils` instead.


## python-ldap

The widely used [python-ldap](https://python-ldap.org) project provides
an importable module named `ldap`.

This goes against the convention that PyPI distribution names should
match the module names.
But, python-ldap pre-dates wide use of that convention, and it's hard
to fix now.

Please install `python-ldap` to get the LDAP bindings.


## ldap-utils

The `ldap` name on PyPI was used for an unrelated collection of
LDAP-related utilities, which is not as popular, and confused users who
install `ldap` to get the `ldap` module.

Please install `ldap-utils` to get that package.


# Why we don't fix this transparently

This could have been a package that depends on `python-ldap`, saving
you the trouble of reading this message.

However, `pip` [has trouble]() with differently-named package that
provide the same module.


# Please: Don't install packages blindly

When you see the exception:

```
ModuleNotFoundError: No module named 'foo'
```

… please research the actual requirements instead of going directly for
`pip install foo`.
The project (distribution) name may differ from the module(s) it
provides.
