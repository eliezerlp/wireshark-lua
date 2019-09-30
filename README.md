# Omi Lua Wireshark Dissectors

<p align = "left">
<a href="https://travis-ci.org/Open-Markets-Initiative/wireshark-lua"><img src = "https://img.shields.io/travis/Open-Markets-Initiative/wireshark-lua.svg?style=flat-square" /></a>
</p>

Lua wireshark dissector scripts provide an easily customized cross platform dissection solution for viewing common binary exchange protocols.

For more information on lua dissectors: [How Lua fits into Wireshark](https://wiki.wireshark.org/Lua "Wireshark Lua Documentation")

## Usage

To dissect packets, place lua script(s) in the wireshark plugins directory.

The standard path on a windows install:

```
C:\Program Files\Wireshark\plugins\[version]\
```
The standard path on a linux install:

```
//usr/share/wireshark/plugins
```
For configuration information: [Wireshark Plugin Configuration](https://www.wireshark.org/docs/wsug_html_chunked/ChPluginFolders.html "Wireshark Configuration Documentation")

Note: Some packets contain enough information to programmatically determine the correct protocol specification and/or version at runtime.  *Many do not.*  If you add multiple dissectors to your plugins folder, wireshark will dissect each "conversation" based on the first matching protocol.  In these cases, please manually select protocol dissector using Analyze | Decode As….

For decoding information: [Wireshark Protocol Decoding](https://www.wireshark.org/docs/wsug_html_chunked/ChCustProtocolDissectionSection.html "Wireshark Protocol Selection Documentation")
## Protocols

|Organization | Division | Data | Protocol | Version | Date | Size | Testing|
|--- | --- | --- | --- | --- | --- | --- | ---|
|[Asx][Asx.Securities.T24.Itch.v1.13.Organization] | Securities | T24 | Itch | [1.13][Asx.Securities.T24.Itch.v1.13.Dissector] | 7/15/2014 | 5081 | Untested|
|[Cboe][Cboe.Futures.DepthOfBook.Pitch.v1.1.6.Organization] | Futures | DepthOfBook | Pitch | [1.1.6][Cboe.Futures.DepthOfBook.Pitch.v1.1.6.Dissector] | 4/8/2019 | 2995 | Verified|
|[Cboe][Cboe.Options.MarketDataFeed.Csm.v1.4.2.Organization] | Options | MarketDataFeed | Csm | [1.4.2][Cboe.Options.MarketDataFeed.Csm.v1.4.2.Dissector] | 5/8/2018 | 3819 | Verified|
|[Cboe][Cboe.Options.MarketLevel2.Csm.v1.0.4.Organization] | Options | MarketLevel2 | Csm | [1.0.4][Cboe.Options.MarketLevel2.Csm.v1.0.4.Dissector] | 5/8/2018 | 2704 | Verified|
|[Cboe][Cboe.Options.OpeningAuction.Csm.v1.0.Organization] | Options | OpeningAuction | Csm | [1.0][Cboe.Options.OpeningAuction.Csm.v1.0.Dissector] | 7/18/2018 | 2794 | Verified|
|[Cboe][Cboe.Options.DepthOfBook.Pitch.v2.39.4.Organization] | Options | DepthOfBook | Pitch | [2.39.4][Cboe.Options.DepthOfBook.Pitch.v2.39.4.Dissector] | 8/21/2018 | 2790 | Verified|
|[Cboe][Cboe.Options.C1.AuctionFeed.Pitch.v1.1.1.Organization] | Options C1 | AuctionFeed | Pitch | [1.1.1][Cboe.Options.C1.AuctionFeed.Pitch.v1.1.1.Dissector] | 12/6/2018 | 1628 | Verified|
|[Cboe][Cboe.Options.Edgx.AuctionFeed.Pitch.v1.1.1.Organization] | Options Edgx | AuctionFeed | Pitch | [1.1.1][Cboe.Options.Edgx.AuctionFeed.Pitch.v1.1.1.Dissector] | 12/6/2018 | 1149 | Verified|
|[Cme][Cme.Mdp3.Sbe.v9.1.Organization] |  | Mdp3 | Sbe | [9.1][Cme.Mdp3.Sbe.v9.1.Dissector] | 3/8/2018 | 8227 | Verified|
|[Cme][Cme.Mdp3.Sbe.v8.1.Organization] |  | Mdp3 | Sbe | [8.1][Cme.Mdp3.Sbe.v8.1.Dissector] | 7/1/2016 | 7237 | Verified|
|[Cme][Cme.Mdp3.Sbe.v6.1.Organization] |  | Mdp3 | Sbe | [6.1][Cme.Mdp3.Sbe.v6.1.Dissector] | 1/9/2016 | 6434 | Verified|
|[Cme][Cme.Mdp3.Sbe.v5.1.Organization] |  | Mdp3 | Sbe | [5.1][Cme.Mdp3.Sbe.v5.1.Dissector] | 8/6/2014 | 6425 | Verified|
|[Cme][Cme.Mdp3.Sbe.v10.1.Organization] |  | Mdp3 | Sbe | [10.1][Cme.Mdp3.Sbe.v10.1.Dissector] | 7/26/2019 | 8676 | Untested|
|[Cme][Cme.Streamline.Sbe.v9.5.Organization] |  | Streamline | Sbe | [9.5][Cme.Streamline.Sbe.v9.5.Dissector] | 4/4/2018 | 5907 | Untested|
|[Cme][Cme.Streamline.Sbe.v8.5.Organization] |  | Streamline | Sbe | [8.5][Cme.Streamline.Sbe.v8.5.Dissector] | 6/2/2017 | 5769 | Untested|
|[Cme][Cme.Futures.iLink3.Sbe.v8.0.Organization] | Futures | iLink3 | Sbe | [8.0][Cme.Futures.iLink3.Sbe.v8.0.Dissector] | 7/24/2019 | 10634 | Untested|
|[Eurex][Eurex.Derivatives.Eobi.T7.v8.0.Organization] | Derivatives | Eobi | T7 | [8.0][Eurex.Derivatives.Eobi.T7.v8.0.Dissector] | 9/23/2019 | 4368 | Untested|
|[Eurex][Eurex.Derivatives.Eobi.T7.v7.1.Organization] | Derivatives | Eobi | T7 | [7.1][Eurex.Derivatives.Eobi.T7.v7.1.Dissector] | 3/14/2019 | 3920 | Untested|
|[Eurex][Eurex.Derivatives.Eobi.T7.v7.0.Organization] | Derivatives | Eobi | T7 | [7.0][Eurex.Derivatives.Eobi.T7.v7.0.Dissector] | 8/20/2018 | 3805 | Untested|
|[Eurex][Eurex.Derivatives.Eobi.T7.v6.1.Organization] | Derivatives | Eobi | T7 | [6.1][Eurex.Derivatives.Eobi.T7.v6.1.Dissector] | 3/20/2018 | 3677 | Untested|
|[Eurex][Eurex.Derivatives.Eobi.T7.v6.0.Organization] | Derivatives | Eobi | T7 | [6.0][Eurex.Derivatives.Eobi.T7.v6.0.Dissector] | 10/23/2017 | 3674 | Verified|
|[Eurex][Eurex.Derivatives.Eobi.T7.v5.0.Organization] | Derivatives | Eobi | T7 | [5.0][Eurex.Derivatives.Eobi.T7.v5.0.Dissector] | 6/9/2017 | 3567 | Untested|
|[Eurex][Eurex.Derivatives.Eobi.T7.v4.0.Organization] | Derivatives | Eobi | T7 | [4.0][Eurex.Derivatives.Eobi.T7.v4.0.Dissector] | 11/11/2016 | 3564 | Untested|
|[Eurex][Eurex.Derivatives.Eobi.T7.v3.0.Organization] | Derivatives | Eobi | T7 | [3.0][Eurex.Derivatives.Eobi.T7.v3.0.Dissector] | 8/3/2015 | 3374 | Verified|
|[Eurex][Eurex.Derivatives.Eobi.T7.v2.5.Organization] | Derivatives | Eobi | T7 | [2.5][Eurex.Derivatives.Eobi.T7.v2.5.Dissector] | 11/7/2014 | 3354 | Untested|
|[Ice][Ice.Futures.Mdf.iMpact.v1.1.34.Organization] | Futures | Mdf | iMpact | [1.1.34][Ice.Futures.Mdf.iMpact.v1.1.34.Dissector] | 9/4/2018 | 8820 | Verified|
|[Ice][Ice.Futures.Mdf.iMpact.v1.1.33.Organization] | Futures | Mdf | iMpact | [1.1.33][Ice.Futures.Mdf.iMpact.v1.1.33.Dissector] | 8/6/2018 | 8615 | Verified|
|[Ice][Ice.Futures.Mdf.iMpact.v1.1.24.Organization] | Futures | Mdf | iMpact | [1.1.24][Ice.Futures.Mdf.iMpact.v1.1.24.Dissector] | 3/30/2016 | 7852 | Verified|
|[Miax][Miax.Options.cTom.Mach.v1.3.Organization] | Options | cTom | Mach | [1.3][Miax.Options.cTom.Mach.v1.3.Dissector] | 3/16/2018 | 2719 | Untested|
|[Miax][Miax.Options.cTom.Mach.v1.1.Organization] | Options | cTom | Mach | [1.1][Miax.Options.cTom.Mach.v1.1.Dissector] | 7/15/2016 | 2707 | Verified|
|[Miax][Miax.Options.Tom.Mach.v2.3.Organization] | Options | Tom | Mach | [2.3][Miax.Options.Tom.Mach.v2.3.Dissector] | 6/10/2019 | 2624 | Untested|
|[Miax][Miax.Options.Tom.Mach.v2.2.Organization] | Options | Tom | Mach | [2.2][Miax.Options.Tom.Mach.v2.2.Dissector] | 3/16/2018 | 2564 | Untested|
|[Miax][Miax.Options.Tom.Mach.v1.9.Organization] | Options | Tom | Mach | [1.9][Miax.Options.Tom.Mach.v1.9.Dissector] | 1/15/2016 | 2470 | Verified|
|[Miax][Miax.Pearl.Tom.Mach.v1.0.Organization] | Pearl | Tom | Mach | [1.0][Miax.Pearl.Tom.Mach.v1.0.Dissector] | 2/27/2017 | 2547 | Untested|
|[Nasdaq][Nasdaq.Equities.Orders.Ouch.v4.2.Organization] |  Equities | Orders | Ouch | [4.2][Nasdaq.Equities.Orders.Ouch.v4.2.Dissector] | 7/8/2019 | 2737 | Untested|
|[Nasdaq][Nasdaq.Bx.Equities.TotalView.Itch.v5.0.Organization] | Bx Equities | TotalView | Itch | [5.0][Nasdaq.Bx.Equities.TotalView.Itch.v5.0.Dissector] | 5/23/2018 | 3197 | Untested|
|[Nasdaq][Nasdaq.Bx.Options.DepthOfMarket.Itch.v1.3.Organization] | Bx Options | DepthOfMarket | Itch | [1.3][Nasdaq.Bx.Options.DepthOfMarket.Itch.v1.3.Dissector] | 11/2/2017 | 3100 | Untested|
|[Nasdaq][Nasdaq.Bx.Options.TopOfMarket.Itch.v1.2.Organization] | Bx Options | TopOfMarket | Itch | [1.2][Nasdaq.Bx.Options.TopOfMarket.Itch.v1.2.Dissector] | 11/2/2017 | 2008 | Untested|
|[Nasdaq][Nasdaq.Equities.Aggregated.Itch.v2.0.Organization] | Equities | Aggregated | Itch | [2.0][Nasdaq.Equities.Aggregated.Itch.v2.0.Dissector] | 9/12/2017 | 2763 | Untested|
|[Nasdaq][Nasdaq.Equities.Level2.Itch.v2.0.Organization] | Equities | Level2 | Itch | [2.0][Nasdaq.Equities.Level2.Itch.v2.0.Dissector] | 5/3/2018 | 2404 | Untested|
|[Nasdaq][Nasdaq.Equities.Noi.Itch.v3.0.Organization] | Equities | Noi | Itch | [3.0][Nasdaq.Equities.Noi.Itch.v3.0.Dissector] | 9/12/2017 | 1787 | Untested|
|[Nasdaq][Nasdaq.Equities.TotalView.Itch.v5.0.Organization] | Equities | TotalView | Itch | [5.0][Nasdaq.Equities.TotalView.Itch.v5.0.Dissector] | 9/12/2017 | 3521 | Untested|
|[Nasdaq][Nasdaq.Equities.TotalView.Itch.v4.1.Organization] | Equities | TotalView | Itch | [4.1][Nasdaq.Equities.TotalView.Itch.v4.1.Dissector] | 6/12/2014 | 2284 | Untested|
|[Nasdaq][Nasdaq.Ise.OrderComboFeed.Itch.v1.1.Organization] | Ise | OrderComboFeed | Itch | [1.1][Nasdaq.Ise.OrderComboFeed.Itch.v1.1.Dissector] | 6/13/2017 | 1893 | Verified|
|[Nasdaq][Nasdaq.Ise.OrderFeed.Itch.v1.1.Organization] | Ise | OrderFeed | Itch | [1.1][Nasdaq.Ise.OrderFeed.Itch.v1.1.Dissector] | 8/23/2017 | 1954 | Untested|
|[Nasdaq][Nasdaq.Ise.TopComboQuoteFeed.Itch.v1.0.Organization] | Ise | TopComboQuoteFeed | Itch | [1.0][Nasdaq.Ise.TopComboQuoteFeed.Itch.v1.0.Dissector] | 8/23/2017 | 2170 | Verified|
|[Nasdaq][Nasdaq.Nom.Bono.Itch.v3.2.Organization] | Nom | Bono | Itch | [3.2][Nasdaq.Nom.Bono.Itch.v3.2.Dissector] | 11/2/2017 | 2015 | Untested|
|[Nasdaq][Nasdaq.Nom.Itto.Itch.v4.0.Organization] | Nom | Itto | Itch | [4.0][Nasdaq.Nom.Itto.Itch.v4.0.Dissector] | 2/8/2018 | 2946 | Untested|
|[Nasdaq][Nasdaq.Phlx.MarketDepth.Itch.v1.6.Organization] | Phlx | MarketDepth | Itch | [1.6][Nasdaq.Phlx.MarketDepth.Itch.v1.6.Dissector] | 3/8/2018 | 3308 | Untested|
|[Nasdaq][Nasdaq.Phlx.MarketDepth.Itch.v1.5.Organization] | Phlx | MarketDepth | Itch | [1.5][Nasdaq.Phlx.MarketDepth.Itch.v1.5.Dissector] | 9/30/2015 | 3319 | Untested|
|[Nasdaq][Nasdaq.Phlx.Orders.Itch.v1.9.Organization] | Phlx | Orders | Itch | [1.9][Nasdaq.Phlx.Orders.Itch.v1.9.Dissector] | 8/10/2015 | 2406 | Untested|
|[Nasdaq][Nasdaq.Phlx.Topo.Itch.v3.3.Organization] | Phlx | Topo | Itch | [3.3][Nasdaq.Phlx.Topo.Itch.v3.3.Dissector] | 11/2/2017 | 2024 | Untested|
|[Nasdaq][Nasdaq.Psx.Bbo.Itch.v2.1.Organization] | Psx | Bbo | Itch | [2.1][Nasdaq.Psx.Bbo.Itch.v2.1.Dissector] | 5/3/2018 | 1839 | Untested|
|[Nasdaq][Nasdaq.Psx.LastSale.Itch.v2.1.Organization] | Psx | LastSale | Itch | [2.1][Nasdaq.Psx.LastSale.Itch.v2.1.Dissector] | 5/3/2018 | 2851 | Untested|
|[Nasdaq][Nasdaq.Psx.TotalView.Itch.v5.0.Organization] | Psx | TotalView | Itch | [5.0][Nasdaq.Psx.TotalView.Itch.v5.0.Dissector] | 5/3/2018 | 3191 | Untested|
|[Nyse][Nyse.Equities.OpenBook.Ultra.v2.1.b.Organization] |  Equities | OpenBook | Ultra | [2.1.b][Nyse.Equities.OpenBook.Ultra.v2.1.b.Dissector] | 3/9/2018 | 1365 | Verified|
|[Nyse][Nyse.Amex.Equities.OpenBook.Ultra.v2.1.b.Organization] | Amex Equities | OpenBook | Ultra | [2.1.b][Nyse.Amex.Equities.OpenBook.Ultra.v2.1.b.Dissector] | 3/9/2018 | 1371 | Verified|
|[Nyse][Nyse.Equities.Bbo.Xdp.v2.4.g.Organization] | Equities | Bbo | Xdp | [2.4.g][Nyse.Equities.Bbo.Xdp.v2.4.g.Dissector] | 1/29/2018 | 2667 | Verified|
|[Nyse][Nyse.Equities.Bqt.Xdp.v2.1.a.Organization] | Equities | Bqt | Xdp | [2.1.a][Nyse.Equities.Bqt.Xdp.v2.1.a.Dissector] | 4/4/2018 | 3961 | Untested|
|[Nyse][Nyse.Equities.Bqt.Xdp.v1.7.a.Organization] | Equities | Bqt | Xdp | [1.7.a][Nyse.Equities.Bqt.Xdp.v1.7.a.Dissector] | 7/24/2017 | 3867 | Verified|
|[Nyse][Nyse.Equities.ImbalancesFeed.Xdp.v2.2.a.Organization] | Equities | ImbalancesFeed | Xdp | [2.2.a][Nyse.Equities.ImbalancesFeed.Xdp.v2.2.a.Dissector] | 3/8/2019 | 2608 | Verified|
|[Nyse][Nyse.Equities.ImbalancesFeed.Xdp.v2.1.f.Organization] | Equities | ImbalancesFeed | Xdp | [2.1.f][Nyse.Equities.ImbalancesFeed.Xdp.v2.1.f.Dissector] | 2/1/2018 | 2522 | Verified|
|[Nyse][Nyse.Equities.IntegratedFeed.Xdp.v2.1.g.Organization] | Equities | IntegratedFeed | Xdp | [2.1.g][Nyse.Equities.IntegratedFeed.Xdp.v2.1.g.Dissector] | 1/29/2018 | 4161 | Verified|
|[Nyse][Nyse.Equities.Amex.IntegratedFeed.Xdp.v2.1.g.Organization] | Equities Amex | IntegratedFeed | Xdp | [2.1.g][Nyse.Equities.Amex.IntegratedFeed.Xdp.v2.1.g.Dissector] | 1/29/2018 | 4161 | Verified|
|[Nyse][Nyse.Equities.Arca.Bbo.Xdp.v2.4.c.Organization] | Equities Arca | Bbo | Xdp | [2.4.c][Nyse.Equities.Arca.Bbo.Xdp.v2.4.c.Dissector] | 7/13/2016 | 2670 | Verified|
|[Nyse][Nyse.Options.ComplexFeed.Xdp.v1.3.a.Organization] | Options | ComplexFeed | Xdp | [1.3.a][Nyse.Options.ComplexFeed.Xdp.v1.3.a.Dissector] | 2/28/2018 | 2025 | Verified|
|[Nyse][Nyse.Options.DeepFeed.Xdp.v1.3.a.Organization] | Options | DeepFeed | Xdp | [1.3.a][Nyse.Options.DeepFeed.Xdp.v1.3.a.Dissector] | 2/28/2018 | 2269 | Untested|
|[Nyse][Nyse.Options.TopFeed.Xdp.v1.3.a.Organization] | Options | TopFeed | Xdp | [1.3.a][Nyse.Options.TopFeed.Xdp.v1.3.a.Dissector] | 2/28/2018 | 3140 | Untested|
|[Opra][Opra.Options.Recipient.Obdi.v2.9.Organization] | Options | Recipient | Obdi | [2.9][Opra.Options.Recipient.Obdi.v2.9.Dissector] | 10/24/2018 | 5665 | Untested|

## Development

Updates are greatly appreciated; however, this entire repository is source generated...including the words you are reading right now. Code generation requires a different workflow.  The recommended process is to create an issue with suggested script edits and explanation.  If the changes are applicable to some or all protocols, we will update the model and regenerate.

|Protocol Count | Generated Lines|
|--- | ---|
|69 | 252,659|

Note: Our dissector model is still under rapid development.

## Testing

Please report any dissection errors as issues.  Include a small note on the protocol and version, and a minimal capture demonstrating the problem. Also consider including a link or pdf specification documenting the correct behavior.

Production captures are required for protocol verification.  If your organization has the rights to donate captures, and you wish to make the world a better place, please contact us.

## Open Markets Initiative

The Open Markets Initiative (Omi) is a group of technologists dedicated to enhancing the stability of electronic financial markets using modern development methods.

Please check out our other projects: [Omi Directory](https://github.com/Open-Markets-Initiative/Directory "Open Markets Initiative Repository Directory")

## Disclaimer

Any similarities between existing people, places and/or protocols is purely incidental.

Enjoy.

[Asx.Securities.T24.Itch.v1.13.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Asx "Australian Securities Exchange"
[Asx.Securities.T24.Itch.v1.13.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Asx/Asx.Securities.T24.Itch.v1.13.Script.Dissector.lua "Australian Securities Exchange 1.13 Wireshark Dissector"
[Cboe.Futures.DepthOfBook.Pitch.v1.1.6.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Cboe "Chicago Board Options Exchange"
[Cboe.Futures.DepthOfBook.Pitch.v1.1.6.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Cboe/Cboe.Futures.DepthOfBook.Pitch.v1.1.6.Script.Dissector.lua "Chicago Board Options Exchange 1.1.6 Wireshark Dissector"
[Cboe.Options.C1.AuctionFeed.Pitch.v1.1.1.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Cboe "Chicago Board Options Exchange"
[Cboe.Options.C1.AuctionFeed.Pitch.v1.1.1.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Cboe/Cboe.Options.C1.AuctionFeed.Pitch.v1.1.1.Script.Dissector.lua "Chicago Board Options Exchange 1.1.1 Wireshark Dissector"
[Cboe.Options.Edgx.AuctionFeed.Pitch.v1.1.1.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Cboe "Chicago Board Options Exchange"
[Cboe.Options.Edgx.AuctionFeed.Pitch.v1.1.1.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Cboe/Cboe.Options.Edgx.AuctionFeed.Pitch.v1.1.1.Script.Dissector.lua "Chicago Board Options Exchange 1.1.1 Wireshark Dissector"
[Cboe.Options.DepthOfBook.Pitch.v2.39.4.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Cboe "Chicago Board Options Exchange"
[Cboe.Options.DepthOfBook.Pitch.v2.39.4.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Cboe/Cboe.Options.DepthOfBook.Pitch.v2.39.4.Script.Dissector.lua "Chicago Board Options Exchange 2.39.4 Wireshark Dissector"
[Cboe.Options.MarketDataFeed.Csm.v1.4.2.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Cboe "Chicago Board Options Exchange"
[Cboe.Options.MarketDataFeed.Csm.v1.4.2.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Cboe/Cboe.Options.MarketDataFeed.Csm.v1.4.2.Script.Dissector.lua "Chicago Board Options Exchange 1.4.2 Wireshark Dissector"
[Cboe.Options.MarketLevel2.Csm.v1.0.4.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Cboe "Chicago Board Options Exchange"
[Cboe.Options.MarketLevel2.Csm.v1.0.4.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Cboe/Cboe.Options.MarketLevel2.Csm.v1.0.4.Script.Dissector.lua "Chicago Board Options Exchange 1.0.4 Wireshark Dissector"
[Cboe.Options.OpeningAuction.Csm.v1.0.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Cboe "Chicago Board Options Exchange"
[Cboe.Options.OpeningAuction.Csm.v1.0.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Cboe/Cboe.Options.OpeningAuction.Csm.v1.0.Script.Dissector.lua "Chicago Board Options Exchange 1.0 Wireshark Dissector"
[Cme.Mdp3.Sbe.v5.1.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Cme "Chicago Mercantile Exchange"
[Cme.Mdp3.Sbe.v5.1.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Cme/Cme.Mdp3.Sbe.v5.1.Script.Dissector.lua "Chicago Mercantile Exchange 5.1 Wireshark Dissector"
[Cme.Mdp3.Sbe.v6.1.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Cme "Chicago Mercantile Exchange"
[Cme.Mdp3.Sbe.v6.1.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Cme/Cme.Mdp3.Sbe.v6.1.Script.Dissector.lua "Chicago Mercantile Exchange 6.1 Wireshark Dissector"
[Cme.Mdp3.Sbe.v8.1.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Cme "Chicago Mercantile Exchange"
[Cme.Mdp3.Sbe.v8.1.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Cme/Cme.Mdp3.Sbe.v8.1.Script.Dissector.lua "Chicago Mercantile Exchange 8.1 Wireshark Dissector"
[Cme.Mdp3.Sbe.v9.1.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Cme "Chicago Mercantile Exchange"
[Cme.Mdp3.Sbe.v9.1.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Cme/Cme.Mdp3.Sbe.v9.1.Script.Dissector.lua "Chicago Mercantile Exchange 9.1 Wireshark Dissector"
[Cme.Mdp3.Sbe.v10.1.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Cme "Chicago Mercantile Exchange"
[Cme.Mdp3.Sbe.v10.1.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Cme/Cme.Mdp3.Sbe.v10.1.Script.Dissector.lua "Chicago Mercantile Exchange 10.1 Wireshark Dissector"
[Cme.Streamline.Sbe.v8.5.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Cme "Chicago Mercantile Exchange"
[Cme.Streamline.Sbe.v8.5.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Cme/Cme.Streamline.Sbe.v8.5.Script.Dissector.lua "Chicago Mercantile Exchange 8.5 Wireshark Dissector"
[Cme.Streamline.Sbe.v9.5.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Cme "Chicago Mercantile Exchange"
[Cme.Streamline.Sbe.v9.5.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Cme/Cme.Streamline.Sbe.v9.5.Script.Dissector.lua "Chicago Mercantile Exchange 9.5 Wireshark Dissector"
[Cme.Futures.iLink3.Sbe.v8.0.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Cme "Chicago Mercantile Exchange"
[Cme.Futures.iLink3.Sbe.v8.0.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Cme/Cme.Futures.iLink3.Sbe.v8.0.Script.Dissector.lua "Chicago Mercantile Exchange 8.0 Wireshark Dissector"
[Eurex.Derivatives.Eobi.T7.v2.5.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Eurex "Eurex Exchange"
[Eurex.Derivatives.Eobi.T7.v2.5.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Eurex/Eurex.Derivatives.Eobi.T7.v2.5.Script.Dissector.lua "Eurex Exchange 2.5 Wireshark Dissector"
[Eurex.Derivatives.Eobi.T7.v3.0.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Eurex "Eurex Exchange"
[Eurex.Derivatives.Eobi.T7.v3.0.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Eurex/Eurex.Derivatives.Eobi.T7.v3.0.Script.Dissector.lua "Eurex Exchange 3.0 Wireshark Dissector"
[Eurex.Derivatives.Eobi.T7.v4.0.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Eurex "Eurex Exchange"
[Eurex.Derivatives.Eobi.T7.v4.0.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Eurex/Eurex.Derivatives.Eobi.T7.v4.0.Script.Dissector.lua "Eurex Exchange 4.0 Wireshark Dissector"
[Eurex.Derivatives.Eobi.T7.v5.0.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Eurex "Eurex Exchange"
[Eurex.Derivatives.Eobi.T7.v5.0.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Eurex/Eurex.Derivatives.Eobi.T7.v5.0.Script.Dissector.lua "Eurex Exchange 5.0 Wireshark Dissector"
[Eurex.Derivatives.Eobi.T7.v6.0.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Eurex "Eurex Exchange"
[Eurex.Derivatives.Eobi.T7.v6.0.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Eurex/Eurex.Derivatives.Eobi.T7.v6.0.Script.Dissector.lua "Eurex Exchange 6.0 Wireshark Dissector"
[Eurex.Derivatives.Eobi.T7.v6.1.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Eurex "Eurex Exchange"
[Eurex.Derivatives.Eobi.T7.v6.1.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Eurex/Eurex.Derivatives.Eobi.T7.v6.1.Script.Dissector.lua "Eurex Exchange 6.1 Wireshark Dissector"
[Eurex.Derivatives.Eobi.T7.v7.0.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Eurex "Eurex Exchange"
[Eurex.Derivatives.Eobi.T7.v7.0.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Eurex/Eurex.Derivatives.Eobi.T7.v7.0.Script.Dissector.lua "Eurex Exchange 7.0 Wireshark Dissector"
[Eurex.Derivatives.Eobi.T7.v7.1.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Eurex "Eurex Exchange"
[Eurex.Derivatives.Eobi.T7.v7.1.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Eurex/Eurex.Derivatives.Eobi.T7.v7.1.Script.Dissector.lua "Eurex Exchange 7.1 Wireshark Dissector"
[Eurex.Derivatives.Eobi.T7.v8.0.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Eurex "Eurex Exchange"
[Eurex.Derivatives.Eobi.T7.v8.0.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Eurex/Eurex.Derivatives.Eobi.T7.v8.0.Script.Dissector.lua "Eurex Exchange 8.0 Wireshark Dissector"
[Ice.Futures.Mdf.iMpact.v1.1.24.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Ice "Intercontinental Exchange"
[Ice.Futures.Mdf.iMpact.v1.1.24.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Ice/Ice.Futures.Mdf.iMpact.v1.1.24.Script.Dissector.lua "Intercontinental Exchange 1.1.24 Wireshark Dissector"
[Ice.Futures.Mdf.iMpact.v1.1.33.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Ice "Intercontinental Exchange"
[Ice.Futures.Mdf.iMpact.v1.1.33.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Ice/Ice.Futures.Mdf.iMpact.v1.1.33.Script.Dissector.lua "Intercontinental Exchange 1.1.33 Wireshark Dissector"
[Ice.Futures.Mdf.iMpact.v1.1.34.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Ice "Intercontinental Exchange"
[Ice.Futures.Mdf.iMpact.v1.1.34.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Ice/Ice.Futures.Mdf.iMpact.v1.1.34.Script.Dissector.lua "Intercontinental Exchange 1.1.34 Wireshark Dissector"
[Miax.Options.cTom.Mach.v1.1.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Miax "Miami International Securities Exchange"
[Miax.Options.cTom.Mach.v1.1.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Miax/Miax.Options.cTom.Mach.v1.1.Script.Dissector.lua "Miami International Securities Exchange 1.1 Wireshark Dissector"
[Miax.Options.cTom.Mach.v1.3.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Miax "Miami International Securities Exchange"
[Miax.Options.cTom.Mach.v1.3.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Miax/Miax.Options.cTom.Mach.v1.3.Script.Dissector.lua "Miami International Securities Exchange 1.3 Wireshark Dissector"
[Miax.Options.Tom.Mach.v1.9.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Miax "Miami International Securities Exchange"
[Miax.Options.Tom.Mach.v1.9.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Miax/Miax.Options.Tom.Mach.v1.9.Script.Dissector.lua "Miami International Securities Exchange 1.9 Wireshark Dissector"
[Miax.Options.Tom.Mach.v2.2.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Miax "Miami International Securities Exchange"
[Miax.Options.Tom.Mach.v2.2.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Miax/Miax.Options.Tom.Mach.v2.2.Script.Dissector.lua "Miami International Securities Exchange 2.2 Wireshark Dissector"
[Miax.Options.Tom.Mach.v2.3.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Miax "Miami International Securities Exchange"
[Miax.Options.Tom.Mach.v2.3.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Miax/Miax.Options.Tom.Mach.v2.3.Script.Dissector.lua "Miami International Securities Exchange 2.3 Wireshark Dissector"
[Miax.Pearl.Tom.Mach.v1.0.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Miax "Miami International Securities Exchange"
[Miax.Pearl.Tom.Mach.v1.0.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Miax/Miax.Pearl.Tom.Mach.v1.0.Script.Dissector.lua "Miami International Securities Exchange 1.0 Wireshark Dissector"
[Nasdaq.Bx.Equities.TotalView.Itch.v5.0.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nasdaq "National Association of Securities Dealers Automated Quotations"
[Nasdaq.Bx.Equities.TotalView.Itch.v5.0.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nasdaq/Nasdaq.Bx.Equities.TotalView.Itch.v5.0.Script.Dissector.lua "National Association of Securities Dealers Automated Quotations 5.0 Wireshark Dissector"
[Nasdaq.Bx.Options.TopOfMarket.Itch.v1.2.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nasdaq "National Association of Securities Dealers Automated Quotations"
[Nasdaq.Bx.Options.TopOfMarket.Itch.v1.2.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nasdaq/Nasdaq.Bx.Options.TopOfMarket.Itch.v1.2.Script.Dissector.lua "National Association of Securities Dealers Automated Quotations 1.2 Wireshark Dissector"
[Nasdaq.Bx.Options.DepthOfMarket.Itch.v1.3.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nasdaq "National Association of Securities Dealers Automated Quotations"
[Nasdaq.Bx.Options.DepthOfMarket.Itch.v1.3.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nasdaq/Nasdaq.Bx.Options.DepthOfMarket.Itch.v1.3.Script.Dissector.lua "National Association of Securities Dealers Automated Quotations 1.3 Wireshark Dissector"
[Nasdaq.Ise.OrderComboFeed.Itch.v1.1.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nasdaq "National Association of Securities Dealers Automated Quotations"
[Nasdaq.Ise.OrderComboFeed.Itch.v1.1.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nasdaq/Nasdaq.Ise.OrderComboFeed.Itch.v1.1.Script.Dissector.lua "National Association of Securities Dealers Automated Quotations 1.1 Wireshark Dissector"
[Nasdaq.Ise.OrderFeed.Itch.v1.1.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nasdaq "National Association of Securities Dealers Automated Quotations"
[Nasdaq.Ise.OrderFeed.Itch.v1.1.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nasdaq/Nasdaq.Ise.OrderFeed.Itch.v1.1.Script.Dissector.lua "National Association of Securities Dealers Automated Quotations 1.1 Wireshark Dissector"
[Nasdaq.Ise.TopComboQuoteFeed.Itch.v1.0.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nasdaq "National Association of Securities Dealers Automated Quotations"
[Nasdaq.Ise.TopComboQuoteFeed.Itch.v1.0.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nasdaq/Nasdaq.Ise.TopComboQuoteFeed.Itch.v1.0.Script.Dissector.lua "National Association of Securities Dealers Automated Quotations 1.0 Wireshark Dissector"
[Nasdaq.Nom.Bono.Itch.v3.2.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nasdaq "National Association of Securities Dealers Automated Quotations"
[Nasdaq.Nom.Bono.Itch.v3.2.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nasdaq/Nasdaq.Nom.Bono.Itch.v3.2.Script.Dissector.lua "National Association of Securities Dealers Automated Quotations 3.2 Wireshark Dissector"
[Nasdaq.Nom.Itto.Itch.v4.0.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nasdaq "National Association of Securities Dealers Automated Quotations"
[Nasdaq.Nom.Itto.Itch.v4.0.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nasdaq/Nasdaq.Nom.Itto.Itch.v4.0.Script.Dissector.lua "National Association of Securities Dealers Automated Quotations 4.0 Wireshark Dissector"
[Nasdaq.Phlx.MarketDepth.Itch.v1.5.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nasdaq "National Association of Securities Dealers Automated Quotations"
[Nasdaq.Phlx.MarketDepth.Itch.v1.5.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nasdaq/Nasdaq.Phlx.MarketDepth.Itch.v1.5.Script.Dissector.lua "National Association of Securities Dealers Automated Quotations 1.5 Wireshark Dissector"
[Nasdaq.Phlx.MarketDepth.Itch.v1.6.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nasdaq "National Association of Securities Dealers Automated Quotations"
[Nasdaq.Phlx.MarketDepth.Itch.v1.6.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nasdaq/Nasdaq.Phlx.MarketDepth.Itch.v1.6.Script.Dissector.lua "National Association of Securities Dealers Automated Quotations 1.6 Wireshark Dissector"
[Nasdaq.Phlx.Orders.Itch.v1.9.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nasdaq "National Association of Securities Dealers Automated Quotations"
[Nasdaq.Phlx.Orders.Itch.v1.9.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nasdaq/Nasdaq.Phlx.Orders.Itch.v1.9.Script.Dissector.lua "National Association of Securities Dealers Automated Quotations 1.9 Wireshark Dissector"
[Nasdaq.Phlx.Topo.Itch.v3.3.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nasdaq "National Association of Securities Dealers Automated Quotations"
[Nasdaq.Phlx.Topo.Itch.v3.3.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nasdaq/Nasdaq.Phlx.Topo.Itch.v3.3.Script.Dissector.lua "National Association of Securities Dealers Automated Quotations 3.3 Wireshark Dissector"
[Nasdaq.Psx.LastSale.Itch.v2.1.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nasdaq "National Association of Securities Dealers Automated Quotations"
[Nasdaq.Psx.LastSale.Itch.v2.1.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nasdaq/Nasdaq.Psx.LastSale.Itch.v2.1.Script.Dissector.lua "National Association of Securities Dealers Automated Quotations 2.1 Wireshark Dissector"
[Nasdaq.Psx.TotalView.Itch.v5.0.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nasdaq "National Association of Securities Dealers Automated Quotations"
[Nasdaq.Psx.TotalView.Itch.v5.0.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nasdaq/Nasdaq.Psx.TotalView.Itch.v5.0.Script.Dissector.lua "National Association of Securities Dealers Automated Quotations 5.0 Wireshark Dissector"
[Nasdaq.Psx.Bbo.Itch.v2.1.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nasdaq "National Association of Securities Dealers Automated Quotations"
[Nasdaq.Psx.Bbo.Itch.v2.1.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nasdaq/Nasdaq.Psx.Bbo.Itch.v2.1.Script.Dissector.lua "National Association of Securities Dealers Automated Quotations 2.1 Wireshark Dissector"
[Nasdaq.Equities.Aggregated.Itch.v2.0.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nasdaq "National Association of Securities Dealers Automated Quotations"
[Nasdaq.Equities.Aggregated.Itch.v2.0.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nasdaq/Nasdaq.Equities.Aggregated.Itch.v2.0.Script.Dissector.lua "National Association of Securities Dealers Automated Quotations 2.0 Wireshark Dissector"
[Nasdaq.Equities.Level2.Itch.v2.0.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nasdaq "National Association of Securities Dealers Automated Quotations"
[Nasdaq.Equities.Level2.Itch.v2.0.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nasdaq/Nasdaq.Equities.Level2.Itch.v2.0.Script.Dissector.lua "National Association of Securities Dealers Automated Quotations 2.0 Wireshark Dissector"
[Nasdaq.Equities.Noi.Itch.v3.0.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nasdaq "National Association of Securities Dealers Automated Quotations"
[Nasdaq.Equities.Noi.Itch.v3.0.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nasdaq/Nasdaq.Equities.Noi.Itch.v3.0.Script.Dissector.lua "National Association of Securities Dealers Automated Quotations 3.0 Wireshark Dissector"
[Nasdaq.Equities.Orders.Ouch.v4.2.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nasdaq "National Association of Securities Dealers Automated Quotations"
[Nasdaq.Equities.Orders.Ouch.v4.2.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nasdaq/Nasdaq.Equities.Orders.Ouch.v4.2.Script.Dissector.lua "National Association of Securities Dealers Automated Quotations 4.2 Wireshark Dissector"
[Nasdaq.Equities.TotalView.Itch.v4.1.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nasdaq "National Association of Securities Dealers Automated Quotations"
[Nasdaq.Equities.TotalView.Itch.v4.1.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nasdaq/Nasdaq.Equities.TotalView.Itch.v4.1.Script.Dissector.lua "National Association of Securities Dealers Automated Quotations 4.1 Wireshark Dissector"
[Nasdaq.Equities.TotalView.Itch.v5.0.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nasdaq "National Association of Securities Dealers Automated Quotations"
[Nasdaq.Equities.TotalView.Itch.v5.0.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nasdaq/Nasdaq.Equities.TotalView.Itch.v5.0.Script.Dissector.lua "National Association of Securities Dealers Automated Quotations 5.0 Wireshark Dissector"
[Nyse.Amex.Equities.OpenBook.Ultra.v2.1.b.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nyse "New York Stock Exchange"
[Nyse.Amex.Equities.OpenBook.Ultra.v2.1.b.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nyse/Nyse.Amex.Equities.OpenBook.Ultra.v2.1.b.Script.Dissector.lua "New York Stock Exchange 2.1.b Wireshark Dissector"
[Nyse.Equities.OpenBook.Ultra.v2.1.b.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nyse "New York Stock Exchange"
[Nyse.Equities.OpenBook.Ultra.v2.1.b.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nyse/Nyse.Equities.OpenBook.Ultra.v2.1.b.Script.Dissector.lua "New York Stock Exchange 2.1.b Wireshark Dissector"
[Nyse.Equities.Amex.IntegratedFeed.Xdp.v2.1.g.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nyse "New York Stock Exchange"
[Nyse.Equities.Amex.IntegratedFeed.Xdp.v2.1.g.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nyse/Nyse.Equities.Amex.IntegratedFeed.Xdp.v2.1.g.Script.Dissector.lua "New York Stock Exchange 2.1.g Wireshark Dissector"
[Nyse.Equities.Arca.Bbo.Xdp.v2.4.c.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nyse "New York Stock Exchange"
[Nyse.Equities.Arca.Bbo.Xdp.v2.4.c.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nyse/Nyse.Equities.Arca.Bbo.Xdp.v2.4.c.Script.Dissector.lua "New York Stock Exchange 2.4.c Wireshark Dissector"
[Nyse.Equities.Bbo.Xdp.v2.4.g.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nyse "New York Stock Exchange"
[Nyse.Equities.Bbo.Xdp.v2.4.g.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nyse/Nyse.Equities.Bbo.Xdp.v2.4.g.Script.Dissector.lua "New York Stock Exchange 2.4.g Wireshark Dissector"
[Nyse.Equities.Bqt.Xdp.v1.7.a.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nyse "New York Stock Exchange"
[Nyse.Equities.Bqt.Xdp.v1.7.a.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nyse/Nyse.Equities.Bqt.Xdp.v1.7.a.Script.Dissector.lua "New York Stock Exchange 1.7.a Wireshark Dissector"
[Nyse.Equities.Bqt.Xdp.v2.1.a.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nyse "New York Stock Exchange"
[Nyse.Equities.Bqt.Xdp.v2.1.a.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nyse/Nyse.Equities.Bqt.Xdp.v2.1.a.Script.Dissector.lua "New York Stock Exchange 2.1.a Wireshark Dissector"
[Nyse.Equities.ImbalancesFeed.Xdp.v2.1.f.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nyse "New York Stock Exchange"
[Nyse.Equities.ImbalancesFeed.Xdp.v2.1.f.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nyse/Nyse.Equities.ImbalancesFeed.Xdp.v2.1.f.Script.Dissector.lua "New York Stock Exchange 2.1.f Wireshark Dissector"
[Nyse.Equities.ImbalancesFeed.Xdp.v2.2.a.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nyse "New York Stock Exchange"
[Nyse.Equities.ImbalancesFeed.Xdp.v2.2.a.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nyse/Nyse.Equities.ImbalancesFeed.Xdp.v2.2.a.Script.Dissector.lua "New York Stock Exchange 2.2.a Wireshark Dissector"
[Nyse.Equities.IntegratedFeed.Xdp.v2.1.g.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nyse "New York Stock Exchange"
[Nyse.Equities.IntegratedFeed.Xdp.v2.1.g.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nyse/Nyse.Equities.IntegratedFeed.Xdp.v2.1.g.Script.Dissector.lua "New York Stock Exchange 2.1.g Wireshark Dissector"
[Nyse.Options.ComplexFeed.Xdp.v1.3.a.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nyse "New York Stock Exchange"
[Nyse.Options.ComplexFeed.Xdp.v1.3.a.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nyse/Nyse.Options.ComplexFeed.Xdp.v1.3.a.Script.Dissector.lua "New York Stock Exchange 1.3.a Wireshark Dissector"
[Nyse.Options.DeepFeed.Xdp.v1.3.a.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nyse "New York Stock Exchange"
[Nyse.Options.DeepFeed.Xdp.v1.3.a.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nyse/Nyse.Options.DeepFeed.Xdp.v1.3.a.Script.Dissector.lua "New York Stock Exchange 1.3.a Wireshark Dissector"
[Nyse.Options.TopFeed.Xdp.v1.3.a.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Nyse "New York Stock Exchange"
[Nyse.Options.TopFeed.Xdp.v1.3.a.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Nyse/Nyse.Options.TopFeed.Xdp.v1.3.a.Script.Dissector.lua "New York Stock Exchange 1.3.a Wireshark Dissector"
[Opra.Options.Recipient.Obdi.v2.9.Organization]: https://github.com/Open-Markets-Initiative/wireshark-lua/tree/master/Opra "Options Price Reporting Authority"
[Opra.Options.Recipient.Obdi.v2.9.Dissector]: https://github.com/Open-Markets-Initiative/wireshark-lua/blob/master/Opra/Opra.Options.Recipient.Obdi.v2.9.Script.Dissector.lua "Options Price Reporting Authority 2.9 Wireshark Dissector"
