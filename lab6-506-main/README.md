��#   l a b 6 - 5 0 6 
 
 1. Download Lab6-506-main
  1a. Download zip, extract the zip 
2. In CMD, open your folder
  2a. CD C:\Users\Tasha\Downloads\lab6-506-main\lab6-506-main\Freeradius>
3. Build Freedaius docker
  3a. C:\Users\Tasha\Downloads\lab6-506-main\lab6-506-main\Freeradius>docker build . -t shrek --no-cache
  ![image](https://github.com/tbonutti/LAB506/assets/137101671/89f659e0-3642-4f11-9370-7265b54b00cb)
4. Run the Container
  4a. C:\Users\Tasha\Downloads\lab6-506-main\lab6-506-main\Freeradius>docker run -d --name my-shrek-radius-server -p 1812:1812/udp -p 1813:1813/udp shrek:latest
  ![image](https://github.com/tbonutti/LAB506/assets/137101671/b1c8d924-ca1b-43cc-9dd1-dfe482517b13)
5. CD to FlaskApp
  5a. VD C:\Users\Tasha\Downloads\lab6-506-main\lab6-506-main\flaskapp
6. Build Flaskapp docker
  6a. C:\Users\Tasha\Downloads\lab6-506-main\lab6-506-main\flaskapp>docker build . -t bob --no-cache
  ![image](https://github.com/tbonutti/LAB506/assets/137101671/93a743e7-4e11-4f64-87b3-99d712e16ed6)
7. Run the container with 5000 instead of 1812 and 1813 UDP
  7a. C:\Users\Tasha\Downloads\lab6-506-main\lab6-506-main\flaskapp>docker run -d --name my-bob-flask-app -p 5000:5000 bob:latest
  ![image](https://github.com/tbonutti/LAB506/assets/137101671/9d0519d4-3bb5-46c1-b2bc-9a0dd2dd3569)
9. Website log in http://127.0.0.1:5000/home
  Username: tasha
  Password:  Awesome13!
  ![image](https://github.com/tbonutti/LAB506/assets/137101671/44584b3e-de6d-427d-92c9-e05e6aca51b0)
done
