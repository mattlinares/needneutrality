# Need Neutrality

Citizens demand net neutrality – all the while, ISPs and US regulators want to junk it. This is a proposal for a system to slow down websites that undermine net neutrality by benefitting from top-tier download speeds.

A browser extension to defend Net Neutrality – currently this proposal needs developers and other contributors. Please fork, pull request, start your own repo or get in touch <matthew.linares@opendemocracy.net> if you want to further this idea. I have so far added a browser boilerplate from https://extensionizr.com.


The browser extension has two objectives, the first being the priority:

1) It slows down the load speed of sites who are thought to be paying for preferential data delivery to users, that is sites who undermine net neutrality by paying for its opposite. It does this by reading URLs from a public database of such sites, and injecting delays into the page at load time. In this way, users of the extension penalise those sites and reduce the benefits to them of undermining net neutrality.

2) It measures download times from certain sites, comparing them with others, in order to detect suspected preferential service. Those measurements would be compared on a central server and added to the public database. This assumes that websites will use preferential service from ISPs without notifying the public. If some other public mechanism emerges which allows us to know which sites are paying for preferential speeds, that data would be the best source to populate the database that this extension relies on.



## 1 Proposed site slowdown function


- Browser downloads list of urls known to be benefitting from tiering. If list is very long, a subset of the list may be used – this can be decided by the client, or by the database server which may seek to distribute the effects of the slowdown.

- When visiting one of the blacklisted urls, the extension places a delay function into the loading schedule of the webpage. It may, optionally, show a message or logo to let the user know that this is a target site.



## 2 Proposed site speed measurement


- This function would crowd-source information on which sites load faster and which slower, in a bid to work out which are paying for preferred access. Using some appropriate method the browser measures the download speed of certain elements on a given site, and comparable elements on other sites, which it sends back to the database in order to benchmark site speeds. This can be used as the basis for queries to ISPs and the sites themselves about preferential service, as a precursor to blacklisting those sites.

This will probably require complex network theory and may be difficult to accurately implement. It may not be necessary if the url blacklist is updated by other means e.g. consumer requests to ISPs and websites suspected of using preferential access.

