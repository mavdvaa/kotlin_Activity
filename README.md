Вывод: 
---------------------------- PROCESS STARTED (6536) for package com.example.birthday ----------------------------
2026-03-15 15:56:43.771  6536-6536  LifecycleDemo           com.example.birthday                 D  onCreate: Activity создана
2026-03-15 15:56:43.815  6536-6536  LifecycleDemo           com.example.birthday                 D  onStart: Activity видна
2026-03-15 15:56:43.823  6536-6536  LifecycleDemo           com.example.birthday                 D  onResume: Activity в фокусе
2026-03-15 15:56:50.878  6536-6536  LifecycleDemo           com.example.birthday                 D  onPause: Activity приостановлена
2026-03-15 15:56:50.885  6536-6536  LifecycleDemo           com.example.birthday                 D  onStop: Activity скрыта
2026-03-15 15:56:50.918  6536-6536  LifecycleDemo           com.example.birthday                 D  onDestroy: Activity уничтожена
2026-03-15 15:56:50.970  6536-6536  LifecycleDemo           com.example.birthday                 D  onCreate: Activity создана
2026-03-15 15:56:50.983  6536-6536  LifecycleDemo           com.example.birthday                 D  onStart: Activity видна
2026-03-15 15:56:50.988  6536-6536  LifecycleDemo           com.example.birthday                 D  onResume: Activity в фокусе
2026-03-15 15:56:53.108  6536-6536  LifecycleDemo           com.example.birthday                 D  onPause: Activity приостановлена
2026-03-15 15:56:53.113  6536-6536  LifecycleDemo           com.example.birthday                 D  onStop: Activity скрыта
2026-03-15 15:56:53.128  6536-6536  LifecycleDemo           com.example.birthday                 D  onDestroy: Activity уничтожена
2026-03-15 15:56:53.175  6536-6536  LifecycleDemo           com.example.birthday                 D  onCreate: Activity создана
2026-03-15 15:56:53.184  6536-6536  LifecycleDemo           com.example.birthday                 D  onStart: Activity видна
2026-03-15 15:56:53.185  6536-6536  LifecycleDemo           com.example.birthday                 D  onResume: Activity в фокусе
2026-03-15 15:56:55.946  6536-6536  LifecycleDemo           com.example.birthday                 D  onPause: Activity приостановлена
2026-03-15 15:56:57.121  6536-6536  LifecycleDemo           com.example.birthday                 D  onStop: Activity скрыта
2026-03-15 15:56:57.135  6536-6536  LifecycleDemo           com.example.birthday                 D  onDestroy: Activity уничтожена
2026-03-15 15:57:06.142  6536-6536  LifecycleDemo           com.example.birthday                 D  onCreate: Activity создана
2026-03-15 15:57:06.173  6536-6536  LifecycleDemo           com.example.birthday                 D  onStart: Activity видна
2026-03-15 15:57:06.175  6536-6536  LifecycleDemo           com.example.birthday                 D  onResume: Activity в фокусе
2026-03-15 15:57:14.792  6536-6536  LifecycleDemo           com.example.birthday                 D  onPause: Activity приостановлена
2026-03-15 15:57:14.822  6536-6536  LifecycleDemo           com.example.birthday                 D  onStop: Activity скрыта
2026-03-15 15:57:50.806  6536-6536  LifecycleDemo           com.example.birthday                 D  onRestart: Activity перезапущена
2026-03-15 15:57:50.807  6536-6536  LifecycleDemo           com.example.birthday                 D  onStart: Activity видна
2026-03-15 15:57:50.808  6536-6536  LifecycleDemo           com.example.birthday                 D  onResume: Activity в фокусе
---------------------------- PROCESS ENDED (6536) for package com.example.birthday ----------------------------

логи (onCreate: Activity создана, onStart: Activity видна, onResume: Activity в фокусе) - запуск приложения. 
логи (onPause: Activity приостановлена, onStop: Activity скрыта, onDestroy: Activity уничтожена, onCreate: Activity создана, onStart: Activity видна, onResume: Activity в фокусе) - при повороте экрана, так как уничтожается старая Activity и создается новая.
логи (onPause: Activity приостановлена, onStop: Activity скрыта) - при сворачивании приложения нажатием на кнопку Home. логи (onRestart: Activity перезапущена, onStart: Activity видна, onResume: Activity в фокусе) - при открытии приложения из начального экрана.

При добавлении finish():
---------------------------- PROCESS STARTED (6688) for package com.example.birthday ----------------------------
2026-03-15 15:59:32.134  6688-6688  LifecycleDemo           com.example.birthday                 D  onCreate: Activity создана
2026-03-15 15:59:33.370  6688-6688  LifecycleDemo           com.example.birthday                 D  onDestroy: Activity уничтожена
2026-03-15 16:00:17.390  6688-6688  LifecycleDemo           com.example.birthday                 D  onCreate: Activity создана
2026-03-15 16:00:18.020  6688-6688  LifecycleDemo           com.example.birthday                 D  onDestroy: Activity уничтожена
2026-03-15 16:00:22.421  6688-6688  LifecycleDemo           com.example.birthday                 D  onCreate: Activity создана
2026-03-15 16:00:23.021  6688-6688  LifecycleDemo           com.example.birthday                 D  onDestroy: Activity уничтожена

Так как добавлен finish(), Activity сразу завершается и не переходит в другие состояния.
