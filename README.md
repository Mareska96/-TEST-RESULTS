Obavljeno je testiranje koda calculator-java po metodi Crne kutije.

Definisao sam nekoliko test primera:

Osnovno sabiranje:
Ulaz: "2+3"
Očekivani izlaz: "5"

Osnovno oduzimanje:
Ulaz: "5-2"
Očekivani izlaz: "3"

Osnovno množenje:
Ulaz: "4*6"
Očekivani izlaz: "24"

Osnovno deljenje:
Ulaz: "8/2"
Očekivani izlaz: "4"

Kombinacija operacija:
Ulaz: "(2+3)*4-6/2"
Očekivani izlaz: "17"

Delenje nulom:
Ulaz: "5/0"
Očekivani izlaz: "Greška"

Nakon testiranja, nisam primetio greške,propust ili nedostatke. Kod calculator-java se pokreće normalno.


Jedinični test:

import unittest
from your_calculator_module import Calculate

class TestCalculator(unittest.TestCase):
    def test_calculate(self):
        self.assertEqual(Calculate("2+3"), 5)
        self.assertEqual(Calculate("4*5"), 20)
        self.assertEqual(Calculate("10/2"), 5)
        self.assertEqual(Calculate("3+4*2"), 11)
        self.assertEqual(Calculate("(3+4)*2"), 14)
        self.assertEqual(Calculate("5*(2+3)"), 25)
        self.assertEqual(Calculate("-5+3"), -2)
        self.assertEqual(Calculate("2.5+1.3"), 3.8)

if __name__ == '__main__':
    unittest.main()
