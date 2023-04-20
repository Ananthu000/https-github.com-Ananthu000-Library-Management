#Library-Management
class Library:
    def __init__(self, books):
        self.books = books

    def list_books(self):
        print("________Available Books__________")
        for book in self.books:
            print(book)

    def borrow_book(self, borrow_book):
        if borrow_book in self.books:
            print("Get Your Book Now")
            self.books.remove(borrow_book)
        else:
            print("Book not Available")

    def return_book(self, return_book):
        print("You have returned the book")
        self.books.append(return_book)


books = ['c', 'c++', 'Java', 'Python']
o = Library(books)

msg = '''
      1. Display Book
      2. Borrow Book
      3. Return Book
      4. Exit
'''

while True:
    print(msg)
    ch = int(input("Enter your choice : "))

    if ch == 1:
        o.list_books()
    elif ch == 2:
        book = input("Enter Book Name to Borrow : ")
        o.borrow_book(book)
    elif ch == 3:
        book = input("Enter Book Name to Return : ")
        o.return_book(book)
    else:
        print("Thank You come again")
        quit()
