# learn_linux_by_doing

#removing file test-1
rm test-1

#renaming file
mv top5-highest-temperatures.csv top-5-highest-temperatures.csv

#top 5 highest recorded temperatures
sort -t, -k2 -nr satelite_temperature_data.csv | head -n 5 > ../analyzed/top-5-highest-temparatures.csv

#top 5 lowest recorded temperatures
sort -t, -k2 -n satelite_temperature_data.csv | head -n 5 > ../analyzed/top-5-lowest-temparatures.csv

#heat data for my country
grep Rwanda satelite_temperature_data.csv > ../analyzed/country-heat_data.csv
