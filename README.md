# LLaMA Model Interaction with Tkinter

Dette repository indeholder en Python-applikation, der bruger Tkinter til at oprette en grafisk brugergrænseflade (GUI) til interaktion med en LLaMA-model fra Hugging Face. Applikationen tillader brugeren at indtaste tekst og se genereret output fra modellen direkte i GUI'en.

## Funktionalitet

- **Input Tekstfelt:** Brugeren kan indtaste tekst, som vil blive sendt til LLaMA-modellen.
- **Send Knap:** Når brugeren klikker på "Send", sendes input til modellen for generering af et svar.
- **Output Tekstfelt:** Viser både brugerens input og modellens genererede svar i et scrolled text-felt.

## Installation

Før du kan køre applikationen, skal du sørge for, at du har Python 3.8 eller nyere installeret. Følg nedenstående trin for at opsætte miljøet:

1. **Clone Repository:**

   ```bash
   git clone https://github.com/yourusername/llama-tkinter-interaction.git
   cd llama-tkinter-interaction
   ```

2. **Opret Virtuelt Miljø (Valgfrit men anbefalet):**

   ```bash
   python3 -m venv venv
   source venv/bin/activate  # For Linux/macOS
   venv\Scripts\activate  # For Windows
   ```

3. **Installer Krævede Pakker:**

   ```bash
   pip install torch transformers tkinter
   ```

4. **Kør Applikationen:**

   ```bash
   python app.py
   ```

## Model

Applikationen bruger modellen `Groq/Llama-3-Groq-8B-Tool-Use` fra Hugging Face. Du kan ændre `model_name` variablen i `app.py` for at bruge en anden model, hvis nødvendigt.

## Kode Forklaring

- **Model Initialisering:** Modellen og tokenizer initialiseres ved hjælp af `AutoTokenizer` og `AutoModelForCausalLM` fra Hugging Face's Transformers bibliotek.
- **generate_response() Funktion:** Håndterer input fra brugeren, genererer output fra modellen, og opdaterer GUI'en med resultatet.
- **Tkinter GUI:** GUI'en består af et tekstfelt til brugerinput, en "Send" knap, og et scrolled text-felt til at vise både input og output.

## Eksempel på Brug

1. Start applikationen ved at køre `app.py`.
2. Indtast tekst i inputfeltet.
3. Klik på "Send" for at generere et svar fra modellen.
4. Se både din input og modellens output i outputfeltet.

## Bidrag

Bidrag er velkomne! Du kan lave en pull request, hvis du ønsker at tilføje nye funktioner eller rette fejl.

## Licens

Dette projekt er licenseret under MIT License - se [LICENSE](LICENSE) filen for detaljer.

