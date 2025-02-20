When I was asked to give this talk, I had to answer a surprisingly difficult question: why do I study ferns?

When you study something for long enough, it is possible to become lost in the details, to be unable to see the forest for the trees (or fronds).

I could give you a stock answer - ferns are important for biodiversity, which is a major part of the global Sustainable Development Goals, etc.

And that's true, but not the real reason that I study ferns.

When I think about it, the real reason that I study ferns is because they are mysterious. Ferns are uniformly green and lack the showy flowers of other plants. Yet, beneath this seemingly simple guise, they harbor a diversity of forms. In my research, I've had the chance to uncover the secrets behind some of the mysteries of ferns, which is incredibly thrilling and keeps me coming back to them.

I first realized this as an undergraduate student at UC Berkeley when I took a field course on tropical biology. For the final project, I had to choose a species and study it in the field. At the recommendation of the professor, I selected filmy ferns, a tropical fern with extremely thin leaves. Spending time with these plants in the wild absolutely hooked me on ferns. I developed what biologists call a "search image", sort of an innate feeling for not only what an organism looks like, but where it is likely to be found. And because filmy ferns are quite small and often overlooked, I was even able to document the first records (in written science anyways) of some species on the island.

I am not the first to be puzzled and subsequently intrigued by ferns.

Before the age of modern botany, ferns were classified along with other organisms that reproduce by spores as "cryptogams". "Crypto" because they lack flowers and it was not obvious how they could reproduce.

It did not take long after the invention of the microscope for botanists to realize that ferns don't need flowers to reproduce, and in fact that many of the organisms lumped together as "cryptogams" are not closely related. But ferns still harbor mysteries that we are only now working out with the help of new technologies.

So tonight, first I want to introduce you to some of the mysteries of ferns, then to explain how I am taking inspiration from a seemingly unconnected field - open source software - to better understand these plants and support science.

So, what are ferns exactly?

When you think of a fern, you probably picture something like this: a small bushy plant growing in the forest understory.

Now that is correct, but it turns out there are also a wide variety of other habitats occupied by ferns.

Ferns grow in deserts, under remarkably harsh circumstances...

some have extremely thin leaves, like the filmy ferns I mentioned earlier...

some ferns can grow as big as trees...

and others are aquatic.

Despite this variation in form, two easily observable characteristics unite all ferns: they reproduce by spores (as mentioned), and they have vascular tissue, in other words, little tubes that transport water along the stem.

However, it turns out another group of land plants also possess these characteristics, the lycophytes. Because of these similarities, ferns and lycophytes have traditionally been lumped together as "pteridophytes", or "ferns and fern allies". But we actually now know from DNA that they are distinct. In fact, true ferns are more closely related to flowering plants than they are to lycophytes. Although it may seem like a technicality, this is a mind-blowing discovery that was only possible because of DNA sequencing. 

Let's come back to the "typical" image of a fern again.

Now, if you were to look very carefully near the base of this fern, you might find another plant that looks entirely different.

Well it turns out, this is a fern too!

And that is because ferns have a unique lifecycle consisting of two distinct halves. The technical term for these are the sporophyte (on the left) and the gametophyte (on the right). The sporophyte is the larger plant that we normally think of as a fern; the gametophyte is much smaller and typically cannot be identified to species based on their appearance. In fact, botanists say these gametophytes are "cryptic" - there's that crypto again - because they all kind of look the same, even though they belong to different species.

In fact, for a very long time fern gametophytes were largely overlooked by botanists because they are so small and hard to find in the first place, and once you find one, you don't even know what species it is. But recently, that is starting to change, thanks to DNA sequencing. Now I can sequence the DNA of gametophytes that I collect in the field, and use that DNA to identify it to species in a practice sometimes called "DNA barcoding".

And this is where open-source comes in. You might think "what the heck could fern gametophytes have to do with open-source"? The reason is that even if I sequence the DNA of a mysterious fern gametophyte, I can't tell you what species it is without a DNA match -- that is, I have to have a reference database to search against. Fortunately though, there is a global database of DNA sequences that every researcher contributes to when they publish their studies, called GenBank. Since GenBank is an open database, I can query the DNA of my mystery gametophyte against it and find a match on GenBank, if not to the exact species, typically at least to genus. Imagine if GenBank were proprietary and I lacked access to it. Even if I had a lab capable of sequencing the mystery gametophyte myself, I still could not find a match for it! In other words, having open data is absolutely key to making scientific progress in the age of data science.

Open-source software has fostered amazing technological progress: for example, the open-source operating system "linux" literally forms the backbone of most computing systems today including databases, email servers, and even probes sent into space. In the same way, open data enables scientific progress that otherwise would absolutely not be possible. For the remainder of my talk, I'd like to give two examples from ferns.

One of my major research goals is to understand the evolutionary relationships of all fern species using DNA. As we saw earlier with ferns and lycophytes, there are some hidden aspects of evolution that we can only uncover with DNA. This project is called "FTOL", for the "Fern Tree of Life". Here, "tree" refers to phylogenetic tree, the branching diagram that shows how species are related to each other.

Now it would be nearly impossible for me to go out and sample DNA of all living fern species to build the tree, but fortunately, I don't have to, thanks to GenBank, the DNA database that I mentioned earlier. In addition to using GenBank as a reference database for conducting DNA queries, I can also analyze the data within it to understand how species are related to each other.

However, having access to a massive database is a double-edged sword. When I started this project, I realized that the data in GenBank are constantly growing, and therefore that any tree I could make would be outdated within days. So I wrote code to automate the entire process (well, almost the entire process) so that it could be repeated on a regular basis to update the tree. This code is publicly available on the web so that anybody can run it.

The result is not only the biggest fern phylogeny to date, but one that has kept up as new data accumulate. And most importantly, this has fueled other new research. For example, this is a recent paper that used FTOL to understand fern symbiosis with ants. That's right - fern symbiosis with ants. If you thought only flowers produce nectar, you would be wrong. It turns out that some ferns also produce nector without having flowers, and that they do this to attract ants who then protect the plant. These researchers were able to use FTOL to determine that this ant-fern relationship arose around the same time that many ferns started living on trees as epiphytes, and in fact that they may have co-opted the ants from the trees. So I think this is super cool and am very excited to see FTOL used in this way.

Another area that has been transformed by taking an open approach is taxonomy, or the science of naming organisms. The taxonomic system we use today started with Linnaeaus in the 1700s and has remained remarkably unchanged since. For example, the scientific name for our species is Homo sapiens; Homo is the genus and sapiens is the species. This is the hierarchical system set up by Linnaeaus that we still use today. And for a long time, the way that these names were determined was sort of the opposite of an open approach - it was usually done by one or a few experts, who published their best stab at taxonomy of a particular group based on all the information available to them at the time.

However, in the age of big data and open science, some of us in the fern world are trying to take a different approach. We call this the Pteridophyte Phylogeny Group (remember, pteridophytes include ferns and lycophytes), or PPG. And unlike traditional taxonomic systems, we have an open-source, community driven-model.

The PPG community includes nearly 200 researchers from over 60 countries. Membership is completely open - anybody with an interest in ferns and lycophytes is welcome to join.

One aspect of PPG that is strikingly different from any other taxonomic system that we know of is that we use a public forum to carry out our discussions. We use GitHub, which is actually a website that is mainly used by software developers. But the collaboration tools of GitHub also make it perfect for this kind of project.

On our GitHub discussion form (AKA, the issue tracker, which is normally used by software developers for tracking bugs), we evaluate the merits of the latest research and determine the implications for the names we give to ferns. Since it is open, there is a complete record and justification for all our decisions. The actual taxonomic decisions are made by voting using Google Forms, and then I post the results back on GitHub.

So far, we have evaluated nearly 80 new names that have been published recently. Furthermore, the taxonomic system is available through a web portal called World Flora. This portal provides taxonomic data for all plants on the planet, not just ferns. And researchers studying other groups of plants are also forming their own networks like PPG to bring in expertise from as wide a range as possible.

So I hope you can see how integrating some of the tools and ethos of open-source software into botany has allowed us to make new discoveries and accelerate science.

However, although I think the benefits of open science are clear, there are still many barriers to making it more widespread. It requires technical knowledge and takes time. And this while the primary incentive driving research continues to be publishing more papers. Every time I update FTOL I am contributing to science, but am I not publishing a new paper. So there needs to be a change in the incentive structure of how we do science. If that can happen I am sure that we will continue to make more discoveries about ferns and other mysterious organisms.
