Influential Billboard Slot Selection
Algorithms: Bi-criteria Approximation & Randomized Profit Maximization
This repository contains the implementation of two algorithms for solving the Influential Billboard Slot Selection problem:
Bi-criteria Approximation Algorithm – to select the set of slots which will satisfy the demand of all the advertisers or products.
Randomized Profit Maximization – to maximize influence across users for multiple advertisers or products, considering both demand and Budget constraints.
The objective is to select an optimal set of billboard slots such that:
The influence demands of advertisers are satisfied.
The selection respects the cost/budget constraints.
Influence is distributed efficiently among the targeted users.

📁 Files Overview
File	                                        Description
BB_NYC.csv                     -          Billboard slot data (ID and cost).
new_ub.csv                     -          User influence data. Each user is associated with a dictionary of billboard IDs and influence values.
advertiser_1.csv               -          Demand values (for Bi-criteria Algorithm).
advertiser_10.csv	       -          Demand and payment values (for Randomized Profit Maximization).
Product_user_map_NYC.csv       -          Mapping of products to interested user IDs.
📊 Dataset Description 
1. BB_NYC.csv

Contains billboard data with the following columns:

    B_index – Unique identifier of the billboard.

    Cost – Cost to select this billboard slot.

2. new_ub.csv

Contains influence data for each user:

    UserId – Unique identifier of the user.

    Influenced Billboards – Dictionary in string form mapping billboard_id → influence_value.


3. advertiser_1.csv

Used for :

    Demand – Required influence for each advertiser.

    Payment – Budget limit for each advertiser.

5. Product_user_map.csv

Maps venue categories to interested users:

    Venue Category – Product/advertiser category.

    User IDs – Comma-separated list of interested user IDs.

🔧 Dependencies

Ensure the following Python packages are installed:

pip install numpy
pip install pandas

Other modules used:

    csv (standard)

    ast or eval

    random, math, time (standard)

🚀 How to Run
1. Bi-criteria Approximation Algorithm

Input Files Required:

    BB_NYC.csv

    new_ub.csv

    advertiser.csv

Steps:

    Ensure all CSV files are in the same directory as the script.

    Run the Python file:

python bi_criteria_approximation.py

This will:

    Load billboard and influence data.

    Select slots such that the influence demands are met.

    Output selected billboard indices and timing.

2. Randomized Profit Maximization Algorithm

Input Files Required:

    BB_NYC.csv

    new_ub.csv

    Product_user_map_NYC.csv

    advertiser.csv

Steps:

    Ensure all CSV files are present.

    Run the Python file:

python randomized_profit_maximization.py

This will:

    Load multiple advertisers' influence demands and budgets.

    Map users to products.

    Select billboard slots to maximize total influence under advertiser constraints.


    If you are using our datasets and codes then please cite our works.


