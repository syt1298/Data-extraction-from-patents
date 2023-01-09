# Data-extraction-from-patents

## Introduction

Patent Trial and Appeal Board (PTAB) API is a RESTful API with an easy to use search interface. You can easily browse USPTO PTAB public documents, search for specific content, and request a bulk download of PTAB content.  
The PTAB API synchronizes close to real time with the PTAB E2E (end-to-end) system making the latest public America Invents Action (AIA) Trials information and documents available.

## Problem statement

To extract the decision statement and the prior arts from the document.There are a wide range of PDFs starting from 1997 to 2021 which consist of different patterns. Many PDFs also consist of application numbers, docket numbers, confirmation numbers etc. The decision of the patent board is provided. We distinguish PDFs using the application numbers and they can be obtained using regular expressions.

## Dataset information

The data is extracted by calling the PTAB API. The pdfs are stored in a folder and are converted into text and are all stored. 

## Approach

Conducted experiments using parsing methods and regular expressions. Also used cosine similarity to get the similarity among documents.To extract the decision statement, we tried different approaches:

• Used regular expressions for a group of documents i.e used re.search(). A pandas data frame is created with columns as application number, text, decision text and decision.

• Used parsing method by using an if condition with (’affirmed.’, ’AFFIRMED’, ’Affirmed.’) in a text document.

