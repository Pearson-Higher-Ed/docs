# Frequently Aasked Questions

This is not currently an official FAQ but can become one once enough teams have
integrated the SDKs into their workflows, based on queries in the PDA HELP
chatroom on HipChat.


## Auth

> When I try to get a component through `npm install` I get the following error:

```
[ERROR] npm ERR! Could not authenticate admin : @pearson-components/[component-name]
```

If it's a public component, it shouldn't require any authentication to be 
installed into your project.

Your .npmrc file should contain the following:

```
registry=http://registry.npmjs.org/
config=0
progress=false
```

and if this line is in your .npmrc file:

```
always-auth: true
```

either set it to false, or remove it entirely. Otherwise you may get errors such as

```
[ERROR] npm ERR! 404 User not found : @pearson-components/<component name>
```

It's possible that you have a root npmrc file overriding the local one.
Check that you only have the local npmrc file involved.


## Fonts don't load in Internet Explorer (or they do, but vanish on refresh)

Various caching headers are known to cause IE some trouble with external files
like fonts. The usual culprits are

* `cache-control: no-store`
* `Pragma: no-cache` (on https)

## Next...

