
Here’s the updated README incorporating all the detailed functionality, the TUI, Git integration, and future plans:

---

# CPM: Cancerous Project Manager  

**CPM** (Cancerous Project Manager) is a **bash-based C++ project manager** built for developers who crave a streamlined project management experience without the baggage of full IDEs. Whether you’re using Neovim or just prefer lightweight tools, CPM has you covered with its intuitive TUI and Git-backed folder structure management.  

Why "Cancerous"? Because this tool is as chaotic as its origin story: born out of frustration, built in Bash, and fueled by the desire to keep things uniform and manageable across projects.  

---

## Features  

### Terminal User Interface (TUI)  
The included TUI (shown below) provides a simple, menu-driven interface for managing your C++ projects.  
![CPM TUI Screenshot](./Screenshot.png)  

### Command-Line Options  
Use CPM directly from the terminal with the following commands:  
```text  
Usage:  
  cpm new <project_name>        Create new project  
  cpm add class <name>          Add new class  
  cpm add header <name>         Add new header  
  cpm add package <name> [ver]  Add package  
  cpm rm class <name>           Remove class  
  cpm rm header <name>          Remove header  
  cpm info                      Show project information  
```  

### Key Functionality  

1. **Create New Project**  
   Initializes a new C++ project with a uniform folder structure, including a `src/` directory to house all your classes.  

2. **Add New Classes and Headers**  
   - Adds source (`.cpp`) and header (`.h`) files to your project.  
   - Automatically sets up boilerplate code, with a wizard to let you choose which sections (e.g., constructors, destructors, methods) to include.  
   - Each class gets its own folder under `src/` for better organization.  

3. **Remove Classes/Headers**  
   - Safely removes files from the project while ensuring Git commits reflect these changes.  

4. **Add Packages**  
   - (Currently using CMake package management.)  
   - Support for a header-only package manager is planned for the future.  

5. **Show Project Info**  
   - Displays Git commit history.  
   - Lists all classes in the project.  
   - Future features will build on this to provide additional insights and utilities.  

6. **Git Integration**  
   - Every time you add a class, CPM commits the changes to Git automatically.  
   - For removals, CPM also ensures a clean Git history.  

---

## Installation  

Clone the repository and make the script executable:  
```bash  
git clone https://github.com/yourusername/cpm.git  
cd cpm  
chmod +x cpm  
```  

Add it to your PATH for convenient usage:  
```bash  
export PATH=$PATH:/path/to/cpm  
```  

---

## Folder Structure  

CPM enforces a uniform folder structure for all projects:  
```text  
project_root/  
├── src/  
│   ├── Class1/  
│   │   ├── Class1.h  
│   │   └── Class1.cpp  
│   ├── Class2/  
│   │   ├── Class2.h  
│   │   └── Class2.cpp  
├── include/ (for external libraries, if any)  
├── CMakeLists.txt  
└── README.md  
```  

This organization ensures consistency across all projects, making it easier to navigate and maintain.  

---

## Roadmap  

- [x] **TUI Support** for easy navigation and management.  
- [x] **Git Integration** for automatic commits on add/remove operations.  
- [x] **Boilerplate Setup** for new classes with customizable sections.  
- [ ] **Header-Only Package Manager** to simplify dependency management.  
- [ ] **Advanced Info Tab** to display project statistics and future utilities.  
- [ ] **Build System Enhancements** for smoother CMake integration.  

---

## Contributing  

Contributions are welcome! If you have ideas for new features or want to improve existing functionality, feel free to open an issue or submit a pull request.  

---

## License  

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.  

---

**Welcome to the chaos of CPM. Happy hacking!** 🎉  

 
