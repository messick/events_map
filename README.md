# Hillary Map
This project displays Hillary events on a Google Map, using the Google Maps JavaScript API and the Google Maps Geocoding API.

## Configuration
You can configure the settings using the `config` object in the index.html file. Below are the possible settings:

- `api_key`: String. Set this to your API key for the Google Maps and Google Maps Geocoding APIs
- `categorize_by_event_type`: Boolean; defaults to `true`. Set this to `true` if you want events to be separated into layers by event type (i.e. phone bank, party, voter registration, etc.).
- `all_events_icon`: String. Set this to the URL of the pin icon to use for events if `categorize_by_event_type` is set to `false`.
- `search_descriptions`: Boolean; defaults to `true`. Set this to `true` if you want the events to be classified into types based on the keywords that appear in the event descriptions, not just the keywords in the event titles. (Note that event descriptions will only be used to classify event type in the scenario in which no part of the event title matches any of the event type keywords.)
- `default_to_user_location`: Boolean; defaults to `true`. Set this to `true` if you want the map to automatically try to find events near the user's location, unless the user has specifically searched for a location.
- `date_filter`: Object; defaults to:

    'date_filter': {
      'start_date': new Date().toISOString(),
      'end_date': new Date('2017-12-31').toISOString()
    }

 This is an object containing two keys with string values. The first key is `start_date` and the second is `end_date`. Together these two keys limit the date range of events that will display on the map.
