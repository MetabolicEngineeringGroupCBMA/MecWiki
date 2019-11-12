#!/usr/bin/env python
# -*- coding: utf-8 -*-

##########################################################################################################

'''
This page contains your user id and password for the mail plugin. This page
will be imported as a module, so be careful not to introduce syntax errors.
Your mail contacts are on the page mail-contacts by default, see last line
below
The formatting of email addresses on the mail contacts page should comply with
RFC2822 (http://www.faqs.org/rfcs/rfc2822). Some examples are:
user@example.com
user@example.com, anotheruser@example.com
User <user@example.com>
User <user@example.com>, Another User <anotheruser@example.com>
A Group:Chris Jones <c@a.test>,joe@where.test,John <jdoe@one.test>;
'''

smtpserver      =  'mail.uminho.pt'
smtpport        =  25
smtptimeout     =  30
smtphostname    =  'localhost'
smtpuser        =  'd1234'                               # a12345 or d1234
smtppass        =  'password     '                       # webmail password
sender          =  'Bat_Man@bio.uminho.pt'               # JohnDoe@somewhere.pt
extra_recipient =  'sentwp<karl12+wikidpad@gmail.com>'  # karl12@gmail.com
contacts_page   =  'mail-contacts'

##########################################################################################################

keyid               = 'keyID'                             # <=== change this to your own keyID
passphrase          = 'PASSWORD'                          # <=== change this to your own password for that key
subject             = 'Signature for stamping'
to                  = '<clear@stamper.itconsult.co.uk>'
recipients          = None                                # add more recipients here if you like!
content             = '''
This email contains a GnuPrivacyGuard signature of the file

$zipfilename

This signature was created $timestamp
using the key $keyid

This text was sent to PGP Digital Timestamping Service ($to) for stamping. 
The URL of this service is http://www.itconsult.co.uk/stamper.htm
The last PGP signature in this email text is a trusted timestamp from stamper.

The verification of this timestamp using stampers public key
(http://www.itconsult.co.uk/stamper/stampinf.htm) followed by verification of
GnuPrivacyGuard signature using $keyid proves that the file

$zipfilename

existed at least as early as the time and date given above.
'''

path_to_ape_lin ='tclsh /home/bjorn/.ApE/apeextractor/ApE.vfs/lib/app-AppMain/AppMain.tcl'
path_to_ape_win ='"C:\\Program Files\\ApE\\ApE.exe"'
path_to_ape_mac =''

##########################################################################################################

template_separator  = 'templates'
flankuplength       = 200
flankdnlength       = 200
max_product_size    = 10000
homology_limit      = 12
cutoff_featured_template = 6
cutoff_detailed_figure   = 5
cutoff_minimum_lines_for_report_in_subpage = 20

report_header= '''
  ==============
  PCR simulation
  ==============
'''

report_for_each_simulation = '$anneal_primers'

report_for_each_amplicon =  '''
PCR product from $template_name
>$forward_primer_name
$forward_primer_sequence
>$reverse_primer_name
$reverse_primer_sequence
>$product_name
$product_sequence
$figure
suggested PCR programs
$pcr_program
'''

 #uncomment the following lines to get flanking sequences in report
 #>upstream_flanking_sequence
 #$upstream_flanking_sequence
 #>downstream_flanking_sequence
 #$downstream_flanking_sequence

 ########### settings for flavios primers
 #report_header=""
 #report_for_each_simulation = ""
 #report_for_each_amplicon = '''$forward_primer_name
 #$reverse_primer_name
 #$figure
 #>upstream_flanking_sequence
 #$upstream_flanking_sequence
