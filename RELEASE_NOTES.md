# Release Notes v1.1.0 – Order Billing Service 
## 🚀 Added - Спеціальна базова ставка доставки для міста Київ (`80.0 UAH`). 
- Явна передача параметру \`tax\_rate\` зі значенням за замовчуванням \`0.20\`.

- ## 🔄 Changed - Збільшено коефіцієнт розрахунку доставки за вагу з \`12.0\` до \`15.0 UAH/кг\`.
- Проведено рефакторинг зв'язності модуля \`billing.py\` (перехід до Data Coupling).

## ⚠️ Breaking Changes - Видалено глобальну змінну \`GLOBAL\_TAX\_RATE\` (Common Coupling). 
- Змінено сигнатуру функції \`calculate\_delivery\_cost\`
— замість об'єкта \`CustomerProfile\` приймаються примітиви \`city\` та \`weight\_kg\` (Stamp Coupling).
- Розділено функцію з прапорцем \`mode\_flag\` на дві окремі функції \`process\_standard\_invoice\` та \`process\_tax\_exempt\_invoice\` (Control Coupling).
