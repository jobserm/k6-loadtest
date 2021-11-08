## Load test Jobserm
* Powered by [grafana/k6](https://github.com/grafana/k6)

## Test logic
* Slowly increase virtual user (VU) from 1-50 in 1min
* Then Hold 50 users for 3 mins
* Then slowly decrease 50 to 0 users in 30secs
* Backend request durations must be `p(95)<800ms`
* Frontend request durations  must be `p(95)<250`

### Test
`docker run -i loadimpact/k6 run - < k6-test.js`
