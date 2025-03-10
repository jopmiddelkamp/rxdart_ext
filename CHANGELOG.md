## 0.1.3 - Nov 23, 2021

- Update `rxdart` to `0.27.3`.
- Refactor `NotReplayValueConnectableStream` and `StateConnectableStream` by using `rxdart`'s `AbstractConnectableStream`.
- Add `StateStream.asBroadcastStateStream` extension method.
- Add `Future<void> delay(int milliseconds)` function.

## 0.1.2 - Sep 11, 2021

- Update dependencies
    - `rxdart` to `0.27.2` 
    - `meta` to `1.7.0`
- Split into multiple libraries:
    - `not_replay_value_stream`
    - `operators`
    - `single`
    - `state_stream`
    - `utils`
    - `rxdart_ext`: includes all the above.
- **utils**: Add `Sink<void>.addNull()` extension.
- **state_stream**:
    - Add `StateStream`
    - Add `StateSubject`.
    - Add `StateConnectableStream`, `Stream.publishState()`, `Stream.shareState()`.
- **single**: Add `Single.retry()`.
- **operators**:
    - Add `Stream.doneOnError()`.
    - Add `Stream.flatMapBatches()`.
    - Add `Stream.flatMapBatchesSingle()`.
- Internal: migrated from `pedantic` to `lints`.

## 0.1.1 - Jul 8, 2021

- Stable release: see change logs of `0.1.1-dev.x` versions.
    - **Add `Single` type.**
    - Operators refactoring.

## 0.1.1-dev.3 - Jul 7, 2021

- Add `Single.asVoid`.
- Refactoring operators.

## 0.1.1-dev.2 - Jul 5, 2021

- Add `Single.mapTo`.
- Refactoring operators.

## 0.1.1-dev.1 - Jun 10, 2021

- Change return type of `Stream.ignoreElements()` to `Stream<Never>`.
- Refactor `Single`
    - Add `Single.fromStream`.
    - Remove `Single.zip2` (move to `RxSingles`).
    - Add operators
        - `debug`.
        - `doOnCancel`.
        - `doOnData`.
        - `doOnError`.
        - `doOnListen`.
        - `onErrorResumeNextSingle`.
        - `onErrorResumeSingle`.
        - `onErrorReturn`.
        - `onErrorReturnWith`.
    - Add `RxSingles`
        - `zip2`.
        - `forkJoin2`.

## 0.1.1-dev.0 - May 14, 2021

- **Add `Single`.**

## 0.1.0 - May 7, 2021

- Support `rxdart: ^0.27.0`.
- Add `asVoid`.

## 0.0.1 - Feb 28, 2021

- Add `doOn` extension.
- Update dependencies to latest version.

## 0.0.1-nullsafety.7 - Feb 8, 2021

- Add `whereNotNull`.
- Update `ignoreElements` and `ignoreErrors`.
- Update `ForwardingSinkMixin`.
- Rename `ListenNullStreamExtension` to `CollectStreamExtension`.
- Update docs.

## 0.0.1-nullsafety.6 - Jan 31, 2021

- Enhance `debug` operator: prints current stacktrace, including location, line and member if not provide the
  identifier (ie. it is `null`).

## 0.0.1-nullsafety.5 - Jan 31, 2021

- Added `ValueStreamController`: like a single-subscription `StreamController` except the stream of this controller is a
  single-subscription `NotReplayValueStream`.
- Added `toNotReplayValueStream` extension: converts a `Stream` to a single-subscription `NotReplayValueStream`.

## 0.0.1-nullsafety.4 - Jan 23, 2021

- Now, return type of `collect`  is `StreamSubscription<T>`.

## 0.0.1-nullsafety.3 - Jan 21, 2021

- Added `distinctBy`.
- Removed generic type of `CollectStreamSubscription`.

## 0.0.1-nullsafety.2 - Jan 08, 2021

- Update dependency: `rxdart: ^0.26.0-nullsafety.1`.

## 0.0.1-nullsafety.1 - Dec 24, 2020

- Fix missing exports.

## 0.0.1-nullsafety.0 - Dec 24, 2020

- Initial version.
