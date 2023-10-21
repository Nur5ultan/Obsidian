---
tags: customtkinter
---

### Создайте виджеты из фрейма
Если вы хотите создавать новые виджеты самостоятельно, потому что вам нужно что-то, что не реализовано в Customtkinter, вы можете легко это сделать. Далее я создал Spinbox на основе значений с плавающей точкой.

Сначала вы создаете новый класс, который наследуется от `customtkinter.CTkFrame`:
```python
import customtkinter

class WidgetName(customtkinter.CTkFrame):
    def __init__(self, *args,
                 width: int = 100,
                 height: int = 32,
                 **kwargs):
        super().__init__(*args, width=width, height=height, **kwargs)
```

Делая это, у вас уже есть виджет, размер которого задается значениями атрибутов width и height по умолчанию. И он также поддерживает все атрибуты CTkFrame, такие как fg_color и corner_radius.

### Создайте spinbox из фрейма[](https://customtkinter.tomschimansky.com/tutorial/spinbox#create-spinbox-from-frame "Прямая ссылка для создания spinbox из фрейма")

Простая реализация Spinbox на основе float может выглядеть следующим образом:
```python
class FloatSpinbox(customtkinter.CTkFrame):
    def __init__(self, *args,
                 width: int = 100,
                 height: int = 32,
                 step_size: Union[int, float] = 1,
                 command: Callable = None,
                 **kwargs):
        super().__init__(*args, width=width, height=height, **kwargs)

        self.step_size = step_size
        self.command = command

        self.configure(fg_color=("gray78", "gray28"))  # set frame color

        self.grid_columnconfigure((0, 2), weight=0)  # buttons don't expand
        self.grid_columnconfigure(1, weight=1)  # entry expands

        self.subtract_button = customtkinter.CTkButton(self, text="-", width=height-6, height=height-6,
                                                       command=self.subtract_button_callback)
        self.subtract_button.grid(row=0, column=0, padx=(3, 0), pady=3)

        self.entry = customtkinter.CTkEntry(self, width=width-(2*height), height=height-6, border_width=0)
        self.entry.grid(row=0, column=1, columnspan=1, padx=3, pady=3, sticky="ew")

        self.add_button = customtkinter.CTkButton(self, text="+", width=height-6, height=height-6,
                                                  command=self.add_button_callback)
        self.add_button.grid(row=0, column=2, padx=(0, 3), pady=3)

        # default value
        self.entry.insert(0, "0.0")

    def add_button_callback(self):
        if self.command is not None:
            self.command()
        try:
            value = float(self.entry.get()) + self.step_size
            self.entry.delete(0, "end")
            self.entry.insert(0, value)
        except ValueError:
            return

    def subtract_button_callback(self):
        if self.command is not None:
            self.command()
        try:
            value = float(self.entry.get()) - self.step_size
            self.entry.delete(0, "end")
            self.entry.insert(0, value)
        except ValueError:
            return

    def get(self) -> Union[float, None]:
        try:
            return float(self.entry.get())
        except ValueError:
            return None

    def set(self, value: float):
        self.entry.delete(0, "end")
        self.entry.insert(0, str(float(value)))
```

Конечно, вы могли бы добавить метод configure или несколько атрибутов для настройки цветов в методе init.

Но с помощью приведенной выше реализации вы можете использовать spinbox следующим образом:
```python
app = customtkinter.CTk()

spinbox_1 = FloatSpinbox(app, width=150, step_size=3)
spinbox_1.pack(padx=20, pady=20)

spinbox_1.set(35)
print(spinbox_1.get())

app.mainloop()
```

[[Python/customtkinter]]