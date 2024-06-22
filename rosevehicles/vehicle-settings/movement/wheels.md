---
description: Settings physics wheels for vehicle
---

# Wheels

```yaml
Wheels:
  Default_Settings:
    Radius: 0.8 #Радиус колеса в метрах мб
    Model_Radius: 0.34 #радиус колеса на текстуре
    Width: 0.3 #Ширина колеса
    Axle_Direction: "-1 0 0"
    Steering: UNUSED #Какое у нас колесо? Рулевое, ленивое, отзеркаленное.
    Engine_Fraction: 0.2
    Friction_Slip: 1.0 #трение между шиной. Коеффициент.
    Roll_Influence: 0.5 #Коэффициент влияния на крен (Опрокидывание крч)
    Extra_Damping: 0.04
    Brake: 1000
    Skid:
      Start_When: 0.1
      Particles:
        - "CAMPFIRE_SIGNAL_SMOKE 3 0.0 0.0 0.0 0.0"
    Suspension: #Подвеска
      Max_Force: 5000.0 #Сила подвески
      Rest_Length: 0.4 #Длина подвески
      Stiffness: 2.3 #Жесткость подвески.
      Max_Travel: 1400.0 #Максимальный ход подвески в см.
      Direction: "0.0 -1.0 0.0" #Направление подвески
      Damping: #демпфирование подвески колеса
        Compression: 0.5 #Демпфирование колеса при сжатии подвески
        Relaxation: 0.4 #Демпфирование колеса при расширении подвески
    Rotate: #Поворот колеса
      Enable: false #Включен ли поворот колеса
      Speed: 0.0 #deg/sec Скорость поворота
      Speed_Reset: 0.0 #deg/sec Скорость возвращения колеса
      Max_Angle: 0.0 #deg Максимальный поворот

  wheel_1:
    Offset: "0.86 0.0 1.75" #Локация колеса. В каком месте транспорта оно.
    Steering: UNUSED
    Brake: 500
    Rotate: #Поворот колеса
      Enable: true #Включен ли поворот колеса
      Max_Angle: 38.0 #deg Максимальный поворот

  wheel_2:
    Offset: "-0.86 0.0 1.75" #Локация колеса. В каком месте транспорта оно.
    Steering: UNUSED
    Brake: 500
    Rotate: #Поворот колеса
      Enable: true #Включен ли поворот колеса
      Max_Angle: 38.0 #deg Максимальный поворот

  wheel_3:
    Offset: "0.86 0.0 -1.75" #Локация колеса. В каком месте транспорта оно.
    Brake: 1000
    Steering: DIRECT

  wheel_4:
    Offset: "-0.86 0.0 -1.75" #Локация колеса. В каком месте транспорта оно.
    Brake: 1000
    Steering: DIRECT
```
