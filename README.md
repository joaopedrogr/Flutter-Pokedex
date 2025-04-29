# Pokedex

## 🚀 About the Project
The Pokedex Flutter is a web application built using the Flutter framework that displays a list of Pokémon with detailed information about each one. It consumes a public REST API (PokéAPI) and integrates with Firebase for backend features. Although the project was built using Flutter, only the web version is available in the repository due to deployment limitations.

Key Features:
- Dynamic Pokémon List: Fetches and displays Pokémon dynamically from the PokéAPI.
- Pokémon Details Page: View detailed information about a selected Pokémon, including types, stats, height, and weight.
- Responsive Design: Fully optimized for both desktop and mobile devices.
- API Integration: Fetches real-time data from the PokéAPI.
- Firebase Integration: Uses Firebase for authentication and/or data handling (depending on the configured features).

The Pokedex Flutter project is a great opportunity to learn Flutter fundamentals, API integration, and Firebase usage in a real-world scenario.

---

## 🖼 Screenshots

### Flutter version

<p>
  <img src="/assets/loginMobile.png" width="200"> &nbsp;&nbsp;
  <img src="/assets/registerMobile.png" width="200"> &nbsp;&nbsp;
  <img src="/assets/homeMobile.png" width="200"> &nbsp;&nbsp;
  <img src="/assets/detailsMobile.png" width="200"> 
</p>


### Web version
<p>
  <img src="/assets/login.png"> 
  <img src="/assets/register.png">
  <img src="/assets/home.png">
  <img src="/assets/details.png">
</p>


### Access the Web version at: https://flutter-pokedex1-tlj4.vercel.app/

---

## 🛠 Technologies Used
- Language: Dart
- Framework: Flutter
- State Management: setState / Provider
- Routing: Navigator / named routes
- Styling: Flutter UI Widgets
- API: PokéAPI (https://pokeapi.co/)
- Backend: Firebase
- Compatibility: Desktop & Mobile (Web version deployed)

---

## 📋 Requirements
- Flutter SDK (3.x or higher)
- Dart SDK
- Recommended Editor: VS Code or Android Studio
- Firebase Project (optional, if backend features are enabled)

---

## 📥 Installing or Cloning the Repository
To install and run the project locally, follow these steps:

### Clone the Repository

```
git clone https://github.com/your-username/Flutter-Pokedex.git

```

### Navigate to the project folder

```
cd Flutter-Pokedex
```

### Install dependencies

```
flutter pub get
```

### Start the application

```
flutter run -d chrome
```

The app will be available at http://localhost:PORT (depending on your configuration).

---

## 🎯 Learning Objectives
- API Integration: The app integrates with the PokéAPI to fetch Pokémon data dynamically. For example:
```
Future<void> fetchPokemonList() async {
  final response = await http.get(Uri.parse("https://pokeapi.co/api/v2/pokemon?limit=50"));
  if (response.statusCode == 200) {
    final data = json.decode(response.body);
    setState(() {
      pokemonList = data['results'];
    });
  }
}
```
- Firebase Integration: The app uses Firebase for authentication or backend features, for example:
```
Future<void> loginUser(String email, String password) async {
  try {
    UserCredential user = await FirebaseAuth.instance.signInWithEmailAndPassword(
      email: email,
      password: password,
    );
    print("User logged in: ${user.user?.email}");
  } catch (e) {
    print("Login error: $e");
  }
}

```
- State Management: Uses setState, optionally Provider, for managing the UI state.
- Componentization: Uses reusable widgets such as PokemonCard, DetailScreen, and TypeBadge.
- Responsive Design: Layouts adapt to different screen sizes using Flutter’s responsive layout techniques.
- Performance Optimization: Uses caching, efficient network calls, and Flutter’s build optimization techniques.
