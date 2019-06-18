# Email Analysis Tool
This repo is intended to be a set of tools for basic analysis of email inboxes, for initial triage only.

##Email Parser - Images
Takes an email inbox in MBOX form and outputs a list of all the emails with images attached and the time differences between when they were sent and when the images were created

The images are also decoded and pulled out of the inbox for further Analysis

## Email Parser - Text
Takes an email inbox in MBOX form and extracts text from various MIME types (docx, pdf, plain) and outputs a list of the emails with text (cleaned and preprocessed)

##Facial Recognition
Takes a folder of images (e.g. extracted from an inbox by Email Parser - Images) and tries to identify faces in the images. Outputs two folders one with the images it thinks contains faces and one that contains images it thinks do not.

Also puts face images into equal length vectors (using PCA) to enable follow on analysis (e.g. image similarity)

##Convert MailDir to MBox
Converts a MailDir folder (and it's subfolder) to an MBox file for use in Email Parser - Images and Email Parser - Text.
