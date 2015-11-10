* Changes in 2.0
- Breaking changes to the base Random Op and the Sample Op will break existing experiment / namespace assignments. If you wish to upgrade but keep these old changes you can toggle compatibility mode using ```ExperimentSetup.toggleCompatibleHash(true)```. One valid reason for not upgrading is that this will be incompatible with assignments generated by other PlanOut implementations so if you are using PlanOut cross-platform then you will want to keep this flag on. Otherwise, it is recommended to use non-compatibility mode since it is substantially faster.

* Changes in 1.3
- PlanOut.js now comes packaged with an ExperimentSetup utility that allows the registering of inputs to an experiment after the experiment has already been defined. It currently only works with the Namespace class.

* Changes in 1.2.3
- Exposure now only gets logged on the get function call if it is a valid parameter as defined by getParamNames() 

* Changes in 1.2
- The return value of assign now determines whether or not an exposure event will
  be automatically logged. If either a truth-y value or nothing is returned from assign, then exposure
  will be logged. If a false-y value (excluding undefined) is returned then exposure will not be logged.

-getParams(experimentName) is now a function on the namespace class 