---
title: How I Passed eJPT
layout: note
categories:
  - certs
  - hacking
  - ejpt
---
In today's blog post, I will be going over my experience passing INE's eJPT (Junior Penetration Tester) certification. I'll briefly document my experience, lessons learned, and overall thoughts.

# Why go for it?

The first question to ask is why I was even interested in this certification.

The primary reason is because I needed a certification which can signal to HR practically-relevant pen-testing experience before going for something as substantial as the OSCP. The only certification that bridges this gap, as far as I know, is the eJPT.

Other well-known certs, such as the CPTS and PNPT, are either on the same level of the OSCP, or too niche to matter on a resume. That said, the eJPT itself isn't high-level enough that it replaces those heavy-hitters, but it's also not negligible.

Moreover, I wanted a professional test-oriented experience in regard to pen-testing to help solidify my basic skills and quicken some of my learning.

# My Experience

## Payment and Learning Material

I paid $199 for both the voucher (which includes a complimentary retake) as well as 3 months of eJPT-specific learning material from INE. Originally, it was $299, but a discount code I found online took off a hundred bucks! (I promise you I do not remember the code; but I had used AI to look for it, so try that)

I only had two weeks to cram so I couldn't afford paying for the voucher only and haphazardly deciding which material to study online.

The learning material itself was very professional and well-structured. You could tell the instructor (Alexis Ahmed) knew what he was talking about, and the courses themselves (structured sequentially under the Penetration Testing Student learning path) are properly organized.

Some of the content was definitely slightly repetitive, but not only is that unavoidable, but the individual courses are also supposed to be self-sufficient and independent to some extent, so it's understandable.

## Note Structure

I was taking notes using Obsidian and forming my own knowledge base that doubles as a methodology/playbook.

For example, I'd separate the phases (e.g., Reconnaissance, Post-Exploitation) sequentially and include therein their associated techniques, with dedicated tool pages and vector pages (e.g., SMB, FTP).

I should probably dedicate an entire blog to this, since it's not an exam-specific endeavor, and the way to take notes properly for hacking is more complicated than it seems, but for now, I'll keep it at that.

When actually taking the exam, I had one big Markdown-formatted page organized across "Nmap scans", "Comprehensive Findings" and "Questions".

## The Exam & Some Tips

You have 48 hours to pass the exam, and *I* was given 45 questions total.

You are not handed a specific target like a CTF; you're simply part of the network you're supposed to test the security of (using a browser-based cloud Kali environment), and expected to find hosts manually and work your way into internal machines.

I really liked that aspect because it felt extremely realistic for the sort of engagement you can expect in the real world.

I did not think the questions were sequential, as some of them referenced things I would've only reached during post-exploitation of, say, the third main target in the network (vis-à-vis the IP ordering).

That said, I think you should go question-by-question, and only branch out once one of the questions references something you must dedicate some time to, such as extensive web-app enumeration. This is because a question can directly hint at the answer (such as a MCQ asking what a user's password is; simply try all four options).

I initially spent a good amount of time running various Nmap scans to get a good idea of the working environment, and I hopped from machine to machine across the various pen-test phases as I saw fit based on the questions.

Evidently, I was oftentimes hopping between questions and skipping forth to answer what I could confidently answer in the moment whilst delegating what I couldn't to a later point.

It was immediately apparent how essential the note-taking was, as you had to keep track of your findings, flags, techniques attempted, etc. as you progressed.

## How Hard is it?

Objectively speaking (that is, weighing the exam based on the difficulty of knowing what enumeration to perform and what techniques to utilize, including the occasional inferred answers), I can confidently say the eJPT exam is **not difficult**.

That said, keep in mind that this perspective is objective. Realistically speaking, the difficulty is relative to your preparation and experience. I already had novice experience with HTB labs and similar CTF-style platforms. If someone is starting out from scratch or has little to no relevant pen-testing experience, then the exam is bound to be much harder for them.

Not to mention, if the (fairly generous) time limit gets to you or a question stumping you leads to a halt in progress, the exam might also end up being harder for you. Regardless, I do think this is an exception, and most people usually find the exam relatively easy to pass as long as you prepared decently.

## Compared to CTFs and Labs

If you're using INE's material, you're probably wondering if it's harder or easier than the included labs and CTFs.

The main difference which I believe makes the exam ever so slightly harder on a net level is that it includes multiple machines. This can quickly get overwhelming, whereas a CTF is only concerned with one machine, and labs are even less stressful as they're only concerned with a specific task like SMB enumeration.

But on a single-target level, it just comes down to the machine. Some of them would be harder than the CTFs, some easier.

Don't overthink it. Just practice, take notes, and go pass.

# Lessons Learned

A few lessons learned (some specific to the exam, some general) include:

- Expect that initial enumeration and reconnaissance will take a while; don't rush it unnecessarily.
- Before you do a version scan, a Windows host might genuinely look indistinguishable from a Linux host; don't haphazardly assume the OS (and don't fully trust Nmap's output either).
- When using Metasploit modules, ensure you customize the variables as needed; changing the `TARGETURI`, for instance, is the difference between exploitation netting a shell or silently failing.
- When a username is found, consider a dictionary attack (maybe parallel to other techniques); stick to the wordlist emphasized in the *Letter of Engagement* (like `rockyou.txt`).
- Don't overthink the questions or attempt fancy techniques; the core toolset given to you in your offline machine is more than enough.

# Final Thoughts

Overall, it was a great learning experience. I definitely recommend this certification to anyone seeking to solidify their amateur pen-testing skills if the premium doesn't bother you.

That said, adjust your expectations accordingly — this cert is beginner-friendly and primarily *meant* to act as a stepping-stone, so don't pat yourself on the back too hard after getting it, haha.
