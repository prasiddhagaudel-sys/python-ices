library = []

def add_book():
    name = input("Enter book name: ")
    author = input("Enter author name: ")

    book = [name, author]
    library.append(book)

    print("Book added successfully.")

def delete_book():
    name = input("Enter book name to delete: ")

    for book in library:
        if book[0].lower() == name.lower():
            library.remove(book)
            print("Book deleted.")
            return

    print("Book not found.")

def search_book():
    name = input("Enter book name: ")

    for book in library:
        if book[0].lower() == name.lower():
            print("Book Name:", book[0])
            print("Author:", book[1])
            return

    print("Book not found.")

def search_author():
    author = input("Enter author name: ")
    found = False

    for book in library:
        if book[1].lower() == author.lower():
            print("Book Name:", book[0])
            print("Author:", book[1])
            found = True

    if found == False:
        print("No books found.")

def display_books():
    if len(library) == 0:
        print("Library is empty.")
    else:
        print("\nBooks in Library:")
        for book in library:
            print("Book:", book[0], "| Author:", book[1])

while True:
    print("\nLibrary Management System")
    print("1. Add Book")
    print("2. Delete Book")
    print("3. Search by Book Name")
    print("4. Search by Author")
    print("5. Display All Books")
    print("6. Exit")

    choice = input("Enter your choice: ")

    if choice == "1":
        add_book()
    elif choice == "2":
        delete_book()
    elif choice == "3":
        search_book()
    elif choice == "4":
        search_author()
    elif choice == "5":
        display_books()
    elif choice == "6":
        print("Thank you.")
        break
    else:
        print("Invalid choice.")