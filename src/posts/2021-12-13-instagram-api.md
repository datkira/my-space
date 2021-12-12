---
title: 'Instagram Graph API: Overview, Content Publishing, Limitations, and References to do quickly'
description: Lorem ipsum dolor sit amet, consectetur adipiscing elit.
date: 2022-12-13
---


>  In this article, I will use my experience to summarize all of the things I think you should know before work with it.

## Overview
- Instagram Graph API only supports Instagram Business or Creator Account.
- You need to add the product Instagram Graph API in your app, and you must request approval from them before accessing it.
  ![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1626023691157/tao4brX2qy.png)
> To avoid disruption of service to your app and business, developers previously using the Legacy API should instead rely on Instagram Basic Display API and Instagram Graph API. Please request approval for required permissions through the App Review process.

### Limitations

- **Content Publishing** is **only available to Instagram Business Users**. It means that Instagram Creator Account is not supported.
- Reels are not supported.
- Ordering results is not supported.
- All endpoints support cursor-based pagination, but the User Insights edge is the only endpoint that supports time-based pagination.

## Content Publishing

> It only supports for Instagram Business Account

There are two steps to publish an object to Instagram:

1. Use the POST /{ig-user-id}/media endpoint to upload a photo and create an IG Container. To get ig-user-id, follow this page: https://developers.facebook.com/docs/instagram-api/getting-started
2. Use the POST /{ig-user-id}/media_publish endpoint to publish the photo using its container.

### Limitations

- Can only be used to publish to business IG User accounts, Creator IG User accounts are not supported.
- Accounts are limited to 25 API-published posts within a 24 hour period.
- JPEG is the only image format supported. Extended JPEG formats such as MPO and JPS are not supported.
- Stories are not supported.
- Shopping tags are not supported.
- Branded content tags are not supported.
- Filters are not supported.
- Multi-image posts are not supported.
- If the caption contains a hashtag, it should be HTML URL-encoded as %23 in the request.
- Publishing to IGTV is not supported.

## References

I will introduce you to references that are useful.

- **Introducing**: https://developers.facebook.com/blog/post/2021/01/26/introducing-instagram-content-publishing-api/
- **Test API**: https://developers.facebook.com/tools/explorer/
- **Content publishing**: https://developers.facebook.com/docs/instagram-api/guides/content-publishing/
- **Flow and Code example** (ReactJS), so useful to test in the client site, I extremely appreciate this article: https://medium.com/geekculture/how-to-publish-content-with-the-instagram-graph-api-806ec9c56588

## Summary

Instagram Graph API has a lot of limitations because It's released in few years recently. So I hope that It will be supported more in the future (multiple posts, get account_type,…) and you will have fun and clear in my article.

