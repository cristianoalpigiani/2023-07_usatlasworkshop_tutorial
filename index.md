---
layout: workshop      # DON'T CHANGE THIS.
# More detailed instructions (including how to fill these variables for an
# online workshop) are available at
# https://carpentries.github.io/workshop-template/customization/index.html
venue: "2023 US ATLAS Workshop @ Yale University"        # brief name of the institution that hosts the workshop without address (e.g., "Euphoric State University")
#address: "FIXME"      # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria"), videoconferencing URL, or 'online'
#country: "FIXME"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1#Current_codes) for the institution that hosts the workshop
#language: "FIXME"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) for the workshop
#latitude: "45"        # decimal latitude of workshop venue (use https://www.latlong.net/)
#longitude: "-1"       # decimal longitude of the workshop venue (use https://www.latlong.net)
humandate: "July 19, 2023"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
#humantime: "FIXME"    # human-readable times for the workshop e.g., "9:00 am - 4:30 pm CEST (7:00 am - 2:30 pm UTC)"
#startdate: FIXME      # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
#enddate: FIXME        # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["Amber Roepe-Gier", "Verena Martinez", "Doug Benjamin", "Cristiano Alpigiani"] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
#helper: ["helper one", "helper two"]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
#email: ["first@example.org","second@example.org"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
collaborative_notes: https://usatlas.readthedocs.io/projects/af-docs/en/latest/ # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document (e.g., https://pad.carpentries.org/2015-01-01-euphoria)
#eventbrite:           # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
---

<div class="alert alert-success">
  This tutorial wants to guide the users through the baseline setup to submit a job at an analysis facility (UChicago in this tutorial). It is based on the material presented in this <a href="https://cecilia-duran.github.io/2022-04_gh_usatlas_af_qst/index.html">this</a> tutorial (credits Cecilia Duran).
</div>

> ## Prerequisites
>
>
> This assumes you already have:
>
> - <strong>A CERN account</strong>
>
> - <strong>The respective X509 Proxy Certificate, e.g. to access ATLAS Data</strong>. You can use the same you copied on lxplus (in case you already did it) or download it from this CERN page: <a href="https://cafiles.cern.ch/cafiles/">https://cafiles.cern.ch/cafiles/</a>.
>
>
{: .prereq}

<hr/>

<h2 id="general">General Information</h2>

{% comment %} INTRODUCTION {% endcomment %}

{% include swc/intro.html %}

{% comment %} AUDIENCE {% endcomment %}

{% include swc/who.html %}

{% comment %} LOCATION {% endcomment %}

<p id="where">
  <strong>Where:</strong>
  <strong>Luce Hall</strong>, 34 Hillhouse Avenue in New Haven, CT. More info ,<a href="https://conferencesandevents.yale.edu/about-us/venues/luce-hall"></a>.
</p>

{% comment %} DATE {% endcomment %}

{% if page.humandate %}
<p id="when">
  <strong>When:</strong>
  {{page.humandate}}.
  {% include workshop_calendar.html %}
</p>
{% endif %}

{% comment %} SPECIAL REQUIREMENTS {% endcomment %}

<p id="requirements">
  <strong>Requirements:</strong>
    No specific requirements. Participants must bring a laptop with a Mac, Linux, or Windows operating system.
</p>

{% comment %} CONTACT EMAIL ADDRESS {% endcomment %}

<p id="contact">
  <strong>Contact:</strong>
  Please email <a href='mailto:amber.roepe-gier@cern.ch,Verena.Martinez@cern.ch,Douglas.Benjamin@cern.ch,Cristiano.Alpigiani@cern.ch'>the tutorial organizers</a>. 

  
</p>

<hr/>
{% comment%} CODE OF CONDUCT {% endcomment %}

<h2 id="code-of-conduct">Code of Conduct</h2>
<p>
Everyone who participates in Carpentries activities is required to conform to the <a href="https://docs.carpentries.org/topic_folders/policies/code-of-conduct.html">Code of Conduct</a>. 
This document also outlines how to report an incident if needed.
</p>

<hr/>
{% comment %} DOCUMENTATION {% endcomment %}

<h2 id="Documentation">Documentation</h2>
<p> You can find a lot of useful information in <a href="https://usatlas.readthedocs.io/projects/af-docs/en/latest/">Public Documentation for US ATLAS Analysis Facilities</a>. </p>


{% comment%} SCHEDULE {% endcomment %}

{% include base_path.html %}

<hr/>
<h2 id="schedule">Schedule</h2>

<div class="syllabus">
  
  <table class="table table-striped">
    <tr> <td colspan="3"> <font color="yellow"><strong>Pre tutorial</strong></font> </td> </tr>
     <tr> <td class="col-md-2">Before</td>      <td class="col-md-3"><a href="{{ relative_root_path }}/00-uchicago_af_intro/index.html">Intro on AF</a> </td> <td class="col-md-7"> Why having an Analysis Facility at US-ATLAS? </td> </tr>      
     <tr> <td class="col-md-2">09:45-10:00</td> <td class="col-md-3"><a href="{{ relative_root_path }}/01-accountrequest/index.html">UChicago account request</a> </td> <td class="col-md-7"> How can I join Chicago US-ATLAS analysis facility? </td> </tr>
     <tr> <td class="col-md-2">10:00</td>       <td class="col-md-3"><strong>Coffee</strong> </td> <td class="col-md-7"> Enjoy it! </td> </tr>
    <tr> <td colspan="3"> <font color="LimeGreen"><strong>Main tutorial</strong></font> </td> </tr>
     <tr> <td class="col-md-2">10:30</td>       <td class="col-md-3"><a href="{{ relative_root_path }}/02-atlasenv/index.html">ATLAS environment setup</a> </td> <td class="col-md-7"> Is it like we were on lxplus? </td> </tr>
     <tr> <td class="col-md-2">10:45</td>       <td class="col-md-3"><a href="{{ relative_root_path }}/03-htcondor/index.html">HT Condor</a> </td> <td class="col-md-7"> How Do I handle jobs with HTCondor? </td> </tr>
     <tr> <td class="col-md-2">11:15</td>       <td class="col-md-3"><a href="{{ relative_root_path }}/04-jupyter_lab/index.html">Jupiter Lab</a> </td> <td class="col-md-7"> What is JupyterLab? </td> </tr>
     <tr> <td class="col-md-2">EXTRA</td>       <td class="col-md-3"><a href="{{ relative_root_path }}/05-coffea_casa/index.html">Coffea Casa </a> </td> <td class="col-md-7"> What is Coffea Casa? </td> </tr>
     <tr> <td class="col-md-2">EXTRA</td>       <td class="col-md-3"><a href="{{ relative_root_path }}/06-goodpractices/index.html">Good Practises</a> </td> <td class="col-md-7"> How can we make the best use of the resources at the Analysis Facility? </td> </tr>
  </table>

</div>


{% comment %} SURVEYS {% endcomment %}

<h2 id="surveys">Surveys</h2>
<p>Please be sure to complete these surveys before and after the workshop.</p>
<p><a href="https://indico.cern.ch/event/1258537/surveys/4452">Pre-workshop Survey</a></p>
<p><a href="">Post-workshop Survey</a> Do we want to have one??????</p>

<hr/>

