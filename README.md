# Aprinderea și Stingerea Treptată a LED-urilor (Efect Fade-In / Fade-Out) 💡

Acest depozit conține sursele și documentația pentru un proiect de design digital/FPGA ce implementează un efect vizual de tip **fade-in** și **fade-out** pe un set de LED-uri. Proiectul permite reglarea perioadei de tranziție (viteza efectului) și este conceput pentru a rula pe o placă de dezvoltare cu FPGA (ex. **Basys 3**).

## 📁 Structura Repository-ului

- **`fsm.vhd`** - Fișierul sursă VHDL principal, conținând mașina de stări (Finite State Machine - FSM) și logica de control (PWM) pentru intensitatea LED-urilor.
- **`inteligent.xdc`** / **`basys3_master.txt`** - Fișierele de constrângeri (XDC) utilizate pentru a mapa porturile logice din cod pe pinii fizici ai plăcii FPGA Basys 3.
- **`fade_final_TOP.txt`** - Modulul Top-Level al proiectului.
- **`project_2/`** - Director ce conține fișierele specifice mediului de dezvoltare (ex. Vivado).
- **`Teme proiect II.pdf`** & **`Proiect.txt`** - Cerințele și documentația/raportul proiectului.
- **`1.jpg`, `2.jpg`, `3.jpg`, `4.jpg`** - Imagini cu demonstrarea funcționării, schema bloc sau setup-ul fizic.

## 🛠️ Tehnologii și Hardware Utilizat

* **Limbaj de descriere hardware (HDL):** VHDL
* **Placă de dezvoltare:** Digilent Basys 3 (FPGA Xilinx Artix-7)
* **Mediu de dezvoltare (IDE):** Xilinx Vivado

## 📖 Descrierea Proiectului

Proiectul folosește un semnal **PWM (Pulse Width Modulation)** a cărui valoare a factorului de umplere (duty cycle) este incrementată și decrementată continuu cu ajutorul unui contor și al unei Mașini cu Stări Finite (FSM). 
Acest lucru permite:
1. Creșterea treptată a intensității luminoase a LED-urilor (Fade-In).
2. Scăderea treptată a intensității (Fade-Out).
3. **Perioadă reglabilă:** Viteza cu care are loc tranziția poate fi controlată prin intermediul switch-urilor / butoanelor de pe placă.

## 🚀 Cum să folosești acest proiect

1. Clonează acest repository local.
2. Deschide mediul **Vivado**.
3. Creează un proiect nou și adaugă sursele VHDL (`.vhd` / modulele TOP).
4. Adaugă fișierul de constrângeri `.xdc` corespunzător plăcii tale.
5. Rulează sinteza, implementarea și generează fișierul bitstream (`.bit`).
6. Încarcă bitstream-ul pe placa Basys 3 și testează funcționalitatea cu ajutorul switch-urilor și LED-urilor.

## 👨‍💻 Autor

- **Vlad Macuc** ([@vladmacuc](https://github.com/vladmacuc))
