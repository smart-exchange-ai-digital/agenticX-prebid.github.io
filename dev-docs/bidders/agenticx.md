---
layout: bidder
title: AgenticX
description: Prebid.js and Prebid Server bidder adapter for AgenticX
biddercode: agenticx
media_types:
  - banner
  - video
  - audio
gdpr_supported: true
usp_supported: true
gpp_supported: true
user_sync: true
schain_supported: true
pbjs: true
pbs: true
sidebarType: 1
---

## Overview

AgenticX is a digital advertising platform that supports banner, video & audio ads through its Prebid.js and Prebid Server adapters. The adapters use OpenRTB standards for request and response formatting.

## Bid Params

{: .table .table-bordered .table-striped }
| Name        | Scope    | Type    | Description                                                              | Example    |
|-------------|----------|---------|--------------------------------------------------------------------------|------------|
| `bidfloor`  | optional | number  | Bid Floor                                                                | `0.01`     |
| `testMode`  | optional | integer | Parameter to indicate prebid test mode. Allowed values: `0`, `1`         | `1`        |
| `sspId`     | optional | string  | Supply Partner ID                                                        | `'111111'` |
| `siteId`    | optional | string  | Supply Partner Site ID                                                   | `'222222'` |

{: .alert.alert-info :}
In Prebid Server, all impressions in a single request must use the same `sspId` and `siteId` values. Requests that mix different values (including an impression that omits them) are rejected with a bad input error.
