# Mapping Non-English Language Movie Theaters and Speakers

Since moving to New Jersey to go to Rutgers, I have been impressed by the cultural diversity present here.  The many cultures and nationalities comprising our community are reflected in the languages spoken here, and one of the reflections of the languages spoken here is in the languages movies are shown in in theaters, a diverse offering apparent when you check the movie listings.  To explore this, I collected data on the languages of movies being shown across the state and in the adjacent metropolitan areas via web scraping of the movie listings on <a href="https://www.cinemaclock.com/"> CinemaClock.com </a> for the week of 04/22/24.

I then mapped the theaters along with two types data related to language diversity from the US Census Bureau: the percentage of the population that's foreign-born (from Census table B16005), available by census tract, and the percentage of the population speaking specific individual languages (from table B16001 via Social Explorer with assistance from  Professor Payne), available by PUMA (Public Use Microdata Area, areas containing roughly 100,000 people which may be the size of a county or of a neighborhood in an urban area).  Data cleaning was needed on the theaters side following the web scraping process; less so for the census data, though a lot of steps were needed to bring all the components together. 

The first map shows percentage foreign-born by census tract across the state and Metro areas as a choropleth map, with movie theaters showing non-English movies indicated by blue dots of varying size which is based on the number of non-English movies being shown by the theater at the time of data colection. Nine of the top eleven theaters by number of non-English films being shown are labeled on the map.  Several of these top theaters are in the immediate vicinity of New Brunswick.

![Alt text](NJ Theaters Langs 01B.png "NJ Theaters Langs")

# Interactive Map:

For an interactive map showing detailed info for each theater, please download the html file from Google drive here and open it on your PC:
<a href="https://drive.google.com/file/d/1ZBO3bXPVjO3kZ4ZLvsIY_1FLbu2CY2E-/view?usp=drive_link"> Google drive link- final version </a>

The interactive map contains markers for 256 theaters (including 46 closed theaters), with a backdrop choropleth map of Percent Foreign Born by census tract. Theaters are classified as showing more than one, or one or fewer, non-English movies. Popup & tooltip (mouse-over) info for each theater includes (along with Theater Name and Address) the number of total and non-English language movies being shown at the theater and the list of languages with movies being shown for the week of 4/22/24.    Additionally, the popup for each theater includes the "PUMA Exceptional language": the language with the highest percentage of speakers relative to the US overall percentage of speakers, for the PUMA the theater is located in, along with the % comparison.  This info was calculated for each PUMA via Excel and then added to the theaters by spatial join.

For an earlier version of the interactive map, click here:
<a href="https://nclvt73.github.io/Command_line_GIS/Theaters_langs_folium_01.html"> Github link- initial version. </a>

# Individual Language Maps:

I first created three sets of small multiple maps of selected language groupings; these are followed by full-sized maps for each language.  Each of the maps shows the percentage of the population speaking the given language, by PUMA (Public Use Microdata Area), as of 2021, with lighter green & yellow indicating a higher concentration.  I used a common set of bins across all 12 maps to allow comparison.  The yellow dots are movie theaters showing at least one film in the given language the week of 04/22/24.

For the 12 languages shown here, I chose a mix of languages that are among the most commonly spoken in New Jersey (such as Spanish &  Chinese), and languages that movies are commonly shown in, like Japanese and French.  Some, like Hindi and Korean fit both of these profiles.  Malayalam stands out as being one of the most popular languages for movies to be shown in despite a relatively less substantial portion of the population speaking it.  Gujarati, on the other hand, has a bigger population while only one movie is being shown in it (in Manhattan).  Spanish stands out for the degree to which its population dwarfs the other languages, yet only a few movies are being shown in it.  Japanese is the opposite case, with a huge number of movie showings and a small population (testament to the popularity of Japanese movies such as anime among non speakers). Portuguese and Tagalog are both fairly commonly spoken (in the Top 10), yet have no movie showings.  Chinese, the third most commonly spoken language after English & Spanish, has just a few movie showings.  The Top 15 languages from both sides are below.

![Alt text](Langs compare.JPG "Languages")


![Alt text](Indian_Small.JPG "Indian small")

![Alt text](Asian_Small.JPG "Asian small")

![Alt text](Romance_Small.JPG "Romance small")

#

![Alt text](Theaters_Hindi.png "Hindi map")

![Alt text](Theaters_Malayalam.png "Malayalam map")

![Alt text](Theaters_Gujarati.png "Gujarati map")

![Alt text](Theaters_Telugu.png "Telugu map")

![Alt text](Theaters_Japanese.png "Japanese map")

![Alt text](Theaters_Korean.png "Korean map")

![Alt text](Theaters_Chinese.png "Chinese map")

![Alt text](Theaters_Tagalog.png "Tagalog map")

![Alt text](Theaters_Spanish.png "Spanish map")

![Alt text](Theaters_French.png "French map")

![Alt text](Theaters_Italian.png "Italian map")

![Alt text](Theaters_Portuguese.png "Portuguese map")

This project was produced by Nathaniel Lange as part of the course Command-line GIS with Professor Will Payne at the Bloustein School of Planning and Public Policy, Spring 2024 semester.


