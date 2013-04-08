ZWave Command Class Definitions
========

I've looked at a lot of ZWave products and I've read a lot of information about it. As a result this document is a definition of ZWave command classes I've been able to understand so far. As more command classes are discovered they will be added here.

FIELD_PARAMETERS - This is sometimes a dictionary and other times an array of dictionaries. This should always be the later.


```json
{
  "ZWAVE_CLASSES": {
    "COMMAND_CLASS": [
      {
        "FIELD_KEY": "40",
        "FIELD_NAME": "COMMAND_CLASS_SWITCH_TOGGLE_BINARY",
        "FIELD_DESCRIPTION": "Command Class Switch Toggle Binary",
        "COMMANDS": [
          {
            "FIELD_KEY": "3",
            "FIELD_NAME": "SWITCH_TOGGLE_BINARY_REPORT",
            "FIELD_DESCRIPTION": "Switch Toggle Binary Report",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Status",
              "FIELD_TYPE": "BYTE",
              "FIELD_TYPEhashcode": "1",
              "FIELD_BIT_DEF": [
                {
                  "FIELD_KEY": "2",
                  "FIELD_FLAG_DESCRIPTION": "off",
                  "FIELD_FLAG_MASK": "0"
                },
                {
                  "FIELD_KEY": "1",
                  "FIELD_FLAG_DESCRIPTION": "on",
                  "FIELD_FLAG_MASK": "255"
                }
              ],
              "FIELD_VALUE_ATTRIBUTES": {
                "FIELD_KEY": "0",
                "FIELD_HAS_CONSTANTS": "True",
                "FIELD_IS_HEX": "True"
              }
            }
          },
          {
            "FIELD_KEY": "2",
            "FIELD_NAME": "SWITCH_TOGGLE_BINARY_GET",
            "FIELD_DESCRIPTION": "Switch Toggle Binary Get"
          },
          {
            "FIELD_KEY": "1",
            "FIELD_NAME": "SWITCH_TOGGLE_BINARY_SET",
            "FIELD_DESCRIPTION": "Switch Toggle Binary Set"
          }
        ]
      },
      {
        "FIELD_KEY": "133",
        "FIELD_NAME": "COMMAND_CLASS_ASSOCIATION",
        "FIELD_DESCRIPTION": "Command Class Association",
        "COMMANDS": [
          {
            "FIELD_KEY": "6",
            "FIELD_NAME": "ASSOCIATION_GROUPINGS_REPORT",
            "FIELD_DESCRIPTION": "Association Groupings Report",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Supported Groupings",
              "FIELD_TYPE": "BYTE",
              "FIELD_TYPEhashcode": "1",
              "FIELD_VALUE_ATTRIBUTES": {
                "FIELD_KEY": "0",
                "FIELD_HAS_CONSTANTS": "False",
                "FIELD_IS_HEX": "False"
              }
            }
          },
          {
            "FIELD_KEY": "5",
            "FIELD_NAME": "ASSOCIATION_GROUPINGS_GET",
            "FIELD_DESCRIPTION": "Association Groupings Get"
          },
          {
            "FIELD_KEY": "4",
            "FIELD_NAME": "ASSOCIATION_REMOVE",
            "FIELD_DESCRIPTION": "Association Remove",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Node ID(s)",
                "FIELD_TYPE": "ARRAY",
                "FIELD_TYPEhashcode": "5",
                "FIELD_ARRAY_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_IS_ASCII": "False",
                  "FIELD_LEN": "255"
                }
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Grouping identifier",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              }
            ]
          },
          {
            "FIELD_KEY": "3",
            "FIELD_NAME": "ASSOCIATION_REPORT",
            "FIELD_DESCRIPTION": "Association Report",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "3",
                "FIELD_NAME": "Node ID(s)",
                "FIELD_TYPE": "ARRAY",
                "FIELD_TYPEhashcode": "5",
                "FIELD_ARRAY_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_IS_ASCII": "False",
                  "FIELD_LEN": "255"
                }
              },
              {
                "FIELD_KEY": "2",
                "FIELD_NAME": "Reports to follow",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Max Nodes Supported",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Grouping identifier",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              }
            ]
          },
          {
            "FIELD_KEY": "2",
            "FIELD_NAME": "ASSOCIATION_GET",
            "FIELD_DESCRIPTION": "Association Get",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Grouping identifier",
              "FIELD_TYPE": "BYTE",
              "FIELD_TYPEhashcode": "1",
              "FIELD_VALUE_ATTRIBUTES": {
                "FIELD_KEY": "0",
                "FIELD_HAS_CONSTANTS": "False",
                "FIELD_IS_HEX": "False"
              }
            }
          },
          {
            "FIELD_KEY": "1",
            "FIELD_NAME": "ASSOCIATION_SET",
            "FIELD_DESCRIPTION": "Association Set",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Node ID(s)",
                "FIELD_TYPE": "ARRAY",
                "FIELD_TYPEhashcode": "5",
                "FIELD_ARRAY_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_IS_ASCII": "False",
                  "FIELD_LEN": "255"
                }
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Grouping identifier",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              }
            ]
          }
        ]
      },
      {
        "FIELD_KEY": "132",
        "FIELD_NAME": "COMMAND_CLASS_WAKE_UP",
        "FIELD_DESCRIPTION": "Command Class Wake Up",
        "COMMANDS": [
          {
            "FIELD_KEY": "8",
            "FIELD_NAME": "WAKE_UP_NO_MORE_INFORMATION",
            "FIELD_DESCRIPTION": "Wake Up No More Information"
          },
          {
            "FIELD_KEY": "7",
            "FIELD_NAME": "WAKE_UP_NOTIFICATION",
            "FIELD_DESCRIPTION": "Wake Up Notification"
          },
          {
            "FIELD_KEY": "6",
            "FIELD_NAME": "WAKE_UP_INTERVAL_REPORT",
            "FIELD_DESCRIPTION": "Wake Up Interval Report",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "NodeID",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Seconds",
                "FIELD_TYPE": "BIT_24",
                "FIELD_TYPEhashcode": "4",
                "bit_24": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              }
            ]
          },
          {
            "FIELD_KEY": "5",
            "FIELD_NAME": "WAKE_UP_INTERVAL_GET",
            "FIELD_DESCRIPTION": "Wake Up Interval Get"
          },
          {
            "FIELD_KEY": "4",
            "FIELD_NAME": "WAKE_UP_INTERVAL_SET",
            "FIELD_DESCRIPTION": "Wake Up Interval Set",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "NodeID",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Seconds",
                "FIELD_TYPE": "BIT_24",
                "FIELD_TYPEhashcode": "4",
                "bit_24": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              }
            ]
          }
        ]
      },
      {
        "FIELD_KEY": "137",
        "FIELD_NAME": "COMMAND_CLASS_LANGUAGE",
        "FIELD_DESCRIPTION": "Command Class Language",
        "COMMANDS": [
          {
            "FIELD_KEY": "3",
            "FIELD_NAME": "LANGUAGE_REPORT",
            "FIELD_DESCRIPTION": "Language Report",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Country",
                "FIELD_TYPE": "ARRAY",
                "FIELD_TYPEhashcode": "5",
                "FIELD_ARRAY_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_IS_ASCII": "True",
                  "FIELD_LEN": "2"
                }
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Language",
                "FIELD_TYPE": "ARRAY",
                "FIELD_TYPEhashcode": "5",
                "FIELD_ARRAY_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_IS_ASCII": "True",
                  "FIELD_LEN": "3"
                }
              }
            ]
          },
          {
            "FIELD_KEY": "2",
            "FIELD_NAME": "LANGUAGE_GET",
            "FIELD_DESCRIPTION": "Language Get"
          },
          {
            "FIELD_KEY": "1",
            "FIELD_NAME": "LANGUAGE_SET",
            "FIELD_DESCRIPTION": "Language Set",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Country",
                "FIELD_TYPE": "ARRAY",
                "FIELD_TYPEhashcode": "5",
                "FIELD_ARRAY_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_IS_ASCII": "True",
                  "FIELD_LEN": "2"
                }
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Language",
                "FIELD_TYPE": "ARRAY",
                "FIELD_TYPEhashcode": "5",
                "FIELD_ARRAY_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_IS_ASCII": "True",
                  "FIELD_LEN": "3"
                }
              }
            ]
          }
        ]
      },
      {
        "FIELD_KEY": "136",
        "FIELD_NAME": "COMMAND_CLASS_PROPRIETARY",
        "FIELD_DESCRIPTION": "Command Class Proprietary",
        "COMMANDS": [
          {
            "FIELD_KEY": "3",
            "FIELD_NAME": "PROPRIETARY_REPORT",
            "FIELD_DESCRIPTION": "Proprietary Report",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Data",
              "FIELD_TYPE": "ARRAY",
              "FIELD_TYPEhashcode": "5",
              "FIELD_ARRAY_ATTRIBUTES": {
                "FIELD_KEY": "0",
                "FIELD_IS_ASCII": "False",
                "FIELD_LEN": "255"
              }
            }
          },
          {
            "FIELD_KEY": "2",
            "FIELD_NAME": "PROPRIETARY_GET",
            "FIELD_DESCRIPTION": "Proprietary Get",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Data",
              "FIELD_TYPE": "ARRAY",
              "FIELD_TYPEhashcode": "5",
              "FIELD_ARRAY_ATTRIBUTES": {
                "FIELD_KEY": "0",
                "FIELD_IS_ASCII": "False",
                "FIELD_LEN": "255"
              }
            }
          },
          {
            "FIELD_KEY": "1",
            "FIELD_NAME": "PROPRIETARY_SET",
            "FIELD_DESCRIPTION": "Proprietary Set",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Data",
              "FIELD_TYPE": "ARRAY",
              "FIELD_TYPEhashcode": "5",
              "FIELD_ARRAY_ATTRIBUTES": {
                "FIELD_KEY": "0",
                "FIELD_IS_ASCII": "False",
                "FIELD_LEN": "255"
              }
            }
          }
        ]
      },
      {
        "FIELD_KEY": "41",
        "FIELD_NAME": "COMMAND_CLASS_SWITCH_TOGGLE_MULTILEVEL",
        "FIELD_DESCRIPTION": "Command Class Switch Toggle Multilevel",
        "COMMANDS": [
          {
            "FIELD_KEY": "5",
            "FIELD_NAME": "SWITCH_TOGGLE_MULTILEVEL_STOP_LEVEL_CHANGE",
            "FIELD_DESCRIPTION": "Switch Toggle Multilevel Stop Level Change"
          },
          {
            "FIELD_KEY": "4",
            "FIELD_NAME": "SWITCH_TOGGLE_MULTILEVEL_START_LEVEL_CHANGE",
            "FIELD_DESCRIPTION": "Switch Toggle Multilevel Start Level Change",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_TYPE": "STRUCT_BYTE",
              "FIELD_TYPEhashcode": "7",
              "bitfield": {
                "FIELD_KEY": "3",
                "FIELD_NAME": "Reserved Field",
                "FIELD_BIT_MASK": "31",
                "FIELD_OFFSET": "0"
              },
              "FIELD_BIT_DEF": [
                {
                  "FIELD_KEY": "2",
                  "FIELD_FLAG_DESCRIPTION": "Ignore start level",
                  "FIELD_FLAG_MASK": "32"
                },
                {
                  "FIELD_KEY": "1",
                  "FIELD_FLAG_DESCRIPTION": "Reserved bit",
                  "FIELD_FLAG_MASK": "64"
                },
                {
                  "FIELD_KEY": "0",
                  "FIELD_FLAG_DESCRIPTION": "Roll over",
                  "FIELD_FLAG_MASK": "128"
                }
              ]
            }
          },
          {
            "FIELD_KEY": "3",
            "FIELD_NAME": "SWITCH_TOGGLE_MULTILEVEL_REPORT",
            "FIELD_DESCRIPTION": "Switch Toggle Multilevel Report",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Status",
              "FIELD_TYPE": "BYTE",
              "FIELD_TYPEhashcode": "1",
              "FIELD_BIT_DEF": [
                {
                  "FIELD_KEY": "2",
                  "FIELD_FLAG_DESCRIPTION": "(on/enable)",
                  "FIELD_FLAG_MASK": "255"
                },
                {
                  "FIELD_KEY": "1",
                  "FIELD_FLAG_DESCRIPTION": "(off/disable)",
                  "FIELD_FLAG_MASK": "0"
                }
              ],
              "FIELD_VALUE_ATTRIBUTES": {
                "FIELD_KEY": "0",
                "FIELD_HAS_CONSTANTS": "True",
                "FIELD_IS_HEX": "True"
              }
            }
          },
          {
            "FIELD_KEY": "2",
            "FIELD_NAME": "SWITCH_TOGGLE_MULTILEVEL_GET",
            "FIELD_DESCRIPTION": "Switch Toggle Multilevel Get"
          },
          {
            "FIELD_KEY": "1",
            "FIELD_NAME": "SWITCH_TOGGLE_MULTILEVEL_SET",
            "FIELD_DESCRIPTION": "Switch Toggle Multilevel Set"
          }
        ]
      },
      {
        "FIELD_KEY": "134",
        "FIELD_NAME": "COMMAND_CLASS_VERSION",
        "FIELD_DESCRIPTION": "Command Class Version",
        "COMMANDS": [
          {
            "FIELD_KEY": "20",
            "FIELD_NAME": "VERSION_COMMAND_CLASS_REPORT",
            "FIELD_DESCRIPTION": "Version Command Class Report",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Command Class Version",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Requested Command Class",
                "FIELD_TYPE": "ENUM",
                "FIELD_TYPEhashcode": "8",
                "enum": [
                  {
                    "FIELD_KEY": "96",
                    "FIELD_NAME": "COMMAND_CLASS_MULTI_INSTANCE"
                  },
                  {
                    "FIELD_KEY": "81",
                    "FIELD_NAME": "COMMAND_CLASS_MTP_WINDOW_COVERING"
                  },
                  {
                    "FIELD_KEY": "80",
                    "FIELD_NAME": "COMMAND_CLASS_BASIC_WINDOW_COVERING"
                  },
                  {
                    "FIELD_KEY": "69",
                    "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_FAN_STATE"
                  },
                  {
                    "FIELD_KEY": "68",
                    "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_FAN_MODE"
                  },
                  {
                    "FIELD_KEY": "67",
                    "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_SETPOINT"
                  },
                  {
                    "FIELD_KEY": "66",
                    "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_OPERATING_STATE"
                  },
                  {
                    "FIELD_KEY": "64",
                    "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_MODE"
                  },
                  {
                    "FIELD_KEY": "56",
                    "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT"
                  },
                  {
                    "FIELD_KEY": "53",
                    "FIELD_NAME": "COMMAND_CLASS_METER_PULSE"
                  },
                  {
                    "FIELD_KEY": "49",
                    "FIELD_NAME": "COMMAND_CLASS_SENSOR_MULTILEVEL"
                  },
                  {
                    "FIELD_KEY": "48",
                    "FIELD_NAME": "COMMAND_CLASS_SENSOR_BINARY"
                  },
                  {
                    "FIELD_KEY": "144",
                    "FIELD_NAME": "COMMAND_CLASS_ENERGY_PRODUCTION"
                  },
                  {
                    "FIELD_KEY": "42",
                    "FIELD_NAME": "COMMAND_CLASS_CHIMNEY_FAN"
                  },
                  {
                    "FIELD_KEY": "41",
                    "FIELD_NAME": "COMMAND_CLASS_SWITCH_TOGGLE_MULTILEVEL"
                  },
                  {
                    "FIELD_KEY": "40",
                    "FIELD_NAME": "COMMAND_CLASS_SWITCH_TOGGLE_BINARY"
                  },
                  {
                    "FIELD_KEY": "39",
                    "FIELD_NAME": "COMMAND_CLASS_SWITCH_ALL"
                  },
                  {
                    "FIELD_KEY": "38",
                    "FIELD_NAME": "COMMAND_CLASS_SWITCH_MULTILEVEL"
                  },
                  {
                    "FIELD_KEY": "37",
                    "FIELD_NAME": "COMMAND_CLASS_SWITCH_BINARY"
                  },
                  {
                    "FIELD_KEY": "34",
                    "FIELD_NAME": "COMMAND_CLASS_APPLICATION_STATUS"
                  },
                  {
                    "FIELD_KEY": "33",
                    "FIELD_NAME": "COMMAND_CLASS_CONTROLLER_REPLICATION"
                  },
                  {
                    "FIELD_KEY": "32",
                    "FIELD_NAME": "COMMAND_CLASS_BASIC"
                  },
                  {
                    "FIELD_KEY": "137",
                    "FIELD_NAME": "COMMAND_CLASS_LANGUAGE"
                  },
                  {
                    "FIELD_KEY": "136",
                    "FIELD_NAME": "COMMAND_CLASS_PROPRIETARY"
                  },
                  {
                    "FIELD_KEY": "135",
                    "FIELD_NAME": "COMMAND_CLASS_INDICATOR"
                  },
                  {
                    "FIELD_KEY": "134",
                    "FIELD_NAME": "COMMAND_CLASS_VERSION"
                  },
                  {
                    "FIELD_KEY": "133",
                    "FIELD_NAME": "COMMAND_CLASS_ASSOCIATION"
                  },
                  {
                    "FIELD_KEY": "132",
                    "FIELD_NAME": "COMMAND_CLASS_WAKE_UP"
                  },
                  {
                    "FIELD_KEY": "131",
                    "FIELD_NAME": "COMMAND_CLASS_NETWORK_STAT"
                  },
                  {
                    "FIELD_KEY": "129",
                    "FIELD_NAME": "COMMAND_CLASS_CLOCK"
                  },
                  {
                    "FIELD_KEY": "128",
                    "FIELD_NAME": "COMMAND_CLASS_BATTERY"
                  },
                  {
                    "FIELD_KEY": "14",
                    "FIELD_NAME": "REQUEST_NODE_INFO"
                  },
                  {
                    "FIELD_KEY": "13",
                    "FIELD_NAME": "DELETE_ROUTE"
                  },
                  {
                    "FIELD_KEY": "12",
                    "FIELD_NAME": "ASSIGN_ROUTE"
                  },
                  {
                    "FIELD_KEY": "118",
                    "FIELD_NAME": "COMMAND_CLASS_LOCK"
                  },
                  {
                    "FIELD_KEY": "117",
                    "FIELD_NAME": "COMMAND_CLASS_PROTECTION"
                  },
                  {
                    "FIELD_KEY": "115",
                    "FIELD_NAME": "COMMAND_CLASS_POWERLEVEL"
                  },
                  {
                    "FIELD_KEY": "114",
                    "FIELD_NAME": "COMMAND_CLASS_MANUFACTURER_SPECIFIC"
                  },
                  {
                    "FIELD_KEY": "113",
                    "FIELD_NAME": "COMMAND_CLASS_ALARM"
                  },
                  {
                    "FIELD_KEY": "112",
                    "FIELD_NAME": "COMMAND_CLASS_CONFIGURATION"
                  }
                ]
              }
            ]
          },
          {
            "FIELD_KEY": "19",
            "FIELD_NAME": "VERSION_COMMAND_CLASS_GET",
            "FIELD_DESCRIPTION": "Version Command Class Get",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Requested Command Class",
              "FIELD_TYPE": "ENUM",
              "FIELD_TYPEhashcode": "8",
              "enum": [
                {
                  "FIELD_KEY": "96",
                  "FIELD_NAME": "COMMAND_CLASS_MULTI_INSTANCE"
                },
                {
                  "FIELD_KEY": "81",
                  "FIELD_NAME": "COMMAND_CLASS_MTP_WINDOW_COVERING"
                },
                {
                  "FIELD_KEY": "80",
                  "FIELD_NAME": "COMMAND_CLASS_BASIC_WINDOW_COVERING"
                },
                {
                  "FIELD_KEY": "69",
                  "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_FAN_STATE"
                },
                {
                  "FIELD_KEY": "68",
                  "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_FAN_MODE"
                },
                {
                  "FIELD_KEY": "67",
                  "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_SETPOINT"
                },
                {
                  "FIELD_KEY": "66",
                  "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_OPERATING_STATE"
                },
                {
                  "FIELD_KEY": "64",
                  "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_MODE"
                },
                {
                  "FIELD_KEY": "56",
                  "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT"
                },
                {
                  "FIELD_KEY": "53",
                  "FIELD_NAME": "COMMAND_CLASS_METER_PULSE"
                },
                {
                  "FIELD_KEY": "49",
                  "FIELD_NAME": "COMMAND_CLASS_SENSOR_MULTILEVEL"
                },
                {
                  "FIELD_KEY": "48",
                  "FIELD_NAME": "COMMAND_CLASS_SENSOR_BINARY"
                },
                {
                  "FIELD_KEY": "144",
                  "FIELD_NAME": "COMMAND_CLASS_ENERGY_PRODUCTION"
                },
                {
                  "FIELD_KEY": "42",
                  "FIELD_NAME": "COMMAND_CLASS_CHIMNEY_FAN"
                },
                {
                  "FIELD_KEY": "41",
                  "FIELD_NAME": "COMMAND_CLASS_SWITCH_TOGGLE_MULTILEVEL"
                },
                {
                  "FIELD_KEY": "40",
                  "FIELD_NAME": "COMMAND_CLASS_SWITCH_TOGGLE_BINARY"
                },
                {
                  "FIELD_KEY": "39",
                  "FIELD_NAME": "COMMAND_CLASS_SWITCH_ALL"
                },
                {
                  "FIELD_KEY": "38",
                  "FIELD_NAME": "COMMAND_CLASS_SWITCH_MULTILEVEL"
                },
                {
                  "FIELD_KEY": "37",
                  "FIELD_NAME": "COMMAND_CLASS_SWITCH_BINARY"
                },
                {
                  "FIELD_KEY": "34",
                  "FIELD_NAME": "COMMAND_CLASS_APPLICATION_STATUS"
                },
                {
                  "FIELD_KEY": "33",
                  "FIELD_NAME": "COMMAND_CLASS_CONTROLLER_REPLICATION"
                },
                {
                  "FIELD_KEY": "32",
                  "FIELD_NAME": "COMMAND_CLASS_BASIC"
                },
                {
                  "FIELD_KEY": "137",
                  "FIELD_NAME": "COMMAND_CLASS_LANGUAGE"
                },
                {
                  "FIELD_KEY": "136",
                  "FIELD_NAME": "COMMAND_CLASS_PROPRIETARY"
                },
                {
                  "FIELD_KEY": "135",
                  "FIELD_NAME": "COMMAND_CLASS_INDICATOR"
                },
                {
                  "FIELD_KEY": "134",
                  "FIELD_NAME": "COMMAND_CLASS_VERSION"
                },
                {
                  "FIELD_KEY": "133",
                  "FIELD_NAME": "COMMAND_CLASS_ASSOCIATION"
                },
                {
                  "FIELD_KEY": "132",
                  "FIELD_NAME": "COMMAND_CLASS_WAKE_UP"
                },
                {
                  "FIELD_KEY": "131",
                  "FIELD_NAME": "COMMAND_CLASS_NETWORK_STAT"
                },
                {
                  "FIELD_KEY": "129",
                  "FIELD_NAME": "COMMAND_CLASS_CLOCK"
                },
                {
                  "FIELD_KEY": "128",
                  "FIELD_NAME": "COMMAND_CLASS_BATTERY"
                },
                {
                  "FIELD_KEY": "14",
                  "FIELD_NAME": "REQUEST_NODE_INFO"
                },
                {
                  "FIELD_KEY": "13",
                  "FIELD_NAME": "DELETE_ROUTE"
                },
                {
                  "FIELD_KEY": "12",
                  "FIELD_NAME": "ASSIGN_ROUTE"
                },
                {
                  "FIELD_KEY": "118",
                  "FIELD_NAME": "COMMAND_CLASS_LOCK"
                },
                {
                  "FIELD_KEY": "117",
                  "FIELD_NAME": "COMMAND_CLASS_PROTECTION"
                },
                {
                  "FIELD_KEY": "115",
                  "FIELD_NAME": "COMMAND_CLASS_POWERLEVEL"
                },
                {
                  "FIELD_KEY": "114",
                  "FIELD_NAME": "COMMAND_CLASS_MANUFACTURER_SPECIFIC"
                },
                {
                  "FIELD_KEY": "113",
                  "FIELD_NAME": "COMMAND_CLASS_ALARM"
                },
                {
                  "FIELD_KEY": "112",
                  "FIELD_NAME": "COMMAND_CLASS_CONFIGURATION"
                }
              ]
            }
          },
          {
            "FIELD_KEY": "18",
            "FIELD_NAME": "VERSION_REPORT",
            "FIELD_DESCRIPTION": "Version Report",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "4",
                "FIELD_NAME": "Application Sub Version",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "3",
                "FIELD_NAME": "Application Version",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "2",
                "FIELD_NAME": "Z-Wave Protocol Sub Version",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Z-Wave Protocol Version",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Z-Wave Library Type",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "True"
                }
              }
            ]
          },
          {
            "FIELD_KEY": "17",
            "FIELD_NAME": "VERSION_GET",
            "FIELD_DESCRIPTION": "Version Get"
          }
        ]
      },
      {
        "FIELD_KEY": "39",
        "FIELD_NAME": "COMMAND_CLASS_SWITCH_ALL",
        "FIELD_DESCRIPTION": "Command Class Switch All",
        "COMMANDS": [
          {
            "FIELD_KEY": "5",
            "FIELD_NAME": "SWITCH_ALL_OFF",
            "FIELD_DESCRIPTION": "Switch All Off"
          },
          {
            "FIELD_KEY": "4",
            "FIELD_NAME": "SWITCH_ALL_ON",
            "FIELD_DESCRIPTION": "Switch All On"
          },
          {
            "FIELD_KEY": "3",
            "FIELD_NAME": "SWITCH_ALL_REPORT",
            "FIELD_DESCRIPTION": "Switch All Report",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "State",
              "FIELD_TYPE": "CONST",
              "FIELD_TYPEhashcode": "11",
              "const": [
                {
                  "FIELD_KEY": "3",
                  "FIELD_FLAG_DESCRIPTION": "Included in all on/all off",
                  "FIELD_FLAG_MASK": "0"
                },
                {
                  "FIELD_KEY": "2",
                  "FIELD_FLAG_DESCRIPTION": "Excluded from all off",
                  "FIELD_FLAG_MASK": "2"
                },
                {
                  "FIELD_KEY": "1",
                  "FIELD_FLAG_DESCRIPTION": "Excluded from all on",
                  "FIELD_FLAG_MASK": "1"
                },
                {
                  "FIELD_KEY": "0",
                  "FIELD_FLAG_DESCRIPTION": "Excluded from all on/all off",
                  "FIELD_FLAG_MASK": "0"
                }
              ]
            }
          },
          {
            "FIELD_KEY": "2",
            "FIELD_NAME": "SWITCH_ALL_GET",
            "FIELD_DESCRIPTION": "Switch All Get"
          },
          {
            "FIELD_KEY": "1",
            "FIELD_NAME": "SWITCH_ALL_SET",
            "FIELD_DESCRIPTION": "Switch All Set",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "State",
              "FIELD_TYPE": "CONST",
              "FIELD_TYPEhashcode": "11",
              "const": [
                {
                  "FIELD_KEY": "3",
                  "FIELD_FLAG_DESCRIPTION": "Included in all on/all off",
                  "FIELD_FLAG_MASK": "0"
                },
                {
                  "FIELD_KEY": "2",
                  "FIELD_FLAG_DESCRIPTION": "Excluded from all off",
                  "FIELD_FLAG_MASK": "2"
                },
                {
                  "FIELD_KEY": "1",
                  "FIELD_FLAG_DESCRIPTION": "Excluded from all on",
                  "FIELD_FLAG_MASK": "1"
                },
                {
                  "FIELD_KEY": "0",
                  "FIELD_FLAG_DESCRIPTION": "Excluded from all on/all off",
                  "FIELD_FLAG_MASK": "0"
                }
              ]
            }
          }
        ]
      },
      {
        "FIELD_KEY": "38",
        "FIELD_NAME": "COMMAND_CLASS_SWITCH_MULTILEVEL",
        "FIELD_DESCRIPTION": "Command Class Switch Multilevel",
        "COMMANDS": [
          {
            "FIELD_KEY": "6",
            "FIELD_NAME": "SWITCH_MULTILEVEL_DO_LEVEL_CHANGE",
            "FIELD_DESCRIPTION": "Switch Multilevel Do Level Change",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Value",
              "FIELD_TYPE": "CONST",
              "FIELD_TYPEhashcode": "11",
              "const": [
                {
                  "FIELD_KEY": "1",
                  "FIELD_FLAG_DESCRIPTION": "ON/Enable",
                  "FIELD_FLAG_MASK": "255"
                },
                {
                  "FIELD_KEY": "0",
                  "FIELD_FLAG_DESCRIPTION": "OFF/Disable",
                  "FIELD_FLAG_MASK": "0"
                }
              ]
            }
          },
          {
            "FIELD_KEY": "5",
            "FIELD_NAME": "SWITCH_MULTILEVEL_STOP_LEVEL_CHANGE",
            "FIELD_DESCRIPTION": "Switch Multilevel Stop Level Change"
          },
          {
            "FIELD_KEY": "4",
            "FIELD_NAME": "SWITCH_MULTILEVEL_START_LEVEL_CHANGE",
            "FIELD_DESCRIPTION": "Switch Multilevel Start Level Change",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_TYPE": "STRUCT_BYTE",
              "FIELD_TYPEhashcode": "7",
              "bitfield": {
                "FIELD_KEY": "3",
                "FIELD_NAME": "Reserved",
                "FIELD_BIT_MASK": "31",
                "FIELD_OFFSET": "0"
              },
              "FIELD_BIT_DEF": [
                {
                  "FIELD_KEY": "2",
                  "FIELD_FLAG_DESCRIPTION": "Ignore Start Level",
                  "FIELD_FLAG_MASK": "32"
                },
                {
                  "FIELD_KEY": "1",
                  "FIELD_FLAG_DESCRIPTION": "UP/DOWN",
                  "FIELD_FLAG_MASK": "64"
                },
                {
                  "FIELD_KEY": "0",
                  "FIELD_FLAG_DESCRIPTION": "Roll Over",
                  "FIELD_FLAG_MASK": "128"
                }
              ]
            }
          },
          {
            "FIELD_KEY": "3",
            "FIELD_NAME": "SWITCH_MULTILEVEL_REPORT",
            "FIELD_DESCRIPTION": "Switch Multilevel Report",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Value",
              "FIELD_TYPE": "BYTE",
              "FIELD_TYPEhashcode": "1",
              "FIELD_BIT_DEF": [
                {
                  "FIELD_KEY": "2",
                  "FIELD_FLAG_DESCRIPTION": "SWITCH_ON",
                  "FIELD_FLAG_MASK": "255"
                },
                {
                  "FIELD_KEY": "1",
                  "FIELD_FLAG_DESCRIPTION": "SWITCH_OFF",
                  "FIELD_FLAG_MASK": "0"
                }
              ],
              "FIELD_VALUE_ATTRIBUTES": {
                "FIELD_KEY": "0",
                "FIELD_HAS_CONSTANTS": "True",
                "FIELD_IS_HEX": "False"
              }
            }
          },
          {
            "FIELD_KEY": "2",
            "FIELD_NAME": "SWITCH_MULTILEVEL_GET",
            "FIELD_DESCRIPTION": "Switch Multilevel Get"
          },
          {
            "FIELD_KEY": "1",
            "FIELD_NAME": "SWITCH_MULTILEVEL_SET",
            "FIELD_DESCRIPTION": "Switch Multilevel Set",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Value",
              "FIELD_TYPE": "BYTE",
              "FIELD_TYPEhashcode": "1",
              "FIELD_BIT_DEF": [
                {
                  "FIELD_KEY": "2",
                  "FIELD_FLAG_DESCRIPTION": "SWITCH_ON",
                  "FIELD_FLAG_MASK": "255"
                },
                {
                  "FIELD_KEY": "1",
                  "FIELD_FLAG_DESCRIPTION": "SWITCH_OFF",
                  "FIELD_FLAG_MASK": "0"
                }
              ],
              "FIELD_VALUE_ATTRIBUTES": {
                "FIELD_KEY": "0",
                "FIELD_HAS_CONSTANTS": "True",
                "FIELD_IS_HEX": "False"
              }
            }
          }
        ]
      },
      {
        "FIELD_KEY": "37",
        "FIELD_NAME": "COMMAND_CLASS_SWITCH_BINARY",
        "FIELD_DESCRIPTION": "Command Class Switch Binary",
        "COMMANDS": [
          {
            "FIELD_KEY": "3",
            "FIELD_NAME": "SWITCH_BINARY_REPORT",
            "FIELD_DESCRIPTION": "Switch Binary Report",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Value",
              "FIELD_TYPE": "CONST",
              "FIELD_TYPEhashcode": "11",
              "const": [
                {
                  "FIELD_KEY": "1",
                  "FIELD_FLAG_DESCRIPTION": "ON/Enable",
                  "FIELD_FLAG_MASK": "255"
                },
                {
                  "FIELD_KEY": "0",
                  "FIELD_FLAG_DESCRIPTION": "OFF/Disable",
                  "FIELD_FLAG_MASK": "0"
                }
              ]
            }
          },
          {
            "FIELD_KEY": "2",
            "FIELD_NAME": "SWITCH_BINARY_GET",
            "FIELD_DESCRIPTION": "Switch Binary Get"
          },
          {
            "FIELD_KEY": "1",
            "FIELD_NAME": "SWITCH_BINARY_SET",
            "FIELD_DESCRIPTION": "Switch Binary Set",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Value",
              "FIELD_TYPE": "CONST",
              "FIELD_TYPEhashcode": "11",
              "const": [
                {
                  "FIELD_KEY": "1",
                  "FIELD_FLAG_DESCRIPTION": "ON/Enable",
                  "FIELD_FLAG_MASK": "255"
                },
                {
                  "FIELD_KEY": "0",
                  "FIELD_FLAG_DESCRIPTION": "OFF/Disable",
                  "FIELD_FLAG_MASK": "0"
                }
              ]
            }
          }
        ]
      },
      {
        "FIELD_KEY": "129",
        "FIELD_NAME": "COMMAND_CLASS_CLOCK",
        "FIELD_DESCRIPTION": "Command Class Clock",
        "COMMANDS": [
          {
            "FIELD_KEY": "6",
            "FIELD_NAME": "CLOCK_REPORT",
            "FIELD_DESCRIPTION": "Clock Report",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Minute",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Parameter 1",
                "FIELD_TYPE": "STRUCT_BYTE",
                "FIELD_TYPEhashcode": "7",
                "bitfield": {
                  "FIELD_KEY": "1",
                  "FIELD_NAME": "Hour",
                  "FIELD_BIT_MASK": "31",
                  "FIELD_OFFSET": "0"
                },
                "fieldenum": {
                  "FIELD_KEY": "0",
                  "FIELD_NAME": "Weekday",
                  "FIELD_BIT_MASK": "224",
                  "FIELD_OFFSET": "5",
                  "fieldenum": [
                    { "FIELD_VALUE": "Unused (24 hour clock)" },
                    { "FIELD_VALUE": "Monday" },
                    { "FIELD_VALUE": "Tuesday" },
                    { "FIELD_VALUE": "Wednesday" },
                    { "FIELD_VALUE": "Thursday" },
                    { "FIELD_VALUE": "Friday" },
                    { "FIELD_VALUE": "Saturday" },
                    { "FIELD_VALUE": "Sunday" }
                  ]
                }
              }
            ]
          },
          {
            "FIELD_KEY": "5",
            "FIELD_NAME": "CLOCK_GET",
            "FIELD_DESCRIPTION": "Clock Get"
          },
          {
            "FIELD_KEY": "4",
            "FIELD_NAME": "CLOCK_SET",
            "FIELD_DESCRIPTION": "Clock Set",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Minute",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Parameter 1",
                "FIELD_TYPE": "STRUCT_BYTE",
                "FIELD_TYPEhashcode": "7",
                "bitfield": {
                  "FIELD_KEY": "1",
                  "FIELD_NAME": "Hour",
                  "FIELD_BIT_MASK": "31",
                  "FIELD_OFFSET": "0"
                },
                "fieldenum": {
                  "FIELD_KEY": "0",
                  "FIELD_NAME": "Weekday",
                  "FIELD_BIT_MASK": "224",
                  "FIELD_OFFSET": "5",
                  "fieldenum": [
                    { "FIELD_VALUE": "Unused (24 hour clock)" },
                    { "FIELD_VALUE": "Monday" },
                    { "FIELD_VALUE": "Tuesday" },
                    { "FIELD_VALUE": "Wednesday" },
                    { "FIELD_VALUE": "Thursday" },
                    { "FIELD_VALUE": "Friday" },
                    { "FIELD_VALUE": "Saturday" },
                    { "FIELD_VALUE": "Sunday" }
                  ]
                }
              }
            ]
          }
        ]
      },
      {
        "FIELD_KEY": "34",
        "FIELD_NAME": "COMMAND_CLASS_APPLICATION_STATUS",
        "FIELD_DESCRIPTION": "Command Class Application Status",
        "COMMANDS": [
          {
            "FIELD_KEY": "2",
            "FIELD_NAME": "APPLICATION_REJECTED_REQUEST",
            "FIELD_DESCRIPTION": "Application Rejected Request",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Status",
              "FIELD_TYPE": "BYTE",
              "FIELD_TYPEhashcode": "1",
              "FIELD_VALUE_ATTRIBUTES": {
                "FIELD_KEY": "0",
                "FIELD_HAS_CONSTANTS": "False",
                "FIELD_IS_HEX": "True"
              }
            }
          },
          {
            "FIELD_KEY": "1",
            "FIELD_NAME": "APPLICATION_STATUS_BUSY",
            "FIELD_DESCRIPTION": "Application Status Busy",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Time in SEC",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Status",
                "FIELD_TYPE": "ENUM",
                "FIELD_TYPEhashcode": "8",
                "enum": [
                  {
                    "FIELD_KEY": "2",
                    "FIELD_NAME": "Request queued, executed later"
                  },
                  {
                    "FIELD_KEY": "1",
                    "FIELD_NAME": "Try again in Wait Time seconds"
                  },
                  {
                    "FIELD_KEY": "0",
                    "FIELD_NAME": "Try again later"
                  }
                ]
              }
            ]
          }
        ]
      },
      {
        "FIELD_KEY": "33",
        "FIELD_NAME": "COMMAND_CLASS_CONTROLLER_REPLICATION",
        "FIELD_DESCRIPTION": "Command Class Controller Replication",
        "COMMANDS": [
          {
            "FIELD_KEY": "52",
            "FIELD_NAME": "CTRL_REPLICATION_TRANSFER_SCENE_NAME",
            "FIELD_DESCRIPTION": "Ctrl Replication Transfer Scene Name",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "2",
                "FIELD_NAME": "Scene Name",
                "FIELD_TYPE": "ARRAY",
                "FIELD_TYPEhashcode": "5",
                "FIELD_ARRAY_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_IS_ASCII": "True",
                  "FIELD_LEN": "255"
                }
              },
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Scene ID",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1"
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Sequence Number",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": [
                  {
                    "FIELD_KEY": "1",
                    "FIELD_HAS_CONSTANTS": "False",
                    "FIELD_IS_HEX": "False"
                  },
                  {
                    "FIELD_KEY": "0",
                    "FIELD_HAS_CONSTANTS": "False",
                    "FIELD_IS_HEX": "False"
                  }
                ]
              }
            ]
          },
          {
            "FIELD_KEY": "51",
            "FIELD_NAME": "CTRL_REPLICATION_TRANSFER_SCENE",
            "FIELD_DESCRIPTION": "Ctrl Replication Transfer Scene",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "3",
                "FIELD_NAME": "Level",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1"
              },
              {
                "FIELD_KEY": "2",
                "FIELD_NAME": "Node ID",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1"
              },
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Scene ID",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1"
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Sequence Number",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": [
                  {
                    "FIELD_KEY": "3",
                    "FIELD_HAS_CONSTANTS": "False",
                    "FIELD_IS_HEX": "False"
                  },
                  {
                    "FIELD_KEY": "2",
                    "FIELD_HAS_CONSTANTS": "False",
                    "FIELD_IS_HEX": "False"
                  },
                  {
                    "FIELD_KEY": "1",
                    "FIELD_HAS_CONSTANTS": "False",
                    "FIELD_IS_HEX": "False"
                  },
                  {
                    "FIELD_KEY": "0",
                    "FIELD_HAS_CONSTANTS": "False",
                    "FIELD_IS_HEX": "False"
                  }
                ]
              }
            ]
          },
          {
            "FIELD_KEY": "50",
            "FIELD_NAME": "CTRL_REPLICATION_TRANSFER_GROUP_NAME",
            "FIELD_DESCRIPTION": "Ctrl Replication Transfer Group Name",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "2",
                "FIELD_NAME": "Group Name",
                "FIELD_TYPE": "ARRAY",
                "FIELD_TYPEhashcode": "5",
                "FIELD_ARRAY_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_IS_ASCII": "True",
                  "FIELD_LEN": "255"
                }
              },
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Group ID",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1"
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Sequence Number",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": [
                  {
                    "FIELD_KEY": "1",
                    "FIELD_HAS_CONSTANTS": "False",
                    "FIELD_IS_HEX": "False"
                  },
                  {
                    "FIELD_KEY": "0",
                    "FIELD_HAS_CONSTANTS": "False",
                    "FIELD_IS_HEX": "False"
                  }
                ]
              }
            ]
          },
          {
            "FIELD_KEY": "49",
            "FIELD_NAME": "CTRL_REPLICATION_TRANSFER_GROUP",
            "FIELD_DESCRIPTION": "Ctrl Replication Transfer Group",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "2",
                "FIELD_NAME": "Node ID",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Group ID",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Sequence Number",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              }
            ]
          }
        ]
      },
      {
        "FIELD_KEY": "32",
        "FIELD_NAME": "COMMAND_CLASS_BASIC",
        "FIELD_DESCRIPTION": "Command Class Basic",
        "COMMANDS": [
          {
            "FIELD_KEY": "3",
            "FIELD_NAME": "BASIC_REPORT",
            "FIELD_DESCRIPTION": "Basic Report",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Value",
              "FIELD_TYPE": "BYTE",
              "FIELD_TYPEhashcode": "1",
              "FIELD_BIT_DEF": [
                {
                  "FIELD_KEY": "2",
                  "FIELD_FLAG_DESCRIPTION": "BASIC_ON",
                  "FIELD_FLAG_MASK": "255"
                },
                {
                  "FIELD_KEY": "1",
                  "FIELD_FLAG_DESCRIPTION": "BASIC_OFF",
                  "FIELD_FLAG_MASK": "0"
                }
              ],
              "FIELD_VALUE_ATTRIBUTES": {
                "FIELD_KEY": "0",
                "FIELD_HAS_CONSTANTS": "True",
                "FIELD_IS_HEX": "False"
              }
            }
          },
          {
            "FIELD_KEY": "2",
            "FIELD_NAME": "BASIC_GET",
            "FIELD_DESCRIPTION": "Basic Get"
          },
          {
            "FIELD_KEY": "1",
            "FIELD_NAME": "BASIC_SET",
            "FIELD_DESCRIPTION": "Basic Set",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Value",
              "FIELD_TYPE": "BYTE",
              "FIELD_TYPEhashcode": "1",
              "FIELD_BIT_DEF": [
                {
                  "FIELD_KEY": "2",
                  "FIELD_FLAG_DESCRIPTION": "BASIC_ON",
                  "FIELD_FLAG_MASK": "255"
                },
                {
                  "FIELD_KEY": "1",
                  "FIELD_FLAG_DESCRIPTION": "BASIC_OFF",
                  "FIELD_FLAG_MASK": "0"
                }
              ],
              "FIELD_VALUE_ATTRIBUTES": {
                "FIELD_KEY": "0",
                "FIELD_HAS_CONSTANTS": "True",
                "FIELD_IS_HEX": "False"
              }
            }
          }
        ]
      },
      {
        "FIELD_KEY": "67",
        "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_SETPOINT",
        "FIELD_DESCRIPTION": "Command Class Thermostat Setpoint",
        "COMMANDS": [
          {
            "FIELD_KEY": "5",
            "FIELD_NAME": "THERMOSTAT_SETPOINT_SUPPORTED_REPORT",
            "FIELD_DESCRIPTION": "Thermostat Setpoint Supported Report",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Setpoint(s) supported",
              "FIELD_TYPE": "BITMASK",
              "FIELD_TYPEhashcode": "6",
              "bitmask": {
                "FIELD_KEY": "0",
                "FIELD_PARAMETER": "255",
                ""FIELD_PARAMETER_DESCRIPTION"": "255",
                "FIELD_PARAMETER_START": "255"
              }
            }
          },
          {
            "FIELD_KEY": "4",
            "FIELD_NAME": "THERMOSTAT_SETPOINT_SUPPORTED_GET",
            "FIELD_DESCRIPTION": "Thermostat Setpoint Supported Get"
          },
          {
            "FIELD_KEY": "3",
            "FIELD_NAME": "THERMOSTAT_SETPOINT_REPORT",
            "FIELD_DESCRIPTION": "Thermostat Setpoint Report",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "2",
                "FIELD_NAME": "Setpoint value",
                "FIELD_TYPE": "VARIANT",
                "FIELD_TYPEhashcode": "12",
                "variant": {
                  "-paramoffs": "1",
                  "FIELD_IS_HEX": "False",
                  "-signed": "True",
                  "-sizemask": "7",
                  "-sizeoffs": "0"
                }
              },
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "SetPoint Porperties",
                "FIELD_TYPE": "STRUCT_BYTE",
                "FIELD_TYPEhashcode": "7",
                "fieldenum": [
                  {
                    "FIELD_KEY": "2",
                    "FIELD_NAME": "Size",
                    "FIELD_BIT_MASK": "7",
                    "FIELD_OFFSET": "0",
                    "fieldenum": [
                      { "FIELD_VALUE": "illegal" },
                      { "FIELD_VALUE": "1 Byte" },
                      { "FIELD_VALUE": "2 Bytes" },
                      { "FIELD_VALUE": "illegal" },
                      { "FIELD_VALUE": "4 Bytes" },
                      { "FIELD_VALUE": "illegal" },
                      { "FIELD_VALUE": "illegal" },
                      { "FIELD_VALUE": "illegal" }
                    ]
                  },
                  {
                    "FIELD_KEY": "1",
                    "FIELD_NAME": "Scale",
                    "FIELD_BIT_MASK": "24",
                    "FIELD_OFFSET": "3",
                    "fieldenum": [
                      { "FIELD_VALUE": "Celsius" },
                      { "FIELD_VALUE": "Fahrenheit" }
                    ]
                  }
                ],
                "bitfield": {
                  "FIELD_KEY": "0",
                  "FIELD_NAME": "Precision",
                  "FIELD_BIT_MASK": "224",
                  "FIELD_OFFSET": "5"
                }
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "SetPoint",
                "FIELD_TYPE": "STRUCT_BYTE",
                "FIELD_TYPEhashcode": "7",
                "fieldenum": {
                  "FIELD_KEY": "0",
                  "FIELD_NAME": "Type",
                  "FIELD_BIT_MASK": "15",
                  "FIELD_OFFSET": "0",
                  "fieldenum": [
                    { "FIELD_VALUE": "Heating #1" },
                    { "FIELD_VALUE": "Cooling #1" },
                    { "FIELD_VALUE": "Furnace" },
                    { "FIELD_VALUE": "Dry Air" },
                    { "FIELD_VALUE": "Moist Air" },
                    { "FIELD_VALUE": "Auto changeover" }
                  ]
                }
              }
            ]
          },
          {
            "FIELD_KEY": "2",
            "FIELD_NAME": "THERMOSTAT_SETPOINT_GET",
            "FIELD_DESCRIPTION": "Thermostat Setpoint Get",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "SetPoint",
              "FIELD_TYPE": "STRUCT_BYTE",
              "FIELD_TYPEhashcode": "7",
              "fieldenum": {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Type",
                "FIELD_BIT_MASK": "15",
                "FIELD_OFFSET": "0",
                "fieldenum": [
                  { "FIELD_VALUE": "Heating #1" },
                  { "FIELD_VALUE": "Cooling #1" },
                  { "FIELD_VALUE": "Furnace" },
                  { "FIELD_VALUE": "Dry Air" },
                  { "FIELD_VALUE": "Moist Air" },
                  { "FIELD_VALUE": "Auto changeover" }
                ]
              }
            }
          },
          {
            "FIELD_KEY": "1",
            "FIELD_NAME": "THERMOSTAT_SETPOINT_SET",
            "FIELD_DESCRIPTION": "Thermostat Setpoint Set",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "2",
                "FIELD_NAME": "Setpoint value",
                "FIELD_TYPE": "VARIANT",
                "FIELD_TYPEhashcode": "12",
                "variant": {
                  "-paramoffs": "1",
                  "FIELD_IS_HEX": "False",
                  "-signed": "True",
                  "-sizemask": "7",
                  "-sizeoffs": "0"
                }
              },
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "SetPoint Porperties",
                "FIELD_TYPE": "STRUCT_BYTE",
                "FIELD_TYPEhashcode": "7",
                "fieldenum": [
                  {
                    "FIELD_KEY": "2",
                    "FIELD_NAME": "Size",
                    "FIELD_BIT_MASK": "7",
                    "FIELD_OFFSET": "0",
                    "fieldenum": [
                      { "FIELD_VALUE": "illegal" },
                      { "FIELD_VALUE": "1 Byte" },
                      { "FIELD_VALUE": "2 Bytes" },
                      { "FIELD_VALUE": "illegal" },
                      { "FIELD_VALUE": "4 Bytes" },
                      { "FIELD_VALUE": "illegal" },
                      { "FIELD_VALUE": "illegal" },
                      { "FIELD_VALUE": "illegal" }
                    ]
                  },
                  {
                    "FIELD_KEY": "1",
                    "FIELD_NAME": "Scale",
                    "FIELD_BIT_MASK": "24",
                    "FIELD_OFFSET": "3",
                    "fieldenum": [
                      { "FIELD_VALUE": "Celsius" },
                      { "FIELD_VALUE": "Fahrenheit" }
                    ]
                  }
                ],
                "bitfield": {
                  "FIELD_KEY": "0",
                  "FIELD_NAME": "Precision",
                  "FIELD_BIT_MASK": "224",
                  "FIELD_OFFSET": "5"
                }
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "SetPoint",
                "FIELD_TYPE": "STRUCT_BYTE",
                "FIELD_TYPEhashcode": "7",
                "fieldenum": {
                  "FIELD_KEY": "0",
                  "FIELD_NAME": "Type",
                  "FIELD_BIT_MASK": "15",
                  "FIELD_OFFSET": "0",
                  "fieldenum": [
                    { "FIELD_VALUE": "Heating #1" },
                    { "FIELD_VALUE": "Cooling #1" },
                    { "FIELD_VALUE": "Furnace" },
                    { "FIELD_VALUE": "Dry Air" },
                    { "FIELD_VALUE": "Moist Air" },
                    { "FIELD_VALUE": "Auto changeover" }
                  ]
                }
              }
            ]
          }
        ]
      },
      {
        "FIELD_KEY": "115",
        "FIELD_NAME": "COMMAND_CLASS_POWERLEVEL",
        "FIELD_DESCRIPTION": "Command Class Powerlevel",
        "COMMANDS": [
          {
            "FIELD_KEY": "6",
            "FIELD_NAME": "POWERLEVEL_TEST_NODE_REPORT",
            "FIELD_DESCRIPTION": "Powerlevel Test Node Report",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "2",
                "FIELD_NAME": "Test frame ACK count",
                "FIELD_TYPE": "WORD",
                "FIELD_TYPEhashcode": "2",
                "word": {
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Status of operation",
                "FIELD_TYPE": "ENUM",
                "FIELD_TYPEhashcode": "8",
                "enum": [
                  {
                    "FIELD_KEY": "2",
                    "FIELD_NAME": "ZW_TEST_INPROGRESS"
                  },
                  {
                    "FIELD_KEY": "1",
                    "FIELD_NAME": "ZW_TEST_SUCCES"
                  },
                  {
                    "FIELD_KEY": "0",
                    "FIELD_NAME": "ZW_TEST_FAILED"
                  }
                ]
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Test NodeID",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "True",
                  "FIELD_IS_HEX": "True"
                }
              }
            ]
          },
          {
            "FIELD_KEY": "5",
            "FIELD_NAME": "POWERLEVEL_TEST_NODE_GET",
            "FIELD_DESCRIPTION": "Powerlevel Test Node Get"
          },
          {
            "FIELD_KEY": "4",
            "FIELD_NAME": "POWERLEVEL_TEST_NODE_SET",
            "FIELD_DESCRIPTION": "Powerlevel Test Node Set",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "2",
                "FIELD_NAME": "Test frame count",
                "FIELD_TYPE": "WORD",
                "FIELD_TYPEhashcode": "2",
                "word": {
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Power Level",
                "FIELD_TYPE": "ENUM",
                "FIELD_TYPEhashcode": "8",
                "enum": [
                  {
                    "FIELD_KEY": "9",
                    "FIELD_NAME": "minus9dB"
                  },
                  {
                    "FIELD_KEY": "8",
                    "FIELD_NAME": "minus8dB"
                  },
                  {
                    "FIELD_KEY": "7",
                    "FIELD_NAME": "minus7dB"
                  },
                  {
                    "FIELD_KEY": "6",
                    "FIELD_NAME": "minus6dB"
                  },
                  {
                    "FIELD_KEY": "5",
                    "FIELD_NAME": "minus5dB"
                  },
                  {
                    "FIELD_KEY": "4",
                    "FIELD_NAME": "minus4dB"
                  },
                  {
                    "FIELD_KEY": "3",
                    "FIELD_NAME": "minus3dB"
                  },
                  {
                    "FIELD_KEY": "2",
                    "FIELD_NAME": "minus2dB"
                  },
                  {
                    "FIELD_KEY": "1",
                    "FIELD_NAME": "minus1dB"
                  },
                  {
                    "FIELD_KEY": "0",
                    "FIELD_NAME": "NormalPower"
                  }
                ]
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Test nodeID",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              }
            ]
          },
          {
            "FIELD_KEY": "3",
            "FIELD_NAME": "POWERLEVEL_REPORT",
            "FIELD_DESCRIPTION": "Powerlevel Report",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Timeout",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Power Level",
                "FIELD_TYPE": "ENUM",
                "FIELD_TYPEhashcode": "8",
                "enum": [
                  {
                    "FIELD_KEY": "9",
                    "FIELD_NAME": "minus9dB"
                  },
                  {
                    "FIELD_KEY": "8",
                    "FIELD_NAME": "minus8dB"
                  },
                  {
                    "FIELD_KEY": "7",
                    "FIELD_NAME": "minus7dB"
                  },
                  {
                    "FIELD_KEY": "6",
                    "FIELD_NAME": "minus6dB"
                  },
                  {
                    "FIELD_KEY": "5",
                    "FIELD_NAME": "minus5dB"
                  },
                  {
                    "FIELD_KEY": "4",
                    "FIELD_NAME": "minus4dB"
                  },
                  {
                    "FIELD_KEY": "3",
                    "FIELD_NAME": "minus3dB"
                  },
                  {
                    "FIELD_KEY": "2",
                    "FIELD_NAME": "minus2dB"
                  },
                  {
                    "FIELD_KEY": "1",
                    "FIELD_NAME": "minus1dB"
                  },
                  {
                    "FIELD_KEY": "0",
                    "FIELD_NAME": "NormalPower"
                  }
                ]
              }
            ]
          },
          {
            "FIELD_KEY": "2",
            "FIELD_NAME": "POWERLEVEL_GET",
            "FIELD_DESCRIPTION": "Powerlevel Get"
          },
          {
            "FIELD_KEY": "1",
            "FIELD_NAME": "POWERLEVEL_SET",
            "FIELD_DESCRIPTION": "Powerlevel Set",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Timeout",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Power Level",
                "FIELD_TYPE": "ENUM",
                "FIELD_TYPEhashcode": "8",
                "enum": [
                  {
                    "FIELD_KEY": "9",
                    "FIELD_NAME": "minus9dB"
                  },
                  {
                    "FIELD_KEY": "8",
                    "FIELD_NAME": "minus8dB"
                  },
                  {
                    "FIELD_KEY": "7",
                    "FIELD_NAME": "minus7dB"
                  },
                  {
                    "FIELD_KEY": "6",
                    "FIELD_NAME": "minus6dB"
                  },
                  {
                    "FIELD_KEY": "5",
                    "FIELD_NAME": "minus5dB"
                  },
                  {
                    "FIELD_KEY": "4",
                    "FIELD_NAME": "minus4dB"
                  },
                  {
                    "FIELD_KEY": "3",
                    "FIELD_NAME": "minus3dB"
                  },
                  {
                    "FIELD_KEY": "2",
                    "FIELD_NAME": "minus2dB"
                  },
                  {
                    "FIELD_KEY": "1",
                    "FIELD_NAME": "minus1dB"
                  },
                  {
                    "FIELD_KEY": "0",
                    "FIELD_NAME": "NormalPower"
                  }
                ]
              }
            ]
          }
        ]
      },
      {
        "FIELD_KEY": "118",
        "FIELD_NAME": "COMMAND_CLASS_LOCK",
        "FIELD_DESCRIPTION": "Command Class Lock",
        "COMMANDS": [
          {
            "FIELD_KEY": "3",
            "FIELD_NAME": "LOCK_REPORT",
            "FIELD_DESCRIPTION": "Lock Report",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Lock state",
              "FIELD_TYPE": "ENUM",
              "FIELD_TYPEhashcode": "8",
              "enum": [
                {
                  "FIELD_KEY": "1",
                  "FIELD_NAME": "Locked"
                },
                {
                  "FIELD_KEY": "0",
                  "FIELD_NAME": "Unlocked"
                }
              ]
            }
          },
          {
            "FIELD_KEY": "2",
            "FIELD_NAME": "LOCK_GET",
            "FIELD_DESCRIPTION": "Lock Get"
          },
          {
            "FIELD_KEY": "1",
            "FIELD_NAME": "LOCK_SET",
            "FIELD_DESCRIPTION": "Lock Set",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Lock state",
              "FIELD_TYPE": "ENUM",
              "FIELD_TYPEhashcode": "8",
              "enum": [
                {
                  "FIELD_KEY": "1",
                  "FIELD_NAME": "Locked"
                },
                {
                  "FIELD_KEY": "0",
                  "FIELD_NAME": "Unlocked"
                }
              ]
            }
          }
        ]
      },
      {
        "FIELD_KEY": "117",
        "FIELD_NAME": "COMMAND_CLASS_PROTECTION",
        "FIELD_DESCRIPTION": "Command Class Protection",
        "COMMANDS": [
          {
            "FIELD_KEY": "3",
            "FIELD_NAME": "PROTECTION_REPORT",
            "FIELD_DESCRIPTION": "Protection Report",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Protection State",
              "FIELD_TYPE": "ENUM",
              "FIELD_TYPEhashcode": "8",
              "enum": [
                {
                  "FIELD_KEY": "2",
                  "FIELD_NAME": "No operation possible"
                },
                {
                  "FIELD_KEY": "1",
                  "FIELD_NAME": "Protection by sequence"
                },
                {
                  "FIELD_KEY": "0",
                  "FIELD_NAME": "Unprotected"
                }
              ]
            }
          },
          {
            "FIELD_KEY": "2",
            "FIELD_NAME": "PROTECTION_GET",
            "FIELD_DESCRIPTION": "Protection Get"
          },
          {
            "FIELD_KEY": "1",
            "FIELD_NAME": "PROTECTION_SET",
            "FIELD_DESCRIPTION": "Protection Set",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Protection State",
              "FIELD_TYPE": "ENUM",
              "FIELD_TYPEhashcode": "8",
              "enum": [
                {
                  "FIELD_KEY": "2",
                  "FIELD_NAME": "No operation possible"
                },
                {
                  "FIELD_KEY": "1",
                  "FIELD_NAME": "Protection by sequence"
                },
                {
                  "FIELD_KEY": "0",
                  "FIELD_NAME": "Unprotected"
                }
              ]
            }
          }
        ]
      },
      {
        "FIELD_KEY": "68",
        "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_FAN_MODE",
        "FIELD_DESCRIPTION": "Command Class Thermostat Fan Mode",
        "COMMANDS": [
          {
            "FIELD_KEY": "5",
            "FIELD_NAME": "THERMOSTAT_FAN_MODE_SUPPORTED_REPORT",
            "FIELD_DESCRIPTION": "Thermostat Fan Mode Supported Report",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Fan Mode(s) supported",
              "FIELD_TYPE": "BITMASK",
              "FIELD_TYPEhashcode": "6",
              "bitmask": {
                "FIELD_KEY": "0",
                "FIELD_PARAMETER": "255",
                ""FIELD_PARAMETER_DESCRIPTION"": "255",
                "FIELD_PARAMETER_START": "255"
              }
            }
          },
          {
            "FIELD_KEY": "4",
            "FIELD_NAME": "THERMOSTAT_FAN_MODE_SUPPORTED_GET",
            "FIELD_DESCRIPTION": "Thermostat Fan Mode Supported Get"
          },
          {
            "FIELD_KEY": "3",
            "FIELD_NAME": "THERMOSTAT_FAN_MODE_REPORT",
            "FIELD_DESCRIPTION": "Thermostat Fan Mode Report",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Fan",
              "FIELD_TYPE": "STRUCT_BYTE",
              "FIELD_TYPEhashcode": "7",
              "fieldenum": {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Mode",
                "FIELD_BIT_MASK": "15",
                "FIELD_OFFSET": "0",
                "fieldenum": [
                  { "FIELD_VALUE": "Auto/Auto Low" },
                  { "FIELD_VALUE": "On /On Low" },
                  { "FIELD_VALUE": "Auto High" },
                  { "FIELD_VALUE": "On High" }
                ]
              }
            }
          },
          {
            "FIELD_KEY": "2",
            "FIELD_NAME": "THERMOSTAT_FAN_MODE_GET",
            "FIELD_DESCRIPTION": "Thermostat Fan Mode Get"
          },
          {
            "FIELD_KEY": "1",
            "FIELD_NAME": "THERMOSTAT_FAN_MODE_SET",
            "FIELD_DESCRIPTION": "Thermostat Fan Mode Set",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Fan",
              "FIELD_TYPE": "STRUCT_BYTE",
              "FIELD_TYPEhashcode": "7",
              "fieldenum": {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Mode",
                "FIELD_BIT_MASK": "15",
                "FIELD_OFFSET": "0",
                "fieldenum": [
                  { "FIELD_VALUE": "Auto/Auto Low" },
                  { "FIELD_VALUE": "On /On Low" },
                  { "FIELD_VALUE": "Auto High" },
                  { "FIELD_VALUE": "On High" }
                ]
              }
            }
          }
        ]
      },
      {
        "FIELD_KEY": "114",
        "FIELD_NAME": "COMMAND_CLASS_MANUFACTURER_SPECIFIC",
        "FIELD_DESCRIPTION": "Command Class Manufacturer Specific",
        "COMMANDS": [
          {
            "FIELD_KEY": "5",
            "FIELD_NAME": "MANUFACTURER_SPECIFIC_REPORT",
            "FIELD_DESCRIPTION": "Manufacturer Specific Report",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "2",
                "FIELD_NAME": "Product ID",
                "FIELD_TYPE": "WORD",
                "FIELD_TYPEhashcode": "2",
                "word": {
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "True"
                }
              },
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Product Type ID",
                "FIELD_TYPE": "WORD",
                "FIELD_TYPEhashcode": "2",
                "word": {
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "True"
                }
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Manufacturer ID",
                "FIELD_TYPE": "WORD",
                "FIELD_TYPEhashcode": "2",
                "word": {
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "True"
                }
              }
            ]
          },
          {
            "FIELD_KEY": "4",
            "FIELD_NAME": "MANUFACTURER_SPECIFIC_GET",
            "FIELD_DESCRIPTION": "Manufacturer Specific Get"
          }
        ]
      },
      {
        "FIELD_KEY": "113",
        "FIELD_NAME": "COMMAND_CLASS_ALARM",
        "FIELD_DESCRIPTION": "Command Class Alarm",
        "COMMANDS": [
          {
            "FIELD_KEY": "5",
            "FIELD_NAME": "ALARM_REPORT",
            "FIELD_DESCRIPTION": "Alarm Report",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Alarm level",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Alarm Type",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "True"
                }
              }
            ]
          },
          {
            "FIELD_KEY": "4",
            "FIELD_NAME": "ALARM_GET",
            "FIELD_DESCRIPTION": "Alarm Get",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Alarm Type",
              "FIELD_TYPE": "BYTE",
              "FIELD_TYPEhashcode": "1",
              "FIELD_VALUE_ATTRIBUTES": {
                "FIELD_KEY": "0",
                "FIELD_HAS_CONSTANTS": "False",
                "FIELD_IS_HEX": "True"
              }
            }
          }
        ]
      },
      {
        "FIELD_KEY": "112",
        "FIELD_NAME": "COMMAND_CLASS_CONFIGURATION",
        "FIELD_DESCRIPTION": "Command Class Configuration",
        "COMMANDS": [
          {
            "FIELD_KEY": "6",
            "FIELD_NAME": "CONFIGURATION_REPORT",
            "FIELD_DESCRIPTION": "Configuration Report",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "2",
                "FIELD_NAME": "Configuration Value",
                "FIELD_TYPE": "VARIANT",
                "FIELD_TYPEhashcode": "12",
                "variant": {
                  "-paramoffs": "1",
                  "FIELD_IS_HEX": "False",
                  "-signed": "True",
                  "-sizemask": "7",
                  "-sizeoffs": "0"
                }
              },
              {
                "FIELD_KEY": "1",
                "FIELD_TYPE": "STRUCT_BYTE",
                "FIELD_TYPEhashcode": "7",
                "bitfield": [
                  {
                    "FIELD_KEY": "1",
                    "FIELD_NAME": "Size",
                    "FIELD_BIT_MASK": "7",
                    "FIELD_OFFSET": "0"
                  },
                  {
                    "FIELD_KEY": "0",
                    "FIELD_NAME": "Reserved",
                    "FIELD_BIT_MASK": "248",
                    "FIELD_OFFSET": "3"
                  }
                ]
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Parameter Number",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              }
            ]
          },
          {
            "FIELD_KEY": "5",
            "FIELD_NAME": "CONFIGURATION_GET",
            "FIELD_DESCRIPTION": "Configuration Get",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Parameter Number",
              "FIELD_TYPE": "BYTE",
              "FIELD_TYPEhashcode": "1",
              "FIELD_VALUE_ATTRIBUTES": {
                "FIELD_KEY": "0",
                "FIELD_HAS_CONSTANTS": "False",
                "FIELD_IS_HEX": "False"
              }
            }
          },
          {
            "FIELD_KEY": "4",
            "FIELD_NAME": "CONFIGURATION_SET",
            "FIELD_DESCRIPTION": "Configuration Set",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "2",
                "FIELD_NAME": "Configuration Value",
                "FIELD_TYPE": "VARIANT",
                "FIELD_TYPEhashcode": "12",
                "variant": {
                  "-paramoffs": "1",
                  "FIELD_IS_HEX": "False",
                  "-signed": "True",
                  "-sizemask": "7",
                  "-sizeoffs": "0"
                }
              },
              {
                "FIELD_KEY": "1",
                "FIELD_TYPE": "STRUCT_BYTE",
                "FIELD_TYPEhashcode": "7",
                "bitfield": [
                  {
                    "FIELD_KEY": "2",
                    "FIELD_NAME": "Size",
                    "FIELD_BIT_MASK": "7",
                    "FIELD_OFFSET": "0"
                  },
                  {
                    "FIELD_KEY": "1",
                    "FIELD_NAME": "Reserved",
                    "FIELD_BIT_MASK": "120",
                    "FIELD_OFFSET": "3"
                  }
                ],
                "FIELD_BIT_DEF": {
                  "FIELD_KEY": "0",
                  "FIELD_FLAG_DESCRIPTION": "Default",
                  "FIELD_FLAG_MASK": "128"
                }
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Parameter Number",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              }
            ]
          }
        ]
      },
      {
        "FIELD_KEY": "64",
        "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_MODE",
        "FIELD_DESCRIPTION": "Command Class Thermostat Mode",
        "COMMANDS": [
          {
            "FIELD_KEY": "5",
            "FIELD_NAME": "THERMOSTAT_MODE_SUPPORTED_REPORT",
            "FIELD_DESCRIPTION": "Thermostat Mode Supported Report",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Modes Supported",
              "FIELD_TYPE": "BITMASK",
              "FIELD_TYPEhashcode": "6",
              "bitmask": {
                "FIELD_KEY": "0",
                "FIELD_PARAMETER": "255",
                ""FIELD_PARAMETER_DESCRIPTION"": "255",
                "FIELD_PARAMETER_START": "255"
              }
            }
          },
          {
            "FIELD_KEY": "4",
            "FIELD_NAME": "THERMOSTAT_MODE_SUPPORTED_GET",
            "FIELD_DESCRIPTION": "Thermostat Mode Supported Get"
          },
          {
            "FIELD_KEY": "3",
            "FIELD_NAME": "THERMOSTAT_MODE_REPORT",
            "FIELD_DESCRIPTION": "Thermostat Mode Report",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Mode",
              "FIELD_TYPE": "STRUCT_BYTE",
              "FIELD_TYPEhashcode": "7",
              "fieldenum": {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Mode",
                "FIELD_BIT_MASK": "31",
                "FIELD_OFFSET": "0",
                "fieldenum": [
                  { "FIELD_VALUE": "Off" },
                  { "FIELD_VALUE": "Heat" },
                  { "FIELD_VALUE": "Cool" },
                  { "FIELD_VALUE": "Auto" },
                  { "FIELD_VALUE": "Auxiliary/Emergency heat" },
                  { "FIELD_VALUE": "Resume" },
                  { "FIELD_VALUE": "Fan Only" },
                  { "FIELD_VALUE": "Furnace" },
                  { "FIELD_VALUE": "Dry Air" },
                  { "FIELD_VALUE": "Moist air" },
                  { "FIELD_VALUE": "Auto changeover" }
                ]
              }
            }
          },
          {
            "FIELD_KEY": "2",
            "FIELD_NAME": "THERMOSTAT_MODE_GET",
            "FIELD_DESCRIPTION": "Thermostat Mode Get"
          },
          {
            "FIELD_KEY": "1",
            "FIELD_NAME": "THERMOSTAT_MODE_SET",
            "FIELD_DESCRIPTION": "Thermostat Mode Set",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Mode",
              "FIELD_TYPE": "STRUCT_BYTE",
              "FIELD_TYPEhashcode": "7",
              "fieldenum": {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Mode",
                "FIELD_BIT_MASK": "31",
                "FIELD_OFFSET": "0",
                "fieldenum": [
                  { "FIELD_VALUE": "Off" },
                  { "FIELD_VALUE": "Heat" },
                  { "FIELD_VALUE": "Cool" },
                  { "FIELD_VALUE": "Auto" },
                  { "FIELD_VALUE": "Auxiliary/Emergency heat" },
                  { "FIELD_VALUE": "Resume" },
                  { "FIELD_VALUE": "Fan Only" },
                  { "FIELD_VALUE": "Furnace" },
                  { "FIELD_VALUE": "Dry Air" },
                  { "FIELD_VALUE": "Moist air" },
                  { "FIELD_VALUE": "Auto changeover" }
                ]
              }
            }
          }
        ]
      },
      {
        "FIELD_KEY": "80",
        "FIELD_NAME": "COMMAND_CLASS_BASIC_WINDOW_COVERING",
        "FIELD_DESCRIPTION": "Command Class Basic Window Covering",
        "COMMANDS": [
          {
            "FIELD_KEY": "2",
            "FIELD_NAME": "BASIC_WINDOW_COVERING_STOP_LEVEL_CHANGE",
            "FIELD_DESCRIPTION": "Basic Window Covering Stop Level Change"
          },
          {
            "FIELD_KEY": "1",
            "FIELD_NAME": "BASIC_WINDOW_COVERING_START_LEVEL_CHANGE",
            "FIELD_DESCRIPTION": "Basic Window Covering Start Level Change",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_TYPE": "STRUCT_BYTE",
              "FIELD_TYPEhashcode": "7",
              "bitfield": {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Reserved",
                "FIELD_BIT_MASK": "63",
                "FIELD_OFFSET": "0"
              },
              "FIELD_BIT_DEF": {
                "FIELD_KEY": "0",
                "FIELD_FLAG_DESCRIPTION": "Reserved",
                "FIELD_FLAG_MASK": "128"
              }
            }
          }
        ]
      },
      {
        "FIELD_KEY": "96",
        "FIELD_NAME": "COMMAND_CLASS_MULTI_INSTANCE",
        "FIELD_DESCRIPTION": "Command Class Multi Instance",
        "COMMANDS": [
          {
            "FIELD_KEY": "6",
            "FIELD_NAME": "MULTI_INSTANCE_CMD_ENCAP",
            "FIELD_DESCRIPTION": "Multi Instance Cmd Encap",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "3",
                "FIELD_NAME": "Parameter(s)",
                "FIELD_TYPE": "ARRAY",
                "FIELD_TYPEhashcode": "5",
                "FIELD_ARRAY_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_IS_ASCII": "False",
                  "FIELD_LEN": "255"
                }
              },
              {
                "FIELD_KEY": "2",
                "FIELD_NAME": "Command",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "True"
                }
              },
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Command class",
                "FIELD_TYPE": "ENUM",
                "FIELD_TYPEhashcode": "8",
                "enum": [
                  {
                    "FIELD_KEY": "96",
                    "FIELD_NAME": "COMMAND_CLASS_MULTI_INSTANCE"
                  },
                  {
                    "FIELD_KEY": "81",
                    "FIELD_NAME": "COMMAND_CLASS_MTP_WINDOW_COVERING"
                  },
                  {
                    "FIELD_KEY": "80",
                    "FIELD_NAME": "COMMAND_CLASS_BASIC_WINDOW_COVERING"
                  },
                  {
                    "FIELD_KEY": "69",
                    "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_FAN_STATE"
                  },
                  {
                    "FIELD_KEY": "68",
                    "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_FAN_MODE"
                  },
                  {
                    "FIELD_KEY": "67",
                    "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_SETPOINT"
                  },
                  {
                    "FIELD_KEY": "66",
                    "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_OPERATING_STATE"
                  },
                  {
                    "FIELD_KEY": "64",
                    "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_MODE"
                  },
                  {
                    "FIELD_KEY": "56",
                    "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT"
                  },
                  {
                    "FIELD_KEY": "53",
                    "FIELD_NAME": "COMMAND_CLASS_METER_PULSE"
                  },
                  {
                    "FIELD_KEY": "49",
                    "FIELD_NAME": "COMMAND_CLASS_SENSOR_MULTILEVEL"
                  },
                  {
                    "FIELD_KEY": "48",
                    "FIELD_NAME": "COMMAND_CLASS_SENSOR_BINARY"
                  },
                  {
                    "FIELD_KEY": "144",
                    "FIELD_NAME": "COMMAND_CLASS_ENERGY_PRODUCTION"
                  },
                  {
                    "FIELD_KEY": "42",
                    "FIELD_NAME": "COMMAND_CLASS_CHIMNEY_FAN"
                  },
                  {
                    "FIELD_KEY": "41",
                    "FIELD_NAME": "COMMAND_CLASS_SWITCH_TOGGLE_MULTILEVEL"
                  },
                  {
                    "FIELD_KEY": "40",
                    "FIELD_NAME": "COMMAND_CLASS_SWITCH_TOGGLE_BINARY"
                  },
                  {
                    "FIELD_KEY": "39",
                    "FIELD_NAME": "COMMAND_CLASS_SWITCH_ALL"
                  },
                  {
                    "FIELD_KEY": "38",
                    "FIELD_NAME": "COMMAND_CLASS_SWITCH_MULTILEVEL"
                  },
                  {
                    "FIELD_KEY": "37",
                    "FIELD_NAME": "COMMAND_CLASS_SWITCH_BINARY"
                  },
                  {
                    "FIELD_KEY": "34",
                    "FIELD_NAME": "COMMAND_CLASS_APPLICATION_STATUS"
                  },
                  {
                    "FIELD_KEY": "33",
                    "FIELD_NAME": "COMMAND_CLASS_CONTROLLER_REPLICATION"
                  },
                  {
                    "FIELD_KEY": "32",
                    "FIELD_NAME": "COMMAND_CLASS_BASIC"
                  },
                  {
                    "FIELD_KEY": "137",
                    "FIELD_NAME": "COMMAND_CLASS_LANGUAGE"
                  },
                  {
                    "FIELD_KEY": "136",
                    "FIELD_NAME": "COMMAND_CLASS_PROPRIETARY"
                  },
                  {
                    "FIELD_KEY": "135",
                    "FIELD_NAME": "COMMAND_CLASS_INDICATOR"
                  },
                  {
                    "FIELD_KEY": "134",
                    "FIELD_NAME": "COMMAND_CLASS_VERSION"
                  },
                  {
                    "FIELD_KEY": "133",
                    "FIELD_NAME": "COMMAND_CLASS_ASSOCIATION"
                  },
                  {
                    "FIELD_KEY": "132",
                    "FIELD_NAME": "COMMAND_CLASS_WAKE_UP"
                  },
                  {
                    "FIELD_KEY": "131",
                    "FIELD_NAME": "COMMAND_CLASS_NETWORK_STAT"
                  },
                  {
                    "FIELD_KEY": "129",
                    "FIELD_NAME": "COMMAND_CLASS_CLOCK"
                  },
                  {
                    "FIELD_KEY": "128",
                    "FIELD_NAME": "COMMAND_CLASS_BATTERY"
                  },
                  {
                    "FIELD_KEY": "14",
                    "FIELD_NAME": "REQUEST_NODE_INFO"
                  },
                  {
                    "FIELD_KEY": "13",
                    "FIELD_NAME": "DELETE_ROUTE"
                  },
                  {
                    "FIELD_KEY": "12",
                    "FIELD_NAME": "ASSIGN_ROUTE"
                  },
                  {
                    "FIELD_KEY": "118",
                    "FIELD_NAME": "COMMAND_CLASS_LOCK"
                  },
                  {
                    "FIELD_KEY": "117",
                    "FIELD_NAME": "COMMAND_CLASS_PROTECTION"
                  },
                  {
                    "FIELD_KEY": "115",
                    "FIELD_NAME": "COMMAND_CLASS_POWERLEVEL"
                  },
                  {
                    "FIELD_KEY": "114",
                    "FIELD_NAME": "COMMAND_CLASS_MANUFACTURER_SPECIFIC"
                  },
                  {
                    "FIELD_KEY": "113",
                    "FIELD_NAME": "COMMAND_CLASS_ALARM"
                  },
                  {
                    "FIELD_KEY": "112",
                    "FIELD_NAME": "COMMAND_CLASS_CONFIGURATION"
                  }
                ]
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Instance",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              }
            ]
          },
          {
            "FIELD_KEY": "5",
            "FIELD_NAME": "MULTI_INSTANCE_REPORT",
            "FIELD_DESCRIPTION": "Multi Instance Report",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Instances",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1"
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Command class",
                "FIELD_TYPE": "ENUM",
                "FIELD_TYPEhashcode": "8",
                "enum": [
                  {
                    "FIELD_KEY": "96",
                    "FIELD_NAME": "COMMAND_CLASS_MULTI_INSTANCE"
                  },
                  {
                    "FIELD_KEY": "81",
                    "FIELD_NAME": "COMMAND_CLASS_MTP_WINDOW_COVERING"
                  },
                  {
                    "FIELD_KEY": "80",
                    "FIELD_NAME": "COMMAND_CLASS_BASIC_WINDOW_COVERING"
                  },
                  {
                    "FIELD_KEY": "69",
                    "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_FAN_STATE"
                  },
                  {
                    "FIELD_KEY": "68",
                    "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_FAN_MODE"
                  },
                  {
                    "FIELD_KEY": "67",
                    "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_SETPOINT"
                  },
                  {
                    "FIELD_KEY": "66",
                    "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_OPERATING_STATE"
                  },
                  {
                    "FIELD_KEY": "64",
                    "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_MODE"
                  },
                  {
                    "FIELD_KEY": "56",
                    "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT"
                  },
                  {
                    "FIELD_KEY": "53",
                    "FIELD_NAME": "COMMAND_CLASS_METER_PULSE"
                  },
                  {
                    "FIELD_KEY": "49",
                    "FIELD_NAME": "COMMAND_CLASS_SENSOR_MULTILEVEL"
                  },
                  {
                    "FIELD_KEY": "48",
                    "FIELD_NAME": "COMMAND_CLASS_SENSOR_BINARY"
                  },
                  {
                    "FIELD_KEY": "144",
                    "FIELD_NAME": "COMMAND_CLASS_ENERGY_PRODUCTION"
                  },
                  {
                    "FIELD_KEY": "42",
                    "FIELD_NAME": "COMMAND_CLASS_CHIMNEY_FAN"
                  },
                  {
                    "FIELD_KEY": "41",
                    "FIELD_NAME": "COMMAND_CLASS_SWITCH_TOGGLE_MULTILEVEL"
                  },
                  {
                    "FIELD_KEY": "40",
                    "FIELD_NAME": "COMMAND_CLASS_SWITCH_TOGGLE_BINARY"
                  },
                  {
                    "FIELD_KEY": "39",
                    "FIELD_NAME": "COMMAND_CLASS_SWITCH_ALL"
                  },
                  {
                    "FIELD_KEY": "38",
                    "FIELD_NAME": "COMMAND_CLASS_SWITCH_MULTILEVEL"
                  },
                  {
                    "FIELD_KEY": "37",
                    "FIELD_NAME": "COMMAND_CLASS_SWITCH_BINARY"
                  },
                  {
                    "FIELD_KEY": "34",
                    "FIELD_NAME": "COMMAND_CLASS_APPLICATION_STATUS"
                  },
                  {
                    "FIELD_KEY": "33",
                    "FIELD_NAME": "COMMAND_CLASS_CONTROLLER_REPLICATION"
                  },
                  {
                    "FIELD_KEY": "32",
                    "FIELD_NAME": "COMMAND_CLASS_BASIC"
                  },
                  {
                    "FIELD_KEY": "137",
                    "FIELD_NAME": "COMMAND_CLASS_LANGUAGE"
                  },
                  {
                    "FIELD_KEY": "136",
                    "FIELD_NAME": "COMMAND_CLASS_PROPRIETARY"
                  },
                  {
                    "FIELD_KEY": "135",
                    "FIELD_NAME": "COMMAND_CLASS_INDICATOR"
                  },
                  {
                    "FIELD_KEY": "134",
                    "FIELD_NAME": "COMMAND_CLASS_VERSION"
                  },
                  {
                    "FIELD_KEY": "133",
                    "FIELD_NAME": "COMMAND_CLASS_ASSOCIATION"
                  },
                  {
                    "FIELD_KEY": "132",
                    "FIELD_NAME": "COMMAND_CLASS_WAKE_UP"
                  },
                  {
                    "FIELD_KEY": "131",
                    "FIELD_NAME": "COMMAND_CLASS_NETWORK_STAT"
                  },
                  {
                    "FIELD_KEY": "129",
                    "FIELD_NAME": "COMMAND_CLASS_CLOCK"
                  },
                  {
                    "FIELD_KEY": "128",
                    "FIELD_NAME": "COMMAND_CLASS_BATTERY"
                  },
                  {
                    "FIELD_KEY": "14",
                    "FIELD_NAME": "REQUEST_NODE_INFO"
                  },
                  {
                    "FIELD_KEY": "13",
                    "FIELD_NAME": "DELETE_ROUTE"
                  },
                  {
                    "FIELD_KEY": "12",
                    "FIELD_NAME": "ASSIGN_ROUTE"
                  },
                  {
                    "FIELD_KEY": "118",
                    "FIELD_NAME": "COMMAND_CLASS_LOCK"
                  },
                  {
                    "FIELD_KEY": "117",
                    "FIELD_NAME": "COMMAND_CLASS_PROTECTION"
                  },
                  {
                    "FIELD_KEY": "115",
                    "FIELD_NAME": "COMMAND_CLASS_POWERLEVEL"
                  },
                  {
                    "FIELD_KEY": "114",
                    "FIELD_NAME": "COMMAND_CLASS_MANUFACTURER_SPECIFIC"
                  },
                  {
                    "FIELD_KEY": "113",
                    "FIELD_NAME": "COMMAND_CLASS_ALARM"
                  },
                  {
                    "FIELD_KEY": "112",
                    "FIELD_NAME": "COMMAND_CLASS_CONFIGURATION"
                  }
                ],
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              }
            ]
          },
          {
            "FIELD_KEY": "4",
            "FIELD_NAME": "MULTI_INSTANCE_GET",
            "FIELD_DESCRIPTION": "Multi Instance Get",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Command class",
              "FIELD_TYPE": "ENUM",
              "FIELD_TYPEhashcode": "8",
              "enum": [
                {
                  "FIELD_KEY": "96",
                  "FIELD_NAME": "COMMAND_CLASS_MULTI_INSTANCE"
                },
                {
                  "FIELD_KEY": "81",
                  "FIELD_NAME": "COMMAND_CLASS_MTP_WINDOW_COVERING"
                },
                {
                  "FIELD_KEY": "80",
                  "FIELD_NAME": "COMMAND_CLASS_BASIC_WINDOW_COVERING"
                },
                {
                  "FIELD_KEY": "69",
                  "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_FAN_STATE"
                },
                {
                  "FIELD_KEY": "68",
                  "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_FAN_MODE"
                },
                {
                  "FIELD_KEY": "67",
                  "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_SETPOINT"
                },
                {
                  "FIELD_KEY": "66",
                  "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_OPERATING_STATE"
                },
                {
                  "FIELD_KEY": "64",
                  "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_MODE"
                },
                {
                  "FIELD_KEY": "56",
                  "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT"
                },
                {
                  "FIELD_KEY": "53",
                  "FIELD_NAME": "COMMAND_CLASS_METER_PULSE"
                },
                {
                  "FIELD_KEY": "49",
                  "FIELD_NAME": "COMMAND_CLASS_SENSOR_MULTILEVEL"
                },
                {
                  "FIELD_KEY": "48",
                  "FIELD_NAME": "COMMAND_CLASS_SENSOR_BINARY"
                },
                {
                  "FIELD_KEY": "144",
                  "FIELD_NAME": "COMMAND_CLASS_ENERGY_PRODUCTION"
                },
                {
                  "FIELD_KEY": "42",
                  "FIELD_NAME": "COMMAND_CLASS_CHIMNEY_FAN"
                },
                {
                  "FIELD_KEY": "41",
                  "FIELD_NAME": "COMMAND_CLASS_SWITCH_TOGGLE_MULTILEVEL"
                },
                {
                  "FIELD_KEY": "40",
                  "FIELD_NAME": "COMMAND_CLASS_SWITCH_TOGGLE_BINARY"
                },
                {
                  "FIELD_KEY": "39",
                  "FIELD_NAME": "COMMAND_CLASS_SWITCH_ALL"
                },
                {
                  "FIELD_KEY": "38",
                  "FIELD_NAME": "COMMAND_CLASS_SWITCH_MULTILEVEL"
                },
                {
                  "FIELD_KEY": "37",
                  "FIELD_NAME": "COMMAND_CLASS_SWITCH_BINARY"
                },
                {
                  "FIELD_KEY": "34",
                  "FIELD_NAME": "COMMAND_CLASS_APPLICATION_STATUS"
                },
                {
                  "FIELD_KEY": "33",
                  "FIELD_NAME": "COMMAND_CLASS_CONTROLLER_REPLICATION"
                },
                {
                  "FIELD_KEY": "32",
                  "FIELD_NAME": "COMMAND_CLASS_BASIC"
                },
                {
                  "FIELD_KEY": "137",
                  "FIELD_NAME": "COMMAND_CLASS_LANGUAGE"
                },
                {
                  "FIELD_KEY": "136",
                  "FIELD_NAME": "COMMAND_CLASS_PROPRIETARY"
                },
                {
                  "FIELD_KEY": "135",
                  "FIELD_NAME": "COMMAND_CLASS_INDICATOR"
                },
                {
                  "FIELD_KEY": "134",
                  "FIELD_NAME": "COMMAND_CLASS_VERSION"
                },
                {
                  "FIELD_KEY": "133",
                  "FIELD_NAME": "COMMAND_CLASS_ASSOCIATION"
                },
                {
                  "FIELD_KEY": "132",
                  "FIELD_NAME": "COMMAND_CLASS_WAKE_UP"
                },
                {
                  "FIELD_KEY": "131",
                  "FIELD_NAME": "COMMAND_CLASS_NETWORK_STAT"
                },
                {
                  "FIELD_KEY": "129",
                  "FIELD_NAME": "COMMAND_CLASS_CLOCK"
                },
                {
                  "FIELD_KEY": "128",
                  "FIELD_NAME": "COMMAND_CLASS_BATTERY"
                },
                {
                  "FIELD_KEY": "14",
                  "FIELD_NAME": "REQUEST_NODE_INFO"
                },
                {
                  "FIELD_KEY": "13",
                  "FIELD_NAME": "DELETE_ROUTE"
                },
                {
                  "FIELD_KEY": "12",
                  "FIELD_NAME": "ASSIGN_ROUTE"
                },
                {
                  "FIELD_KEY": "118",
                  "FIELD_NAME": "COMMAND_CLASS_LOCK"
                },
                {
                  "FIELD_KEY": "117",
                  "FIELD_NAME": "COMMAND_CLASS_PROTECTION"
                },
                {
                  "FIELD_KEY": "115",
                  "FIELD_NAME": "COMMAND_CLASS_POWERLEVEL"
                },
                {
                  "FIELD_KEY": "114",
                  "FIELD_NAME": "COMMAND_CLASS_MANUFACTURER_SPECIFIC"
                },
                {
                  "FIELD_KEY": "113",
                  "FIELD_NAME": "COMMAND_CLASS_ALARM"
                },
                {
                  "FIELD_KEY": "112",
                  "FIELD_NAME": "COMMAND_CLASS_CONFIGURATION"
                }
              ]
            }
          }
        ]
      },
      {
        "FIELD_KEY": "53",
        "FIELD_NAME": "COMMAND_CLASS_METER_PULSE",
        "FIELD_DESCRIPTION": "Command Class Meter Pulse",
        "COMMANDS": [
          {
            "FIELD_KEY": "5",
            "FIELD_NAME": "METER_PULSE_REPORT",
            "FIELD_DESCRIPTION": "Meter Pulse Report",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Pulse Count",
              "FIELD_TYPE": "DWORD",
              "FIELD_TYPEhashcode": "3",
              "dword": {
                "FIELD_KEY": "0",
                "FIELD_HAS_CONSTANTS": "False",
                "FIELD_IS_HEX": "False"
              }
            }
          },
          {
            "FIELD_KEY": "4",
            "FIELD_NAME": "METER_PULSE_GET",
            "FIELD_DESCRIPTION": "Meter Pulse Get"
          }
        ]
      },
      {
        "FIELD_KEY": "128",
        "FIELD_NAME": "COMMAND_CLASS_BATTERY",
        "FIELD_DESCRIPTION": "Command Class Battery",
        "COMMANDS": [
          {
            "FIELD_KEY": "3",
            "FIELD_NAME": "BATTERY_REPORT",
            "FIELD_DESCRIPTION": "Battery Report",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Battery level(%)",
              "FIELD_TYPE": "BYTE",
              "FIELD_TYPEhashcode": "1",
              "FIELD_BIT_DEF": {
                "FIELD_KEY": "1",
                "FIELD_FLAG_DESCRIPTION": "battery low",
                "FIELD_FLAG_MASK": "255"
              },
              "FIELD_VALUE_ATTRIBUTES": {
                "FIELD_KEY": "0",
                "FIELD_HAS_CONSTANTS": "True",
                "FIELD_IS_HEX": "False"
              }
            }
          },
          {
            "FIELD_KEY": "2",
            "FIELD_NAME": "BATTERY_GET",
            "FIELD_DESCRIPTION": "Battery Get"
          }
        ]
      },
      {
        "FIELD_KEY": "144",
        "FIELD_NAME": "COMMAND_CLASS_ENERGY_PRODUCTION",
        "FIELD_DESCRIPTION": "Command Class Energy Production",
        "COMMANDS": [
          {
            "FIELD_KEY": "3",
            "FIELD_NAME": "ENERGY_PRODUCTION_REPORT",
            "FIELD_DESCRIPTION": "Energy Production Report",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "2",
                "FIELD_NAME": "Value",
                "FIELD_TYPE": "VARIANT",
                "FIELD_TYPEhashcode": "12",
                "variant": {
                  "-paramoffs": "1",
                  "FIELD_IS_HEX": "False",
                  "-signed": "True",
                  "-sizemask": "7",
                  "-sizeoffs": "0"
                }
              },
              {
                "FIELD_KEY": "1",
                "FIELD_TYPE": "STRUCT_BYTE",
                "FIELD_TYPEhashcode": "7",
                "bitfield": [
                  {
                    "FIELD_KEY": "2",
                    "FIELD_NAME": "Size",
                    "FIELD_BIT_MASK": "7",
                    "FIELD_OFFSET": "0"
                  },
                  {
                    "FIELD_KEY": "1",
                    "FIELD_NAME": "Scale",
                    "FIELD_BIT_MASK": "24",
                    "FIELD_OFFSET": "3"
                  },
                  {
                    "FIELD_KEY": "0",
                    "FIELD_NAME": "Precision",
                    "FIELD_BIT_MASK": "224",
                    "FIELD_OFFSET": "5"
                  }
                ]
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Parameter Number",
                "FIELD_TYPE": "ENUM",
                "FIELD_TYPEhashcode": "8",
                "enum": [
                  {
                    "FIELD_KEY": "3",
                    "FIELD_NAME": "Total production time"
                  },
                  {
                    "FIELD_KEY": "2",
                    "FIELD_NAME": "Energy production today"
                  },
                  {
                    "FIELD_KEY": "1",
                    "FIELD_NAME": "Total energy production"
                  },
                  {
                    "FIELD_KEY": "0",
                    "FIELD_NAME": "Instant energy production"
                  }
                ]
              }
            ]
          },
          {
            "FIELD_KEY": "2",
            "FIELD_NAME": "ENERGY_PRODUCTION_GET",
            "FIELD_DESCRIPTION": "Energy Production Get",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Parameter Number",
              "FIELD_TYPE": "ENUM",
              "FIELD_TYPEhashcode": "8",
              "enum": [
                {
                  "FIELD_KEY": "3",
                  "FIELD_NAME": "Total production time"
                },
                {
                  "FIELD_KEY": "2",
                  "FIELD_NAME": "Energy production today"
                },
                {
                  "FIELD_KEY": "1",
                  "FIELD_NAME": "Total energy production"
                },
                {
                  "FIELD_KEY": "0",
                  "FIELD_NAME": "Instant energy production"
                }
              ]
            }
          }
        ]
      },
      {
        "FIELD_KEY": "49",
        "FIELD_NAME": "COMMAND_CLASS_SENSOR_MULTILEVEL",
        "FIELD_DESCRIPTION": "Command Class Sensor Multilevel",
        "COMMANDS": [
          {
            "FIELD_KEY": "5",
            "FIELD_NAME": "SENSOR_MULTILEVEL_REPORT",
            "FIELD_DESCRIPTION": "Sensor Multilevel Report",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "2",
                "FIELD_NAME": "Value",
                "FIELD_TYPE": "VARIANT",
                "FIELD_TYPEhashcode": "12",
                "variant": {
                  "-paramoffs": "1",
                  "FIELD_IS_HEX": "False",
                  "-signed": "True",
                  "-sizemask": "7",
                  "-sizeoffs": "0"
                }
              },
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Parameter 2",
                "FIELD_TYPE": "STRUCT_BYTE",
                "FIELD_TYPEhashcode": "7",
                "bitfield": [
                  {
                    "FIELD_KEY": "2",
                    "FIELD_NAME": "Size",
                    "FIELD_BIT_MASK": "0",
                    "FIELD_OFFSET": "0"
                  },
                  {
                    "FIELD_KEY": "1",
                    "FIELD_NAME": "Scale",
                    "FIELD_BIT_MASK": "3",
                    "FIELD_OFFSET": "0"
                  },
                  {
                    "FIELD_KEY": "0",
                    "FIELD_NAME": "Precision",
                    "FIELD_BIT_MASK": "5",
                    "FIELD_OFFSET": "0"
                  }
                ]
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Sensor Type",
                "FIELD_TYPE": "ENUM",
                "FIELD_TYPEhashcode": "8",
                "enum": [
                  {
                    "FIELD_KEY": "3",
                    "FIELD_NAME": "Luminance"
                  },
                  {
                    "FIELD_KEY": "2",
                    "FIELD_NAME": "General purpose value"
                  },
                  {
                    "FIELD_KEY": "1",
                    "FIELD_NAME": "Temperature"
                  }
                ]
              }
            ]
          },
          {
            "FIELD_KEY": "4",
            "FIELD_NAME": "SENSOR_MULTILEVEL_GET",
            "FIELD_DESCRIPTION": "Sensor Multilevel Get"
          }
        ]
      },
      {
        "FIELD_KEY": "48",
        "FIELD_NAME": "COMMAND_CLASS_SENSOR_BINARY",
        "FIELD_DESCRIPTION": "Command Class Sensor Binary",
        "COMMANDS": [
          {
            "FIELD_KEY": "3",
            "FIELD_NAME": "SENSOR_BINARY_REPORT",
            "FIELD_DESCRIPTION": "Sensor Binary Report",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Value",
              "FIELD_TYPE": "CONST",
              "FIELD_TYPEhashcode": "11",
              "const": [
                {
                  "FIELD_KEY": "1",
                  "FIELD_FLAG_DESCRIPTION": "Event",
                  "FIELD_FLAG_MASK": "255"
                },
                {
                  "FIELD_KEY": "0",
                  "FIELD_FLAG_DESCRIPTION": "Idle",
                  "FIELD_FLAG_MASK": "0"
                }
              ]
            }
          },
          {
            "FIELD_KEY": "2",
            "FIELD_NAME": "SENSOR_BINARY_GET",
            "FIELD_DESCRIPTION": "Sensor Binary Get"
          }
        ]
      },
      {
        "FIELD_KEY": "135",
        "FIELD_NAME": "COMMAND_CLASS_INDICATOR",
        "FIELD_DESCRIPTION": "Command Class Indicator",
        "COMMANDS": [
          {
            "FIELD_KEY": "3",
            "FIELD_NAME": "INDICATOR_REPORT",
            "FIELD_DESCRIPTION": "Indicator Report",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Value",
              "FIELD_TYPE": "BYTE",
              "FIELD_TYPEhashcode": "1",
              "FIELD_BIT_DEF": [
                {
                  "FIELD_KEY": "2",
                  "FIELD_FLAG_DESCRIPTION": "(on/enable)",
                  "FIELD_FLAG_MASK": "255"
                },
                {
                  "FIELD_KEY": "1",
                  "FIELD_FLAG_DESCRIPTION": "(off/disable)",
                  "FIELD_FLAG_MASK": "0"
                }
              ],
              "FIELD_VALUE_ATTRIBUTES": {
                "FIELD_KEY": "0",
                "FIELD_HAS_CONSTANTS": "True",
                "FIELD_IS_HEX": "True"
              }
            }
          },
          {
            "FIELD_KEY": "2",
            "FIELD_NAME": "INDICATOR_GET",
            "FIELD_DESCRIPTION": "Indicator Get"
          },
          {
            "FIELD_KEY": "1",
            "FIELD_NAME": "INDICATOR_SET",
            "FIELD_DESCRIPTION": "Indicator Set",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Value",
              "FIELD_TYPE": "BYTE",
              "FIELD_TYPEhashcode": "1",
              "FIELD_BIT_DEF": [
                {
                  "FIELD_KEY": "2",
                  "FIELD_FLAG_DESCRIPTION": "(on/enable)",
                  "FIELD_FLAG_MASK": "255"
                },
                {
                  "FIELD_KEY": "1",
                  "FIELD_FLAG_DESCRIPTION": "(off/disable)",
                  "FIELD_FLAG_MASK": "0"
                }
              ],
              "FIELD_VALUE_ATTRIBUTES": {
                "FIELD_KEY": "0",
                "FIELD_HAS_CONSTANTS": "True",
                "FIELD_IS_HEX": "True"
              }
            }
          }
        ]
      },
      {
        "FIELD_KEY": "143",
        "FIELD_NAME": "COMMAND_CLASS_MULTI_CMD",
        "FIELD_DESCRIPTION": "Multi Command Command Class",
        "COMMANDS": {
          "FIELD_KEY": "1",
          "FIELD_NAME": "MULTI_CMD_ENCAP",
          "FIELD_DESCRIPTION": "Multi Command Encapsulated Command",
          "-cmdrecursive": "true",
          "FIELD_PARAMETERS": {
            "FIELD_KEY": "0",
            "FIELD_NAME": "Number of commands",
            "FIELD_TYPE": "BYTE",
            "FIELD_TYPEhashcode": "1",
            "-encaptype": "amount",
            "FIELD_VALUE_ATTRIBUTES": {
              "FIELD_KEY": "0",
              "FIELD_HAS_CONSTANTS": "False",
              "FIELD_IS_HEX": "False"
            }
          },
          "variant_group": {
            "FIELD_KEY": "1",
            "FIELD_NAME": "Encapsulated Command",
            "-paramoffs": "0",
            "-variantFIELD_KEY": "0",
            "-paramOffs": "0",
            "-sizemask": "255",
            "-sizeoffs": "0",
            "FIELD_TYPEhashcode": "13",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Command Length",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "-encaptype": "length",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Command Class",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "-encaptype": "cmdclass",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "2",
                "FIELD_NAME": "Command",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "-encaptype": "COMMANDS",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "3",
                "FIELD_NAME": "Data",
                "FIELD_TYPE": "VARIANT",
                "FIELD_TYPEhashcode": "12",
                "-encaptype": "cmdparams",
                "variant": {
                  "-paramoffs": "0",
                  "FIELD_IS_HEX": "False",
                  "-signed": "False",
                  "-sizemask": "255",
                  "-sizeoffs": "0"
                }
              }
            ]
          }
        }
      },
      {
        "FIELD_KEY": "70",
        "FIELD_NAME": "COMMAND_CLASS_CLIMATE_CONTROL_SCHEDULE",
        "FIELD_DESCRIPTION": "Climate Control Schedule Command Class",
        "COMMANDS": [
          {
            "FIELD_KEY": "1",
            "FIELD_NAME": "SCHEDULE_SET",
            "FIELD_DESCRIPTION": "Schedule Set Command"
          },
          {
            "FIELD_KEY": "2",
            "FIELD_NAME": "SCHEDULE_GET",
            "FIELD_DESCRIPTION": "Schedule Get Command",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Weekday",
              "FIELD_TYPE": "BYTE",
              "FIELD_TYPEhashcode": "1",
              "FIELD_BIT_DEF": [
                {
                  "FIELD_KEY": "2",
                  "FIELD_FLAG_DESCRIPTION": "(on/enable)",
                  "FIELD_FLAG_MASK": "255"
                },
                {
                  "FIELD_KEY": "1",
                  "FIELD_FLAG_DESCRIPTION": "(off/disable)",
                  "FIELD_FLAG_MASK": "0"
                }
              ],
              "FIELD_VALUE_ATTRIBUTES": {
                "FIELD_KEY": "0",
                "FIELD_HAS_CONSTANTS": "True",
                "FIELD_IS_HEX": "True"
              }
            }
          },
          {
            "FIELD_KEY": "3",
            "FIELD_NAME": "SCHEDULE_REPORT",
            "FIELD_DESCRIPTION": "Schedule Report Command",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Weekday",
                "FIELD_TYPE": "STRUCT_BYTE",
                "FIELD_TYPEhashcode": "7",
                "bitfield": [
                  {
                    "FIELD_KEY": "1",
                    "FIELD_NAME": "Reserved",
                    "FIELD_BIT_MASK": "248",
                    "FIELD_OFFSET": "3"
                  },
                  {
                    "FIELD_KEY": "0",
                    "FIELD_NAME": "Weekday",
                    "FIELD_BIT_MASK": "7",
                    "FIELD_OFFSET": "0"
                  }
                ]
              },
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Switchpoint 0 byte 1",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "2",
                "FIELD_NAME": "Switchpoint 0 byte 2",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "3",
                "FIELD_NAME": "Switchpoint 0 byte 3",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "4",
                "FIELD_NAME": "Switchpoint 1 byte 1",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "5",
                "FIELD_NAME": "Switchpoint 1 byte 2",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "6",
                "FIELD_NAME": "Switchpoint 1 byte 3",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "7",
                "FIELD_NAME": "Switchpoint 2 byte 1",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "8",
                "FIELD_NAME": "Switchpoint 2 byte 2",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "9",
                "FIELD_NAME": "Switchpoint 2 byte 3",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "10",
                "FIELD_NAME": "Switchpoint 3 byte 1",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "11",
                "FIELD_NAME": "Switchpoint 3 byte 2",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "12",
                "FIELD_NAME": "Switchpoint 3 byte 3",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "13",
                "FIELD_NAME": "Switchpoint 4 byte 1",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "14",
                "FIELD_NAME": "Switchpoint 4 byte 2",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "15",
                "FIELD_NAME": "Switchpoint 4 byte 3",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "16",
                "FIELD_NAME": "Switchpoint 5 byte 1",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "17",
                "FIELD_NAME": "Switchpoint 5 byte 2",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "18",
                "FIELD_NAME": "Switchpoint 5 byte 3",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "19",
                "FIELD_NAME": "Switchpoint 6 byte 1",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "20",
                "FIELD_NAME": "Switchpoint 6 byte 2",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "21",
                "FIELD_NAME": "Switchpoint 6 byte 3",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "22",
                "FIELD_NAME": "Switchpoint 7 byte 1",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "23",
                "FIELD_NAME": "Switchpoint 7 byte 2",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "24",
                "FIELD_NAME": "Switchpoint 7 byte 3",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "25",
                "FIELD_NAME": "Switchpoint 8 byte 1",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "26",
                "FIELD_NAME": "Switchpoint 8 byte 2",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "27",
                "FIELD_NAME": "Switchpoint 8 byte 3",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              }
            ]
          },
          {
            "FIELD_KEY": "4",
            "FIELD_NAME": "SCHEDULE_CHANGED_GET",
            "FIELD_DESCRIPTION": "Schedule Changed Get Command",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "Weekday",
              "FIELD_TYPE": "STRUCT_BYTE",
              "FIELD_TYPEhashcode": "7",
              "bitfield": [
                {
                  "FIELD_KEY": "1",
                  "FIELD_NAME": "Reserved",
                  "FIELD_BIT_MASK": "248",
                  "FIELD_OFFSET": "3"
                },
                {
                  "FIELD_KEY": "0",
                  "FIELD_NAME": "Weekday",
                  "FIELD_BIT_MASK": "7",
                  "FIELD_OFFSET": "0"
                }
              ]
            }
          },
          {
            "FIELD_KEY": "5",
            "FIELD_NAME": "SCHEDULE_CHANGED_REPORT",
            "FIELD_DESCRIPTION": "Schedule Changed Report Command",
            "FIELD_PARAMETERS": {
              "FIELD_KEY": "0",
              "FIELD_NAME": "ChangeCounter",
              "FIELD_TYPE": "BYTE",
              "FIELD_TYPEhashcode": "1",
              "FIELD_VALUE_ATTRIBUTES": {
                "FIELD_KEY": "0",
                "FIELD_HAS_CONSTANTS": "False",
                "FIELD_IS_HEX": "False"
              }
            }
          },
          {
            "FIELD_KEY": "6",
            "FIELD_NAME": "SCHEDULE_OVERRIDE_SET",
            "FIELD_DESCRIPTION": "Schedule Override Set Command",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Override Type",
                "FIELD_TYPE": "STRUCT_BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Override State",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              }
            ]
          },
          {
            "FIELD_KEY": "7",
            "FIELD_NAME": "SCHEDULE_OVERRIDE_GET",
            "FIELD_DESCRIPTION": "Schedule Override Get Command"
          },
          {
            "FIELD_KEY": "8",
            "FIELD_NAME": "SCHEDULE_OVERRIDE_REPORT",
            "FIELD_DESCRIPTION": "Schedule Override Report Command",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Override Type",
                "FIELD_TYPE": "STRUCT_BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              },
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Override State",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              }
            ]
          }
        ]
      },
      {
        "FIELD_KEY": "1",
        "FIELD_NAME": "ZWAVE_COMMAND_CLASS",
        "FIELD_DESCRIPTION": "Z-Wave protocol Command Class",
        "COMMANDS": [
          {
            "FIELD_KEY": "30",
            "FIELD_NAME": "CMD_GET_SUC_NODE_ID",
            "FIELD_DESCRIPTION": "Get SUC Node ID"
          },
          {
            "FIELD_KEY": "26",
            "FIELD_NAME": "CMD_RESERVED_IDS",
            "FIELD_DESCRIPTION": "Reserved ID"
          },
          {
            "FIELD_KEY": "25",
            "FIELD_NAME": "ZWAVE_CMD_RESERVE_NODE_IDS",
            "FIELD_DESCRIPTION": "Reserve Node ID"
          },
          {
            "FIELD_KEY": "24",
            "FIELD_NAME": "CMD_NOP_POWER",
            "FIELD_DESCRIPTION": "NOP Power"
          },
          {
            "FIELD_KEY": "23",
            "FIELD_NAME": "CMD_ACCEPT_LOST",
            "FIELD_DESCRIPTION": "Accept Lost"
          },
          {
            "FIELD_KEY": "22",
            "FIELD_NAME": "CMD_LOST",
            "FIELD_DESCRIPTION": "Lost"
          },
          {
            "FIELD_KEY": "21",
            "FIELD_NAME": "CMD_STATIC_ROUTE_REQUEST",
            "FIELD_DESCRIPTION": "Static Route Request"
          },
          {
            "FIELD_KEY": "20",
            "FIELD_NAME": "CMD_ASSIGN_SUC_RETURN_ROUTE",
            "FIELD_DESCRIPTION": "Assign SUC Return Route"
          },
          {
            "FIELD_KEY": "19",
            "FIELD_NAME": "CMD_SET_SUC_ACK",
            "FIELD_DESCRIPTION": "Set SUC ACK"
          },
          {
            "FIELD_KEY": "18",
            "FIELD_NAME": "CMD_SET_SUC",
            "FIELD_DESCRIPTION": "Set SUC"
          },
          {
            "FIELD_KEY": "17",
            "FIELD_NAME": "CMD_SUC_NODE_ID",
            "FIELD_DESCRIPTION": "SUC Node ID"
          },
          {
            "FIELD_KEY": "16",
            "FIELD_NAME": "CMD_AUTOMATIC_CONTROLLER_UPDATE_START",
            "FIELD_DESCRIPTION": "Automatic Controller Update Start"
          },
          {
            "FIELD_KEY": "15",
            "FIELD_NAME": "CMD_TRANSFER_NEW_PRIMARY_COMPLETE",
            "FIELD_DESCRIPTION": "Transfer New Primary Complete"
          },
          {
            "FIELD_KEY": "14",
            "FIELD_NAME": "CMD_NEW_RANGE_REGISTERED",
            "FIELD_DESCRIPTION": "New Range Registered"
          },
          {
            "FIELD_KEY": "13",
            "FIELD_NAME": "CMD_NEW_NODE_REGISTERED",
            "FIELD_DESCRIPTION": "New Node Registered"
          },
          {
            "FIELD_KEY": "12",
            "FIELD_NAME": "CMD_ASSIGN_RETURN_ROUTE",
            "FIELD_DESCRIPTION": "Assign Return Route"
          },
          {
            "FIELD_KEY": "11",
            "FIELD_NAME": "CMD_TRANSFER_END",
            "FIELD_DESCRIPTION": "Transfer End"
          },
          {
            "FIELD_KEY": "10",
            "FIELD_NAME": "CMD_TRANSFER_RANGE_INFO",
            "FIELD_DESCRIPTION": "Transfer Range Info"
          },
          {
            "FIELD_KEY": "9",
            "FIELD_NAME": "CMD_TRANSFER_NODE_INFO",
            "FIELD_DESCRIPTION": "Transfer Node Info"
          },
          {
            "FIELD_KEY": "8",
            "FIELD_NAME": "CMD_TRANSFER_PRESENTATION",
            "FIELD_DESCRIPTION": "Transfer Presentation"
          },
          {
            "FIELD_KEY": "7",
            "FIELD_NAME": "CMD_COMMAND_COMPLETE",
            "FIELD_DESCRIPTION": "Command Complete"
          },
          {
            "FIELD_KEY": "6",
            "FIELD_NAME": "NODE_RANGE_INFO",
            "FIELD_DESCRIPTION": "Node Range Info"
          },
          {
            "FIELD_KEY": "5",
            "FIELD_NAME": "CMD_GET_NODES_IN_RANGE",
            "FIELD_DESCRIPTION": "Get Nodes In Range"
          },
          {
            "FIELD_KEY": "4",
            "FIELD_NAME": "FIND_NODES_IN_RANGE",
            "FIELD_DESCRIPTION": "Find Nodes In Range"
          },
          {
            "FIELD_KEY": "2",
            "FIELD_NAME": "CMD_REQUEST_NODE_INFO",
            "FIELD_DESCRIPTION": "Request Node Info"
          },
          {
            "FIELD_KEY": "3",
            "FIELD_NAME": "CMD_ASSIGN_IDS",
            "FIELD_DESCRIPTION": "Assign Ids",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "New Home ID",
                "FIELD_TYPE": "DWORD",
                "FIELD_TYPEhashcode": "3",
                "dword": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "True"
                }
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "New node ID",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "False"
                }
              }
            ]
          },
          {
            "FIELD_KEY": "1",
            "FIELD_NAME": "NODE_INFO",
            "FIELD_DESCRIPTION": "Node Info",
            "FIELD_PARAMETERS": [
              {
                "FIELD_KEY": "6",
                "FIELD_NAME": "Command Classes",
                "FIELD_TYPE": "ENUM_ARRAY",
                "FIELD_TYPEhashcode": "9",
                "enum": [
                  {
                    "FIELD_KEY": "97",
                    "FIELD_NAME": "COMMAND_CLASS_MULTI_INSTANCE"
                  },
                  {
                    "FIELD_KEY": "82",
                    "FIELD_NAME": "COMMAND_CLASS_MTP_WINDOW_COVERING"
                  },
                  {
                    "FIELD_KEY": "81",
                    "FIELD_NAME": "COMMAND_CLASS_BASIC_WINDOW_COVERING"
                  },
                  {
                    "FIELD_KEY": "70",
                    "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_FAN_STATE"
                  },
                  {
                    "FIELD_KEY": "69",
                    "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_FAN_MODE"
                  },
                  {
                    "FIELD_KEY": "68",
                    "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_SETPOINT"
                  },
                  {
                    "FIELD_KEY": "67",
                    "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_OPERATING_STATE"
                  },
                  {
                    "FIELD_KEY": "65",
                    "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT_MODE"
                  },
                  {
                    "FIELD_KEY": "57",
                    "FIELD_NAME": "COMMAND_CLASS_THERMOSTAT"
                  },
                  {
                    "FIELD_KEY": "54",
                    "FIELD_NAME": "COMMAND_CLASS_METER_PULSE"
                  },
                  {
                    "FIELD_KEY": "50",
                    "FIELD_NAME": "COMMAND_CLASS_SENSOR_MULTILEVEL"
                  },
                  {
                    "FIELD_KEY": "49",
                    "FIELD_NAME": "COMMAND_CLASS_SENSOR_BINARY"
                  },
                  {
                    "FIELD_KEY": "38",
                    "FIELD_NAME": "COMMAND_CLASS_SWITCH_BINARY"
                  },
                  {
                    "FIELD_KEY": "43",
                    "FIELD_NAME": "COMMAND_CLASS_CHIMNEY_FAN"
                  },
                  {
                    "FIELD_KEY": "42",
                    "FIELD_NAME": "COMMAND_CLASS_SWITCH_TOGGLE_MULTILEVEL"
                  },
                  {
                    "FIELD_KEY": "41",
                    "FIELD_NAME": "COMMAND_CLASS_SWITCH_TOGGLE_BINARY"
                  },
                  {
                    "FIELD_KEY": "40",
                    "FIELD_NAME": "COMMAND_CLASS_SWITCH_ALL"
                  },
                  {
                    "FIELD_KEY": "39",
                    "FIELD_NAME": "COMMAND_CLASS_SWITCH_MULTILEVEL"
                  },
                  {
                    "FIELD_KEY": "145",
                    "FIELD_NAME": "COMMAND_CLASS_ENERGY_PRODUCTION"
                  },
                  {
                    "FIELD_KEY": "35",
                    "FIELD_NAME": "COMMAND_CLASS_APPLICATION_STATUS"
                  },
                  {
                    "FIELD_KEY": "34",
                    "FIELD_NAME": "COMMAND_CLASS_CONTROLLER_REPLICATION"
                  },
                  {
                    "FIELD_KEY": "33",
                    "FIELD_NAME": "COMMAND_CLASS_BASIC"
                  },
                  {
                    "FIELD_KEY": "138",
                    "FIELD_NAME": "COMMAND_CLASS_LANGUAGE"
                  },
                  {
                    "FIELD_KEY": "137",
                    "FIELD_NAME": "COMMAND_CLASS_PROPRIETARY"
                  },
                  {
                    "FIELD_KEY": "136",
                    "FIELD_NAME": "COMMAND_CLASS_INDICATOR"
                  },
                  {
                    "FIELD_KEY": "135",
                    "FIELD_NAME": "COMMAND_CLASS_VERSION"
                  },
                  {
                    "FIELD_KEY": "134",
                    "FIELD_NAME": "COMMAND_CLASS_ASSOCIATION"
                  },
                  {
                    "FIELD_KEY": "133",
                    "FIELD_NAME": "COMMAND_CLASS_WAKE_UP"
                  },
                  {
                    "FIELD_KEY": "132",
                    "FIELD_NAME": "COMMAND_CLASS_NETWORK_STAT"
                  },
                  {
                    "FIELD_KEY": "130",
                    "FIELD_NAME": "COMMAND_CLASS_CLOCK"
                  },
                  {
                    "FIELD_KEY": "129",
                    "FIELD_NAME": "COMMAND_CLASS_BATTERY"
                  },
                  {
                    "FIELD_KEY": "15",
                    "FIELD_NAME": "REQUEST_NODE_INFO"
                  },
                  {
                    "FIELD_KEY": "14",
                    "FIELD_NAME": "DELETE_ROUTE"
                  },
                  {
                    "FIELD_KEY": "13",
                    "FIELD_NAME": "ASSIGN_ROUTE"
                  },
                  {
                    "FIELD_KEY": "119",
                    "FIELD_NAME": "COMMAND_CLASS_LOCK"
                  },
                  {
                    "FIELD_KEY": "118",
                    "FIELD_NAME": "COMMAND_CLASS_PROTECTION"
                  },
                  {
                    "FIELD_KEY": "116",
                    "FIELD_NAME": "COMMAND_CLASS_POWERLEVEL"
                  },
                  {
                    "FIELD_KEY": "115",
                    "FIELD_NAME": "COMMAND_CLASS_MANUFACTURER_SPECIFIC"
                  },
                  {
                    "FIELD_KEY": "114",
                    "FIELD_NAME": "COMMAND_CLASS_ALARM"
                  },
                  {
                    "FIELD_KEY": "113",
                    "FIELD_NAME": "COMMAND_CLASS_CONFIGURATION"
                  }
                ]
              },
              {
                "FIELD_KEY": "5",
                "FIELD_NAME": "Specific Device Class",
                "FIELD_TYPE": "MULTI_ARRAY",
                "FIELD_TYPEhashcode": "10",
                "multi_array": [
                  {
                    "FIELD_BIT_DEF": [
                      {
                        "FIELD_KEY": "20",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_NOT_USED",
                        "FIELD_FLAG_MASK": "0"
                      },
                      {
                        "FIELD_KEY": "20",
                        "FIELD_FLAG_DESCRIPTION": "0",
                        "FIELD_FLAG_MASK": "0"
                      },
                      {
                        "FIELD_KEY": "20",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_SWITCH_TOGGLE_BINARY",
                        "FIELD_FLAG_MASK": "1"
                      },
                      {
                        "FIELD_KEY": "20",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_SWITCH_TOGGLE_MULTILEVEL",
                        "FIELD_FLAG_MASK": "2"
                      }
                    ]
                  },
                  {
                    "FIELD_BIT_DEF": [
                      {
                        "FIELD_KEY": "19",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_NOT_USED",
                        "FIELD_FLAG_MASK": "0"
                      },
                      {
                        "FIELD_KEY": "19",
                        "FIELD_FLAG_DESCRIPTION": "0",
                        "FIELD_FLAG_MASK": "0"
                      },
                      {
                        "FIELD_KEY": "19",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_SWITCH_REMOTE_BINARY",
                        "FIELD_FLAG_MASK": "1"
                      },
                      {
                        "FIELD_KEY": "19",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_SWITCH_REMOTE_MULTILEVEL",
                        "FIELD_FLAG_MASK": "2"
                      },
                      {
                        "FIELD_KEY": "19",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_SWITCH_REMOTE_TOGGLE_BINARY",
                        "FIELD_FLAG_MASK": "3"
                      },
                      {
                        "FIELD_KEY": "19",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_SWITCH_REMOTE_TOGGLE_MULTILEVEL",
                        "FIELD_FLAG_MASK": "4"
                      }
                    ]
                  },
                  {
                    "FIELD_BIT_DEF": [
                      {
                        "FIELD_KEY": "18",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_NOT_USED",
                        "FIELD_FLAG_MASK": "0"
                      },
                      {
                        "FIELD_KEY": "18",
                        "FIELD_FLAG_DESCRIPTION": "0",
                        "FIELD_FLAG_MASK": "0"
                      },
                      {
                        "FIELD_KEY": "18",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_POWER_SWITCH_MULTILEVEL",
                        "FIELD_FLAG_MASK": "1"
                      }
                    ]
                  },
                  {
                    "FIELD_BIT_DEF": [
                      {
                        "FIELD_KEY": "17",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_NOT_USED",
                        "FIELD_FLAG_MASK": "0"
                      },
                      {
                        "FIELD_KEY": "17",
                        "FIELD_FLAG_DESCRIPTION": "0",
                        "FIELD_FLAG_MASK": "0"
                      },
                      {
                        "FIELD_KEY": "17",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_POWER_SWITCH_BINARY",
                        "FIELD_FLAG_MASK": "1"
                      }
                    ]
                  },
                  {
                    "FIELD_BIT_DEF": [
                      {
                        "FIELD_KEY": "16",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_NOT_USED",
                        "FIELD_FLAG_MASK": "0"
                      },
                      {
                        "FIELD_KEY": "16",
                        "FIELD_FLAG_DESCRIPTION": "0",
                        "FIELD_FLAG_MASK": "0"
                      },
                      {
                        "FIELD_KEY": "16",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_REPEATER_SLAVE",
                        "FIELD_FLAG_MASK": "1"
                      }
                    ]
                  },
                  {
                    "FIELD_BIT_DEF": {
                      "FIELD_KEY": "81",
                      "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_NOT_USED",
                      "FIELD_FLAG_MASK": "0"
                    }
                  },
                  {
                    "FIELD_BIT_DEF": [
                      {
                        "FIELD_KEY": "34",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_NOT_USED",
                        "FIELD_FLAG_MASK": "0"
                      },
                      {
                        "FIELD_KEY": "34",
                        "FIELD_FLAG_DESCRIPTION": "0",
                        "FIELD_FLAG_MASK": "0"
                      },
                      {
                        "FIELD_KEY": "34",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_ROUTING_SENSOR_MULTILEVEL",
                        "FIELD_FLAG_MASK": "1"
                      },
                      {
                        "FIELD_KEY": "34",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_CHIMNEY_FAN_SENSOR_MULTILEVEL",
                        "FIELD_FLAG_MASK": "2"
                      }
                    ]
                  },
                  {
                    "FIELD_BIT_DEF": [
                      {
                        "FIELD_KEY": "33",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_NOT_USED",
                        "FIELD_FLAG_MASK": "0"
                      },
                      {
                        "FIELD_KEY": "33",
                        "FIELD_FLAG_DESCRIPTION": "0",
                        "FIELD_FLAG_MASK": "0"
                      },
                      {
                        "FIELD_KEY": "33",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_ROUTING_SENSOR_BINARY",
                        "FIELD_FLAG_MASK": "1"
                      }
                    ]
                  },
                  {
                    "FIELD_BIT_DEF": [
                      {
                        "FIELD_KEY": "9",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_NOT_USED",
                        "FIELD_FLAG_MASK": "0"
                      },
                      {
                        "FIELD_KEY": "9",
                        "FIELD_FLAG_DESCRIPTION": "0",
                        "FIELD_FLAG_MASK": "0"
                      },
                      {
                        "FIELD_KEY": "9",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_THERMOSTAT_HEATING",
                        "FIELD_FLAG_MASK": "1"
                      },
                      {
                        "FIELD_KEY": "9",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_THERMOSTAT_GENERAL",
                        "FIELD_FLAG_MASK": "2"
                      }
                    ]
                  },
                  {
                    "FIELD_BIT_DEF": [
                      {
                        "FIELD_KEY": "3",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_NOT_USED",
                        "FIELD_FLAG_MASK": "0"
                      },
                      {
                        "FIELD_KEY": "3",
                        "FIELD_FLAG_DESCRIPTION": "0",
                        "FIELD_FLAG_MASK": "0"
                      },
                      {
                        "FIELD_KEY": "3",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_PC_CONTROLLER",
                        "FIELD_FLAG_MASK": "1"
                      }
                    ]
                  },
                  {
                    "paramdescloc": {
                      "FIELD_KEY": "0",
                      "FIELD_PARAMETER": "4",
                      ""FIELD_PARAMETER_DESCRIPTION"": "255",
                      "FIELD_PARAMETER_START": "4"
                    }
                  },
                  {
                    "FIELD_BIT_DEF": [
                      {
                        "FIELD_KEY": "49",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_NOT_USED",
                        "FIELD_FLAG_MASK": "0"
                      },
                      {
                        "FIELD_KEY": "49",
                        "FIELD_FLAG_DESCRIPTION": "0",
                        "FIELD_FLAG_MASK": "0"
                      },
                      {
                        "FIELD_KEY": "49",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_ENERGY_PRODUCTION",
                        "FIELD_FLAG_MASK": "1"
                      }
                    ]
                  },
                  {
                    "FIELD_BIT_DEF": [
                      {
                        "FIELD_KEY": "2",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_NOT_USED",
                        "FIELD_FLAG_MASK": "0"
                      },
                      {
                        "FIELD_KEY": "2",
                        "FIELD_FLAG_DESCRIPTION": "0",
                        "FIELD_FLAG_MASK": "0"
                      },
                      {
                        "FIELD_KEY": "2",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_PORTABLE_REMOTE_CONTROLLER",
                        "FIELD_FLAG_MASK": "1"
                      }
                    ]
                  },
                  {
                    "FIELD_BIT_DEF": [
                      {
                        "FIELD_KEY": "65",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_NOT_USED",
                        "FIELD_FLAG_MASK": "0"
                      },
                      {
                        "FIELD_KEY": "65",
                        "FIELD_FLAG_DESCRIPTION": "0",
                        "FIELD_FLAG_MASK": "0"
                      },
                      {
                        "FIELD_KEY": "65",
                        "FIELD_FLAG_DESCRIPTION": "SPECIFIC_TYPE_DOOR_LOCK",
                        "FIELD_FLAG_MASK": "1"
                      }
                    ]
                  }
                ]
              },
              {
                "FIELD_KEY": "4",
                "FIELD_NAME": "Generic Device Class",
                "FIELD_TYPE": "ENUM",
                "FIELD_TYPEhashcode": "8",
                "enum": [
                  {
                    "FIELD_KEY": "18",
                    "FIELD_NAME": "GENERIC_TYPE_SWITCH_REMOTE"
                  },
                  {
                    "FIELD_KEY": "19",
                    "FIELD_NAME": "GENERIC_TYPE_SWITCH_TOGGLE"
                  },
                  {
                    "FIELD_KEY": "64",
                    "FIELD_NAME": "GENERIC_TYPE_ENTRY_CONTROL"
                  },
                  {
                    "FIELD_KEY": "17",
                    "FIELD_NAME": "GENERIC_TYPE_SWITCH_MULTILEVEL"
                  },
                  {
                    "FIELD_KEY": "16",
                    "FIELD_NAME": "GENERIC_TYPE_SWITCH_BINARY"
                  },
                  {
                    "FIELD_KEY": "15",
                    "FIELD_NAME": "GENERIC_TYPE_REPEATER_SLAVE"
                  },
                  {
                    "FIELD_KEY": "80",
                    "FIELD_NAME": "GENERIC_TYPE_SEMI_INTEROPERABLE"
                  },
                  {
                    "FIELD_KEY": "33",
                    "FIELD_NAME": "GENERIC_TYPE_SENSOR_MULTILEVEL"
                  },
                  {
                    "FIELD_KEY": "32",
                    "FIELD_NAME": "GENERIC_TYPE_SENSOR_BINARY"
                  },
                  {
                    "FIELD_KEY": "8",
                    "FIELD_NAME": "GENERIC_TYPE_THERMOSTAT_CONTROLLER"
                  },
                  {
                    "FIELD_KEY": "2",
                    "FIELD_NAME": "GENERIC_TYPE_STATIC_CONTROLLER"
                  },
                  {
                    "FIELD_KEY": "48",
                    "FIELD_NAME": "GENERIC_TYPE_METER_PULSE"
                  },
                  {
                    "FIELD_KEY": "1",
                    "FIELD_NAME": "GENERIC_TYPE_GENERIC_CONTROLLER"
                  },
                  {
                    "FIELD_KEY": "0",
                    "FIELD_NAME": "GENERIC_TYPE_NOT_KNOWN"
                  }
                ]
              },
              {
                "FIELD_KEY": "3",
                "FIELD_NAME": "Basic Device Class",
                "FIELD_TYPE": "ENUM",
                "FIELD_TYPEhashcode": "8",
                "enum": [
                  {
                    "FIELD_KEY": "4",
                    "FIELD_NAME": "BASIC_TYPE_ROUTING_SLAVE"
                  },
                  {
                    "FIELD_KEY": "3",
                    "FIELD_NAME": "BASIC_TYPE_SLAVE"
                  },
                  {
                    "FIELD_KEY": "2",
                    "FIELD_NAME": "BASIC_TYPE_STATIC_CONTROLLER"
                  },
                  {
                    "FIELD_KEY": "1",
                    "FIELD_NAME": "BASIC_TYPE_CONTROLLER"
                  }
                ]
              },
              {
                "FIELD_KEY": "2",
                "FIELD_NAME": "Reserved",
                "FIELD_TYPE": "BYTE",
                "FIELD_TYPEhashcode": "1",
                "FIELD_VALUE_ATTRIBUTES": {
                  "FIELD_KEY": "0",
                  "FIELD_HAS_CONSTANTS": "False",
                  "FIELD_IS_HEX": "True"
                }
              },
              {
                "FIELD_KEY": "1",
                "FIELD_NAME": "Security",
                "FIELD_TYPE": "STRUCT_BYTE",
                "FIELD_TYPEhashcode": "7",
                "FIELD_BIT_DEF": [
                  {
                    "FIELD_KEY": "0",
                    "FIELD_FLAG_DESCRIPTION": "Optional Functionality",
                    "FIELD_FLAG_MASK": "128"
                  },
                  {
                    "FIELD_KEY": "1",
                    "FIELD_FLAG_DESCRIPTION": "Sensor 1000ms",
                    "FIELD_FLAG_MASK": "64"
                  },
                  {
                    "FIELD_KEY": "2",
                    "FIELD_FLAG_DESCRIPTION": "Sensor 250ms",
                    "FIELD_FLAG_MASK": "32"
                  },
                  {
                    "FIELD_KEY": "3",
                    "FIELD_FLAG_DESCRIPTION": "Beam Capability",
                    "FIELD_FLAG_MASK": "16"
                  },
                  {
                    "FIELD_KEY": "4",
                    "FIELD_FLAG_DESCRIPTION": "Routing Slave",
                    "FIELD_FLAG_MASK": "8"
                  },
                  {
                    "FIELD_KEY": "5",
                    "FIELD_FLAG_DESCRIPTION": "Specific Device",
                    "FIELD_FLAG_MASK": "4"
                  },
                  {
                    "FIELD_KEY": "6",
                    "FIELD_FLAG_DESCRIPTION": "Controller",
                    "FIELD_FLAG_MASK": "2"
                  },
                  {
                    "FIELD_KEY": "7",
                    "FIELD_FLAG_DESCRIPTION": "Security",
                    "FIELD_FLAG_MASK": "1"
                  }
                ]
              },
              {
                "FIELD_KEY": "0",
                "FIELD_NAME": "Capability",
                "FIELD_TYPE": "STRUCT_BYTE",
                "FIELD_TYPEhashcode": "7",
                "fieldenum": [
                  {
                    "FIELD_KEY": "3",
                    "FIELD_NAME": "Protocol Version",
                    "FIELD_BIT_MASK": "7",
                    "FIELD_OFFSET": "0",
                    "fieldenum": [
                      { "FIELD_VALUE": "Reserved" },
                      { "FIELD_VALUE": "Z-Wave Version 2.0" },
                      { "FIELD_VALUE": "Z-Wave Version 3.0" },
                      { "FIELD_VALUE": "Z-Wave Version 4.0" },
                      { "FIELD_VALUE": "Reserved" },
                      { "FIELD_VALUE": "Reserved" },
                      { "FIELD_VALUE": "Reserved" },
                      { "FIELD_VALUE": "Reserved" }
                    ]
                  },
                  {
                    "FIELD_KEY": "2",
                    "FIELD_NAME": "Max baud rate",
                    "FIELD_BIT_MASK": "56",
                    "FIELD_OFFSET": "3",
                    "fieldenum": [
                      { "FIELD_VALUE": "Reserved" },
                      { "FIELD_VALUE": "9600 Baud" },
                      { "FIELD_VALUE": "40000 Baud" },
                      { "FIELD_VALUE": "Reserved" },
                      { "FIELD_VALUE": "Reserved" },
                      { "FIELD_VALUE": "Reserved" },
                      { "FIELD_VALUE": "Reserved" },
                      { "FIELD_VALUE": "Reserved" }
                    ]
                  }
                ],
                "FIELD_BIT_DEF": [
                  {
                    "FIELD_KEY": "1",
                    "FIELD_FLAG_DESCRIPTION": "Routing",
                    "FIELD_FLAG_MASK": "64"
                  },
                  {
                    "FIELD_KEY": "0",
                    "FIELD_FLAG_DESCRIPTION": "Listening",
                    "FIELD_FLAG_MASK": "128"
                  }
                ]
              }
            ]
          },
          {
            "FIELD_KEY": "0",
            "FIELD_NAME": "ZWAVE_CMD_NOP",
            "FIELD_DESCRIPTION": "NOP"
          }
        ]
      },
      {
        "FIELD_KEY": "2",
        "FIELD_NAME": "ZWAVE_COMMAND_CLASS_SENSOR",
        "FIELD_DESCRIPTION": "Z-Wave Zensor Cmd Class",
        "COMMANDS": [
          {
            "FIELD_KEY": "1",
            "FIELD_NAME": "ZWAVE_ZENSOR_CMD_BIND_REQ",
            "FIELD_DESCRIPTION": "Zensor Request Bind"
          },
          {
            "FIELD_KEY": "2",
            "FIELD_NAME": "ZWAVE_ZENSOR_CMD_BIND_ACCEPT",
            "FIELD_DESCRIPTION": "Zensor Accept Bind"
          },
          {
            "FIELD_KEY": "3",
            "FIELD_NAME": "ZWAVE_ZENSOR_CMD_BIND_COMPLETE",
            "FIELD_DESCRIPTION": "Zensor Bind Complete"
          }
        ]
      }
    ]
  }
}

```