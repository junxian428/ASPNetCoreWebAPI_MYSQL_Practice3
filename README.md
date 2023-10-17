CREATE TABLE user (
    Id INT PRIMARY KEY,
    Username VARCHAR(255),
    Mail VARCHAR(255),
    PhoneNumber VARCHAR(20),
    Skillsets VARCHAR(255),
    Hobby VARCHAR(255)
);

CREATE TABLE Authors (
    AuthorId INT AUTO_INCREMENT PRIMARY KEY,
    Name VARCHAR(255)
);

CREATE TABLE Books (
    BookId INT AUTO_INCREMENT PRIMARY KEY,
    Title VARCHAR(255),
    AuthorId INT,
    FOREIGN KEY (AuthorId) REFERENCES Authors(AuthorId)
);


INSERT INTO Authors (Name) VALUES ('Author 1');
INSERT INTO Authors (Name) VALUES ('Author 2');

INSERT INTO Books (Title, AuthorId) VALUES ('Book 1', 1);
INSERT INTO Books (Title, AuthorId) VALUES ('Book 2', 1);
INSERT INTO Books (Title, AuthorId) VALUES ('Book 3', 2);


POST 
{
  "bookId": 4,
  "title": "string",
  "authorId": 3,
  "author": {
    "authorId": 3,
    "name": "Ho Weng Yin",
    "books": []
  }
}


PUT

{
  "bookId": 4,
  "title": "string123123123131",
  "authorId": 3,
  "author": {
    "authorId": 3,
    "name": "string",
    "books": []
  }
}
