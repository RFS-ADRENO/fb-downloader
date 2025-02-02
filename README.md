# fb-downloader v1.0.14

#### Downloads HD videos from Facebook

##### Developed By

[![N|Solid](https://blog.tcmhack.in/wp-content/uploads/2019/04/cropped-tcmhack-logo.png)](https://admin.tcmhack.in)

and

<strong style="font-size: 40px">[XaviaBot](https://github.com/XaviaTeam)</strong>

FB Downloader is a simple JavaScript package which provides a facility to download videos form Facebook in available quality

It is open source with a [public repository](https://github.com/RFS-ADRENO/fb-downloader.git) on GitHub.

## Installation

You can install this package via below command

```sh
npm i @xaviabot/fb-downloader
```

<hr />

## Example

```javascript
import getFBInfo from "@xaviabot/fb-downloader";

// OR

const getFBInfo = require("@xaviabot/fb-downloader");

getFBInfo("https://www.facebook.com/watch?v=272591278381388")
    .then((result) => console.log("Result:", result))
    .catch((error) => console.log("Error:", error));

// OR

async function printFBInfo() {
    try {
        const result = await getFBInfo(
            "https://www.facebook.com/watch?v=272591278381388"
        );
        console.log("Result:", result);
    } catch (error) {
        console.log("Error:", error);
    }
}

printFBInfo();
```

### Cookies and User-Agent (Optional)

```javascript
const cookies = "your-facebook-cookies";
const userAgent = "your-user-agent";

getFBInfo(
    "https://www.facebook.com/watch?v=272591278381388",
    cookies,
    userAgent
)
    .then((result) => console.log("Result:", result))
    .catch((error) => console.log("Error:", error));
```

### OUTPUT

```json
{
    "url": "https://www.facebook.com/watch?v=272591278381388",
    "sd": "https://video.fudr3-1.fna.fbcdn.net/v/t42.1790-2/275801506_172276165130059_885167449675909210_n.mp4?_nc_cat=104&ccb=1-5&_nc_sid=985c63&efg=eyJybHIiOjMxMSwicmxhIjo1MTIsInZlbmNvZGVfdGFnIjoic3ZlX3NkIn0%3D&_nc_ohc=APPv2eMIya0AX8rCmCw&rl=311&vabr=173&_nc_ht=video.fudr3-1.fna&oh=00_AT9_UUFN4fyEEJCeNhCy6__4rLWt6mKo49KRBN4QlVyvQA&oe=625119EC",
    "hd": "https://scontent.fudr3-1.fna.fbcdn.net/v/t66.36240-6/120162803_2190017344494785_2810101870338104985_n.mp4?_nc_cat=108&ccb=1-5&_nc_sid=985c63&efg=eyJybHIiOjE1MDAsInJsYSI6MTAyNCwidmVuY29kZV90YWciOiJvZXBfaGQifQ%3D%3D&_nc_ohc=lnorxsFd2IQAX_SqjXK&rl=1500&vabr=239&_nc_ht=scontent.fudr3-1.fna&oh=00_AT85Uldp0pZ9FpbyVgfvVIyF0RgBQlrHcwEmtmKZNSERWQ&oe=6256D07D",
    "title": "&#x2022; Date Gone Wrong &#x1f606;&#x1f606;&#x1f926;&#x200d;&#x2642;&#xfe0f;",
    "thumbnail": "https://scontent.fudr3-1.fna.fbcdn.net/v/t15.5256-10/275173684_1165104900988683_8395349523361992483_n.jpg?stp=dst-jpg_p960x960&_nc_cat=101&ccb=1-5&_nc_sid=df419e&_nc_ohc=2x6n-Qlr4fsAX_q11Ey&_nc_ht=scontent.fudr3-1.fna&oh=00_AT_u8NDG6_FTGzUGFaj27LSgRcTQpNTaR_lZcNLv329dzg&oe=62559E88"
}
```
