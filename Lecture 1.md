# EECS 388 - Intro to Computer Security

January 4, 2017.

## What is computer security?

Security is separated from most CS disciplines by the difference between these two disasters: a bridge collapsing and 9/11. One was caused by the forces of nature acting against human error, and the other was an engineered disaster.

> Computer security studies how systems behave in the presence of an adversary.

That is, an *intelligence* that actively tries to make the system misbehave. What are their motives? Capabilities? Degrees of access?

## The security mindset

You have to think like an **attacker and a defender**. Attacker: Understanding techniques for circumventing security, and ways that it can break. Defender: know what you’re defending and against whom. Weighing benefits vs costs: no system is ever completely secure.

## Why study attacks?

To identify vulnerabilities that can be fixed. Creating incentives for vendors to be careful. Learning about new classes of threats.

## Insecurity terminology

* **Level-0 problem (“Assault”)**: Actual malicious attempt to cause harm
* **Level-1 problem (“Vulnerability”)**: Specific errors that could be exploited in an assault
* **Level-2 problem (“Weakness”)**: Factors that predispose systems to vulnerability

An **“attack”** is an assault recipe, and vulnerabilities are ingredients. For example, a malicious email can lead users to a fake login form. That would be an attack.

## Thinking like an attacker

For every system you interact with, think about what it means to be secure, and imagine how it could be exploited by an attacker.

* Look for weakest links
* Identify assumptions that could be falsified
* Thinking outside of the box: not constrained by system designer’s worldview

For example, every disk system made the assumption that RAM disappears instantly. That assumption isn’t exactly true - Halderman and his students used this to get access to private keys in RAM before they disappeared a couple seconds after shutdown.

## Thinking as a defender

Try to craft a policy about what you’re trying to protect. Which assets? Which properties are you trying to enforce for those assets?

Say you’re trying to secure the CS building. That really means you’re trying to guard the upper floors after hours to protect against theft.

**Create a threat model**: Which kinds of attacks are worth defending against? Which are not?

Let’s say you’re trying to protect the CS building. It’s probably not worth preparing for an attack with a tank, because it’s too expensive and extremely unlikely. The expected cost (chance of attack times cost of attack) is too low to have a benefit.

**Technical vs nontechnical countermeasures**: card reader on door vs jail.

## Security policies

Which *assets* are you trying to protect?

* Confidentiality: only authorized people can read info
* Integrity: auth can change
* Availability: auth can access it
* Privacy: ill defined
* Authenticity: actors are who they claim to be

## Assessing risk

It’s all about *rational paranoia.*

What would security breaches cost us?

* Direct cost: design, implementation, enforcement, false positives
* Indirect cost: lost productivity, added complexity

Challenge is rationally cost vs risk: human psych makes reasoning about high cost / low probability events hard. Unfortunately, that’s how many attacks are. Someone could break into a bank and steal all the money. That’s really low probability but should we keep advancing the tech?

## Secure design

**Security is a process and not a product.** Don’t try to convince yourself that a system is secure; convince yourself that it’s not secure and try to see if you fail.