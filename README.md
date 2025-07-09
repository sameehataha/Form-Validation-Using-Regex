# Form-Validation-Using-Regex 
# Form Validation App

A comprehensive registration form with real-time validation built using vanilla JavaScript, HTML, and CSS. Features robust client-side validation for all form fields with instant feedback and user-friendly error messages.

## Features

- 🔐 **Real-time Validation**: Instant feedback as users type
- 📝 **Multiple Field Types**: First name, last name, email, and password validation
- 👁️ **Password Visibility Toggle**: Show/hide password functionality
- ⚡ **Regex Validation**: Strong pattern matching for all fields
- 🎨 **Visual Feedback**: Color-coded error states and messages
- 📱 **Responsive Design**: Works seamlessly across different screen sizes
- ✅ **Success Redirect**: Automatic redirection upon successful form submission
- 🚫 **Empty Field Detection**: Prevents submission of incomplete forms

## Validation Rules

### Name Fields (First Name & Last Name)
- Must contain only alphabetic characters
- Case-insensitive validation
- No numbers or special characters allowed

### Email
- Must follow standard email format (user@domain.com)
- Supports dots and hyphens in username and domain
- Validates domain extensions (2-3 characters)

### Password
- **Minimum 8 characters** required
- Must contain at least **one lowercase letter**
- Must contain at least **one uppercase letter**
- Must contain at least **one digit**
- Must contain at least **one special character** (!@#$%^&*)

## Technologies Used

- **HTML5**: Semantic structure and form elements
- **CSS3**: Modern styling with flexbox and responsive design
- **Vanilla JavaScript**: Form validation logic and DOM manipulation
- **Regular Expressions**: Pattern matching for validation rules
- **UI Light Library**: Component library for consistent styling
- **Material Icons**: Google Material Design icons for UI elements

## Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- No additional installations required

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/form-validation-app.git
```

2. Navigate to the project directory:
```bash
cd form-validation-app
```

3. Open `index.html` in your web browser:
```bash
open index.html
```
Or simply double-click the `index.html` file.

## Usage

1. **Fill out the form**: Enter your details in each field
2. **Real-time feedback**: See validation messages as you type
3. **Error correction**: Fix any highlighted errors before submission
4. **Password visibility**: Click the eye icon to show/hide password
5. **Submit**: Click "Create Account" when all fields are valid
6. **Success**: You'll be redirected to a success page upon completion

## File Structure

```
form-validation-app/
├── index.html          # Main HTML structure
├── index.js            # JavaScript validation logic
├── style.css           # Custom styles and responsive design
├── success.html        # Success page (to be created)
└── README.md           # This file
```

## Key Features Explained

### Real-time Validation
The app validates fields as users type using the `keyup` event listener, providing immediate feedback.

### Switch Statement Logic
Uses a clean switch statement to handle different field types efficiently.

### Regex Patterns
- **Name**: `/^[a-z]+$/i` - Only alphabetic characters
- **Email**: `/^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{2,3})+$/` - Standard email format
- **Password**: `/^(?=.*\d)(?=.*[!@#$%^&*])(?=.*[a-z])(?=.*[A-Z]).{8,}$/` - Strong password requirements

### Visual Error States
- Red border for invalid fields
- Error messages with specific requirements
- Empty field warnings

### Password Toggle
Interactive show/hide password functionality with Material Icons.

## Customization

### Modifying Validation Rules
Edit the regex patterns in `index.js`:
```javascript
let nameRegex = /^[a-z]+$/i;
let emailRegex = /^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{2,3})+$/;
let passwordRegex = /^(?=.*\d)(?=.*[!@#$%^&*])(?=.*[a-z])(?=.*[A-Z]).{8,}$/;
```

### Styling
Modify colors and styling in `style.css`:
```css
.error {
  border: 2px solid red;
}

.error-message,
.empty-field {
  color: red;
}
```

### Adding New Fields
1. Add HTML structure in `index.html`
2. Create validation logic in `index.js`
3. Add corresponding CSS styles

## Known Issues

- **Minor Bug**: There's a typo in line 84 (`eFlag = flase;` should be `eFlag = false;`)
- **Success Page**: The success.html page needs to be created
- **Password Button**: The password toggle button needs proper targeting

## Bug Fixes Needed

```javascript
// Line 84 - Fix typo
eFlag = false; // Instead of eFlag = flase;

// Password button targeting
let pwdTarget = document.querySelector('[data-key="password"]');
```

## Browser Support

- Chrome (recommended)
- Firefox
- Safari
- Edge
- Any modern browser with ES6+ support

## Security Note

This is client-side validation only. **Always implement server-side validation** for production applications as client-side validation can be bypassed.

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Future Enhancements

- [ ] Add confirm password field
- [ ] Implement phone number validation
- [ ] Add date of birth field
- [ ] Create animated success page
- [ ] Add form progress indicator
- [ ] Implement accessibility features

## License

This project is open source and available under the [MIT License](LICENSE).

## Acknowledgments

- [UI Light](https://uilight.netlify.app/) for the component library
- [Google Material Icons](https://fonts.google.com/icons) for the icons
- [MDN Web Docs](https://developer.mozilla.org/) for regex patterns and validation techniques

---

**Happy Coding! 🚀**
