# Changelog

## 0.1.1

- Fix the add-on refusing to start with "Serial device ... not found" even
  when the RAVEn is present. The startup check used `bashio::fs.device_exists`,
  which in the bashio shipped by the base image only accepts block devices;
  serial ports are character devices.

## 0.1.0

- Initial release. Wraps raven2mqtt 0.1.0 as a Home Assistant add-on with MQTT
  auto-discovery and UART device selection.
