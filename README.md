class Uczeń:
    def __init__(self, imię, nazwisko, klasa):
        self.imię = imię
        self.nazwisko = nazwisko
        self.klasa = klasa
        self.oceny = {}

    def dodaj_ocenę(self, przedmiot, ocena):
        if przedmiot in self.oceny:
            self.oceny[przedmiot].append(ocena)
        else:
            self.oceny[przedmiot] = [ocena]

    def wyświetl_info(self):
        print(f"Uczeń: {self.imię} {self.nazwisko}, Klasa: {self.klasa}")

class User:
    def __init__(self, username, email):
        self.username = username
        self.email = email
        self.logged_in = False

    def zaloguj(self):
        self.logged_in = True
        return f"Zalogowano użytkownika {self.username}."

    def wyloguj(self):
        self.logged_in = False
        return f"Wylogowano użytkownika {self.username}."

    def wyświetl_info(self):
        print(f"Użytkownik: {self.username}, Email: {self.email}")
