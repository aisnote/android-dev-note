# 4. Network layer

RestFul API used below component:
> com.squareup.retrofit2


It's pretty easily to create the interface and build the instance like:

```kotlin
val retrofit = Retrofit.Builder()
        .baseUrl(inPutBaseUrl.trim())
        .addConverterFactory(ScalarsConverterFactory.create())
        //.addConverterFactory(MoshiConverterFactory.create())
        .addConverterFactory(MoshiConverterFactory.create(getMoshi()))
        // The call adapter handles threads
        .addCallAdapterFactory(CoroutineCallAdapterFactory())
        .callbackExecutor(mExecutorService)
        .client(client)
        .build()

return retrofit.create(LomoService::class.java)

```

And the **LomoService** is a interface class like below:

```Kotlin
interface LomoService {
    @Headers("Accept: text/plain")
    @GET("system")
    fun getSystemInfo(): Deferred<Response<String>>
}
```