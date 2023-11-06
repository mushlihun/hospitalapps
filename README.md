# Hospital-Mobile-App

## Backend

- This application's backend is written in pure `PHP` and it does not include a `REST Api`. Therefore, the application should be able to access the PC's localhost.
- Connect your device to the PC and run the below commands to redirect the device's desired port to the PC's desired port. This will grant the device access to the PC's localhost. This works on both real devices as well as emulators.
- `ADB` tools must be installed in your PC for this to work.

```bash
adb reverse tcp:8000 tcp:8000
adb reverse tcp:8001 tcp:8001
```

> _Port 8000 is used to access the general backend. Port 8001 is used to access the PDF files which are stored in the PC. These are uploaded from the web application._

- Two seperate server instances will have to be running in order to access the general backend as well as the PDF files.
- Therefore, you need to navigate to the folder where you have stored the backend script.

```bash
cd path/folder-name
```

- Open up `cmd` or `PowerShell` and run the below command to server the `API`.
- This will serve the `PHP API` on port 8000 of your PC.

```php
php -S 0.0.0.0:8000
```

- Now go to the folder where you have stored the web application files.
- Note that there is a folder called `lab-reports`. This is where all the lab reports are stored in.
- Open up `cmd` or `PowerShell` and run the below command to serve the `API` for

```php
php -S 0.0.0.0:8001
```

## Frontend

### 🔨 Installation (Windows Only)

- Follow the below steps to get up and running
- Run the following `commands` inside Visual Studio Code or any other IDE which has a terminal or you can just use `cmd`

> 👯 Clone the repository

- Clone this repo to your local machine using `https://github.com/mushlihun/hospitalapps`

```shell

$ git clone https://github.com/mushlihun/hospitalapps.git

```

> 🏃‍♂️ Run and test the application

- Run the following commands to run and test the application in an emulator or a real device

```dart

$ flutter pub get
$ flutter run
