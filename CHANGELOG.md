# 1.4.0 (10/13/2016)

* Optimizations to the diffing algorithm
* Setters on generated classes are not created if an @EpoxyAttribute field is marked as `final`
* Adds @EpoxyModelClass annotation to force a model to have a generated class, even if it doesn't have any @EpoxyAttribute fields
* Fix to not generate methods for package private @EpoxyAttribute fields that are in a different package from the generated class
* Have generated classes duplicate any super methods that have the model as the return type to help with chaining

# 1.3.0 (09/15/2016)

* Add support for using the view holder pattern with models. See the readme for more information.
* Throw an exception if `EpoxyAdapter#notifyDataSetChanged()` is called when diffing is enabled. It doesn't make sense to allow this alongside diffing, and calling this is most likely to be an accidental mixup with `notifyModelsChanged()`.
* Some performance improvements with the diffing algorithm.

# 1.2.0 (09/07/2016)

* Change signature of `EpoxyAdapter#onModelBound` to include the model position
* Fix EpoxyModel hashcode to include the layout specified by `getDefaultLayout`
* Enforce that the id of an `EpoxyModel` cannot change once it has been added to the adapter
* Add optional hash parameter to the `EpoxyAttribute` annotation to exclude a field from being included in the generated hashcode method.

# 1.1.0 (08/24/2016)

* Initial release
