1. Add the package to your `pubspec.yaml` like this:
```yaml
  flutter_form_bloc:
    git:
      url: https://github.com/Cavin6080/form_bloc.githttps://github.com/cavin-7span/7span-packages-flutter.git
      path: packages/flutter_no_internet_widget
```


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
                // This child is your custom widget that you want to show
                child: NoInternetScreen(),
              ),
              online: widget!,
            );
          },
          debugShowCheckedModeBanner: false,
        )
```