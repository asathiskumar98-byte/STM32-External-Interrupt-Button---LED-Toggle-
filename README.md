# STM32 External Interrupt (Button - LED Toggle)

This project demonstrates how to use an **External Interrupt (EXTI)** to control an LED using a **push button** on the STM32F446RE Nucleo board.

---

## ⚙️ Description
- When the **user button (PC13)** is pressed, it triggers an **EXTI interrupt**.
- Inside the **interrupt handler**, the **LED (PA5)** toggles its state.
- The LED remains in its toggled state until the next button press.
- The project is developed using **STM32CubeIDE** and **HAL libraries**.

---

## 🧰 Hardware Setup

| Pin  | Function | Description            |
|------|-----------|------------------------|
| PC13 | Input     | User button (EXTI)     |
| PA5  | Output    | LED (active HIGH)      |

---

## 🧩 Key Files

| File | Description |
|------|--------------|
| **main.c** | Initializes GPIO and configures EXTI |
| **stm32f4xx_it.c** | Handles the interrupt (toggles LED) |
| **main.h** | Header file for main source |
| **stm32f4xx_it.h** | Interrupt declarations |
| **STM32_Button_LED_Interrupt.ioc** | Pin & clock configuration file |

---

## 🚀 How to Build and Run
1. Open the project in **STM32CubeIDE**.
2. Connect your **Nucleo STM32F446RE** board.
3. Build → Debug → Run.
4. Press the blue **USER button** → observe LED toggle (PA5).

---

## 🧾 License
This project follows the STMicroelectronics software license included in the `LICENSE` file.

---

## 🧠 Bonus Tip
You can add **software debounce** by adding a small delay inside the interrupt handler, or better — use a **timer-based debounce** to make it more reliable.
