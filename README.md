## 计算器 MCP
基于 Model Context Protocol (MCP) 的数值计算器，提供了简单的加减乘除、幂运算、平方根运算和整数阶乘运算。


# Tools
```
{
  "tools": [
    {
      "name": "add",
      "description": "执行浮点数加法运算",
      "inputSchema": {
        "type": "object",
        "properties": {
          "a": {
            "title": "A",
            "type": "number"
          },
          "b": {
            "title": "B",
            "type": "number"
          }
        },
        "required": [
          "a",
          "b"
        ],
        "title": "addArguments"
      }
    },
    {
      "name": "subtract",
      "description": "执行浮点数减法运算",
      "inputSchema": {
        "type": "object",
        "properties": {
          "a": {
            "title": "A",
            "type": "number"
          },
          "b": {
            "title": "B",
            "type": "number"
          }
        },
        "required": [
          "a",
          "b"
        ],
        "title": "subtractArguments"
      }
    },
    {
      "name": "multiply",
      "description": "执行浮点数乘法运算",
      "inputSchema": {
        "type": "object",
        "properties": {
          "a": {
            "title": "A",
            "type": "number"
          },
          "b": {
            "title": "B",
            "type": "number"
          }
        },
        "required": [
          "a",
          "b"
        ],
        "title": "multiplyArguments"
      }
    },
    {
      "name": "divide",
      "description": "执行浮点数除法运算\n    Args:\n        b: 除数（必须非零）\n    ",
      "inputSchema": {
        "type": "object",
        "properties": {
          "a": {
            "title": "A",
            "type": "number"
          },
          "b": {
            "title": "B",
            "type": "number"
          }
        },
        "required": [
          "a",
          "b"
        ],
        "title": "divideArguments"
      }
    },
    {
      "name": "power",
      "description": "计算幂运算",
      "inputSchema": {
        "type": "object",
        "properties": {
          "base": {
            "title": "Base",
            "type": "number"
          },
          "exponent": {
            "title": "Exponent",
            "type": "number"
          }
        },
        "required": [
          "base",
          "exponent"
        ],
        "title": "powerArguments"
      }
    },
    {
      "name": "sqrt",
      "description": "计算平方根",
      "inputSchema": {
        "type": "object",
        "properties": {
          "number": {
            "title": "Number",
            "type": "number"
          }
        },
        "required": [
          "number"
        ],
        "title": "sqrtArguments"
      }
    },
    {
      "name": "factorial",
      "description": "计算整数阶乘",
      "inputSchema": {
        "type": "object",
        "properties": {
          "n": {
            "title": "N",
            "type": "integer"
          }
        },
        "required": [
          "n"
        ],
        "title": "factorialArguments"
      }
    }
  ]
}
```

## MCP 服务器配置
```
{
    "mcpServers": {
        "calculator": {
        "command": "uv",
        "args": [
            "run", "calculator.py"
            ]
        }
    }
}
```