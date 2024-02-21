[https://apify.com/epctex/tiktok-comment-scraper](https://apify.com/epctex/tiktok-comment-scraper?fpr=yhdrb)

# Actor - Tiktok Comments Scraper

## Tiktok Comments scraper

Since Tiktok doesn't provide a good and free API, this actor should help you to retrieve data from it.

The Tiktok Comments data scraper supports the following features:

- Unlock Tiktok Insights - Gain comprehensive insights from Tiktok videos with ease.

- Efficient Data Retrieval - Extract comments, user details, and music information using minimal input parameters.

- Overcome API Limitations - Sidestep Tiktok's API restrictions and access valuable data effortlessly.

- In-Depth Comment Details - Gather author info, timestamps, likes, and more for each comment.

- Streamlined Scraping - Scrape multiple videos seamlessly, manage pagination, and set proxy configurations effortlessly.


## Bugs, fixes, updates and changelog

This scraper is under active development. If you have any feature requests you can create an issue from [here](https://github.com/epctex/tiktok-comments-scraper/issues).

## Input Parameters

The input of this scraper should be JSON containing the list of pages on Tiktok Comments that should be visited. Possible fields are:

- `startUrls`: (Required) (Array) List of Tiktok video URLs. You should only provide the URLs of videos.

- `maxItems`: (Optional) (Number) You can limit scraped comments. This should be useful when you search through the videos where there are a lot of comments.

- `endPage`: (Optional) (Number) The end page limitation for the comments. You can limit the number of pages you want to retrieve the comments from. The `endPage` effects each of the video URLs individually.

- `proxy`: (Required) (Proxy Object) Proxy configuration.

This solution requires the use of **Proxy servers**, either your own proxy servers or you can use [Apify Proxy](https://www.apify.com/docs/proxy).

### Compute Unit Consumption

The actor optimized to run blazing fast and scrape many as listings as possible. Therefore, it forefronts all listing detail requests. If actor doesn't block very often it'll scrape 100 listings in 1 minute with ~0.03-0.05 compute units.

### Tiktok Comments Scraper Input example

```json
{
  "startUrls": [
    "https://www.tiktok.com/@deborahyowa/video/7173615947603922181?is_copy_url=1&is_from_webapp=v1",
    "https://www.tiktok.com/@argenby/video/7171782248281165058?is_copy_url=1&is_from_webapp=v1",
    "https://www.tiktok.com/@cznburak/video/7161858444830461190?is_copy_url=1&is_from_webapp=v1"
  ],
  "customMapFunction": "(object) => { return {...object} }",
  "maxItems": 200,
  "endPage":1,
  "proxy": {
    "useApifyProxy": true
  }
}
```

## During the Run

During the run, the actor will output messages letting you know what is going on. Each message always contains a short label specifying which page from the provided list is currently specified.
When items are loaded from the page, you should see a message about this event with a loaded item count and total item count for each page.

If you provide incorrect input to the actor, it will immediately stop with failure state and output an explanation of what is wrong.

## Tiktok Comments Export

During the run, the actor stores results into a dataset. Each item is a separate item in the dataset.

You can manage the results in any languague (Python, PHP, Node JS/NPM). See the FAQ or <a href="https://www.apify.com/docs/api" target="blank">our API reference</a> to learn more about getting results from this Tiktok Comments actor.

## Other Tiktok Scrapers

If you need different functionalities or all at once, we have solutions for each of them. You can check;

- [Tiktok Hashtag Scraper](https://apify.com/epctex/tiktok-hashtag-scraper)
- [Tiktok Search Scraper](https://apify.com/epctex/tiktok-search-scraper)
- [Tiktok Video Scraper](https://apify.com/epctex/tiktok-video-scraper)

## Scraped Tiktok Comments Properties

The structure of each comment in Tiktok Comments looks like this:

### Comment Detail

```json
{
	"author_pin": false,
	"aweme_id": "7171782248281165058",
	"cid": "7171787686901465902",
	"collect_stat": 0,
	"comment_language": "en",
	"create_time": 1669811972,
	"digg_count": 42526,
	"image_list": null,
	"is_author_digged": false,
	"label_list": null,
	"no_show": false,
	"reply_comment": null,
	"reply_comment_total": 268,
	"reply_id": "0",
	"reply_to_reply_id": "0",
	"share_info": {
		"acl": {
			"code": 1,
			"extra": "{\"item_share_acl\":\"empty item value\"}"
		},
		"desc": "alexのコメント: This is the actual meaning of sigma",
		"title": "Sigma must respect everyone… @ayazkyzz @aman4ek ",
		"url": "https://m.tiktok.com/v/7171782248281165058.html?_d=e9hlia25ee8a8f&comment_author_id=7105545617678664750&preview_pb=0&share_comment_id=7171787686901465902&share_item_id=7171782248281165058&sharer_language=ja-JP&source=h5_m&u_code=0"
	},
	"status": 1,
	"stick_position": 0,
	"text": "This is the actual meaning of sigma",
	"text_extra": [],
	"trans_btn_style": 1,
	"user": {
		"account_labels": null,
		"ad_cover_url": null,
		"advance_feature_item_order": null,
		"advanced_feature_info": null,
		"avatar_thumb": {
			"uri": "tos-useast5-avt-0068-tx/aa12e4c1250f1774a6bc299bb87c8b58",
			"url_list": [
				"https://p16-sign.tiktokcdn-us.com/tos-useast5-avt-0068-tx/aa12e4c1250f1774a6bc299bb87c8b58~c5_100x100.jpg?x-expires=1692957600&x-signature=xdcSGNgBwc0GhX21ZpOcGX8WOko%3D",
				"https://p19-sign.tiktokcdn-us.com/tos-useast5-avt-0068-tx/aa12e4c1250f1774a6bc299bb87c8b58~c5_100x100.jpg?x-expires=1692957600&x-signature=vKQKN6kPwOxYSNnk5AZr1eziXwo%3D",
				"https://p16-sign.tiktokcdn-us.com/tos-useast5-avt-0068-tx/aa12e4c1250f1774a6bc299bb87c8b58~c5_100x100.jpeg?x-expires=1692957600&x-signature=8j%2FBXd3%2FFQi%2BJtCPtcv62IV3Feo%3D"
			]
		},
		"bold_fields": null,
		"can_message_follow_status_list": null,
		"can_set_geofencing": null,
		"cha_list": null,
		"cover_url": null,
		"custom_verify": "",
		"enterprise_verify_reason": "",
		"events": null,
		"followers_detail": null,
		"geofencing": null,
		"homepage_bottom_toast": null,
		"item_list": null,
		"mutual_relation_avatars": null,
		"need_points": null,
		"nickname": "alex",
		"platform_sync_info": null,
		"relative_users": null,
		"search_highlight": null,
		"sec_uid": "MS4wLjABAAAA7vpB3z_9t3fRfuaZC8zkuo7v_SI_Z2DZJ9WxY4IzPrZJJ0TZFBiYFbgk3iglgOPC",
		"shield_edit_field_info": null,
		"type_label": null,
		"uid": "7105545617678664750",
		"unique_id": "error_7690",
		"user_profile_guide": null,
		"user_tags": null,
		"white_cover_url": null
	},
	"user_buried": false,
	"user_digged": 0
}
```

## Contact
Please visit us through [epctex.com](https://epctex.com) to see all the products that is available for you. If you are looking for any custom integration or so, please reach out to us through the chat box in [epctex.com](https://epctex.com). In need of support? [devops@epctex.com](mailto:devops@epctex.com) is at your service.
