# PYRO Thermal Intelligence

AI-powered monitoring and classification of satellite-detected thermal hotspots using NASA FIRMS, geospatial data, and machine learning.

## Project Overview

PYRO Thermal Intelligence is a geospatial monitoring platform designed to analyze satellite-detected thermal hotspots and provide geographical context for understanding potential fire events and persistent heat sources.

The system combines satellite observations, open geographic data, and machine learning to support hotspot exploration and experimental classification.

## Problem Statement

Thermal hotspots detected by satellites can originate from different sources, including agricultural burning, natural fires, industrial activity, mining, and other heat-producing activities.

Identifying the possible source of a hotspot requires more than its location alone. PYRO aims to combine thermal observations with geographic context to support more informed analysis.

## Key Features

- Satellite thermal hotspot data visualization
- Interactive geographic mapping
- Hotspot classification using a machine learning prototype
- Geographic context using open geospatial data
- Land-cover-based feature enrichment
- Date-based hotspot exploration

## Technology Stack

### Backend
- Python
- FastAPI
- SQLAlchemy

### Frontend
- React
- Leaflet

### Database
- PostgreSQL

### Machine Learning
- Scikit-learn
- Random Forest classifier

### Data Sources
- NASA FIRMS satellite thermal anomaly data
- OpenStreetMap geographic data
- ESA WorldCover land-cover data

## System Architecture

1. Satellite thermal hotspot observations are retrieved from NASA FIRMS.
2. Geographic and land-cover information is used to enrich hotspot records where available.
3. Relevant features are processed for machine learning.
4. The classification model produces an experimental hotspot category.
5. The backend provides hotspot data through API endpoints.
6. The frontend displays hotspot locations and related information on an interactive map.

## Hotspot Categories

The current demonstration focuses on the following categories:

- Agricultural Fire
- Forest / Natural Fire
- Other / Unknown

Additional categories, such as industrial and mining sources, may be introduced when sufficient reliable labelled training data becomes available.

## Data Sources

- NASA FIRMS: https://firms.modaps.eosdis.nasa.gov/
- OpenStreetMap: https://www.openstreetmap.org/
- ESA WorldCover: https://worldcover.esa.int/

Users should follow the respective data providers' terms, attribution requirements, and usage policies.

## Project Status

PYRO Thermal Intelligence is an evolving prototype.

The availability and accuracy of geographic enrichment depend on external data services. Classification performance depends on the quality, quantity, and representativeness of labelled training data.

Experimental classifications must not be treated as confirmed fire alerts or as a replacement for official emergency information.

## Security

- Store API keys and credentials in environment variables.
- Do not commit `.env` files or private credentials.
- Configure environment variables locally before running the backend.
- Follow the usage limits and policies of external data providers.

## Future Improvements

- Expand the labelled training dataset.
- Improve classification accuracy and evaluation.
- Add historical hotspot analysis.
- Improve geographic enrichment reliability.
- Introduce model evaluation metrics and confidence reporting.
- Support additional hotspot categories when sufficient data is available.
- Improve deployment, monitoring, and documentation.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
