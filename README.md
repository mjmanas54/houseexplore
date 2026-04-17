# HouseExplore 🏠

A Django-based web application for exploring, listing, and managing real estate properties. HouseExplore connects property sellers with potential buyers through an intuitive web interface.

## Features

### For Property Seekers
- **Search Properties**: Search houses by city and location
- **Browse Listings**: View detailed property information with images
- **Contact Dealers**: Direct contact form to reach property sellers via email
- **Real-time Chat**: Built-in messaging system to communicate with sellers

### For Property Sellers
- **User Authentication**: Secure signup/login system
- **Add Listings**: Create detailed property listings with:
  - Property images (up to 3 photos)
  - Pricing and area details
  - BHK configuration
  - Amenities (CCTV, power backup, lifts, etc.)
- **Manage Listings**: View and delete your property listings
- **Dealer Profile**: Automatic dealer profile creation

### Key Functionalities
- 🔍 City and location-based property search
- 📧 Automated email notifications for dealer-customer connections
- 💬 Real-time chat between buyers and sellers
- 🏢 Property amenity tracking (CCTV, garage, lifts, etc.)
- 📱 Responsive web interface

## Tech Stack

- **Backend**: Django 5.0.6
- **Database**: SQLite (default), MySQL support available
- **Frontend**: HTML, CSS, JavaScript
- **Key Libraries**:
  - Pillow (Image handling)
  - BeautifulSoup4 (Web scraping)
  - Matplotlib (Data visualization)
  - NumPy & SciPy (Data processing)

## Installation

### Prerequisites
- Python 3.8+
- pip

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/mjmanas54/houseexplore.git
   cd houseexplore
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run migrations**
   ```bash
   python manage.py migrate
   ```

5. **Create a superuser (optional)**
   ```bash
   python manage.py createsuperuser
   ```

6. **Run the development server**
   ```bash
   python manage.py runserver
   ```

7. **Access the application**
   Open your browser and go to `http://127.0.0.1:8000/`

## Configuration

### Email Settings
To enable email functionality for dealer-customer communication, configure the following in `houseexplore/settings.py`:

```python
EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
EMAIL_HOST = 'your-smtp-server.com'
EMAIL_PORT = 587
EMAIL_USE_TLS = True
EMAIL_HOST_USER = 'your-email@example.com'
EMAIL_HOST_PASSWORD = 'your-password'
```

### Media Files
Property images are stored in the `media/house_images/` directory. Ensure the `media` folder has appropriate write permissions.

## Project Structure

```
houseexplore/
├── home/                   # Main Django app
│   ├── models.py          # Database models (House, Dealer, City, etc.)
│   ├── views.py           # View logic
│   ├── urls.py            # URL routing
│   └── admin.py           # Admin configurations
├── houseexplore/          # Project settings
├── templates/             # HTML templates
├── static/                # CSS, JS, images
├── media/                 # User-uploaded files
├── db.sqlite3            # SQLite database
└── manage.py             # Django management script
```

## Database Models

- **City**: Stores city information
- **Location**: Stores location/area within cities
- **House**: Property listings with details and amenities
- **Dealer**: Property seller information
- **Customer**: Potential buyer contact information
- **Message**: Chat messages between users
- **CustomerContacted**: Contact form submissions

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is open source and available under the [MIT License](LICENSE).

## Contact

For questions or support, please contact:
- **Author**: Manas Jayaswal
- **Email**: manas.jayaswal.cse21@itbhu.ac.in
- **GitHub**: [@mjmanas54](https://github.com/mjmanas54)

---

Built with ❤️ using Django
