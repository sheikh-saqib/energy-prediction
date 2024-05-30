Forecasting energy availability from renewable sources:

Description -

The goal of this project was to determine whether or not a service could be implemented inside the structure of our business. The goal of this service is to give free energy to local customers when there is excess renewable energy available, especially in light of rising energy costs. An investigation into historical energy records from 2000 to the present was carried out in order to evaluate this. The main objective was to create a predictive system that could accurately predict the conditions of excess renewable energy at least 24 hours in advance.

In the first phase, careful consideration was given to thoroughly examining the dataset. To guarantee data integrity and coherence, extensive data inspection, cleaning, and preprocessing were required. In addition, outside studies were conducted to determine appropriate cutoff points for excess energy. This required gathering data from reliable.

In this phase, the focus was on creating a solid base for future modelling projects. The foundation for the creation of precise predictive models in later project stages was laid by carefully analysing the dataset and researching about suitable thresholds.

Dataset -
File Name: brighton_001.csv to brighton_128.csv
Source: Moodle

Instructions -

Running the Code:

1. Download and extract the project repository from the zip folder.
2. Ensure that you have Python installed on your system
3. Open the Jupyter Notebook EnergyCompany.ipynb.
4. Change the directory variable according to the folder structure of the machine
5. Follow the instructions and code comments in the notebook to execute the code step by step.

Assumptions -

1.  Assumptions for wind energy calculation :
    a) The assumed number of windmills is 116 in Brighton (Reference - https://www.rampionoffshore.com/#:~:text=The%20wind%20farm%20comprises%20116,coast%20in%20the%20English% 20Channel.)

    b) The dimensions of the windmill i.e., radius of the turbine, swept area of the turbine, and air density are assumed to be 12m, 452.4 m^2, and 1.225 kg/m^3 respectively.
    (Reference - https://www.e-education.psu.edu/emsc297/node/649#:~:text=Thus%2C%20the%20power%20available%20to,variable%20input%20is%20wind%20speed.)

2.  Assumptions for solar energy calculation :
    a) The assumed number of solar panels is 369 in Brighton (Reference - https://www.brighton-hove.gov.uk/news/2023/hundreds-council-homes-switch-solar-power.)

    b) The dimensions of the solar panels i.e., surface area and efficiency are assumed to be 20m^2 and 20% respectively.
    (Reference - https://www.saurenergy.com/solar-energy-blog/here-is-how-you-can-calculate-the-annual-solar-energy-output-of-a-photovoltaic-system)

3.  Research and Assumptions for Electicity Threshold:

    a) The average value of electricity used per year in Brighton is 3332kWh from 2017 to 2022 (Reference: https://lginform.local.gov.uk/reports/lgastandard?mod-metric=3801&mod-area=E06000043&mod-group=AllUnitaryLaInCountry_England&mod-type=namedComparisonGroup)

        i-e 3332/365 = 9.12kWh per day (Verified by Reference - https://www.utilitybidder.co.uk/compare-business-energy/what-is-the-average-household-energy-usage/#:~:text=What%20is%20the%20average%20electricity,factors%20that%20affect%20this%20figure.)

    b) The above calculations and sources leads us to the assumption that the Hourly Consumption ≈ 0.38kWh in Brighton (i-e 9.12/24 kWh)

    c) Total Number of Houses in Brighton 121,401 which gives us 46.13238 mWH consumption per hour. (Reference - https://www.brighton-hove.gov.uk/sites/default/files/2024-03/census-2021-briefing-city-profile_Muna%20Mohamed.pdf)

    d) Consumer behaviour factor: 2

    d) Threshold Assumed ≈  95 mWH consumption per hour

4. Cost of Electricity per mWH = £50 (Reference - https://businessenergycomparison.com/business-electricity/price-of-1-mwh-of-electricity-in-2023/#:~:text=Price%20Of%201%20MWh%20Electricity,focus%20on%20wholesale%20electricity%20prices.