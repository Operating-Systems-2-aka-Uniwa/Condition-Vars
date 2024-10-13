![Alt text](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a5/Flag_of_the_United_Kingdom_%281-2%29.svg/255px-Flag_of_the_United_Kingdom_%281-2%29.svg.png)

# POSIX Threads - "What A Wonderful World!" Program 

For the requested Assignment, click the link:
[Assignment](Assignment/)

For the detailed Source Codes, click the link:
[Code](Code/)

## Course Information
- **Course**: [Operating Systems II](https://ice.uniwa.gr/education/undergraduate/courses/operating-systems-ii/)
- **Semester**: 4
- **Program of Study**: [UNIWA](https://www.uniwa.gr/)
- **Department**: [Informatics and Computer Engineering](https://ice.uniwa.gr/)
- **Lab Instructor**: [Psarras Nikolaos](https://ice.uniwa.gr/emd_person/20879/)
- **Academic Season**: 2021-2022

## Student Information
- **Name**: Athanasiou Vasileios Evangelos
- **Student ID**: 19390005
- **Status**: Undergraduate

## Assignment Title
**Title**: POSIX Threads-based Synchronization for Printing Sequence "What A Wonderful World!"

## Assignment Overview

This project involves creating a program that uses **POSIX Threads** and **synchronization mechanisms** to repeatedly print the phrase:

`What A Wonderful World!`

The phrase will be printed continuously by three separate threads, with each thread responsible for printing a specific word in the sequence:
- **Thread 1**: Prints `"What A "`
- **Thread 2**: Prints `"Wonderful "`
- **Thread 3**: Prints `"World!"`

The program ensures the correct order of printing by using synchronization primitives. Two versions of the program are provided:
1. **Version 1**: Using semaphores for synchronization.
2. **Version 2**: Using condition variables for synchronization.

## Objectives

- Implement **multi-threading** using the **POSIX threads** (`pthread`) library.
- Use **semaphores** and **condition variables** to control synchronization between the threads.
- Demonstrate how the threads communicate to print the sequence `"What A Wonderful World!"` in the correct order.

## Program Structure

### Version 1: Using Semaphores
- **POSIX Semaphores** (`sem_init`, `sem_wait`, `sem_post`) are used to control the execution sequence of threads.
- Each thread prints its part of the phrase and signals the next thread using semaphores.
- This version demonstrates semaphore-based synchronization, ensuring that the sequence is printed without race conditions.

### Version 2: Using Condition Variables
- **Condition Variables** (`pthread_cond_wait`, `pthread_cond_signal`, `pthread_cond_broadcast`) are used to manage synchronization between threads.
- A condition variable is used to put threads into a waiting state until their turn comes to print their part of the phrase.
- This version demonstrates condition variable-based synchronization, providing a different mechanism for thread communication.

## Key Features

- **Thread Synchronization**: Ensures that the threads execute in the correct order.
- **Parallel Execution**: Multiple threads work together to print the sequence continuously.
- **Mutex Protection**: The critical sections of code are protected using **mutexes** to prevent race conditions.
- **Infinite Loop**: Threads run in an infinite loop to repeatedly print the phrase until manually terminated.

## Requirements

- **Operating System**: Linux-based OS or any Unix-like system that supports POSIX threads and semaphores.
- **Compiler**: GCC (GNU Compiler Collection).
- **Libraries**: POSIX Threads (`pthread`) and POSIX Semaphores (`semaphore.h` for the first version).

## Compilation and Usage

### 1. Clone the Repository
Download the repository to your local machine:
```
git clone https://github.com/Operating-Systems-2-aka-Uniwa/Threads-Synchronization.git
```

### 2. Compile the source code
Compile with gcc compiler the source codes and the flag `-pthread` to activate POSIX threads and `-lrt` to activate semaphores:
```
gcc -o semaphores semaphores.c -lpthread -lrt
gcc -o condition_vars condition_vars.c -pthread
```
### 3. Run the code
Execute the executable file:
```
./semaphores
./condition_vars
```

![Alt text](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5c/Flag_of_Greece.svg/255px-Flag_of_Greece.svg.png)

# Πρόγραμμα POSIX Threads - "What a Wonderful World!"

Για την ζητούμενη Άσκηση, κάντε κλικ στον σύνδεσμο:
[Άσκηση](Assignment/)

Για τους λεπτομερείς Πηγαίους Κώδικες, κάντε κλικ στον σύνδεσμο:
[Κωδικός](Code/)

## Πληροφορίες Μαθήματος
- **Μάθημα**: [Λειτουργικά Συστήματα II](https://ice.uniwa.gr/education/undergraduate/courses/operating-systems-ii/)
- **Εξάμηνο**: 4
- **Πρόγραμμα Σπουδών**: [UNIWA](https://www.uniwa.gr/)
- **Τμήμα**: [Πληροφορική και Μηχανική Υπολογιστών](https://ice.uniwa.gr/)
- **Υπεύθυνος Εργαστηρίου**: [Ψαράς Νικόλαος](https://ice.uniwa.gr/emd_person/20879/)
- **Ακαδημαϊκή Χρονιά**: 2021-2022

## Πληροφορίες Φοιτητή
- **Όνομα**: Αθανασίου Βασίλειος Ευάγγελος
- **Αριθμός Μητρώου**: 19390005
- **Κατάσταση**: Προπτυχιακός

## Τίτλος Άσκησης
**Τίτλος**: Συγχρονισμός με Βάση το POSIX Threads για την Εκτύπωση της Φράσης "Τι Υπέροχος Κόσμος!"

## Επισκόπηση Άσκησης

Αυτό το έργο περιλαμβάνει τη δημιουργία ενός προγράμματος που χρησιμοποιεί **POSIX Threads** και **μηχανισμούς συγχρονισμού** για να εκτυπώνει επανειλημμένα τη φράση:

`Τι Υπέροχος Κόσμος!`

Η φράση θα εκτυπώνεται συνεχώς από τρία ξεχωριστά νήματα, με κάθε νήμα υπεύθυνο για την εκτύπωση μιας συγκεκριμένης λέξης στη σειρά:
- **Νήμα 1**: Εκτυπώνει `"What a Wonderful"`
- **Νήμα 2**: Εκτυπώνει `"World"`
- **Νήμα 3**: Εκτυπώνει `"!"`

Το πρόγραμμα εξασφαλίζει τη σωστή σειρά εκτύπωσης χρησιμοποιώντας συγχρονιστικά primitives. Δύο εκδόσεις του προγράμματος παρέχονται:
1. **Έκδοση 1**: Χρησιμοποιώντας σημαφόρους για συγχρονισμό.
2. **Έκδοση 2**: Χρησιμοποιώντας μεταβλητές κατάστασης για συγχρονισμό.

## Στόχοι

- Υλοποίηση **πολυνηματικής εκτέλεσης** χρησιμοποιώντας τη βιβλιοθήκη **POSIX threads** (`pthread`).
- Χρήση **σημαφόρων** και **μεταβλητών κατάστασης** για τον έλεγχο του συγχρονισμού μεταξύ των νημάτων.
- Επίδειξη του τρόπου επικοινωνίας των νημάτων για την εκτύπωση της φράσης `"Τι Υπέροχος Κόσμος!"` στη σωστή σειρά.

## Δομή Προγράμματος

### Έκδοση 1: Χρήση Σημαφόρων
- **POSIX Σημαφόροι** (`sem_init`, `sem_wait`, `sem_post`) χρησιμοποιούνται για τον έλεγχο της σειράς εκτέλεσης των νημάτων.
- Κάθε νήμα εκτυπώνει το μέρος της φράσης και ειδοποιεί το επόμενο νήμα χρησιμοποιώντας σημαφόρους.
- Αυτή η έκδοση επιδεικνύει τον συγχρονισμό με βάση σημαφόρους, διασφαλίζοντας ότι η σειρά εκτύπωσης γίνεται χωρίς συνθήκες ανταγωνισμού.

### Έκδοση 2: Χρήση Μεταβλητών Κατάστασης
- **Μεταβλητές Κατάστασης** (`pthread_cond_wait`, `pthread_cond_signal`, `pthread_cond_broadcast`) χρησιμοποιούνται για τη διαχείριση του συγχρονισμού μεταξύ των νημάτων.
- Μια μεταβλητή κατάστασης χρησιμοποιείται για να τοποθετήσει τα νήματα σε κατάσταση αναμονής μέχρι να έρθει η σειρά τους να εκτυπώσουν το μέρος της φράσης.
- Αυτή η έκδοση επιδεικνύει τον συγχρονισμό με βάση μεταβλητές κατάστασης, παρέχοντας έναν διαφορετικό μηχανισμό για την επικοινωνία των νημάτων.

## Κύρια Χαρακτηριστικά

- **Συγχρονισμός Νημάτων**: Εξασφαλίζει ότι τα νήματα εκτελούνται στη σωστή σειρά.
- **Παράλληλη Εκτέλεση**: Πολλαπλά νήματα συνεργάζονται για να εκτυπώσουν τη φράση συνεχώς.
- **Προστασία Μεταβλητών**: Οι κρίσιμες περιοχές κώδικα προστατεύονται με τη χρήση **mutex** για να αποφεύγονται οι συνθήκες ανταγωνισμού.
- **Ατέρμον Βρόχος**: Τα νήματα εκτελούνται σε ατέρμον βρόχο για να εκτυπώνουν επανειλημμένα τη φράση μέχρι να τερματιστούν χειροκίνητα.

## Απαιτήσεις

- **Λειτουργικό Σύστημα**: Λειτουργικό σύστημα βασισμένο σε Linux ή οποιοδήποτε Unix-like σύστημα που υποστηρίζει POSIX threads και σημαφόρους.
- **Μεταγλωττιστής**: GCC (GNU Compiler Collection).
- **Βιβλιοθήκες**: POSIX Threads (`pthread`) και POSIX Σημαφόροι (`semaphore.h` για την πρώτη έκδοση).

## Εγκατάσταση και Χρήση

### 1. Κλωνοποιήστε το Αποθετήριο
Κατεβάστε το αποθετήριο στον τοπικό σας υπολογιστή:
```
git clone https://github.com/Operating-Systems-2-aka-Uniwa/Threads-Synchronization.git
```
### 2. Μεταγλωττίστε τον Πηγαίο Κώδικα
Συγκεντρώστε τους πηγαίους κώδικες με τον μεταγλωττιστή gcc και τη σημαία `-pthread` για να ενεργοποιήσετε τα POSIX threads και `-lrt` για να ενεργοποιήσετε τους σημαφόρους:
```
gcc -o semaphores semaphores.c -lpthread -lrt
gcc -o condition_vars condition_vars.c -pthread
```
### 3. Εκτελέστε τον Κώδικα
Εκτελέστε το εκτελέσιμο αρχείο:
```
./semaphores
./condition_vars
```
