In our boilerplate, you can use the widget like this:

```dart
    MaterialApp.router(
          routerConfig: _appRouter.config(),
          title: 'Boilerplate code',
          theme: AppTheme.lightTheme,
          themeMode: themeMode,
          localizationsDelegates: context.localizationDelegates,
          supportedLocales: context.supportedLocales,
          locale: context.locale,
          builder: (BuildContext context, Widget? widget) {
            ErrorWidget.builder = (details) {
              return ErrorScreen(details: details);
            };
            return InternetWidget(
              offline: const FullScreenWidget(
                child: NoInternetScreen(),
              ),
              online: widget!,
            );
          },
          debugShowCheckedModeBanner: false,
        )
```