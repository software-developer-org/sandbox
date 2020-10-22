# **Semantic Versioning**
(according to [Semantic Versioning 2.0.0](https://semver.org/))

## **What is Semantic Versioning?**

> Under this scheme, version numbers and the way they change convey meaning about the underlying code and
what has been modified from one version to the next.
>
> > 1. **MAJOR version when you make incompatible API changes,** 
> > 2. **MINOR version when you add functionality in a backwards compatible manner, and**
> > 3. **PATCH version when you make backwards compatible bug fixes.**

### **Applying the 'X.Y.Z'-scheme on an example**

**'Version 1.9.0'**

- **'1'**
  - Major version -> the declared public API
  - if its 0, initial development, API should not be considered as stable
  - incremented if any backwards _incompatible_ changes are introduced to the public API
  - Minor _and_ Patch version MUST be reset to 0 when major version is incremented
- **'9'**
  - Minor version
  - incremented if new, backwards _compatible_ functionality is introduced to the public API
  - incremented if any public API functionality is marked as deprecated
  - Patch version MUST be reset to 0 when minor version is incremented
- **'0'**
  - Patch version
  - incremented if only backwards compatible bug fixes are introduced
  - (bug fix is defined as an internal change that fixes incorrect behavior)
   
## **Why Semantic Versioning?**

The format of marking and structuring software versions arises through the necessity to manage and compare
systems with a lot of packages and their dependencies.
