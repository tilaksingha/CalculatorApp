Concise and easy-to-read cheat sheets for **Node.js**, **XML**, and **SQL**. The cheatsheets are written in **Markdown** to ensure they look beautiful when viewed on GitHub, VSCode, or any markdown-supported editor.

---

### **Node.js Cheat Sheet**

```markdown
# 🟢 Node.js Cheat Sheet

## Basics
- Install: `npm install <package>`
- Run File: `node <filename.js>`
- Initialize Project: `npm init`

## Common Commands
- `console.log()`: Print to the console.
- `require()`: Import a module.
- `module.exports`: Export module.
- `process.argv`: Command line arguments.
- `fs.readFileSync(path)`: Read file synchronously.
- `fs.writeFileSync(path, data)`: Write file synchronously.

## HTTP Server Example
```javascript
const http = require('http');
http.createServer((req, res) => {
  res.write('Hello World');
  res.end();
}).listen(3000);
```

## Working with Packages
- Install: `npm install <package-name>`
- Uninstall: `npm uninstall <package-name>`
- Global Install: `npm install -g <package-name>`
- Package List: `npm list`

## Promises & Async
```javascript
async function fetchData() {
  const data = await fetch(url);
  console.log(data);
}
```

## Popular Modules
- **Express**: Web framework.
- **Axios**: HTTP requests.
- **Mongoose**: MongoDB connection.
- **Body-parser**: Parse HTTP body.
```

---

### **XML Cheat Sheet**

```markdown
# 📄 XML Cheat Sheet

## Basics
- **Syntax**: `<element>Content</element>`
- **Attributes**: `<element attribute="value">`
- **Comments**: `<!-- Comment -->`

## Example XML Structure
```xml
<?xml version="1.0" encoding="UTF-8"?>
<bookstore>
  <book category="fiction">
    <title>Harry Potter</title>
    <author>J.K. Rowling</author>
  </book>
</bookstore>
```

## Key Concepts
- **Root Element**: One parent element.
- **Elements**: Defines data, wrapped in `<tags>`.
- **Attributes**: Add extra info to elements.

## Special Characters
- `&lt;` = `<`
- `&gt;` = `>`
- `&amp;` = `&`

## Prolog
```xml
<?xml version="1.0" encoding="UTF-8"?>
```

## CDATA
Used to include characters that would otherwise be recognized as markup.
```xml
<![CDATA[<text>]]>
```

## XSLT (Transform XML)
```xml
<xsl:stylesheet version="1.0">
  <xsl:template match="/">
    <html><body><h2>Transformed Content</h2></body></html>
  </xsl:template>
</xsl:stylesheet>
```
```

---

### **SQL Cheat Sheet**

```markdown
# 💾 SQL Cheat Sheet

## Basics
- **SELECT**: Retrieve data.
- **INSERT**: Add new records.
- **UPDATE**: Modify existing records.
- **DELETE**: Remove records.
- **CREATE TABLE**: Create a new table.

## Data Types
- `INT`, `VARCHAR(n)`, `DATE`, `BOOLEAN`, `TEXT`

## SELECT Syntax
```sql
SELECT column_name FROM table_name;
```

## INSERT Syntax
```sql
INSERT INTO table_name (column1, column2) VALUES (value1, value2);
```

## UPDATE Syntax
```sql
UPDATE table_name SET column1 = value1 WHERE condition;
```

## DELETE Syntax
```sql
DELETE FROM table_name WHERE condition;
```

## Joins
- **INNER JOIN**: Matches records with both tables.
- **LEFT JOIN**: All records from the left table + matching ones from the right.
- **RIGHT JOIN**: All records from the right table + matching ones from the left.

## Join Example
```sql
SELECT Orders.OrderID, Customers.CustomerName
FROM Orders
INNER JOIN Customers ON Orders.CustomerID = Customers.CustomerID;
```

## Aggregation Functions
- **COUNT()**: Counts rows.
- **SUM()**: Adds values.
- **AVG()**: Averages values.

## Grouping and Filtering
- **GROUP BY**: Group rows.
- **HAVING**: Filter after grouping.

```sql
SELECT column_name, COUNT(*)
FROM table_name
GROUP BY column_name
HAVING COUNT(*) > 5;
```

## Constraints
- **PRIMARY KEY**: Uniquely identifies each row.
- **FOREIGN KEY**: Links two tables together.
- **NOT NULL**: Prevents NULL values.
- **UNIQUE**: Ensures all values are unique.

## Create Table Example
```sql
CREATE TABLE Customers (
  ID INT PRIMARY KEY,
  Name VARCHAR(255),
  Age INT,
  Country VARCHAR(255)
);
```
```

---

These cheat sheets should be copy-paste friendly into any markdown editor or platform that supports Markdown (like GitHub).