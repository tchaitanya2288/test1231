# /var/www/cgi-bin/
[root@reposerver www]# cat cgi-bin/checkbox.py
#!/usr/bin/python

# Import modules for CGI handling
import cgi, cgitb

# Create instance of FieldStorage
form = cgi.FieldStorage()

# Get data from fields
if form.getvalue('Python'):
        course_flag = "ON"
        #import mysql.connector
        import MySQLdb

        # Open database connection
        db = MySQLdb.connect("localhost","root","redhat")

        #db = MySQLdb.connect("server.minnu.com","root","redhat","test_minnu" )

        # prepare a cursor object using cursor() method
        cursor = db.cursor()

        # execute SQL query using execute() method.
        cursor.execute("SELECT VERSION()")

        # Fetch a single row using fetchone() method.
        data = cursor.fetchone()

        print ("Database version : %s " % data)

        # disconnect from server
        db.close()
else:
   course_flag = "OFF"

if form.getvalue('Perl'):
   Perl_flag = "ON"
else:
   Perl_flag = "OFF"

print "Content-type:text/html\r\n\r\n"
print "<html>"
print "<head>"
print "<title>Checkbox - Third CGI Program</title>"
print "</head>"
print "<body>"
print "<h2> CheckBox Python is : %s</h2>" % course_flag
print "<h2> CheckBox Perl is : %s</h2>" % Perl_flag
print "<h2> Check the Database Server Version : %s</h2>" % data
print "</body>"
print "</html>"

