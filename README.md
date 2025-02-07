class Book:
    def __init__(self, title=None, author=None, ISBN=None, price=None):
        self.title = title
        self.author = author
        self.ISBN = ISBN
        self.price = price

    def display_info(self):
        print(f"Title: {self.title}")
        print(f"Author: {self.author}")
        print(f"ISBN: {self.ISBN}")
        print(f"Price: ${self.price:.2f}")
    
    def is_expensive(self):
        if self.price > 50:
            print(f"{self.title} is an expensive book!")
        else:
            print(f"{self.title} is reasonably priced.")
    

# Test the class
books = []
n = int(input("How many books would you like to create? "))

# Creating books using default and parameterized constructors
for _ in range(n):
    choice = input("Do you want to input book details? (yes/no): ")
    if choice.lower() == 'yes':
        title = input("Enter the title: ")
        author = input("Enter the author: ")
        ISBN = input("Enter the ISBN: ")
        price = float(input("Enter the price: "))
        book = Book(title, author, ISBN, price)
    else:
        book = Book()  # Default constructor
    books.append(book)

# Display info for each book
for book in books:
    book.display_info()
    book.is_expensive()
