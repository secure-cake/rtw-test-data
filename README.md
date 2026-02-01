# Rapid Triage Case Data - AI Testing
"Are you using AI for incident-response investigations?" - My answer...sort of! At this point, using AI for increased efficiencies is my goal, NOT to have AI do something that I don't fully understand how to do already. 

Thus far, one of the most effective testing/learning mechanisms for me, is first manually analyzing a case (triage-data output), then exerpimenting with AI review and validation. 

I have HUGE concerns about accuracy, repeatability, privacy/security, and quantifiable efficiancies. So, I present to you some sample, "test" case data for review, upload, analysis, prompt testing/refinement, etc. 

Go [HERE](https://github.com/secure-cake/rapid-endpoint-investigations/wiki/Rapid-Endpoint-Investigations-%E2%80%90-Wiki-Home) if you want to review my rapid-triage workflow!

## Case 1 Win11
The [Case1](https://github.com/secure-cake/rtw-test-data/blob/main/Case1-Windows-KAPE-and-RTW.7z) zip file contains raw rapid-triage artifacts, as well as KAPE-processed artifacts. Additionally, the [SPOILERS](https://github.com/secure-cake/rtw-test-data/blob/main/Case1-Win11-SPOILERS.7z) zip contains a bunch of pre-identified artifacts so you can "cheat!" Review, understand the case and contents, then upload discrete artifacts to your AI of choice, test prompts, review accuracy/output, refine, repeat!

## Case 2 Win11
The [Case2](https://github.com/secure-cake/rtw-test-data/blob/main/Case2-Windows-KAPE-and-RTW.7z) zip is just another malware-infected machine for your review/analysis, with [SPOILERS](https://github.com/secure-cake/rtw-test-data/blob/main/Case2-Win11-SPOIILERS.7z) zip. 

## IMPORTANT
Both Case1 and Case2 are "outlined" in the Rapid Triage Test Data [SPOILERS PDF](https://github.com/secure-cake/rtw-test-data/blob/main/Rapid-Triage-Test-Data-SPOILERS.pdf). 

NOTE: There is NO malware in this data, just malware artifacts. 

## AI Prompt Example
This is just a very simple example, to illustrate an approach! I fed Claude a CSV services list (part of RTW output), then asked: 

``
Can you help me analyze a list of Windows Services to identify remote access services?
``

In response, I got a list of 20+ "remote access" services, from RDP to Remote Registry, all of which were non-malicious, except one! Accurate? I suppose so! Efficient, not so much!

``
Examine the services csv and find any third-party remote access services installed in non-standard paths.
``

In response, I got a list of ONE service, the "evil" one I knew existed from my previous analysis. Accurate...100%. Efficient, now we're talkin'!

I went on from there to feed Claude EVTX, query for events related to the "evil" service installation, etc., etc. 



## Stay Tuned!
More to come. 
