Incase you get Toml docoder error while running the streamlit

Refer: https://discuss.streamlit.io/t/toml-docoder-error/1400

Open terminal execute these commands -
```
streamlit config show > ~/.streamlit/config.toml
rm -i ~/.streamlit/config.toml
```
This will completly remove the config.toml file
