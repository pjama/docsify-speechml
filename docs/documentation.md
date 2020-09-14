# SpeechML Documentation

?> To get started and issue requests to the SpeechML API, sign up<br/> for an API key at the [Sellbit Marketplace](https://apis.sellbit.io/apis/philip-jama).

## Endpoints

### POST /api/v1/predict
<span class="endpoint"><span class="api-method">POST</span> /api/v1/predict</span>

> sdjfhskdj

#### HEADERS

* `Authorization`: Supply your API_KEY

#### PARAMS

* `file`: An audio file satisfying the following format:
  * *16bit 44khz wav?*
  * *max 600 seconds?*

#### REQUEST

```shell
# Retrieve example audio file
curl -fsSLO https://api.philipjama.com/samples/audio-segment.wav

# Segment and identify speakers
curl -X POST \
  -H "Authorization: Bearer API_KEY" \
  -F file=@audio-segment.wav \
  https://api.philipjama.com/predict
```

#### RESPONSE

```json
[0,0,2,2,2,1,1,1,0,1,2,0,1,1,1,2,1,-1,-1,0]
```

----

### GET /api/v1/health
<span class="endpoint"><span class="api-method">GET</span> /api/v1/health</span>


#### HEADERS

* none

#### PARAMS

* none


#### REQUEST

```shell
# Segment and identify speakers
curl -X GET \
  -H "Authorization: Bearer API_KEY" \
  https://api.philipjama.com/health
```

#### RESPONSE

```json
{ "healthy": "true" }
```
