Criterion E: Product development
--------------------------------

**The structure and organisation of the webpages**

**Techniques**

**CSS**

CSS was attached to all the forms on the web page to maintain the uniformity of
pages. The style sheet is attached to the web page in the head section. The link
to the style sheet is shown below:

The style sheet can be attached on many pages and it will ensure that the
formatting of all pages is the same.

The highlighted part above is the main link to the style sheet and the rest is
its descriprion.

In the highlighted part, there is a certain syntax that is followed.

1.  Setting the relationship between the style sheet and the web page. This is
    done using rel= “stylesheet”. We can also use more than one style sheets in
    a web page, but in that case it is important to give each of them a
    different name.

2.  Setting the path for finding the css file:
    \<..href="ITGS/tabs/dropdowntabfiles/glowtabs.css..\> here we are specifying
    the path for the web page to find our style sheet. The link shows that my
    css file is in a folder named dropdowntabfiles which is in tabs which is
    further in ITGS.

3.  By using \<style type="text/css"\> we are allowing only 2 type of style
    sheets that is cascading style sheets or css and text style sheets.

The screen shot for my css file is shown below:

![](media/73c55ebeb5ed6ee690a14586156a3fe9.png)

![](media/06c67f15a65592a48f0ad40772eb005b.png)

![](media/2de8f2a879e86d562de61a39d6fba6ce.png)

**Photo editing and creation:**

Logo for the shop:

I initially got a picture of ice-cream from the internet:

![](media/3a1e6e568df78844a92d51741adc17c7.jpg)

I then opened it with Corel PHOTO-PAINT X5 for editing, I used the ripple effect
to create the background of the logo

![](media/1ac3da07f7e34147ade9060d5fd00985.png)

After editing it looked something like this:

![](media/4e37446299be165708049d129eb5e2a9.jpg)

I then removed the background of the image and used insert text to show the name
of the shop, what is received after the editing was this:

![](media/4e0a9b32095279ce6adad494adc558f3.jpg)

I liked the logo however, I thought that this looked more like a back ground
image while I wanted it to be somewhat like a logo so I further took the photo
for editing in picasa:

![](media/3542c79003b5e6439f966951cba92b1f.png)

Here I used the two border option and choose the colour, I later chose the film
grate option to give it a professional texture. What I received at the end of
this was:

![](media/c490a0ca68f6b187579b452b3818be53.jpg)

![](media/093db636fb430a0465f6a9f5df706ef8.png)

I also created images for the purpose of buttons. I used Adobe photoshop CS5.5
Initially when I started making the image, I had a piture in mind. I wanted to
create an image that would inication home and would serve the purpose of a home
button. So the images below show the steps that I followed:

![](media/b79ee8c8b9bac3595c15ba059a787158.png)

![](media/77dd9320dbd177b8cf8c44038986b9ac.png)

I created the same type of image in different shades of colour to act as
rollover image:

![](media/103fc74d2dd1e03661bc1547deffa848.jpg)

![](media/a826057efd0835a4a2cc1e3c03b77c8c.jpg)

For creating these images, I chose to size of clipboard to be 66X66 pixels. I
found that this size was most appropriate for the specific purpose It was
created for.

**Link to database**

In my project, I have linked a database named snowfurl.mdb. This database is
used both for submitting and extraction of data.

Submitting data: Similar programing was used for adding a new customer and
adding a new product to the database through the asp file. The coding is shown
below:

1.  The portion highlighted in yellow shows that the web page is linked to
    snowfurl.mdb, which is in the folder *itgsprogram* in D drive.

2.  The portion highlighted in sea green shows the command for entering the the
    received data from the web page into the database. Each of the fields have
    been alloted different varibales such as strTB1, strTB2, strTB3.. till
    strTB6. These variables are defined at the start of the code. In the code,
    the exact name of the field is entered against the variable. This is because
    the data stored in a variable will be copied into the corresponding fields.
    For eg, the data stored in strTB1 will be copied in *customername* field.

3.  strCommand = "INSERT INTO customer
    (customername,address,mobphone1,mobphone2,landphone,email)

>   this command is written to define the table and the fields in which the data
>   has to be entered. It shows that the data has to entered in the table
>   *customer* and into the fields specified in the bracket

1.  Response.Write("Thank you! Your data has been added.") This command is used
    as a response after the other commands are executed. This states that once
    the data is stored in the database, the following message should appear:
    "Thank you! Your data has been added”

Receiving and displaying data:

This type of code was used for forms that searched for records such as a product
or a customer record. The data was received and then displayed as a form in
which it can be edited. This can be split into 2 parts, receiving the
information and displaying it. For receiving the code is:

1.  The portion highlighted yellow set the query string to the variable *strTB3*
    which is *mobphone1*. This means that the record will be searched in the
    database depending on this value.

2.  However, I have given an option of entering 2mobile numbers. I later thought
    that it would be necessary to keep this in consideration. The correct record
    should be found depending on any of the numbers that have been stored. To do
    this, the code highlighted in sea green colour was included. In this a
    command is give to select from either *mobphone1* or *mophone2*. The number
    that the user will type will be stored as a variable *strTB3*. Therefore in
    the code it is mentioned that the value of *strTB3* should be equal to
    either of the 2 fields mentioned above.

3.  In the product form, the information is extracted in the same way although
    the user chooses from the options given in a drop down menu. The code used
    was : pr = pr & "\<option value=" & ors("BARCODE") & "\>" & ors("PRODUCT") &
    " " & ors("BARCODE") & "\</option\>". In this, the fields *barcode* and
    *product* are diplayed althought *barcode* is used to find the records from
    the data base.

For extracting the data from the database and displaying it in an editable form:

First, the variables are defined as follows:

Here, the variables are defined and alloted their respective filed in the
database table.

![](media/e51bcc3336904a112873bd469efd5aa7.png)

After this, a form was created named *customer edit*. The value to displayed
were entered in the form of a variable corresponding to the field. In the
picture below, the code is shown along with design of the form:

In the coding, it can be seen that after creating an input box and setting its
input format as text, the value has also been defined in the form, for eg. In
case of the field *mobphone2* that is the Alternate mobile number from the form,
the value has been defined this way: value= \<%=strTB6%\>. This variable
contains the information from the database and it will be displayed in the form.

**Navigation**

The navigation has been made simpler by attaching a styles sheet of buttons to
all web pages. Therfore, all the pages will be navigable through any page that
is open and there is an option to return back to home page on all the pages.

![](media/6fd588095b6c8e29211be3d5b1c6c25f.png)

A part as shown above is present on all the pages.

Linking of buttons: a style sheet was attached for the design of the buttons,
the coding for this is shown on page 2. The hyperlink of these buttons is done
this way:

The statements with “href=…” shows the path of the destination.

I have used a rollover image as the home button, the coding is done in the
following way:

1.  The original image is HOME.jpg which is sited by the address: \<imgsrc=
    “BUTTONS/HOME.jpg”..

2.  onMouseOver="MM\_swapImage('Image3','','BUTTONS/HOME-2.jpg',1)": When the
    mouse pointer comes over the picture, the image should swap to Image3 which
    is in the folder BUTTONS and named HOME-2.jpg.

3.  onMouseOut="MM\_swapImgRestore()" means that when the mouse in not on the
    picture, the original picture is restored.

4.  href=<http://localhost:801/>: this shows that the image is link to the
    address <http://localhost:801/>.

![](media/b40cb4d875665d3c92ec39e6d27c2819.png)

In order to access .asp file formats in the browser, I have mapped my home page
on the IIS 7 manager:

Therefore, the address is <http://localhost:801/>

The port set for the site is 801 and the file is named index (therefore the web
page will be chosen by default)
