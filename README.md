# Python-esercizio-exercise.
Programma della spesa.

# “Gestione spese personale”

# input e logica
lista = []
def aggiungi_spesa(lista):
    nome_spesa = input("nome spesa? ")
    importo = float(input("importo? ")) 

    spesa = {"nome": nome_spesa, "Importo": importo}

    lista.append(spesa)

    return spesa

def mostra_spesa(lista):
    for spesa in lista:
        print(f"{spesa['nome']} \n {spesa['Importo']}")   # output: - pizza \n - 10 
    return                                  # da correggere : perche 
    

def totale_spesa(lista):
    totale = 0
    for spesa in lista:
        print(f"{spesa['nome']}, {spesa['Importo']}")
        totale += float(spesa['Importo'])   
    return totale

def spesa_massima(lista):
    importo_max = 0
    for spesa in lista:
        if float(spesa["Importo"]) > importo_max:
            importo_max = float(spesa["Importo"]) 
    return importo_max

# Menu principale #
spese = []
while True:
    print("MENU...")
    scelta = input("scegli: ")

    if scelta == "1":
        print(aggiungi_spesa(lista))
    elif scelta == "2":
        print(mostra_spesa(lista))
    elif scelta == "3":
        print(totale_spesa(lista))
    elif scelta == "4":
        print(spesa_massima(lista))      
    elif scelta == "5":
        print("Esco dal programma")
        break
