# outsystems-integration
Using APS inside an outsystems application

## Testing the app

1. You need to create an [APS](https://aps.autodesk.com/) app - follow [Create an account](https://tutorials.autodesk.io/#create-an-account)
2. As pointed out [here](https://aps.autodesk.com/en/docs/oauth/v2/reference/http/gettoken-POST/#section-3-client-credentials-grant-type) for a **2-legged access token** we'll need to combine the **client id** and **client secret** and base64 encode it: `${Base64(<client_id>:<client_secret>)}`  \
The simplest is to use a utility like [base64encode.org](https://www.base64encode.org/) to do that. Paste the value you got in the `Base64ClientIdClientSecret` Site Property  \
E.g. if my **client id** is `abcd` and **client secret** is `efg` then I need to base64 encode `abcd:efg` and I end up with `YWJjZDplZmc=`. \
![](/credentials.png)

3. Create a bucket for your [APS](https://aps.autodesk.com/) app using either this [utility](https://oss-manager.autodesk.io/) or the [Visual Studio Code extension](https://aps.autodesk.com/blog/forge-visual-studio-code) and paste the name of the bucket in the `BucketName` Site Property \
![](/bucket-name.png)

See [blog post]() for more details.