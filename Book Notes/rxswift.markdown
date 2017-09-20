## RxSwift - Reactive Programming With Swift
by raywenderlich.com

### Section 1: Getting Started with RxSwift
* In its essence, RxSwift simplifies developing asynchronous programs by allowing your code to react to new data and process it in sequential, isolated manner.
* RxSwift solves the problem of different syntax in asynchronous API's offered by Apple's SDK such as delegates, closures, NotificationCenter and so on.
* Core issues with writing asynchronous code are: a) order in which pieces of work are performed and b) shared mutable data.
* In general, RxSwift tries to address the following issues:
  * State, specifically - mutable state.
  * Imperative programming - you use it to tell the app exactly when and how to do things. All the CPU does is follow lengthy sequences of simple instructions.
  * Side effects - ie. any change to the state outside of the current scope.
  * Declarative code - you can work with asynchronous code, but make the same assumptions as in a simple for loop: that you're working with immutable data and you can execute code in sequential, deterministic way.
  * Reactive systems - always keep the UI up to date.

### Foundation of RxSwift
* Reactive programming isn't a new concept - Microsoft introduced server side framework called Reactive Extensions for .NET (Rx). Later, it became a built-in core library in .NET 4.0. Since 2012, it is an open source component. This allowed other languages to reimplement the same functionality, which turned Rx into a cross-platform standard.
* Observables:
  * Observable<T> provides the foundation of RxCode: it allows one or more observers to react to any events in real time and update the app UI.
  * Observable<T> conforms to protocol ObservableType, and it contains only three types of events:
    * Next event - event which carries the latest ("next") data value. This is the way observers receive value.
    * Completed event - event which terminates the event sequence with success. It means Observable completed its life-cycle and won't emit any other events.
    * Error event - Observable terminates with an error and it will not emit other events.
* Operators:
  * You can apply Rx operators to the pieces of input emitted by an Observable to deterministically process inputs and outputs until the expression has been resolved to a final value, which you can then use to cause side effects. 
  Example:
    UIDevice.rx.orientation
      .filter { value in
        return value != .landscape
      }
      .map { _ in
        return "Portrait is the best"
      }
      .subscribe(onNext: { string in
        showAlert(text: string)
        })
* Schedulers
  * These are the Rq equivalent of dispatch queues - on steroids and much easier to use.
  * You can schedule different pieces of work of the same subscription on different schedulers to achieve the best performance.

* You don't have to start a project from scratch to make it a reactive app; you can iteratively refactor pieces of existing project, or use RxSwift when appending new features to your app.
* MVVM and RxSwift do play nicely together.

* Since RxSwift doesn't know anything about any Cocoa or UIKit-specific classes, there is RxCocoa holding all classes that specifically aid development for UIKit and Cocoa. It adds reactive extensions to many UI components so that you can subscribe for various UI events out of the box.
*
