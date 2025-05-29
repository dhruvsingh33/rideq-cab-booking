# RideQ - Modern Ride-Hailing App

A modern ride-hailing application built with Flutter and Supabase, featuring real-time location tracking, fare calculation, and driver-passenger matching.

## Features

- Real-time location tracking
- Interactive Google Maps integration
- Fare calculation based on distance
- Driver-passenger matching system
- Real-time ride status updates
- Anonymous authentication
- Clean and modern UI

## Tech Stack

- **Frontend**: Flutter
- **Backend**: Supabase
- **Maps**: Google Maps API
- **Real-time Updates**: Supabase Realtime
- **Authentication**: Supabase Auth

## Quick Start

1. Clone the repository:
```bash
git clone https://github.com/dhruvsingh33/rideq-cab-booking-app.git
cd rideq-cab-booking-app
```

2. Install dependencies:
```bash
cd flutter
flutter pub get
```

3. Run the app:
```bash
flutter run
```

## Setup Instructions

### 1. Supabase Setup

The project is already configured with a Supabase backend. The credentials are set up in the main.dart file.

### 2. Google Maps Setup

1. Get a Google Maps API key from the [Google Cloud Console](https://console.cloud.google.com/)
2. Enable the following APIs:
   - Maps SDK for Android
   - Maps SDK for iOS
   - Directions API
   - Places API

3. Update the API key in:
   - Android: `flutter/android/app/src/main/AndroidManifest.xml`
   - iOS: `flutter/ios/Runner/AppDelegate.swift`

### 3. Driver Simulation

To test the app with a simulated driver, run the following SQL query in your Supabase database:

```sql
insert into public.drivers (id, model, number, location, is_available)
    values
    ('a040ae05-3928-4cbf-8577-bbad6125c3fe', 'Ford Focus', 'GHI-789', ST_GeographyFromText('SRID=4326;POINT(-122.0854 37.4223983)'), true);
```

## Development

This project uses:
- Flutter for the mobile application
- Supabase for backend services
- Google Maps for location services
- Real-time updates for live tracking

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
