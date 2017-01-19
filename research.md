---
layout: default
title: Research
---

My research has been primarily focused on Web Security. I've worked on three
main areas:

* Securing users from vulnerabilities such as Cross-Site Scripting (XSS) and
Cross-Site Request Forgery (CSRF), which exploit web application bugs to
attack the user instead.

* Confinement and policy enforcement on untrusted JavaScript code.

* Development of secure Web Applications using the Spreadsheet paradigm.

This page summarizes my research efforts.

### XSSFilt<a name="xssfilt"></a>

When I started my Ph.D., I began with a simple research project -- porting my
advisor's [NDSS 2009 paper][sekar-ndss] which performed server-side XSS
filtering to a client-side Firefox extension.

The core of the NDSS 2009 paper was *taint-inference*, an alternative approach
to taint-tracking which avoids instrusive program instrumentation. Instead,
taint-inference relies on a novel approximate substring-matching algorithm
that infers taint across system boundaries, e.g. between a Web Server and its
Database backend.

I packaged the approximate substring-matching algorithm into a Firefox
extension and used it to infer taint between HTTP request data and HTTP
responses, in a similar fashion to Internet Explorer 8's XSS Filter. The main
difference is that Internet Explorer 8

  The XSS filter I developed for Firefox and my ASIACCS publication about XSS
  and ACSAC publication about CSRF fall into this category.

  I have also developed an XSS scanner, along with tools that allow an
  attacker to use search engines to discover new vulnerable sites. A tech
  report is available here

* <a name="sandbox"></a>Confinement and policy enforcement on untrusted
  JavaScript code.

  We have developed a confinement solution based on ES6 technologies to
  confine JavaScript code with no language restrictions and reasonable
  overhead. The first phase of this research (completed) was to achieve full
  mediation, building a secure confinement runtime. The related paper is in
  submission (available upon request, including implementation). The second
  (ongoing) phase of this project is to build upon the confinement runtime and
  develop a policy framework.

* <a name="spreadsheet"></a>Development of secure Web Applications using the
  Spreadsheet paradigm.

  Spreadsheet are an extremely successful programming paradigm, mostly thanks
  their simplicity and concreteness. In fact, non-programmers routinely use
  spreadsheets to build applications in tabular format, even though they don't
  refer to them as applications. We are studying whether it is possible to
  improve the spreadsheet paradigm and extend its applicability to Web
  Applications. The related paper is in submission (available upon request)

[sekar-ndss]: http://seclab.cs.sunysb.edu/seclab/pubs/ndss09.pdf