# Swagger Petstore MCP Plugin for Cursor

> **Premium Developer Tool** | A comprehensive Model Context Protocol (MCP) plugin for interacting with the Swagger Petstore API directly within Cursor IDE.

## 🚀 Overview

The Swagger Petstore MCP Plugin transforms your Cursor IDE into a powerful API development environment, providing seamless integration with the classic Petstore API. Whether you're learning API development, testing endpoints, or building pet store applications, this plugin offers intelligent code completion and contextual assistance for all Petstore operations.

**Key Features:**
- 🐾 Complete Pet lifecycle management (CRUD operations)
- 🛒 Order processing and inventory tracking
- 👥 User management and authentication
- 📁 File upload capabilities
- 🔍 Advanced search and filtering
- 🛡️ Built-in error handling and recovery
- 📚 Contextual help and parameter validation

## 📦 Installation

1. Ensure you have the MCP server running with the Swagger Petstore configuration
2. Add this plugin to your Cursor workspace
3. The plugin will automatically detect and integrate with your MCP setup

## 🎯 Getting Started

### Quick Start Example

```javascript
// Add a new pet to the store
const newPet = await addPet({
  name: "Buddy",
  category: { id: 1, name: "Dogs" },
  photoUrls: ["https://example.com/buddy.jpg"],
  tags: [{ id: 1, name: "friendly" }],
  status: "available"
});

// Find available pets
const availablePets = await findPetsByStatus("available");

// Place an order
const order = await placeOrder({
  petId: newPet.id,
  quantity: 1,
  shipDate: new Date().toISOString(),
  status: "placed"
});
```

### Authentication

For testing purposes, use the API key `special-key` when authentication is required:

```javascript
// Most operations work without authentication
// For protected operations, the special-key is automatically handled
```

### API Base Information

- **Base URL**: Petstore API endpoint (configured via MCP)
- **Test API Key**: `special-key`
- **Documentation**: [swagger.io](http://swagger.io)
- **Support**: [#swagger on irc.freenode.net](http://swagger.io/irc/)

## 📁 Folder Structure

```
swagger-petstore-plugin/
├── README.md                    # This file
├── .cursorrules                # AI behavior configuration
└── skills/                     # Tool-specific guidance
    ├── uploadFile.md           # File upload operations
    ├── addPet.md              # Pet creation
    ├── updatePet.md           # Pet updates
    ├── findPetsByStatus.md    # Status-based search
    ├── findPetsByTags.md      # Tag-based search
    ├── getPetById.md          # Single pet retrieval
    ├── updatePetWithForm.md   # Form-based updates
    ├── deletePet.md           # Pet deletion
    ├── getInventory.md        # Inventory queries
    ├── placeOrder.md          # Order creation
    ├── getOrderById.md        # Order retrieval
    ├── deleteOrder.md         # Order cancellation
    ├── createUsersWithListInput.md    # Bulk user creation (list)
    ├── getUserByName.md       # User lookup
    ├── updateUser.md          # User modifications
    ├── deleteUser.md          # User deletion
    ├── loginUser.md           # User authentication
    ├── logoutUser.md          # Session termination
    ├── createUsersWithArrayInput.md   # Bulk user creation (array)
    └── createUser.md          # Single user creation
```

## 🛠️ Available Operations

### 🐾 Pet Management
- **addPet** - Create new pets with full metadata
- **updatePet** - Modify existing pet information
- **updatePetWithForm** - Form-based pet updates
- **getPetById** - Retrieve specific pets
- **deletePet** - Remove pets from store
- **findPetsByStatus** - Search by availability status
- **findPetsByTags** - Filter by custom tags
- **uploadFile** - Add pet images and files

### 🛒 Store Operations  
- **getInventory** - Check stock levels by status
- **placeOrder** - Create purchase orders
- **getOrderById** - Retrieve order details
- **deleteOrder** - Cancel pending orders

### 👥 User Management
- **createUser** - Register individual users
- **createUsersWithListInput** - Bulk user creation (list format)
- **createUsersWithArrayInput** - Bulk user creation (array format)
- **getUserByName** - Look up user profiles
- **updateUser** - Modify user information
- **deleteUser** - Remove user accounts
- **loginUser** - Authenticate users
- **logoutUser** - End user sessions

## 🎯 Smart Features

The plugin includes intelligent assistance for:
- **Parameter validation** - Ensures required fields are provided
- **Type checking** - Validates data types before API calls
- **Error recovery** - Suggests fixes for common API errors
- **Status code handling** - Interprets HTTP responses meaningfully
- **Rate limiting awareness** - Helps manage API usage

## 📚 Learning Resources

Each tool includes detailed guidance in the `skills/` directory:
- **When to use** - Specific scenarios and use cases
- **Step-by-step guides** - Parameter handling and response processing  
- **Pro-tips** - Advanced usage patterns
- **Error handling** - Common issues and solutions
- **Real examples** - Working code samples

## 🤝 Contributing

This plugin follows Cursor's MCP plugin standards. Contributions are welcome:
1. Fork the repository
2. Add or enhance skill files in the `skills/` directory
3. Update documentation
4. Submit a pull request

## 📄 License

This plugin is provided as-is for educational and development purposes. Please respect the Swagger Petstore API terms of service.

---

**Made with ❤️ for the Cursor IDE community**