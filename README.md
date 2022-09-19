In this project, a simple search engine for the website <https://www.lawfareblog.com> was created. This website provides legal analysis on US national security issues.


## Submission

1. Create a new repo on github (not a fork of this repo).

1. Run the following commands, and paste their output into the code blocks below.
   
   Task 1, part 1:
   ```
   $ python3 pagerank.py --data=data/small.csv.gz --verbose

    DEBUG:root:computing indices
    DEBUG:root:computing values
    DEBUG:root:i=0 residual=0.18309083580970764
    DEBUG:root:i=1 residual=0.061353832483291626
    DEBUG:root:i=2 residual=0.0316704586148262
    DEBUG:root:i=3 residual=0.01220186147838831
    DEBUG:root:i=4 residual=0.00656816316768527
    DEBUG:root:i=5 residual=0.0028830398805439472
    DEBUG:root:i=6 residual=0.001488335314206779
    DEBUG:root:i=7 residual=0.0007016189629212022
    DEBUG:root:i=8 residual=0.0003513787523843348
    DEBUG:root:i=9 residual=0.00017015726189129055
    DEBUG:root:i=10 residual=8.412973693339154e-05
    DEBUG:root:i=11 residual=4.114600960747339e-05
    DEBUG:root:i=12 residual=2.0203402527840808e-05
    DEBUG:root:i=13 residual=9.919876902131364e-06
    DEBUG:root:i=14 residual=4.837349479203112e-06
    DEBUG:root:i=15 residual=2.416194774923497e-06
    DEBUG:root:i=16 residual=1.1706662235155818e-06
    DEBUG:root:i=17 residual=5.701519967260538e-07
    INFO:root:rank=0 pagerank=5.7749e-01 url=4
    INFO:root:rank=1 pagerank=4.7771e-01 url=6
    INFO:root:rank=2 pagerank=4.1762e-01 url=5
    INFO:root:rank=3 pagerank=3.3517e-01 url=2
    INFO:root:rank=4 pagerank=2.8501e-01 url=3
    INFO:root:rank=5 pagerank=2.6517e-01 url=1
   ```

   Task 1, part 2:
   ```
   $ python3 pagerank.py --data=data/lawfareblog.csv.gz --search_query='corona'

    INFO:root:rank=0 pagerank=1.0038e-03 url=www.lawfareblog.com/lawfare-podcast-united-nations-and-coronavirus-crisis
    INFO:root:rank=1 pagerank=8.9224e-04 url=www.lawfareblog.com/house-oversight-committee-holds-day-two-hearing-government-coronavirus-response
    INFO:root:rank=2 pagerank=7.0390e-04 url=www.lawfareblog.com/britains-coronavirus-response
    INFO:root:rank=3 pagerank=6.9153e-04 url=www.lawfareblog.com/prosecuting-purposeful-coronavirus-exposure-terrorism
    INFO:root:rank=4 pagerank=6.7041e-04 url=www.lawfareblog.com/israeli-emergency-regulations-location-tracking-coronavirus-carriers
    INFO:root:rank=5 pagerank=6.6256e-04 url=www.lawfareblog.com/why-congress-conducting-business-usual-face-coronavirus
    INFO:root:rank=6 pagerank=6.5046e-04 url=www.lawfareblog.com/congressional-homeland-security-committees-seek-ways-support-state-federal-responses-coronavirus
    INFO:root:rank=7 pagerank=6.3620e-04 url=www.lawfareblog.com/paper-hearing-experts-debate-digital-contact-tracing-and-coronavirus-privacy-concerns
    INFO:root:rank=8 pagerank=6.1248e-04 url=www.lawfareblog.com/house-subcommittee-voices-concerns-over-us-management-coronavirus
    INFO:root:rank=9 pagerank=6.0187e-04 url=www.lawfareblog.com/livestream-house-oversight-committee-holds-hearing-government-coronavirus-response

   $ python3 pagerank.py --data=data/lawfareblog.csv.gz --search_query='trump'

    INFO:root:rank=0 pagerank=5.7826e-03 url=www.lawfareblog.com/trump-asks-supreme-court-stay-congressional-subpeona-tax-returns
    INFO:root:rank=1 pagerank=5.2338e-03 url=www.lawfareblog.com/document-trump-revokes-obama-executive-order-counterterrorism-strike-casualty-reporting
    INFO:root:rank=2 pagerank=5.1297e-03 url=www.lawfareblog.com/trump-administrations-worrying-new-policy-israeli-settlements
    INFO:root:rank=3 pagerank=4.6599e-03 url=www.lawfareblog.com/dc-circuit-overrules-district-courts-due-process-ruling-qasim-v-trump
    INFO:root:rank=4 pagerank=4.5934e-03 url=www.lawfareblog.com/donald-trump-and-politically-weaponized-executive-branch
    INFO:root:rank=5 pagerank=4.3071e-03 url=www.lawfareblog.com/how-trumps-approach-middle-east-ignores-past-future-and-human-condition
    INFO:root:rank=6 pagerank=4.0935e-03 url=www.lawfareblog.com/why-trump-cant-buy-greenland
    INFO:root:rank=7 pagerank=3.7591e-03 url=www.lawfareblog.com/oral-argument-summary-qassim-v-trump
    INFO:root:rank=8 pagerank=3.4509e-03 url=www.lawfareblog.com/dc-circuit-court-denies-trump-rehearing-mazars-case
    INFO:root:rank=9 pagerank=3.4484e-03 url=www.lawfareblog.com/second-circuit-rules-mazars-must-hand-over-trump-tax-returns-new-york-prosecutors

   $ python3 pagerank.py --data=data/lawfareblog.csv.gz --search_query='iran'

    INFO:root:rank=0 pagerank=4.5746e-03 url=www.lawfareblog.com/praise-presidents-iran-tweets
    INFO:root:rank=1 pagerank=4.4174e-03 url=www.lawfareblog.com/how-us-iran-tensions-could-disrupt-iraqs-fragile-peace
    INFO:root:rank=2 pagerank=2.6928e-03 url=www.lawfareblog.com/cyber-command-operational-update-clarifying-june-2019-iran-operation
    INFO:root:rank=3 pagerank=1.9391e-03 url=www.lawfareblog.com/aborted-iran-strike-fine-line-between-necessity-and-revenge
    INFO:root:rank=4 pagerank=1.5452e-03 url=www.lawfareblog.com/parsing-state-departments-letter-use-force-against-iran
    INFO:root:rank=5 pagerank=1.5357e-03 url=www.lawfareblog.com/iranian-hostage-crisis-and-its-effect-american-politics
    INFO:root:rank=6 pagerank=1.5258e-03 url=www.lawfareblog.com/announcing-united-states-and-use-force-against-iran-new-lawfare-e-book
    INFO:root:rank=7 pagerank=1.4221e-03 url=www.lawfareblog.com/us-names-iranian-revolutionary-guard-terrorist-organization-and-sanctions-international-criminal
    INFO:root:rank=8 pagerank=1.1788e-03 url=www.lawfareblog.com/iran-shoots-down-us-drone-domestic-and-international-legal-implications
    INFO:root:rank=9 pagerank=1.1463e-03 url=www.lawfareblog.com/israel-iran-syria-clash-and-law-use-force
   ```

   Task 1, part 3:
   ```
   $ python3 pagerank.py --data=data/lawfareblog.csv.gz

    INFO:root:rank=0 pagerank=2.8741e-01 url=www.lawfareblog.com/lawfare-job-board
    INFO:root:rank=1 pagerank=2.8741e-01 url=www.lawfareblog.com/masthead
    INFO:root:rank=2 pagerank=2.8741e-01 url=www.lawfareblog.com/litigation-documents-related-appointment-matthew-whitaker-acting-attorney-general
    INFO:root:rank=3 pagerank=2.8741e-01 url=www.lawfareblog.com/documents-related-mueller-investigation
    INFO:root:rank=4 pagerank=2.8741e-01 url=www.lawfareblog.com/topics
    INFO:root:rank=5 pagerank=2.8741e-01 url=www.lawfareblog.com/about-lawfare-brief-history-term-and-site
    INFO:root:rank=6 pagerank=2.8741e-01 url=www.lawfareblog.com/snowden-revelations
    INFO:root:rank=7 pagerank=2.8741e-01 url=www.lawfareblog.com/support-lawfare
    INFO:root:rank=8 pagerank=2.8741e-01 url=www.lawfareblog.com/upcoming-events
    INFO:root:rank=9 pagerank=2.8741e-01 url=www.lawfareblog.com/our-comments-policy

   $ python3 pagerank.py --data=data/lawfareblog.csv.gz --filter_ratio=0.2

    INFO:root:rank=0 pagerank=1.4021e-01 url=www.lawfareblog.com/todays-headlines-and-commentary-1963
    INFO:root:rank=1 pagerank=1.4021e-01 url=www.lawfareblog.com/todays-headlines-and-commentary-1964
    INFO:root:rank=2 pagerank=1.3865e-01 url=www.lawfareblog.com/todays-headlines-and-commentary-1962
    INFO:root:rank=3 pagerank=9.0550e-02 url=www.lawfareblog.com/todays-headlines-and-commentary-1965
    INFO:root:rank=4 pagerank=8.1725e-02 url=www.lawfareblog.com/cyberlaw-podcast-sandworm-and-grus-global-intifada
    INFO:root:rank=5 pagerank=8.1693e-02 url=www.lawfareblog.com/cyberlaw-podcast-plumbing-depths-artificial-stupidity
    INFO:root:rank=6 pagerank=7.9479e-02 url=www.lawfareblog.com/todays-headlines-and-commentary-1966
    INFO:root:rank=7 pagerank=7.8553e-02 url=www.lawfareblog.com/lawfare-podcast-ben-nimmo-whack-mole-game-disinformation
    INFO:root:rank=8 pagerank=7.8513e-02 url=www.lawfareblog.com/lawfare-podcast-week-was-impeachment
    INFO:root:rank=9 pagerank=7.3923e-02 url=www.lawfareblog.com/cyberlaw-podcast-mistrusting-google
   ```

   Task 1, part 4:
   ```
   $ python3 pagerank.py --data=data/lawfareblog.csv.gz --verbose 
   
    DEBUG:root:computing indices
    DEBUG:root:computing values
    DEBUG:root:i=0 residual=1.3793821334838867
    DEBUG:root:i=1 residual=0.11642514914274216
    DEBUG:root:i=2 residual=0.07495073974132538
    DEBUG:root:i=3 residual=0.031712669879198074
    DEBUG:root:i=4 residual=0.01746140420436859
    DEBUG:root:i=5 residual=0.008529536426067352
    DEBUG:root:i=6 residual=0.0044392067939043045
    DEBUG:root:i=7 residual=0.002238823566585779
    DEBUG:root:i=8 residual=0.0011464565759524703
    DEBUG:root:i=9 residual=0.0005798051133751869
    DEBUG:root:i=10 residual=0.00029213540256023407
    DEBUG:root:i=11 residual=0.00014553092478308827
    DEBUG:root:i=12 residual=7.149828888941556e-05
    DEBUG:root:i=13 residual=3.433692472754046e-05
    DEBUG:root:i=14 residual=1.5638515833416022e-05
    DEBUG:root:i=15 residual=6.266389391385019e-06
    DEBUG:root:i=16 residual=2.8251236017240444e-06
    DEBUG:root:i=17 residual=1.3609912912215805e-06
    DEBUG:root:i=18 residual=4.311152963509812e-07
    INFO:root:rank=0 pagerank=2.8741e-01 url=www.lawfareblog.com/lawfare-job-board
    INFO:root:rank=1 pagerank=2.8741e-01 url=www.lawfareblog.com/masthead
    INFO:root:rank=2 pagerank=2.8741e-01 url=www.lawfareblog.com/litigation-documents-related-appointment-matthew-whitaker-acting-attorney-general
    INFO:root:rank=3 pagerank=2.8741e-01 url=www.lawfareblog.com/documents-related-mueller-investigation
    INFO:root:rank=4 pagerank=2.8741e-01 url=www.lawfareblog.com/topics
    INFO:root:rank=5 pagerank=2.8741e-01 url=www.lawfareblog.com/about-lawfare-brief-history-term-and-site
    INFO:root:rank=6 pagerank=2.8741e-01 url=www.lawfareblog.com/snowden-revelations
    INFO:root:rank=7 pagerank=2.8741e-01 url=www.lawfareblog.com/support-lawfare
    INFO:root:rank=8 pagerank=2.8741e-01 url=www.lawfareblog.com/upcoming-events
    INFO:root:rank=9 pagerank=2.8741e-01 url=www.lawfareblog.com/our-comments-policy

   $ python3 pagerank.py --data=data/lawfareblog.csv.gz --verbose --alpha=0.99999
   
    DEBUG:root:computing indices
    DEBUG:root:computing values
    DEBUG:root:i=0 residual=1.3845856189727783
    DEBUG:root:i=1 residual=0.07088156789541245
    DEBUG:root:i=2 residual=0.01882227510213852
    DEBUG:root:i=3 residual=0.006958262529224157
    DEBUG:root:i=4 residual=0.0027358194347471
    DEBUG:root:i=5 residual=0.0010345563059672713
    DEBUG:root:i=6 residual=0.0003774634387809783
    DEBUG:root:i=7 residual=0.00013533401943277568
    DEBUG:root:i=8 residual=4.8224112106254324e-05
    DEBUG:root:i=9 residual=1.7172435036627576e-05
    DEBUG:root:i=10 residual=6.118058081483468e-06
    DEBUG:root:i=11 residual=2.173422217310872e-06
    DEBUG:root:i=12 residual=7.82504116614291e-07
    INFO:root:rank=0 pagerank=2.8859e-01 url=www.lawfareblog.com/lawfare-job-board
    INFO:root:rank=1 pagerank=2.8859e-01 url=www.lawfareblog.com/masthead
    INFO:root:rank=2 pagerank=2.8859e-01 url=www.lawfareblog.com/litigation-documents-related-appointment-matthew-whitaker-acting-attorney-general
    INFO:root:rank=3 pagerank=2.8859e-01 url=www.lawfareblog.com/documents-related-mueller-investigation
    INFO:root:rank=4 pagerank=2.8859e-01 url=www.lawfareblog.com/topics
    INFO:root:rank=5 pagerank=2.8859e-01 url=www.lawfareblog.com/about-lawfare-brief-history-term-and-site
    INFO:root:rank=6 pagerank=2.8859e-01 url=www.lawfareblog.com/snowden-revelations
    INFO:root:rank=7 pagerank=2.8859e-01 url=www.lawfareblog.com/support-lawfare
    INFO:root:rank=8 pagerank=2.8859e-01 url=www.lawfareblog.com/upcoming-events
    INFO:root:rank=9 pagerank=2.8859e-01 url=www.lawfareblog.com/our-comments-policy

   $ python3 pagerank.py --data=data/lawfareblog.csv.gz --verbose --filter_ratio=0.2
   
    DEBUG:root:computing indices
    DEBUG:root:computing values
    DEBUG:root:i=0 residual=0.45511355996131897
    DEBUG:root:i=1 residual=0.039158087223768234
    DEBUG:root:i=2 residual=0.004644036293029785
    DEBUG:root:i=3 residual=0.000507233664393425
    DEBUG:root:i=4 residual=5.066792436991818e-05
    DEBUG:root:i=5 residual=6.13915290159639e-06
    DEBUG:root:i=6 residual=3.7313798202376347e-06
    DEBUG:root:i=7 residual=2.424092429009761e-07
    INFO:root:rank=0 pagerank=1.4021e-01 url=www.lawfareblog.com/todays-headlines-and-commentary-1963
    INFO:root:rank=1 pagerank=1.4021e-01 url=www.lawfareblog.com/todays-headlines-and-commentary-1964
    INFO:root:rank=2 pagerank=1.3865e-01 url=www.lawfareblog.com/todays-headlines-and-commentary-1962
    INFO:root:rank=3 pagerank=9.0550e-02 url=www.lawfareblog.com/todays-headlines-and-commentary-1965
    INFO:root:rank=4 pagerank=8.1725e-02 url=www.lawfareblog.com/cyberlaw-podcast-sandworm-and-grus-global-intifada
    INFO:root:rank=5 pagerank=8.1693e-02 url=www.lawfareblog.com/cyberlaw-podcast-plumbing-depths-artificial-stupidity
    INFO:root:rank=6 pagerank=7.9479e-02 url=www.lawfareblog.com/todays-headlines-and-commentary-1966
    INFO:root:rank=7 pagerank=7.8553e-02 url=www.lawfareblog.com/lawfare-podcast-ben-nimmo-whack-mole-game-disinformation
    INFO:root:rank=8 pagerank=7.8513e-02 url=www.lawfareblog.com/lawfare-podcast-week-was-impeachment
    INFO:root:rank=9 pagerank=7.3923e-02 url=www.lawfareblog.com/cyberlaw-podcast-mistrusting-google
   
   $ python3 pagerank.py --data=data/lawfareblog.csv.gz --verbose --filter_ratio=0.2 --alpha=0.99999
   
    DEBUG:root:computing indices
    DEBUG:root:computing values
    DEBUG:root:i=0 residual=0.4608026146888733
    DEBUG:root:i=1 residual=0.04114634543657303
    DEBUG:root:i=2 residual=0.00508133927360177
    DEBUG:root:i=3 residual=0.0005808579735457897
    DEBUG:root:i=4 residual=6.311153993010521e-05
    DEBUG:root:i=5 residual=8.358894774573855e-06
    DEBUG:root:i=6 residual=1.6888421896510408e-06
    DEBUG:root:i=7 residual=4.377486106932338e-07
    INFO:root:rank=0 pagerank=1.4210e-01 url=www.lawfareblog.com/todays-headlines-and-commentary-1964
    INFO:root:rank=1 pagerank=1.4210e-01 url=www.lawfareblog.com/todays-headlines-and-commentary-1963
    INFO:root:rank=2 pagerank=1.4051e-01 url=www.lawfareblog.com/todays-headlines-and-commentary-1962
    INFO:root:rank=3 pagerank=9.1691e-02 url=www.lawfareblog.com/todays-headlines-and-commentary-1965
    INFO:root:rank=4 pagerank=8.2831e-02 url=www.lawfareblog.com/cyberlaw-podcast-sandworm-and-grus-global-intifada
    INFO:root:rank=5 pagerank=8.2799e-02 url=www.lawfareblog.com/cyberlaw-podcast-plumbing-depths-artificial-stupidity
    INFO:root:rank=6 pagerank=8.0453e-02 url=www.lawfareblog.com/todays-headlines-and-commentary-1966
    INFO:root:rank=7 pagerank=7.9680e-02 url=www.lawfareblog.com/lawfare-podcast-ben-nimmo-whack-mole-game-disinformation
    INFO:root:rank=8 pagerank=7.9638e-02 url=www.lawfareblog.com/lawfare-podcast-week-was-impeachment
    INFO:root:rank=9 pagerank=7.4978e-02 url=www.lawfareblog.com/cyberlaw-podcast-mistrusting-google
       
   ```

   Task 2, part 1:
   ```
   $ python3 pagerank.py --data=data/lawfareblog.csv.gz --filter_ratio=0.2 --personalization_vector_query='corona'
   
    INFO:root:rank=0 pagerank=1.4197e-01 url=www.lawfareblog.com/todays-headlines-and-commentary-1963
    INFO:root:rank=1 pagerank=1.4197e-01 url=www.lawfareblog.com/todays-headlines-and-commentary-1964
    INFO:root:rank=2 pagerank=1.4038e-01 url=www.lawfareblog.com/todays-headlines-and-commentary-1962
    INFO:root:rank=3 pagerank=9.1607e-02 url=www.lawfareblog.com/todays-headlines-and-commentary-1965
    INFO:root:rank=4 pagerank=8.2756e-02 url=www.lawfareblog.com/cyberlaw-podcast-sandworm-and-grus-global-intifada
    INFO:root:rank=5 pagerank=8.2723e-02 url=www.lawfareblog.com/cyberlaw-podcast-plumbing-depths-artificial-stupidity
    INFO:root:rank=6 pagerank=8.0380e-02 url=www.lawfareblog.com/todays-headlines-and-commentary-1966
    INFO:root:rank=7 pagerank=7.9608e-02 url=www.lawfareblog.com/lawfare-podcast-ben-nimmo-whack-mole-game-disinformation
    INFO:root:rank=8 pagerank=7.9565e-02 url=www.lawfareblog.com/lawfare-podcast-week-was-impeachment
    INFO:root:rank=9 pagerank=7.4910e-02 url=www.lawfareblog.com/cyberlaw-podcast-mistrusting-google
   
   ```

   Task 2, part 2:
   ```
   $ python3 pagerank.py --data=data/lawfareblog.csv.gz --filter_ratio=0.2 --personalization_vector_query='corona' --search_query='-corona'
   
    INFO:root:rank=0 pagerank=1.4197e-01 url=www.lawfareblog.com/todays-headlines-and-commentary-1963
    INFO:root:rank=1 pagerank=1.4197e-01 url=www.lawfareblog.com/todays-headlines-and-commentary-1964
    INFO:root:rank=2 pagerank=1.4038e-01 url=www.lawfareblog.com/todays-headlines-and-commentary-1962
    INFO:root:rank=3 pagerank=9.1607e-02 url=www.lawfareblog.com/todays-headlines-and-commentary-1965
    INFO:root:rank=4 pagerank=8.2756e-02 url=www.lawfareblog.com/cyberlaw-podcast-sandworm-and-grus-global-intifada
    INFO:root:rank=5 pagerank=8.2723e-02 url=www.lawfareblog.com/cyberlaw-podcast-plumbing-depths-artificial-stupidity
    INFO:root:rank=6 pagerank=8.0380e-02 url=www.lawfareblog.com/todays-headlines-and-commentary-1966
    INFO:root:rank=7 pagerank=7.9608e-02 url=www.lawfareblog.com/lawfare-podcast-ben-nimmo-whack-mole-game-disinformation
    INFO:root:rank=8 pagerank=7.9565e-02 url=www.lawfareblog.com/lawfare-podcast-week-was-impeachment
    INFO:root:rank=9 pagerank=7.4910e-02 url=www.lawfareblog.com/cyberlaw-podcast-mistrusting-google

   ```

1. Ensure that all your changes to the `pagerank.py` and `README.md` files are committed to your repo and pushed to github.

1. Get at least 5 stars on your repo.
   (You made trade stars with other students in the class.)

   > **NOTE:**
   > 
   > Recruiters use github profiles to determine who to hire,
   > and pagerank is used to rank user profiles and projects.
   > Links in this graph correspond to who has starred/followed who's repo.
   > By getting more stars on your repo, you'll be increasing your github pagerank, which increases the likelihood that recruiters will hire you.
   > To see an example, [perform a search for `data mining`](https://github.com/search?q=data+mining).
   > Notice that the results are returned "approximately" ranked by the number of stars,
   > but because "some stars count more than others" the results are not exactly ranked by the number of stars.
   > (I asked you not to fork this repo because forks are ranked lower than non-forks.)
   >
   > In some sense, we are doing a "dual problem" to data mining by getting these stars.
   > Recruiters are using data mining to find out who the best people to recruit are,
   > and we are hacking their data mining algorithms by making those algorithms select you instead of someone else.
   >
   > If you're interested in exploring this idea further, here's a python tutorial for extracting GitHub's social graph: <https://www.oreilly.com/library/view/mining-the-social/9781449368180/ch07.html> ; if you're interested in learning more about how recruiters use github profiles, read this Hacker News post: <https://news.ycombinator.com/item?id=19413348>.

1. Submit the url of your repo to sakai.

   Each part is worth 2 points, for 12 points overall.
