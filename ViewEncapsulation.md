# View Encapsulation and Shadow DOM

One of instance members of `ComponentMetaData` or `ViewMetaData` is `encapsulation`. Its data type is `ViewEncapsulation` enum and is defined like below in Angular code.

```
export enum ViewEncapsulation {
  Emulated,
  Native,
  None
}
```

### Consideration to choose 3rd party components

Angular 2 comes with view encapsulation built in, which means it supports for native Shadow DOM or emulate it unless `None` is given in the meta data.
It will end up to have `scoped style`. Why then should it be considered? 
In my opinion, it should be considered when we try to use 3rd party components in Angular 2 projects from style's point of view. 
Most of companies have their own style guide like color theme, font and so on. Sometimes 3rd party libs might not fit with the guideline. 
In that case, we usually tried to overwrite its style.
In Angular 2, however it supports for scoped style with Shadow DOM so that it might be hard to overwrite its styles unless they provide external style files.

### References

* [View Encapsulation in Angular 2](http://blog.thoughtram.io/angular/2015/06/29/shadow-dom-strategies-in-angular2.html)
