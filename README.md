# Swagger Petstore MCP Plugin

A comprehensive MCP (Model Context Protocol) plugin for interacting with the Swagger Petstore API, designed for AI-native development with Cursor IDE.

## Overview

This plugin provides seamless integration with the Swagger Petstore API, offering complete CRUD operations for pets, orders, and users. Perfect for learning API interactions, prototyping e-commerce features, or building pet store applications.

**Key Features:**
- 🐾 Complete pet management (add, update, find, delete)
- 📦 Order processing and tracking
- 👤 User management and authentication
- 📁 File upload capabilities
- 🔍 Advanced search and filtering
- 🛡️ Built-in error handling and validation

## Getting Started

### Prerequisites
- Cursor IDE with MCP support
- API key: `special-key` (for testing authorization filters)

### Installation
1. Add this plugin to your Cursor MCP configuration
2. Ensure the Swagger Petstore server is accessible
3. Use the provided API key for authenticated endpoints

### Quick Start
```javascript
// Find available pets
const availablePets = await findPetsByStatus({ status: "available" });

// Add a new pet
const newPet = await addPet({
  name: "Buddy",
  category: { name: "Dogs" },
  status: "available"
});

// Place an order
const order = await placeOrder({
  petId: newPet.id,
  quantity: 1,
  status: "placed"
});
```

## Folder Structure

```
swagger-petstore-plugin/
├── README.md                 # This file
├── .cursorrules             # AI assistant configuration
└── skills/                  # Tool-specific documentation
    ├── uploadFile.md        # File upload operations
    ├── addPet.md           # Pet creation
    ├── updatePet.md        # Pet updates
    ├── findPetsByStatus.md # Status-based search
    ├── findPetsByTags.md   # Tag-based search
    ├── getPetById.md       # Single pet retrieval
    ├── updatePetWithForm.md # Form-based updates
    ├── deletePet.md        # Pet deletion
    ├── getInventory.md     # Inventory management
    ├── placeOrder.md       # Order creation
    ├── getOrderById.md     # Order retrieval
    ├── deleteOrder.md      # Order cancellation
    ├── createUsersWithListInput.md # Batch user creation
    ├── getUserByName.md    # User lookup
    ├── updateUser.md       # User updates
    ├── deleteUser.md       # User deletion
    ├── loginUser.md        # Authentication
    ├── logoutUser.md       # Session management
    ├── createUsersWithArrayInput.md # Array-based user creation
    └── createUser.md       # Single user creation
```

## API Categories

### 🐾 Pet Operations
- **Add/Update**: Create and modify pet records
- **Search**: Find pets by status, tags, or ID
- **Manage**: Update details and handle deletions
- **Upload**: Add pet images

### 📦 Store Operations  
- **Inventory**: Check stock levels and availability
- **Orders**: Place, track, and cancel orders

### 👤 User Operations
- **Authentication**: Login/logout functionality
- **Management**: Create, update, and delete users
- **Batch Operations**: Handle multiple users at once

## Authentication

Most endpoints require the API key `special-key` for testing. The plugin automatically handles authentication headers when needed.

## Error Handling

The plugin includes comprehensive error handling for common scenarios:
- Invalid pet IDs
- Authentication failures  
- Validation errors
- Network timeouts

## Contributing

When extending this plugin:
1. Add new SKILL.md files to the `skills/` directory
2. Follow the established format with YAML frontmatter
3. Include realistic examples and error scenarios
4. Update this README with new functionality

## Support

For issues related to the Swagger Petstore API, visit:
- [Swagger.io](http://swagger.io)
- [IRC: #swagger on freenode](http://swagger.io/irc/)

---

*Built for AI-native development with Cursor IDE*