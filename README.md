# LatLongToTimezone
LatLongToTimezone Conversion Library for PHP/Codeigniter/Bonfire

Latitude / Longitude Conversion To Timezone within 35 miles accuracy, without using external database

Also includes methods for using Json files Version 0.1 Still WIP

##Usage

Add to your library folder. Call from your controller (also add a view for output). Example controller (Bonfire) not using Json files:

    public function testconvert($lat, $lng)
    {
        $this->load->library('LatLongToTimezone');
        $converter = $this->latlongtotimezone->getInstance();
        $s = $converter->convert($lat, $lng);
        Template::set("lat", $lat);
        Template::set("lng", $lng);
        Template::set("tz", $s);
        Template::render();
    }

##Extras (not required)

1) Also includes other methods for parsing JSON data 2) JSON timezone shape data for U.S. and Canada 3) Zipcode data with coordinates (from GeoNames.org Postal Code files)

##Coming Soon

convert zip to timezone
how to use json files for greater accuracy, if needed
a Bonfire module
