# slapcam

Slap. Hit slap, get video.

```
PORT=1234 TIMEOUT=2 TMP_DIR=./tmp SEGMENT_DIR=./src SEGMENT_FILE_REGEX="segment[0-9]+.mp4" AWS_ACCESS_KEY_ID=_key_id_ AWS_SECRET_ACCESS_KEY=_secret_ BUCKET_NAME=slapcam BUCKET_REGION=us-east-1 SLACK_CHANNEL=slapcam SLACK_TOKEN=_token_here_ ./slapcam
```

```
GET http://127.0.0.1:1234
2015/09/14 12:32:25 Starting slap wait
2015/09/14 12:32:27 Initiating slap
2015/09/14 12:32:27 Running command[ffmpeg -f concat -i ./tmp/slap_wSzKmr/filelist.txt -c copy ./tmp/slap_wSzKmr/joined.mp4]
2015/09/14 12:32:27 Finished joining file
2015/09/14 12:32:27 Starting upload to s3 at 1442190747_slap_wSzKmr.mp4
2015/09/14 12:32:44 Upload complete
2015/09/14 12:32:44 Notifying Slack
2015/09/14 12:32:47 Cleaning up ./tmp/slap_wSzKmr
```
