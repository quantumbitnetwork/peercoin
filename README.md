
Peercoin Official Development Repo
==================================

[![Build Status](https://travis-ci.org/peercoin/peercoin.svg?branch=master)](https://travis-ci.org/peercoin/peercoin)

[![tip for next commit](https://peer4commit.com/projects/19.svg)](https://peer4commit.com/projects/19)

### What is Peercoin?
[Peercoin](https://peercoin.net) (abbreviated PPC), previously known as PPCoin, is the first [cryptocurrency](https://en.wikipedia.org/wiki/Cryptocurrency) design introducing [proof-of-stake consensus](https://peercoin.net/assets/paper/peercoin-paper.pdf) as a security model, with a combined [proof-of-stake](https://peercoin.net/assets/paper/peercoin-paper.pdf)/[proof-of-work](https://en.wikipedia.org/wiki/Proof-of-work_system) minting system. Peercoin is based on [Bitcoin](https://bitcoin.org), while introducing many important innovations to cryptocurrency field including new security model, energy efficiency, better minting model and more adaptive response to rapid change in network computation power.

### Peercoin Resources
* Client and Source:
[Client Binaries](https://peercoin.net/download),
[Source Code](https://github.com/peercoin/peercoin)
* Documentation: [Peercoin Whitepaper](https://peercoin.net/whitepaper),
[Peercoin Wiki](https://github.com/peercoin/peercoin/wiki)
* Help: 
[Forum](https://talk.peercoin.net),
[Intro & Important Links](https://talk.peercoin.net/t/what-is-peercoin-intro-important-links/2889)

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to submit new unit tests for old code.

Unit tests can be compiled and run (assuming they weren't disabled in configure) with:
  make check

Every pull request is built for both Windows and Linux on a dedicated server,
and unit and sanity tests are automatically run. The binaries produced may be
used for manual QA testing — a link to them will appear in a comment on the
pull request posted by [BitcoinPullTester](https://github.com/BitcoinPullTester). See https://github.com/TheBlueMatt/test-scripts
for the build/test scripts.

### Manual Quality Assurance (QA) Testing

Large changes should have a test plan, and should be tested by somebody other
than the developer who wrote the code.

* Developers work in their own forks, then submit pull requests when they think their feature or bug fix is ready.
* If it is a simple/trivial/non-controversial change, then one of the development team members simply pulls it.
* If it is a more complicated or potentially controversial change, then the change may be discussed in the pull request, or the requester may be asked to start a discussion in the [Peercoin Forum](https://talk.peercoin.net) for a broader community discussion. 
* The patch will be accepted if there is broad consensus that it is a good thing. Developers should expect to rework and resubmit patches if they don't match the project's coding conventions (see coding.txt) or are controversial.
* From time to time a pull request will become outdated. If this occurs, and the pull is no longer automatically mergeable; a comment on the pull will be used to issue a warning of closure.  Pull requests closed in this manner will have their corresponding issue labeled 'stagnant'.
* For development ideas and help see [here](https://talk.peercoin.net/c/protocol).

## Branches:

### develop (all pull requests should go here)
The develop branch is used by developers to merge their newly implemented features to.
Pull requests should always be made to this branch (except for critical fixes), and could possibly break the code.
The develop branch is therefore unstable and not guaranteed to work on any system.

### master (only updated by group members)
The master branch get's updates from tested states of the develop branch.
Therefore, the master branch should contain functional but experimental code.

### release-* (the official releases)
The release branch is identified by it's major and minor version number e.g. `release-0.6`.
The official release tags are always made on a release branch.
Release branches will typically branch from or merge tested code from the master branch to freeze the code for release.
Only critical patches can be applied through pull requests directly on this branch, all non critical features should follow the standard path through develop -> master -> release-*


-----------
***********
-----------
Peercoin developer notes
Contents
1 Notes that may be useful when looking to integrate / develop with Peercoin.
1.1 Mainnet
1.2 Testnet
2 Other developer pages
Notes that may be useful when looking to integrate / develop with Peercoin.
Peercoin Attribute	Value
Peercoin source code	https://github.com/ppcoin/ppcoin
Mainnet
Peercoin Attribute	Value
Peercoin Public Address lead Character	P
Peercoin Public Address lead Decimal	50
Peercoin Public Address lead Hex value	0x37
Peercoin Private Address lead Character	7
Peercoin Private Address lead Decimal	183
Peercoin Private Address lead Hex value	0xB7
Peercoin Private Address lead	K
Peercoin magic bytes	\xe6\xe8\xe9\xe5
Peercoin Genesis hash hex (big-endian)	0000000032fe677166d54963b62a4677d8957e87c508eaa4fd7eb1c880cd27e3
Peercoin Genesis hash bytes (little-endian)	\xe3\x27\xcd\x80\xc8\xb1\x7e\xfd\xa4\xea\x08\xc5\x87\x7e\x95\xd8\x77\x46\x2a\xb6\x63\x49\xd5\x66\x71\x67\xfe\x32\x00\x00\x00\x00
Peercoin Genesis tx hash hex	3c2d8f85fab4d17aac558cc648a1a58acff0de6deb890c29985690052c5993c2
Peercoin Genesis tx hash bytes	\xc2\x93\x59\x2c\x05\x90\x56\x98\x29\x0c\x89\xeb\x6d\xde\xf0\xcf\x8a\xa5\xa1\x48\xc6\x8c\x55\xac\x7a\xd1\xb4\xfa\x85\x8f\x2d\x3c
Peercoin default port	9901
Peercoin checkpoints	
Height	Hash
19080	000000000000bca54d9ac17881f94193fd6a270c1bb21c3bf0b37f588a40dbd7
30583	d39d1481a7eecba48932ea5913be58ad3894c7ee6d5a8ba8abeb772c66a6696e
99999	27fd5e1de16a4270eb8c68dee2754a64da6312c7c3a0e99a7e6776246be1ee3f
Testnet
Peercoin Attribute	Value
Peercoin Public Address lead Character	m or n
Peercoin Public Address lead Decimal	
Peercoin Public Address lead Hex value	
Peercoin Private Address lead Character	c
Peercoin Private Address lead Decimal	
Peercoin Private Address lead Hex value	
Peercoin Private Address lead	
Peercoin magic bytes	\xcb\xf2\xc0\xef
Peercoin Genesis hash hex (big-endian)	00000001f757bb737f6596503e17cd17b0658ce630cc727c0cca81aec47c9f06
Peercoin Genesis hash bytes (little-endian)	\x06\x9f\x7c\xc4\xae\x81\xca\x0c\x7c\x72\xcc\x30\xe6\x8c\x65\xb0\x17\xcd\x17\x3e\x50\x96\x65\x7f\x73\xbb\x57\xf7\x01\x00\x00\x00
Peercoin Genesis tx hash hex	3c2d8f85fab4d17aac558cc648a1a58acff0de6deb890c29985690052c5993c2
Peercoin Genesis tx hash bytes	\xc2\x93\x59\x2c\x05\x90\x56\x98\x29\x0c\x89\xeb\x6d\xde\xf0\xcf\x8a\xa5\xa1\x48\xc6\x8c\x55\xac\x7a\xd1\xb4\xfa\x85\x8f\x2d\x3c
Peercoin default port	9903
Peercoin checkpoints	Testnet has no checkpoints
Other developer pages
Constants in peercoin code
Main functions and methods in peercoin code
Peercoin protocol versions
