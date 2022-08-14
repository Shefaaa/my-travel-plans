
# Suitable Meeting Times Service
API Service that return suggestion of suitable meeting times for the meeeting participants.

<h3>Technologies Used</h3>
<ul>
  <li><a href="https://laravel.com/docs/8.x/readme" target="_blank">Laravel 8 </a> Framework</li>
  <li><a href="https://www.php.net/" target="_blank">PHP7.4 </a></li>
  <li><a href="https://getcomposer.org/" target="_blank">Composer </a>- dependency management tool</li>
</ul>


<h3>System install and setup</h3>
<ul>
  <li>Download and install PHP</li>
  <li>Download and install Composer</li>
  <li>Download and install LARAVEL</li>
  <li>Download this Project</li>
  <li>Go to the folder application using cd command on your cmd or terminal.</li>
  <li>Run <code>Composer install</code> command </li>
  <li>Run <code>php artisan key:generate </code></li>
  <li>Run <code>php artisan serve </code>to start up the project</li>
</ul>

<strong>Call API:</strong>
<ul>
 <li>API URL <code>http://127.0.0.1:8000/api/v1/available-times</code></li>
  <li>API Method <code>POST</code></li>
  <li>API Parameters <ul>
    <li>employee_ids: required array of numeric value</li>
    <li>meeting_length: required int value</li>
    <li>meeting_length: required int value</li>
    <li>earlist_meeting_date_time: required datetime <code>"2015-01-02 08:00:00 AM"</code></li>
    <li>latest_meeting_date_time: required datetime <code>"2015-01-02 05:00:00 PM"</code></li>
    <li>office_hours_from <code>"08:00"</code></li>
    <li>office_hours_to <code>"05:00"</code></li>
    </ul></li>
  <li>API Request Body example <code>{
    "employee_ids": [
                       57646786307395936680161735716561753784,
                       259939411636051033617118653993975778241
                   ],
    "meeting_length":45,
    "earlist_meeting_date_time":"2015-01-02 08:00:00 AM",
    "latest_meeting_date_time":"2015-01-03 05:00:00 PM",
    "office_hours_from": "08:00",
    "office_hours_to": "17:00"
}</code></li>
  <li>API Response json array of available times and suggestion with meeting times intervals</br>
  Response body example </br>
  <code>[
   {
        "date": "2015-01-02",
        "available_time": "2015-01-02 09:30 - 2015-01-02 17:00",
        "suggestion_suitable_times": [
            "09:30-10:15",
            "10:30-11:15",
            "11:30-12:15",
            "12:30-13:15",
            "13:30-14:15",
            "14:30-15:15",
            "15:30-16:15"
        ]
    }
]</code></li>
</ul>  
