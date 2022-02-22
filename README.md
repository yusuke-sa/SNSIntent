# SNSIntent
## 主要SNSへのIntent
```Kotlin
/* instagram */
private fun startInstagram() {
    val url = "http://instagram.com/"
    try {
        Intent(Intent.ACTION_VIEW).also {
            it.setPackage("com.instagram.android")
            it.data = Uri.parse(url)
            startActivity(it)
        }
    } catch (e: ActivityNotFoundException) {
        Timber.e("Error")
    }
}

/* YouTube */
private fun startYouTube() {
    val url = "https://www.youtube.com/feed/subscriptions"
    try {
        Intent(Intent.ACTION_VIEW).also {
            it.setPackage("com.google.android.youtube")
            it.data = Uri.parse(url)
            startActivity(it)
        }
    } catch (e: ActivityNotFoundException) {
        Timber.e("Error")
    }
}

/* LINE */
private fun startLine() {
    val url = "https://line.me/R/nv/chat"
    try {
        Intent(Intent.ACTION_VIEW).also {
            it.setPackage("jp.naver.line.android")
            it.data = Uri.parse(url)
            startActivity(it)
        }
    } catch (e: ActivityNotFoundException) {
        Timber.e("Error")
    }
}
```
## なんか作れないものか
