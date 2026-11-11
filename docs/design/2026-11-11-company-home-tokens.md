# Company home: A good fit

Ticket #146. Plan and critique recorded before implementation, 2026-11-11.

## Tokens

| Name | Hex | Role |
| --- | --- | --- |
| Paper | `#F6F8FA` | Main canvas |
| Ink | `#172C32` | Headings and primary text |
| Slate | `#52636B` | Supporting copy |
| Tool blue | `#2457C5` | Company introduction, links, focus |
| Mist | `#E7EDF0` | Sample table headers and quiet separators |
| White | `#FFFFFF` | Reversed text and sample cells |

Type: retain the locally served, licensed **Public Sans**. Its open, practical shapes suit a small publisher of working tools; 800-weight tightly set display type supplies character without a decorative second family. Body 18px/1.65; display 48–80px/1.04; section headings 32–42px/1.12; supporting text 14–16px. Use tabular figures for comparisons, not a monospace metadata skin. Fragment Mono remains a pre-existing licensed asset but need not load. All font license files supplied by the parent are retained.

## Layout and alignment

Company name is the first heading. A blue introduction has one fitted, stepped lower corner; its straight geometry suggests a well-fitted tool, not a spreadsheet brand. Everything else is calm, unboxed and left aligned. A real product earns a wide sample illustration, not a catalogue card.

Desktop:

```text
Company wordmark                         Our app    Support
+-------------------------------------------------------+
| The apps              Useful apps, starting            |
| done well             with Chrome extensions.          |
|                       Explore Sheet Change Detector   |
+--------------------------------------------------+    |
                                                   +----+
Sheet Change Detector    [Sample: old/new comparison     ]
Specific product copy    [Cell | Before | After          ]
View the extension       [Explanation of what changed    ]

Made for the task.       Short, concrete maker approach.
Company                  Support          Privacy  Terms
```

Mobile:

```text
Company wordmark
Our app    Support
+---------------------+
| The apps done well  |
| Useful apps…        |
| Explore product    _|
+-------------------+
Sheet Change Detector
Specific copy / link
[Sample comparison    ]
[Before / After       ]
Maker approach
Support / legal
```

Product overview shares navigation, type, palette, sample language and footer. Its own H1 names Sheet Change Detector, identifies its publisher, explains comparisons, and offers an explicitly disabled install button with a plain explanation. Full workflow, plans and Pro detail remain #147's work, not incomplete catalogue placeholders.

## Principles

- Company identity leads; spreadsheet imagery is confined to the product sample.
- The sample shows two specific cell changes with before/after values, readable without color. It is not a screenshot or a working web app.
- Spend boldness only on the company introduction; no decorative gradients, card grid, fake statistics or stock imagery.
- No animation needed. Visible keyboard focus, a skip link, generous targets, reduced-motion protection, no horizontal scrolling.
- Preserve legal bytes and retain readable fallback styling for their existing markup.

## Pre-build critique and revision

The brief proposed Bricolage Grotesque plus Source Sans 3. Adding both would make an otherwise simple publisher depend on new assets and additional license verification; the existing Public Sans has sufficient range. Revised to one self-hosted family with a deliberate heavy display/light body contrast.

An initial hero concept used a generic “Small tools. Better days.” headline and three product benefit cards. Rejected: that copy could sell any productivity startup, and the cards invent a visual catalogue. Revised to the actual company name as the hero and a single product shown through a concrete before/after example. The maker statement will describe focus and explainability, not announce quality as an unsupported claim.

The fitted corner occurs once, on the company introduction. It is not repeated on links, tables or every section. Removed numeric section labels and arrow-ended links: neither encodes an actual sequence or adds information. This keeps the visual gesture specific and quiet rather than a SaaS kit or broadsheet default.

## Build review

Reviewed browser captures for both routes at 375, 768, 1280 and 1920px. The wide layout keeps company identity separate from the spreadsheet example; mobile uses the same reading order without a horizontally scrolling table. After the first review, increased sample formula text from 11px to 12px on mobile and 13px on tablet, and increased mobile change labels to 11px. The before/after formulas are essential evidence, not expendable metadata. Final captures show no clipped table content or page overflow.

Kept the product overview intentionally small: no plans or Pro capability claims are introduced in #146. The inactive install action names its state in the button and explains the missing verified destination immediately below it. The sample is semantic HTML, explicitly illustrative, and needs no script or assets beyond local fonts and CSS.

Mobile keyboard screenshot review caught the support link's focus outline crowding the preceding paragraph. Added a 12px gap above that link and repeated the focused capture; the outline now has clear space on all sides.
