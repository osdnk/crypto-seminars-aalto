# Crypto Seminars — Aalto University


## TBD

|                   |                  |
| ----------------- | ---------------- |
| **Date**          | 03 June 2026      |
| **Time**          | 11:00–12:00      |
| **Place**         | Maarintie 8, 1171 TU3 |
| **Speaker**       | Shuto Kuriyama          |


## Look Ahead! Practical CCA-secure Steganography: Cover-Source Switching meets Lattice Gaussian Sampling

|                   |                  |
| ----------------- | ---------------- |
| **Date**          | 06 May 2026      |
| **Time**          | 11:00–12:00      |
| **Place**         | Maarintie 8, 1171 TU3 |
| **Speaker**       | Ivy Woo          |
| **Paper title**   | Look Ahead! Practical CCA-secure Steganography: Cover-Source Switching meets Lattice Gaussian Sampling |
| **Paper authors** | Ivy K. Y. Woo, Russell W. F. Lai and Hoover H. F. Yin |

**Abstract.** Steganography studies methods to not only protect the confidentiality of messages but also to conceal the very act of message transmission. Prior provably secure stegosystems are predominantly constructed based on a rejection sampling technique which achieves an encoding rate inversely proportional to the min-entropy of the cover channel.

Furthermore, while replayable chosen-covertext attack (RCCA) secure stegosystems for general channels can be constructed based on standard cryptographic assumptions, it is known [Berndt and Liśkiewicz, EUROCRYPT'18] that achieving (standard) CCA-security for channels with memory in the so-called non-look-ahead model is in general impossible and the only known CCA-secure construction crucially relies on the channels being memoryless.

In this work, we show that the impossibility on CCA-secure stegosystems can be circumvented, in the random oracle model, by dropping the non-look-ahead restriction and by restricting to a natural class of channels which we call "partially sampleable channels''. These capture channels which partly consist of explicitly sampleable distributions, such as Gaussian sensor noise of digital photographs.

To achieve a high encoding rate, we extend the formalisation of stegosystems to capture a technique known as "cover-source switching'' in the practical steganography literature. This allows us to construct CCA-secure stegosystems for Gaussian channels using Gaussian preimage sampling techniques borrowed from lattice-based cryptography, which can theoretically achieve an embedding rate of $1/\omega(\log \log \secpar)$ regardless of the min-entropy of the channel.

Our prototype implementation suggests that our scheme is practical, achieving an embedding rate of 24.7\% in 24-megapixel RAW images in around 1 minute per image.


## Cyclo: Lightweight Lattice-based Folding via Partial Range Checks

|                   |                  |
| ----------------- | ---------------- |
| **Date**          | 22 April 2026    |
| **Time**          | 11:00–12:00      |
| **Place**         | Maarintie 8, 1021 AS3 Saab Space |
| **Speaker**       | Michał Osadnik   |
| **Paper title**   | Cyclo: Lightweight Lattice-based Folding via Partial Range Checks |

**Abstract.** Folding is a powerful technique for constructing efficient succinct proof systems, especially for computations that are expressed in a streaming fashion. In this work, we present Cyclo, a new lattice-based folding protocol that improves upon LatticeFold+ [Boneh and Chen '25] in multiple dimensions and which incorporates, among others, the pay-per-bit techniques from Neo when folding constraints expressed over a field F_q [Nguyen and Setty '25].

Cyclo proposes a new framework for building lattice-based folding schemes that eliminates the need for norm checks on the accumulator by adopting an amortized norm-refreshing design, ensuring that the witness norm grows additively per round within a (generously) bounded number of folds. This design simplifies the protocol and reduces prover overhead.

In particular, Cyclo only performs range checks on the input non-accumulated witness, and when applied to fold constraints over F_q, it does not decompose any witnesses into low-norm chunks within the folding protocol itself.

Cyclo, supporting a complete family of cyclotomic rings, combines two simple building blocks: an extension commitment that reduces the norm of the witness by decomposing it and recommitting, and an l-infinity range test via a sum-check protocol.

We demonstrate, by proving communication and runtime estimates, that the construction results in an efficient and proof-size-friendly folding scheme.

We also establish an algebraic connection between R_q and F_q using the polynomial evaluation map, enabling efficient reduction from R1CS/CCS over F_q to a linear relation over R_q, providing a new and simpler formulation of the techniques in [Nguyen and Setty '25].

In practical settings, Cyclo achieves succinct proof sizes on the order of 30 KB, improving by an order of magnitude over LatticeFold+. Our efficiency benchmarks indicate that our protocol also outperforms LatticeFold+ in practice.


## On Local Invariants for Permutation Equivalence

|                   |                  |
| ----------------- | ---------------- |
| **Date**          | 25 March 2026    |
| **Time**          | 11:00–12:00      |
| **Place**         | T3, CS Building  |
| **Speaker**       | Benjamin Benčina |

**Abstract.** We give an efficiently computable invariant for the (Signed) Permutation Code Equivalence ((S)PCE) problem we call the square class invariant, that was previously not recognised in coding theory. Our invariant naturally yields a distinguisher for the decision version of (S)PCE as defined at Eurocrypt 2025 by Albrecht, Benčina and Lai [ABL25], breaking the hardness assumption that underpins the security of their updatable public-key encryption scheme.

Moreover, we extend a 2023 result by Bruin, Ducas and Gibbons by showing the genus of the Construction A lattice of a code generator matrix with any hull dimension is completely determined by the hull dimension and our square class invariant, and that neither of these genera splits non-trivially into spinor genera (as soon as the lattice dimension is at least 5), implying the genus of the Construction A q-ary lattice encodes all known efficiently computable coding-theoretic invariants for (S)PCE and vice versa.

We also give a complete description of the genus distribution of uniformly random q-ary lattices.

This motivates the definition of a genus of a linear code as the genus of the Construction A lattice of any of its generator matrices, and we adapt the sampling algorithm from [ABL25] to sample from a single genus uniformly at random, and can thus restrict their hardness assumption for (S)PCE to a single genus. Restricting PCE to one genus and using our sampling algorithms is then used with a slight modification to the security proof to mend the scheme from [ABL25].

Finally we show that associating to a linear code generator matrix a quadratic space whose geometry is given by the corresponding Gram matrix and computing its Witt decomposition yields the same invariants that define the code genus, implying two q-ary lattices are locally equivalent if and only if the quadratic spaces associated to their underlying linear codes share a Witt decomposition type.

---------

## Quantum Tokenized Encryption

|                   |                  |
| ----------------- | ---------------- |
| **Date**          | 18 March 2026    |
| **Time**          | 11:00–12:00      |
| **Place**         | T3, CS Building  |
| **Speaker**       | Nikita Machine   |
| **Paper title**   | Quantum Tokenized Encryption |
| **Paper authors** | Nikita Machine and Russell Lai |

**Abstract.** This is a new cryptographic primitive that's best described as PKE where the public keys are quantum states that can only be used to produce one ciphertext each. In the talk, I intend to give a formal definition of this primitive, give a construction from standard lattice assumptions, and demonstrate this construction's security. On the way there, we will encounter a number of definitions and peculiarities of the quantum setting that will both help and hinder us.

Note that this talk will be heavy on quantum concepts and while I will do my best to explain them for those less familiar I will not be able to go too in depth for the sake of time.

---------

## Formal verification of reduction-based cryptography

|                   |                  |
| ----------------- | ---------------- |
| **Date**          | 04 March 2026    |
| **Time**          | 11:00–12:00      |
| **Place**         | T3, CS Building  |
| **Speaker**       | Chris Brzuska    |

**Abstract.** I'll give a brief intro on how formal verification of reduction-based cryptography works --- pretty much regardless of the tool. Then, I'll explain some definitional styles which make formalizing reduction proofs easier (again, regardless of the tool), and discuss some of the limitations of my preferred style in the context of key exchange.

This talk does not have pre-requisits except for being familiar with indistinguishability-based security games in cryptography.

---------

## Primer on Functional Commitments from Lattices

|                   |                  |
| ----------------- | ---------------- |
| **Date**          | 18 February 2026 |
| **Time**          | 11:00–12:00      |
| **Place**         | T3, CS building at Aalto University |
| **Speaker**       | Valerio Cini     |

**Abstract.** In this talk, I will introduce the notion of functional commitment and describe the key motivations behind this primitive. I will then survey recent lattice-based constructions, emphasizing the new techniques and assumptions that have been developed along the way, as well as open questions left to solve. The results presented are based primarily on the following works EC:Wee25, C:AbrMalRoy25, and C:Wee25.

---------

## From interaction to insecurity: Cracking the (Extended) Fiat-Shamir transform

|                   |                  |
| ----------------- | ---------------- |
| **Date**          | 03 December 2025 |
| **Time**          | 11:00–12:00      |
| **Place**         | T6, Konemiehentie 2 (CS Building), 02150 Espoo |
| **Speaker**       | Aleksi Kalsta    |

**Abstract.** Proof and argument systems are core building blocks of modern cryptography, enabling a prover to convince a verifier that a claimed statement is true. The Fiat--Shamir (FS) transform is a general method for removing interaction from public-coin proof and argument systems by replacing the verifier's random challenges with deterministic hashes of the intermediate protocol transcript.

Security analyses in the Random Oracle Model (ROM), together with the absence of attacks on deployed protocols, have provided a lot of confidence in its robustness and have made it widely used in practice. However, a series of contrived counterexamples in the standard model show that the security cannot be established in full generality. Consequently, most practical deployments lack a formal standard-model security proof and rely on heuristic security instead.

A recent attack by Khovratovich, Rothblum, and Soukhanov (KRS, CRYPTO~2025) on \emph{deployed} GKR-based succinct arguments makes this threat far more concrete than earlier counterexamples. Their attack exploits structural features of the GKR protocol via diagonalization and applies fairly broadly. In response, Arnon and Yogev (AY, CRYPTO~2025) propose an \emph{extended Fiat--Shamir} (XFS) transform intended to prevent such attacks.

In this thesis we (i) give a simple (contrived) counterexample to XFS, further illustrating the challenges of soundly removing interaction, and (ii) study the Fiat--Shamir transform of the SumCheck protocol when instantiated with the arithmetization-friendly hash function Poseidon. Concretely, we identify a structured variant of the CICO problem and show that an efficient solver for this problem enables a malicious prover to cheat in the Fiat--Shamir-transformed SumCheck protocol.

We further show how the same technique extends to protocols that invoke SumCheck as a subroutine, including GKR and HyperPlonk.

---------

## RoK and Roll – Verifier-Efficient Random Projection for Õ(λ)-size Lattice Arguments

|                   |                  |
| ----------------- | ---------------- |
| **Date**          | 19 November 2025 |
| **Time**          | 11:00–12:00      |
| **Place**         | T5, Konemiehentie 2 (CS Building), 02150 Espoo |
| **Speaker**       | Michał Osadnik   |
| **Paper title**   | RoK and Roll – Verifier-Efficient Random Projection for Õ(λ)-size Lattice Arguments |
| **Paper authors** | Michał Osadnik, Michael Klooß, Russell W. F. Lai, and Ngoc Khanh Nguyen |

**Abstract.** Succinct non-interactive arguments of knowledge (SNARKs) based on lattice assumptions offer a promising post-quantum alternative to pairing-based systems, but have until now suffered from inherently quadratic proof sizes in the security parameter. We introduce RoK and Roll, the first lattice-based SNARK that breaks the quadratic barrier, achieving communication complexity of Õ(λ) together with a succinct verification time.

The protocol significantly improves upon the state of the art of fully-succinct argument systems established by "RoK, Paper, SISsors'' (RPS) [ASIACRYPT'24] and hinges on two key innovations, presented as reductions of knowledge (RoKs):

-  Structured random projections: We introduce a new technique for structured random projections that allows us to reduce the witness dimensions while approximately preserving its L2 norm and maintaining the desired tensor structure. In order to maintain succinct communication and verification, the projected image is further committed and adjoined to the original relation. This procedure is recursively repeated until dimension of the intermediate witness becomes poly(λ), i.e. independent of the original witness length.
- Unstructured random projection: When the witness is sufficiently small, we let the unstructured projection (over coefficients ℤq) be sent in plain, as in LaBRADOR [CRYPTO'23]. We observe, however, that the strategy from prior works to immediately lift the projection claim to Rq, and into our relation, would impose a quadratic communication cost. Instead, we gradually batch-and-lift the projection a the tower of intermediate ring extensions. This reduces the communication cost to Õ(λ) while maintaining a succinct verification time.

These two techniques, combined with existing RoKs from RPS, yield a succinct argument system with communication complexity Õ(λ) and succinct verification for structured linear relations.

In this talk, I will focus on different variants of projections and present how those can be integrated in the context of SNARKs.

This is a joint work with Michael Klooß, Russell W. F. Lai, and Ngoc Khanh Nguyen.

---------

## Rejection Sampling Techniques in Lattice-based Cryptography

|                   |                  |
| ----------------- | ---------------- |
| **Date**          | 12 November 2025 |
| **Time**          | 11:00–12:00      |
| **Place**         | A142, Konemiehentie 2 (CS Building), 02150 Espoo |
| **Speaker**       | Shuto Kuriyama   |

**Abstract.** The talk summarises rejection sampling techniques, essential for lattice-based signatures and zero-knowledge proofs. Rejection sampling essentially allows you to generate sampling values from one distribution by sampling from another distribution. The technique has existed since Von Neumann introduced it in 1951. It was first introduced in the lattice-based cryptography context by Lyubashevsky in 2012 and was used to make a signature independent of its secret key.

Later, it was used to hide a witness from transcripts in a zero-knowledge proof by [LNP22]. However, rejection sampling algorithms tend to be a computationally-heavy block within a cryptograhpic scheme since it needs to be re-run until its success. Therefore, it is is crucial to improve the expected runtime of a rejection samling algorithm . Several works have proposed rejection sampling algorithms with better expected runtime including Leo Ducas et al. 2013 and Lyubashevsky et al. 2021.

In this talk, we overview the abovementioned rejection sampling algorithms.

---------

## Decomposed LWE and Key-Homomorphic Computation for RAM

|                   |                  |
| ----------------- | ---------------- |
| **Date**          | 29 October 2025  |
| **Time**          | 11:00–12:00      |
| **Place**         | T5, Konemiehentie 2 (CS Building), 02150 Espoo |
| **Speaker**       | Monisha Swarnakar |
| **Paper title**   | Decomposed LWE and Key-Homomorphic Computation for RAM |
| **Paper authors** | Abram, Malavolta, and Roy |

**Abstract.** In this talk, I will present new notions and tools introduced in two recent works by Damiano, Giulio, and Lawrence that push the boundary of succinct cryptographic computation.

The first introduces Succinct Oblivious Tensor Evaluation (OTE) — a two-party primitive that produces additive secret shares of the tensor product of two vectors x and y exchanging two simultaneous messages; crucially, both message sizes and the CRS is independent of the dimension of x. This enables them to obtain the first laconic function evaluation scheme that is adaptively secure from the standard LWE assumption, improving upon Quach, Wee, and Wichs (FOCS 2018).

The second develops Key-Homomorphic Computations for RAM — a new method to construct a public-key encryption scheme, where one can homomorphically transform a ciphertext encrypted under a key x into a ciphertext under (P, P(x)), for any polynomial-time RAM program P : x → y with runtime T and memory L. Combined with other lattice techniques, this allows to construct:

*   Succinct-randomized encodings for RAM programs with encoder complexity (|x| + |y|) poly(log T, log L) and rate-1 encodings.
*   Laconic function evaluation for RAM programs, with encoder runtime bounded by (|x| + |y|) · poly(log T, log L) and rate-1 encodings.
*   Key-policy attribute-based encryption for RAM programs, with ciphertexts of size poly(T). The same scheme can be converted to the register setting, obtaining linear CRS size in the number of parties.

Along with other standard computational assumptions on lattices, all their schemes rely on the hardness of decomposed learning with errors (LWE) problem, which can be interpreted as a circular-security of a natural lattice-based PKE scheme.

---------

## How to use Quantum Indistinguishability Obfuscation

|                   |                  |
| ----------------- | ---------------- |
| **Date**          | 08 October 2025  |
| **Time**          | 13:00–14:00      |
| **Place**         | U410a, Otakaari 1 (the Undergraduate Building), Espoo |
| **Speaker**       | Nikita Machine   |
| **Paper title**   | How to use Quantum Indistinguishability Obfuscation |
| **Paper authors** | Andrea Coladangelo and Sam Gunn |

**Abstract.** Quantum copy protection, introduced by Aaronson, enables giving out a quantum program-description that cannot be meaningfully duplicated. Despite over a decade of study, copy protection is only known to be possible for a very limited class of programs.

As our first contribution, we show how to achieve “best-possible” copy protection for all programs. We do this by introducing quantum state indistinguishability obfuscation (qsiO), a notion of obfuscation for quantum descriptions of classical programs. We show that applying qsiO to a program immediately achieves best-possible copy protection.

Our second contribution is to show that, assuming injective one-way functions exist, qsiO is concrete copy protection for a large family of puncturable programs — significantly expanding the class of copy-protectable programs. A key tool in our proof is a new variant of unclonable encryption (UE) that we call coupled unclonable encryption (cUE). While constructing UE in the standard model remains an important open problem, we are able to build cUE from one-way functions.

If we additionally assume the existence of UE, then we can further expand the class of puncturable programs for which qsiO is copy protection.

Finally, we construct qsiO relative to an efficient quantum oracle.

---------

## ABE for Circuits with poly(λ)-sized Keys from LWE

|                   |                  |
| ----------------- | ---------------- |
| **Date**          | 09 September 2025 |
| **Time**          | 16:00–17:00      |
| **Place**         | T5, Tietotekniikka (CS Building), Espoo |
| **Speaker**       | Valerio Cini     |
| **Paper title**   | ABE for Circuits with poly(λ)-sized Keys from LWE |
| **Paper authors** | Valerio Cini and Hoeteck Wee |

**Abstract.** We present a key-policy attribute-based encryption (ABE) scheme for circuits based on the Learning With Errors (LWE) assumption whose key size is independent of the circuit depth. Our result constituted the first improvement for ABE for circuits from LWE in almost a decade, given by Gorbunov, Vaikuntanathan, and Wee (STOC 2013) and Boneh, et al. (EUROCRYPT 2014) -- we reduce the key size in the latter from poly(depth,λ) to poly(λ).

The starting point of our construction is a recent ABE scheme of Li, Lin, and Luo (TCC 2022), which achieves poly(λ) key size but requires pairings and generic bilinear groups in addition to LWE; we introduce new lattice techniques to eliminate the additional requirements.

Joint work with Hoeteck Wee.

---------

## U Can Touch This! Microarchitectural Timing Attacks via Machine Clears

|                   |                  |
| ----------------- | ---------------- |
| **Date**          | 03 September 2025 |
| **Time**          | 11:00–12:00      |
| **Place**         | T5, Tietotekniikka (CS Building), Espoo |
| **Speaker**       | Billy B. Brumley |

**Abstract.** Microarchitectural timing attacks exploit subtle timing variations caused by hardware behaviors to leak sensitive information. This talk introduces MCHammer, a novel side-channel technique that leverages machine clears induced by self-modifying code detection mechanisms. Unlike most traditional techniques, MCHammer does not require memory access or waiting periods, making it highly efficient.

We compare MCHammer to the classical Flush+Reload technique, improving in terms of trace granularity, providing a powerful side-channel attack vector. Using MCHammer, we successfully recover keys from a deployed implementation of a cryptographic tool. Our findings highlight the practical implications of MCHammer and its potential impact on real-world systems.

---------

## A Practical Lattice-based Direct Anonymous Attestation Scheme from Computational Hardness Assumptions

|                   |                  |
| ----------------- | ---------------- |
| **Date**          | 05 August 2025   |
| **Time**          | 11:00–12:00      |
| **Place**         | M203 in Otakaari 1 |
| **Speaker**       | Joonas Ahola     |

**Abstract.** The design goal of many new PQ cryptographic primitives is that they are fast and small enough to be deployed in current hardware and software. This is also true for more advanced schemes that use these state-of-art primitives as components of their design. In this work, we present one such a scheme - lattice-based Direct Anonymous Attestation - and explain what makes our scheme both practical, and (hopefully) secure.

---------

## Side-Channel Resistance of Lattice-based Cryptographic Schemes

|                   |                  |
| ----------------- | ---------------- |
| **Date**          | 18 June 2025     |
| **Time**          | 11:00–12:00      |
| **Place**         | 021 AS3 Saab Space, Maarintie 8 (TUAS building), Espoo |
| **Speaker**       | Dijam Goran      |

**Abstract.** The risk of a scalable quantum computer being developed in the near future has given rise to the field of lattice-based cryptographic schemes that rely on lattice problems, which are believed to be unsolvable in polynomial time even by quantum computers. In the standardization process conducted by NIST, different lattice-based schemes were evaluated by their practicality, performance and security. However, side-channel resistance of these schemes has received limited attention.

In side-channel attacks, an adversary aims to learn information about sensitive values by exploiting information, such as timing delays and power consumption during a specific time. The main countermeasure against side-channel attacks is masking, which means splitting sensitive variables into several randomized shares that combined result in the original value.

Most literature on masking lattice-based schemes are about masking signature schemes, which are built using zero-knowledge proofs as building blocks. In lattice-based schemes, a zero-knowledge proof is used to prove the knowledge of some short vector s satisfying As = t (SIS-problem). However, in signature schemes a more relaxed solution is sufficient.

For constructing more complex protocols, such as group signatures, an exact proof is required. The latest lattice-based zero-knowledge proof presented in [LNP22] (LNP22), gives an efficient zero-knowledge proof of a vector s satisfying As = t with an exact proof of s being small, making it an attractive option for constructing lattice-based privacy primitives. However, there is currently no research that explicitly focuses on masking this protocol, therefore this paper fills that gap in the literature.

The challenge in masking LNP22 is that it involves several steps not found in the common signature schemes, such as quadratic equations.

In this paper, we study the latest practices in masking lattice-based schemes, and then identify the sensitive steps in LNP22 and provide a masking strategy for acquiring a side-channel secure implementation. Finally, we evaluate the efficiency of our masked design of LNP22 by evaluating the efficiency of each masked component individually. We found that masking incurs a significant overhead on the running time of LNP22, the primary bottleneck being the masked Gaussian sampling step.

---------

## Towards formally verifying the security reductions of the TLS 1.3 key schedule in SSBee

|                   |                  |
| ----------------- | ---------------- |
| **Date**          | 30 April 2025    |
| **Time**          | 13:00–14:00      |
| **Place**         | B119, Konemiehentie 2 (CS Building), Espoo |
| **Speaker**       | Amirhosein Rajabi |
| **Paper authors** | Amirhosein Rajabi, Brzuska, Egger, and Mödersheim |

**Abstract.** TLS is one of the most important cryptographic protocols protecting communications on the Internet. TLS 1.3 key schedule that refers to all cryptographic operations deriving keys for the handshake and record layer, such as handshake and application traffic secrets, among others. Brzuska, Delignat-Lavaud, Egger, Fournet, Kohbrok, Kohlweiss (BDEFKK, AsiaCrypt 2022) reduced the security of TLS 1.3 key schedule to security assumptions of the underlying primitives.

BDEFKK capture the security properties of the key schedule in the state-separating proofs (SSP) framework (Brzuska, Delignat-Lavaud, Fournet, Kohbrok, Kohlweiss, AsiaCrypt 2018). SSP allows to decompose monolithic code-based Bellare-Rogaway style games into modular stateful packages.

Proving code equivalence or functional equivalence of hybrid games is a common technique in cryptographic reductions. Two hybrid games are said to be functionally equivalent if, upon identical inputs to each of their exposed oracles, they both abort or return identical values. Demonstrating code equivalence of hybrid games on paper can be long, tedious, and error-prone, requiring intricate details of different oracles particularly in large and complex proofs.

Brzuska, Egger, and Winkelmann are developing SSBee (https://github.com/sspverif/sspverif/), a novel SMT-based tool, aimed to automate such code equivalence game hops. Moreover, BDEFKK prove the functional equivalence of two pairs of games in their proof of TLS 1.3 key schedule security proof, using an invariant argument, a proof technique imported from program verification.

In a joint work with Brzuska, Egger, and Mödersheim, we are formally verifying the functional equivalences and invariant arguments stated in TLS 1.3 key schedule security proof of BDEFKK using SSBee.

The talk starts with a brief introduction to the SSP framework and SSP style reductions. We will see what invariant arguments are and why they are useful to verification of code equivalence game hops. We then illustrate how SSBee captures functional equivalence steps as well as SSP-style reduction steps with the examples of selected (simplified) lemmata of the BDEFKK TLS 1.3 key schedule proof.

Finally, we conclude with a discussion of conceptual insights and guidelines for dealing with large scale proofs in SSBee and remaining open problems.

---------

## Papercraft: Lattice-based Verifiable Delay Function Implemented

|                   |                  |
| ----------------- | ---------------- |
| **Date**          | 16 April 2025    |
| **Time**          | 13:00–14:00      |
| **Place**         | T5, Konemiehentie 2 (CS Building), Espoo |
| **Speaker**       | Mihał Osadnik    |

**Abstract.** A verifiable delay function (VDF) requires a specified number of sequential steps to compute, yet the validity of its output can be verified efficiently, much faster than recomputing the function from scratch. VDFs are a versatile cryptographic tool with many industrial applications, such as blockchain consensus protocols, lotteries and verifiable randomness. Unfortunately, without exceptions, all known practical VDF constructions are broken by quantum algorithms.

Papercraft is an implementation of a VDF based entirely on lattice techniques and thus plausibly post-quantum secure. Our Papercraft implementation can verify a computation of over 6 minutes in just 7 seconds.

The theory of this work remains somewhat marginal as VDF is mainly based on observations on lattice-based succinct argument systems and existing time-based cryptography. However, it serves as an excellent polygon for exploring concrete efficiency aspects of lattice-based cryptography.

In this talk, I want to explain the VDF construction and then focus on concrete aspects of implementation, including (i) the practical (compared to theoretical) meaning of the "sequentiality" of VDF (ii) the fast arithmetic of (prime) cyclotomic rings (iii) advantage and limits of parallelization (iv) usage of open-source architecture-specific SIMD libraries.

---------

## Distributed Broadcast Encryption from Lattices

|                   |                  |
| ----------------- | ---------------- |
| **Date**          | 02 April 2025    |
| **Time**          | 11:00–12:00      |
| **Place**         | A142, CS Building, Konemiehentie 2, Espoo |
| **Speaker**       | Monisha Swarnakar |
| **Paper title**   | Distributed Broadcast Encryption from Lattices |
| **Paper authors** | Jeffrey Champion and David J. Wu |

**Abstract.** A broadcast encryption scheme allows a user to encrypt a message to 𝑁 recipients with a ciphertext whose size scales sublinearly with 𝑁 . While broadcast encryption enables succinct encrypted broadcasts, it also introduces a strong trust assumption and a single point of failure; namely, there is a central authority who generates the decryption keys for all users in the system.

Distributed broadcast encryption offers an appealing alternative where there is a one-time (trusted) setup process that generates a set of public parameters. Thereafter, users can independently generate their own public keys and post them to a public-key directory. Moreover, anyone can broadcast an encrypted message to any subset of user public keys with a ciphertext whose size scales sublinearly with the size of the broadcast set.

Unlike traditional broadcast encryption, there are no long-term secrets in distributed broadcast encryption and users can join the system at any time (by posting their public key to the public-key directory). Previously, distributed broadcast encryption schemes were known from standard pairing-based assumptions or from powerful tools like indistinguishability obfuscation or witness encryption. In this work, we provide the first distributed broadcast encryption scheme from a falsifiable lattice assumption.

Specifically, we rely on the ℓ-succinct learning with errors (LWE) assumption introduced by Wee (CRYPTO 2024). Previously, the only lattice-based candidate for distributed broadcast encryption goes through general-purpose witness encryption, which in turn is only known from the private-coin evasive LWE assumption, a strong and non-falsifiable lattice assumption. Along the way, we also describe a more direct construction of broadcast encryption from lattices.

---------

## A brief introduction to formal verification of cryptography (with biased focus)

|                   |                  |
| ----------------- | ---------------- |
| **Date**          | 19 March 2025    |
| **Time**          | 11:00–12:00      |
| **Place**         | A142, CS Building, Konemiehentie 2, Espoo |
| **Speaker**       | Chris Brzuska    |

**Abstract.** In this talk, we give a brief introduction to formal verification of cryptography. We start with a discussion of symbolic verification on the example of Tamarin. We then discuss the strength (automatizable, can study large protocols, finds attacks) and limitations (weak computational model) of the symbolic verification style and give a hint of Abadi and Rogaway's ideas to address the limitation via computational soundness.

If time allows, we also briefly discuss tools to formally verify cryptographic reduction proofs, in particular EasyCrypt.

The introduction is biased in the sense that we will only look at very few tools in the presentation (whereas there are quite many) based on what the speaker is familiar with rather than provide a comprehensive survey.

---------

## Lattice-based Proof-Friendly Signatures from Vanishing Short Integer Solutions

|                   |                  |
| ----------------- | ---------------- |
| **Date**          | 05 March 2025    |
| **Time**          | 11:00–12:00      |
| **Place**         | A106, CS Building, Konemiehentie 2, Espoo |
| **Speaker**       | Russell Lai      |
| **Paper title**   | Lattice-based Proof-Friendly Signatures from Vanishing Short Integer Solutions |

**Abstract.** Efficient anonymous credentials are typically constructed by combining proof-friendly signature schemes with compatible zero-knowledge proof systems. Inspired by pairing-based proof-friendly signatures such as Boneh- Boyen (BB) and Boneh-Boyen-Shacham (BBS), we propose a wide family of lattice-based proof-friendly signatures based on variants of the vanishing short integer solution (vSIS) assumption [Cini-Lai-Malavolta, Crypto'23].

In particular, we obtain natural lattice-based adaptions of BB and BBS which, similar to their pairing-based counterparts, admit nice algebraic properties.

[Bootle-Lyubashevsky-Nguyen-Sorniotti, Crypto'23] (BLNS) recently proposed a framework for constructing lattice-based proof-friendly signatures and anonymous credentials, based on another new lattice assumption called ISIS_f parametrised by a fixed function f, with focus on f being the binary decomposition. We introduce a generalised ISIS_f framework, called GenISIS_f, with a keyed and probabilistic function f.

For example, picking f_b(u) = 1/(b-u) with key b for short ring element u leads to algebraic and thus proof-friendly signatures. To better gauge the robustness and proof-friendliness of (Gen)ISIS_f, we consider what happens when the inputs to f are chosen selectively (or even adaptively) by the adversary, and the behaviour under relaxed norm checks. While bit decomposition quickly becomes insecure, our proposed function families seem robust.

---------

## Pseudorandom (Function-Like) Quantum State Generators: New Definitions and Applications

|                   |                  |
| ----------------- | ---------------- |
| **Date**          | 19 February 2025 |
| **Time**          | 17:00–18:00      |
| **Place**         | R030/B119, CS Building, Konemiehentie 2, Espoo |
| **Speaker**       | Nikita Machine   |
| **Paper title**   | Pseudorandom (Function-Like) Quantum State Generators: New Definitions and Applications |
| **Paper authors** | Ananth, Gulati, Qian, and Yuen |

**Abstract.** The talk will discuss pseudorandom states (PRSs) (an important primitive in quantum cryptography) and more particularly a generalisation of pseudorandom states called "pseudorandom function-like states" (PRFSs). PRFSs were first introduced in the earlier paper Cryptography from Pseudorandom Quantum States, which demonstrated how they could be used to build more advanced primitives.

In this paper, the first adaptively-secure construction is given, as well as constructions of bit commitments and symmetric encryption from PRSs that require only classical communication.

---------

## Lattice-based Folding Scheme from Unstructured Lattices

|                   |                  |
| ----------------- | ---------------- |
| **Date**          | 22 January 2025  |
| **Time**          | 15:00–16:00      |
| **Place**         | Y228b, Undergraduate Building, Otakaari 1 |
| **Speaker**       | Shuto Kuriyama   |
| **Paper title**   | Lova: Lattice-Based Folding Scheme from Unstructured Lattices |
| **Paper authors** | Fenzi et al.     |

**Abstract.** The talk revise the recent paper "Lova: Lattice-Based Folding Scheme from Unstructured Lattices" by Fenzi et al., Asiacrypto 2024, that introduced a folding scheme based on the (unstructred) SIS assumption. The new scheme avoids complex computation such as polynomial ring arithmetic required for the existing lattice-based folding scheme (Boneh, Chen, ePrint 2024/257). It enables a simpler yet efficient instantiation of a lattice-based incrementally verifiable computation (IVC).

---------
