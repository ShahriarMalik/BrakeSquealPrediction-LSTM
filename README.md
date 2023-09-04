# Predicting Brake Squealing Events Using LSTM Models

## Description

This project aims to predict brake squealing events using Long Short-Term Memory (LSTM) models. It specifically focuses on the role of `Trigger2`, which indicates when contact is fully established between the brake pad and brake disc.

## Table of Contents

1. [Installation](#Installation)
2. [Usage](#Usage)
3. [Data Channels](#Data-Channels)
4. [Data](#Data)
5. [Contributing](#Contributing)
6. [License](#License)

## Installation

# Install dependencies
pip install -r requirements.txt


## Usage


# Example code to run the LSTM model
from lstm_model import predict_squealing
predict_squealing(input_file='data/input.csv')


## Data Channels
- `VitesseMoteur`: Rotational velocity of the disc (converted to Time Series).
- `T_ON`: Contact duration (converted to Time Series).
- `T_OFF`: Wait time between each contact (converted to Time Series).
- `FZ`: Force on the pin in normal direction.
- `FCT_BI_S`: Blade (pin's support) displacement (Foucault interior edge exit).
- `FCT_BI_E`: Blade (pin's support) displacement (Foucault interior edge entry).
- `FCT_BE_E`: Frontal force on the brake disc (converted to Time Series).
- Various `TC_*` channels: Temperatures in pin 2mm under the surface in contact.
- `DEP_D`: Normal displacement of the disc at a point.
- `Couple_Smoothed`: Torque of the contact.
- `FY_Smoothed`: Force on the pin in the tangential direction.
- `isSquealing`: 0/1 signal indicating squealing events.
- `EdissFY`: Energy dissipated by friction in the contact.
- `Trigger1`: Trigger when the table of the pin starts and stops moving.
- `Trigger2`: Trigger when the table of the pin is at its final position.

## Data

The dataset used in this project is confidential and cannot be shared publicly. However, the code for the implementation is available in this repository.

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request.

## License

This project is licensed under the MIT License. 
