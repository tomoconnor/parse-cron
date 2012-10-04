### parse-cron - parse crontab syntax & determine next scheduled run

The goal of this gem is to parse a crontab timing specification and determine when the
job should be run. It is not a scheduler, it does not run the jobs.

----------------------------------------------------------------------------------

### Usage

#### Initialize parse-cron:
    parse_cron = CronParser.new("0 9,12,15 * * 2-4")
    => #<CronParser:0x007fa5e827d360 @source="0 9,12,15 * * 2-4">


#### Show next scheduled time:
    parse_cron.next "2012-10-02 15:01:00".to_datetime
    => 2012-10-03 09:00:00 +0000
