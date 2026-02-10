# DI.Swift

Swift DI by Antoine Van der Lee

Example

```Swift
private struct LocationAuthServiceKey: InjectionKey {
    static var currentValue: LocationAuthServiceProvider = LocationAuthService()
}

extension InjectedValues {
    var locationAuthService: LocationAuthServiceProvider {
        get { Self[LocationAuthServiceKey.self] }
        set { Self[LocationAuthServiceKey.self] = newValue }
    }
}
```
