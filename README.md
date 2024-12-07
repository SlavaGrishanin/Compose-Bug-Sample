This App crashes with the exception:
```
java.lang.IllegalStateException: Restoring the Navigation back stack failed: destination 132070424 cannot be found from the current destination ComposeNavGraph(0x0) startDestination={Destination(0xe362b7e) route=com.example.typesafenavigation.Login}
```
#### Video demonstration: [compose_crash.webm](compose_crash.webm)
#### https://youtube.com/shorts/u7pN7vgOSAE

Way to reproduce exception:
1. In "Developer options" set "Background process limit" to "No background processes".
2. Open App below
3. Minimize App below and open 2 other apps
4. Open App below again
5. App below crashes with the exception

What is interesting is that App does not throw this exception if:
- ComponentActivity is used instead of AppCompatActivity
- Plain Strings is used for route instead of type safe Object
