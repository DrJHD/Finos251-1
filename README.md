# ISDA percentages

The [Official PDF](https://www.isda.org/a/EqxgE/Eligible-Collateral-Comparison-010523.pdf) are frequently expressed as multiple percentages.
These depend on the breakpoints, which will vary by security but are product dependent. Examples are
given in section 5 of [the asset definition PDF](https://www.rbccm.com/assets/rbccm/docs/legal/doddfrank/Documents/ISDALibrary/ISDA%20Collateral%20Asset%20Definitions%20-%20June%202003.pdf).
The liquidity breakpoints are specified in the row
descriptions. Breakpoints based on asset quality are
described in the notes and shown on the face of the PDF by 
multiple values separated by slashes.

A typical example of a cell with three percentages might be 2%/3%/15%, meaning that a haircut of 2% would be imposed on securities
in credit quality step 1, 3% on securities in credit 
quality steps 2 & 3 and 15% on step 4. It is again common for the lowest quality securities to be restricted to certain issuers only. Different
definitions of quality are given in the notes for
each country of issue.

Exceptions are:
* the US, where the difference is not explained in the notes.

The files representing the 2% and 4% haircuts on sovereign central bank securities differ only in the percentage applied.

It is possible to interpret the notes as meaning that the 2% rate is applicable to US government sponsored enterprises and the 4% rate to other issuers, but the JSON file for the 4% class has an issuerType of "SOVEREIGN_CENTRAL_BANK", which seems to contradict this.

The relevant note reads:

> USPR, CFTC, and SEC: The USPR, CFTC, and SEC rules (which are assumed to follow the CFTC rules for purposes of this comparison) do not define “sovereign debt”. Sovereign debt for purposes of this section of the chart includes: Securities issued or
guaranteed by the ECB or a sovereign entity with a risk weight of 20% or less under applicable regulatory capital rules, certain multilateral development banks and international organizations, and publicly traded debt securities issued by, or asset-backed
securities fully guaranteed as to the payment of principal and interest by, a U.S. Government-sponsored enterprise that is operating with capital support or another form of direct financial assistance received from the U.S. government / publicly traded debt
securities that are investment grade under US capital rules and are neither asset-backed securities, nor issued by the pledgor or an affiliate or a financial institution.

The part after the slash reads as though it would include debentures issued by Microsoft, although this would obviously not be regarded as sovereign debt. A possible interpretation is that this grade is the publicly traded debt of local government bodies. This would seem to match the note in the PDF but not the issuerType of the JSON. The wording appears identical to that in note 3, which does appear to include debentures issued by Microsoft.

The JSON files are included in [this zip](https://github.com/finos/community/files/11352127/EligibleCollateralCriteria_1_28-04-2023.zip), a URL copied from [github](https://github.com/finos/community/discussions/251).

* Japan, where the categories are in JFSA Public Notice No. 19 of 2006. No English language version of this seems to be publicly available on the WWW.