---
layout: workshop      # DON'T CHANGE THIS.
                      # Be sure to update the Carpentry type in _config.yml as well.  
venue: "Transparent and Open Archaeological Science Using R<br><h3>A Short Workshop at the Society of American Archaeology Annual Meeting, Albuquerque Convention Center</h3>"        # brief name of host site without address (e.g., "Euphoric State University")
address: "401 2nd St NW, Albuquerque, NM 87102"      # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria")
country: "us"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1)
language: "en"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/ISO_639-1)
latlng: "35.0873016,-106.6518842"       # decimal latitude and longitude of workshop venue (e.g., "41.7901128,-87.6007318" - use https://www.latlong.net/)
humandate: "April 10, 2019"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "1-5 pm"    # human-readable times for the workshop (e.g., "9:00 am - 4:30 pm")
startdate: 2019-04-10      # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: 2019-04-10         # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["Ben Marwick (University of Washington)"] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
helper: ["Matt Harris (AECOM)", "Liying Wang (University of Washington)"]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["bmarwick@uw.edu"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
collaborative_notes:             # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document
eventbrite:           # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
---

<h2 id="general">General Information</h2>

{% comment %}
  INTRODUCTION

  Edit the general explanatory paragraph below if you want to change
  the pitch.
{% endcomment %}


In recent years serious concerns about the reproducibility and transparency of research have arisen in many scientific disciplines. These concerns reveal a wide gap between scientific practice and scientific ideals, and threaten to erode public support for research. In this workshop we will provide hands-on training in robust techniques, tools and services (all free) to improve the reproducibility and transparency of archaeological research. Most of these tools relate to the R programming language, which is central to recent developments in social and natural sciences.

{% comment %}
  AUDIENCE

  Explain who your audience is.  (In particular, tell readers if the
  workshop is only open to people from a particular institution.
{% endcomment %}
This workshop is suited to novices who have never used R before: <em>no</em> prior experience is necessary. The course is aimed at archaeologists doing research at all career stages.
<p>


{% comment %}
  LOCATION

  This block displays the address and links to maps showing directions
  if the latitude and longitude of the workshop have been set.  You
  can use https://itouchmap.com/latlong.html to find the lat/long of an
  address.
{% endcomment %}
{% if page.latlng %}
<p id="where">
  <strong>Where:</strong>
  {{page.address}}.
  Get directions with
  <a href="//www.openstreetmap.org/?mlat={{page.latlng | replace:',','&mlon='}}&zoom=16">OpenStreetMap</a>
  or
  <a href="//maps.google.com/maps?q={{page.latlng}}">Google Maps</a>. 🌏
</p>
{% endif %}

{% comment %}
  DATE

  This block displays the date and links to Google Calendar.
{% endcomment %}
{% if page.humandate %}
<p id="when">
  <strong>When:</strong>
  {{page.humandate}}.
  {% include workshop_calendar.html %} 📅
</p>
{% endif %}

{% comment %}
  SPECIAL REQUIREMENTS

  Modify the block below if there are any special requirements.
{% endcomment %}
<p id="requirements">
  <strong>Requirements:</strong> Participants must bring a laptop with a
  Mac, Linux, or Windows operating system (not a tablet, Chromebook, etc.) that they have administrative privileges on. They should have a few specific software packages installed (listed <a href="#setup">below</a>).

If you have previously installed these programs, please download and install the most recent versions (your version may be outdated and not work with the activities in this workshop).

If you have problems or questions, please send us an email
  at {% if page.email %}
    <a href='mailto:{{page.email}}'>{{page.email}}</a>
  {% else %}
    <a href='mailto:{{page.email}}'>{{page.email}}</a>
  {% endif %}.

  Participants are also required to abide by our <a href="#coc">Code of Conduct</a>.
</p>


{% comment %}
  CONTACT EMAIL ADDRESS

  Display the contact email address set in the configuration file.
{% endcomment %}
<p id="contact">
  <strong>Contact</strong>:
  Please email
  {% if page.email %}
    {% for email in page.email %}
      {% if forloop.last and page.email.size > 1 %}
        or
      {% else %}
        {% unless forloop.first %}
        ,
        {% endunless %}
      {% endif %}
      <a href='mailto:{{email}}'>{{email}}</a>
    {% endfor %}
  {% else %}
    to-be-announced
  {% endif %}
  for more information. ✉️
</p>

<hr/>

<hr/>


{% comment %}
  SCHEDULE

  Show the workshop's schedule.  Edit the items and times in the table
  to match your plans.  You may also want to change 'Day 1' and 'Day
  2' to be actual dates or days of the week.
{% endcomment %}
<h2 id="schedule">Schedule 🗓️</h2>


<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;}
.tg .tg-yw4l{vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-yw4l"><b>Start time</b></th>
    <th class="tg-yw4l"><b>End time</b></th>
    <th class="tg-yw4l"><b>Topic</b></th>
  </tr>
  <tr>
    <td class="tg-yw4l">1:00</td>
    <td class="tg-yw4l">1:45</td>
    <td class="tg-yw4l">Introduction to <a href="https://www.r-project.org/">R</a> and a <a href="https://www.rstudio.com/">RStudio</a></td>
  </tr>
  <tr>
    <td class="tg-yw4l">2:00</td>
    <td class="tg-yw4l">2:45</td>
    <td class="tg-yw4l">Writing with <a href="https://rmarkdown.rstudio.com/">RMarkdown</a></td>
  </tr>
  <tr>
    <td class="tg-yw4l">3:00</td>
    <td class="tg-yw4l">3:45</td>
    <td class="tg-yw4l"><a href="https://git-scm.com/">Git</a> & <a href="https://github.com/">GitHub</a></td>
  </tr>
  <tr>
    <td class="tg-yw4l">4:00</td>
    <td class="tg-yw4l">4:45</td>
    <td class="tg-yw4l">Data repositories & <a href="https://osf.io">Open Science Framework</a></td>
  </tr>
  <tr>
    <td class="tg-yw4l">4:45</td>
    <td class="tg-yw4l">5:00</td>
    <td class="tg-yw4l"><a href="https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005510">Good enough practices</a></td>
  </tr>
</table>

Between each topic we will have a 15 minute break for fresh air and a strech. We will be using the <a href="https://www.tidyverse.org/">tidyverse</a>, a modern, unified collection of R packages designed for data science. For a more in-depth coverage of many of the topics of the workshop, you may want to read <a href="http://r4ds.had.co.nz/"><em>R for Data Science</em></a> by Hadley Wickham and Garrett Grolemund.
</p>


<hr/>

{% comment %}
  SYLLABUS

  Show what topics will be covered.

  1. If your workshop is R rather than Python, remove the comment
     around that section and put a comment around the Python section.
  2. Some workshops will delete SQL.
  3. Please make sure the list of topics is synchronized with what you
     intend to teach.
  4. You may need to move the div's with class="col-md-6" around inside
     the div's with class="row" to balance the multi-column layout.

  This is one of the places where people frequently make mistakes, so
  please preview your site before committing, and make sure to run
  'tools/check' as well.
{% endcomment %}

<hr/>

{% comment %}
  SETUP

  Delete irrelevant sections from the setup instructions.  Each
  section is inside a 'div' without any classes to make the beginning
  and end easier to find.

  This is the other place where people frequently make mistakes, so
  please preview your site before committing, and make sure to run
  'tools/check' as well.
{% endcomment %}

<h2 id="setup">Setup 🛠️</h2>

<p>
  To participate in this workshop,
  you will need access to the software described below.
  In addition, you will need an up-to-date web browser.
</p>
<p>
  We maintain a list of common issues that occur during installation as a reference for instructors
  that may be useful on the
  <a href = "{{site.swc_github}}/workshop-template/wiki/Configuration-Problems-and-Solutions">Configuration Problems and Solutions wiki page</a>.
</p>


<div id="git"> {% comment %} Start of 'Git' section. {% endcomment %}
  <h3>Git</h3>
  <p>
    Git is a version control system that lets you track who made changes
    to what when and has options for easily updating a shared or public
    version of your code
    on <a href="https://github.com/">github.com</a>. You will need a
    <a href="https://help.github.com/articles/supported-browsers/">supported
    web browser</a>.
  </p>
  <p>
    You will need an account at <a href="https://github.com/">github.com</a>
    for parts of the Git lesson. Basic GitHub accounts are free. We encourage
    you to create a GitHub account if you don't have one already.
    Please consider what personal information you'd like to reveal. For
    example, you may want to review these
    <a href="https://help.github.com/articles/keeping-your-email-address-private/">instructions
    for keeping your email address private</a> provided at GitHub.
  </p>

  <div class="row">
    <div class="col-md-4">
      <h4 id="git-windows">Windows</h4>
      <a href="https://www.youtube.com/watch?v=339AEqk9c-8">Video Tutorial</a>
            <ol>
              <li>Download the Git for Windows <a href="https://git-for-windows.github.io/">installer</a>.</li>
              <li>Run the installer and follow the steps below:
                <ol>
                  {% comment %} Git 2.18.0 Setup {% endcomment %}
                  <li>
                      Click on "Next" four times (two times if you've previously
                      installed Git).  You don't need to change anything
                      in the Information, location, components, and start menu screens.
                  </li>
                  <li>
                      <strong>
                      Select “Use the nano editor by default” and click on “Next”.
                      </strong>
                  </li>
                  {% comment %} Adjusting your PATH environment {% endcomment %}
                  <li>
                      Keep "Use Git from the command line and..." selected and click on "Next".
                      If you forgot to do this programs that you need for the workshop will not work properly.
                      If this happens rerun the installer and select the appropriate option.
                  </li>
                  {% comment %} Choosing the SSH executable {% endcomment %}
                  <li>Click on "Next".</li>
                  {% comment %} Configuring the line ending conversions {% endcomment %}
                  <li>
                      Keep "Checkout Windows-style, commit Unix-style line endings" selected and click on "Next".
                  </li>
                  {% comment %} Configuring the terminal emulator to use with Git Bash {% endcomment %}
                  <li>
                    <strong>
                      Select "Use Windows' default console window" and click on "Next".
                    </strong>
                  </li>
                  {% comment %} Configuring experimental performance tweaks {% endcomment %}
                  <li>Click on "Install".</li>
                  {% comment %} Installing {% endcomment %}
                  {% comment %} Completing the Git Setup Wizard {% endcomment %}
                  <li>Click on "Finish".</li>
                </ol>
              </li>
              <li>
                If your "HOME" environment variable is not set (or you don't know what this is):
                <ol>
                  <li>Open command prompt (Open Start Menu then type <code>cmd</code> and press [Enter])</li>
                  <li>
                    Type the following line into the command prompt window exactly as shown:
                    <p><code>setx HOME "%USERPROFILE%"</code></p>
                  </li>
                  <li>Press [Enter], you should see <code>SUCCESS: Specified value was saved.</code></li>
                  <li>Quit command prompt by typing <code>exit</code> then pressing [Enter]</li>
                </ol>
              </li>
            </ol>
            <p>This will provide you with both Git and Bash in the Git Bash program.</p>
    </div>
    <div class="col-md-4">
      <h4 id="git-macosx">macOS</h4>
      <p>
        Please open the Terminal app, type <code>git --version</code> and press
        <kbd>Enter</kbd>/<kbd>Return</kbd>. If it's not installed already,
        follow the instructions to <code>Install</code> the "command line
        developer tools". <strong>Don't click</strong> "Get Xcode", because that will
        take too long and is not necessary for our Git lesson.
        After installing these tools, there won't be anything in your <code>/Applications</code>
        folder, as they and Git are command line programs.
        <strong>For older versions of OS X (10.5-10.8)</strong> use the
        most recent available installer labelled "snow-leopard"
        <a href="http://sourceforge.net/projects/git-osx-installer/files/">available here</a>.
        Because this installer is not signed by the developer, you may have to
        right click (control click) on the .pkg file, click Open, and click
        Open in the pop-up dialog. You can watch
        <a href="https://www.youtube.com/watch?v=9LQhwETCdwY ">a video tutorial about this case</a>.
      </p>
    </div>
    <div class="col-md-4">
      <h4 id="git-linux">Linux</h4>
      <p>
        If Git is not already available on your machine you can try to
        install it via your distro's package manager. For Debian/Ubuntu run
        <code>sudo apt-get install git</code> and for Fedora run
        <code>sudo dnf install git</code>.
      </p>
    </div>
  </div>
</div> {% comment %} End of 'Git' section. {% endcomment %}


<div id="r"> {% comment %} Start of 'R' section. {% endcomment %}
  <h3>R</h3>

  <p>
    <a href="https://www.r-project.org">R</a> is a programming language
    that is especially powerful for data exploration, visualization, and
    statistical analysis. To interact with R, we use
    <a href="https://www.rstudio.com/">RStudio</a>.
  </p>

  <div class="row">
    <div class="col-md-4">
      <h4 id="r-windows">Windows</h4>
      <a href="https://www.youtube.com/watch?v=q0PjTAylwoU">Video Tutorial</a>
      <p>
        Install R by downloading and running
        <a href="https://cran.r-project.org/bin/windows/base/release.htm">this .exe file</a>
        from <a href="https://cran.r-project.org/index.html">CRAN</a>.
        Also, please install the
        <a href="https://www.rstudio.com/products/rstudio/download/#download">RStudio IDE</a>.
        Note that if you have separate user and admin accounts, you should run the
        installers as administrator (right-click on .exe file and select "Run as
        administrator" instead of double-clicking). Otherwise problems may occur later,
        for example when installing R packages.
      </p>
    </div>
    <div class="col-md-4">
      <h4 id="r-macosx">macOS</h4>
      <a href="https://www.youtube.com/watch?v=5-ly3kyxwEg">Video Tutorial</a>
      <p>
        Install R by downloading and running
        <a href="https://cran.r-project.org/bin/macosx/R-latest.pkg">this .pkg file</a>
        from <a href="https://cran.r-project.org/index.html">CRAN</a>.
        Also, please install the
        <a href="https://www.rstudio.com/products/rstudio/download/#download">RStudio IDE</a>.
      </p>
    </div>
    <div class="col-md-4">
      <h4 id="r-linux">Linux</h4>
      <p>
        You can download the binary files for your distribution
        from <a href="https://cran.r-project.org/index.html">CRAN</a>. Or
        you can use your package manager (e.g. for Debian/Ubuntu
        run <code>sudo apt-get install r-base</code> and for Fedora run
        <code>sudo dnf install R</code>).  Also, please install the
        <a href="https://www.rstudio.com/products/rstudio/download/#download">RStudio IDE</a>.
      </p>
    </div>
  </div>
</div> {% comment %} End of 'R' section. {% endcomment %}

<h2 id="coc">Code of Conduct ✅</h2>
We are dedicated to providing a welcoming and supportive environment for all people, regardless of
background or identity. However, we recognise that some groups in our community are subject to historical
and ongoing discrimination, and may be vulnerable or disadvantaged. Membership in such a specific group
can be on the basis of characteristics such as gender, sexual orientation, disability, physical
appearance, body size, race, nationality, sex, colour, ethnic or social origin, pregnancy, citizenship,
familial status, veteran status, genetic information, religion or belief, political or any other opinion,
membership of a national minority, property, birth, age, or choice of text editor. We do not tolerate
harassment of participants on the basis of these categories, or for any other reason.

Harassment is any form of behaviour intended to exclude, intimidate, or cause discomfort. Because we
are a diverse community, we may have different ways of communicating and of understanding the intent
behind actions. Therefore we have chosen to prohibit certain forms of behaviour in our community,
regardless of intent. Prohibited harassing behaviour includes but is not limited to:

written or verbal comments which have the effect of excluding people on the basis of membership
of a specific group listed above causing someone to fear for their safety, such as through
<p>
  <ul>
      <li>stalking, following, or intimidation</li>
<li>the display of sexual or violent images</li>
<li>unwelcome sexual attention</li>
<li>nonconsensual or unwelcome physical contact</li>
<li>sustained disruption of talks, events or communications</li>
<li>incitement to violence, suicide, or self-harm</li>
<li>continuing to initiate interaction (including photography or recording) with someone after being asked to stop</li>
<li>publication of private communication without consent</li>
     </ul>
    </p>
<p>
Behaviour not explicitly mentioned above may still constitute harassment. The list above should not be taken as exhaustive but rather as a guide to make it easier to enrich all of us and the communities in which we participate. All interactions should be professional regardless of location: harassment is prohibited whether it occurs on- or offline, and the same standards apply to both.
  </p>
<p>
Enforcement of the Code of Conduct will be respectful and not include any harassing behaviors.
  </p>
<p>
Thank you for helping make this a welcoming, friendly community for all.
  </p>
<p>
This code of conduct is an adaptation of the one used by the Software Carpentry Foundation and is a modified version of that used by PyCon, which in turn is forked from a template written by the Ada Initiative and hosted on the Geek Feminism Wiki. Contributors to this document: Adam Obeng, Aleksandra Pawlik, Bill Mills, Carol Willing, Erin Becker, Hilmar Lapp, Kara Woo, Karin Lagesen, Pauline Barmby, Sheila Miguez, Simon Waldman, Tracy Teal.

<h2 id="people">Further reading 📄👀</h2>

<p>Eglen, S. J., Marwick, B., Halchenko, Y. O., Hanke, M., Sufi, S., Gleeson, P., &hellip; &amp; Wachtler, T. (2017). Toward standard practices for sharing computer code and programs in neuroscience. <em>Nature Neuroscience</em> 20(6), 770-773. [<a href="http://doi.org/10.1038/nn.4550" target="_blank">DOI</a>] [<a href="https://doi.org/10.1101/045104" target="_blank">preprint</a>] [<a href="http://faculty.washington.edu/bmarwick/PDFs/Eglen_Marwick_et_al_2017_sharing_code.pdf" target="_blank">PDF</a>]</p>

<p>Marwick, B. 2017 Computational reproducibility in archaeological research: Basic principles and a case study of their implementation. <em>Journal of Archaeological Method and Theory</em> 24(2), 424-450. [<a href="http://doi.org/10.1007/s10816-015-9272-9" target="_blank">DOI</a>] [<a href="https://osf.io/preprints/socarxiv/q4v73" target="_blank">preprint</a>] <a href="https://doi.org/10.6084/m9.figshare.1563661" target="_blank">[code &amp; data]</a></p>

<p>Marwick 2017 Using R and Related Tools for Reproducible Research in Archaeology. In Kitzes, J., Turek, D., &amp; Deniz, F. (Eds.) <em>The Practice of Reproducible Research: Case Studies and Lessons from the Data-Intensive Sciences.</em> Oakland, CA: University of California Press. [<a href="https://www.practicereproducibleresearch.org/case-studies/benmarwick.html" target="_blank">online</a>]</p>

<p>Marwick, B., &amp; Birch, S. 2018 A Standard for the Scholarly Citation of Archaeological Data as an Incentive to Data Sharing. <em>Advances in Archaeological Practice</em> 1-19. [<a href="https://doi.org/10.1017/aap.2018.3" target="_blank">DOI</a>] [<a href="https://osf.io/preprints/socarxiv/py4hz/" target="_blank">preprint</a>] [<a href="http://faculty.washington.edu/bmarwick/PDFs/Marwick-and-Pilaar-Birch-2018-Data-Citation-AAP.pdf" target="_blank">PDF</a>] [<a href="https://doi.org/10.17605/OSF.IO/KSRUZ" target="_blank">code &amp; data</a>]</p>

<p>Marwick, B., Boettiger, C., &amp; Mullen, L. 2017 Packaging data analytical work reproducibly using R (and friends). <em>The American Statistician</em>  [<a href="https://doi.org/10.1080/00031305.2017.1375986" target="_blank">DOI</a>] [<a href="https://doi.org/10.7287/peerj.preprints.3192v1" target="_blank">preprint</a>]</p>

<p>Marwick, B, d’Alpoim Guedes, J., Barton, C. M., Bates, L. A., Baxter, M., Bevan, A., Bollwerk, E. A., Bocinsky, R. K., Brughmans, T., Carter, A. K., Conrad, C., Contreras, D. A., Costa, S., Crema, E. R., Daggett, A., Davies, B., Drake, B. L., Dye, T. S., France, P., Fullagar, R., Giusti, D., Graham, S., Harris, M. D., Hawks, J., Health, S., Huffer, D., Kansa, E. C., Kansa, S. W., Madsen, M. E., Melcher, J., Negre, J., Neiman, F. D., Opitz, R., Orton, D. C., Przstupa, P., Raviele, M., Riel-Savatore, J., Riris, P., Romanowska, I., Smith, J., Strupler, N., Ullah, I. I., Van Vlack, H. G., VanValkenburgh, N., Watrall, E. C., Webster, C., Wells, J., Winters, J., and Wren, C. D. (2017) Open science in archaeology. <em>SAA Archaeological Record</em>, 17(4), pp. 8-14. [<a href="http://onlinedigeditions.com/publication/?i=440506#{%22issue_id%22:440506,%22page%22:10}" target="_blank">PDF</a>] [<a href="https://osf.io/preprints/socarxiv/72n8g/" target="_blank">preprint</a>]</p>

<p>Ram, K. B. Marwick 2017 Building Towards a Future Where Reproducible, Open Science is the Norm. In Kitzes, J., Turek, D., &amp; Deniz, F. (Eds.) <em>The Practice of Reproducible Research: Case Studies and Lessons from the Data-Intensive Sciences.</em> Oakland, CA: University of California Press. [<a href="https://www.practicereproducibleresearch.org/core-chapters/6-future.html" target="_blank">online</a>]</p>

<p>Rokem, A., B. Marwick, V. Staneva 2017 Assessing Reproducibility. In Kitzes, J., Turek, D., &amp; Deniz, F. (Eds.) <em>The Practice of Reproducible Research: Case Studies and Lessons from the Data-Intensive Sciences.</em> Oakland, CA: University of California Press. University of California Press. [<a href="https://www.practicereproducibleresearch.org/core-chapters/2-assessment.html" target="_blank">online</a>]</p>

<h2 id="people">About the instructors 🍎 </h2>

<a href="http://faculty.washington.edu/bmarwick/">Ben Marwick</a> is an Associate Professor of archaeology at the University of Washington. He studies Pleistocene archaeology in mainland Southeast Asia and Australia. He uses R in his day-to-day work and research publications, and has written extensively (including in <em><a href="http://www.nature.com/neuro/journal/v20/n6/full/nn.4550.html">Nature</a></em> and the <em><a href="https://link.springer.com/article/10.1007/s10816-015-9272-9">Journal of Archaeological Method and Theory</a></em>) on the importance of using code to improve the reproducibility of research in archaeology and elsewhere. Ben is the convener of the SAA Open Science Interest Group.
<p>
</p>
<a href="https://matthewdharris.com/">Matt Harris</a> is the Director of GIS,
Data Analysis, & Geoarchaeology in the Cultural Resources Deptartment of AECOM. He is an advanced R user, with a focus on spatial analysis and simulation. He documents many of his explorations using R on his <a href="https://matthewdharris.com/">blog</a>. Matt is a member of the SAA Open Science Interest Group, and has previously instructed R to archaeologists via the SAA Online workshops and in person.
<p>
</p>
