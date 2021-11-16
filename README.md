# do-it-break

It do!

(This is a minimal reproduction of https://github.com/babel/ember-cli-babel/issues/419)

Clone and `ember s`; as soon as it hits tracked-built-ins, you'll see this output:

```
Build Error (broccoli-persistent-filter:Babel > [Babel: tracked-built-ins]) in tracked-built-ins/-private/object.js

/Users/ckrycho/dev/test/do-it-break/tracked-built-ins/-private/object.js: Class private methods are not enabled.
  65 |
  66 |   // @private
> 67 |   #readStorageFor(key) {
     |   ^
  68 |     let storage = this.#storages.get(key);
  69 |
  70 |     if (storage === undefined) {


Stack Trace and Error Report: /var/folders/bw/k3jm2wf96p390m_k4jmhwm5c001321/T/error.dump.d6809848bc20bdeb895ea95b03bfbf87.log
```
