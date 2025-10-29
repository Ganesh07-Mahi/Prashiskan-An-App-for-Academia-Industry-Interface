# Prashiskan-An-App-for-Academia-Industry-Interface
class ParshikshanApp:
    def _init_(self):
        self.academic_projects = []
        self.industry_projects = []

    def add_academic_project(self, title, description, university):
        project = {
            "title": title,
            "description": description,
            "university": university,
            "type": "Academic"
        }
        self.academic_projects.append(project)
        print(f"Academic project '{title}' added successfully!")

    def add_industry_project(self, title, description, company):
        project = {
            "title": title,
            "description": description,
            "company": company,
            "type": "Industry"
        }
        self.industry_projects.append(project)
        print(f"Industry project '{title}' added successfully!")

    def view_all_projects(self):
        print("\n--- All Projects in Parshikshan ---")
        if not self.academic_projects and not self.industry_projects:
            print("No projects available yet.")
            return
        
        for project in self.academic_projects + self.industry_projects:
            print(f"Type: {project['type']}")
            print(f"Title: {project['title']}")
            print(f"Description: {project['description']}")
            if project['type'] == 'Academic':
                print(f"University: {project['university']}")
            else:
                print(f"Company: {project['company']}")
            print("-" * 40)

    def run(self):
        print("Welcome to Parshikshan - Academia-Industry Interface App!")
        while True:
            print("\nOptions:")
            print("1. Add Academic Project")
            print("2. Add Industry Project")
            print("3. View All Projects")
            print("4. Exit")
            choice = input("Enter your choice (1-4): ").strip()
            
            if choice == '1':
                title = input("Enter project title: ")
                description = input("Enter project description: ")
                university = input("Enter university name: ")
                self.add_academic_project(title, description, university)
            elif choice == '2':
                title = input("Enter project title: ")
                description = input("Enter project description: ")
                company = input("Enter company name: ")
                self.add_industry_project(title, description, company)
            elif choice == '3':
                self.view_all_projects()
            elif choice == '4':
                print("Thank you for using Parshikshan. Goodbye!")
                break
            else:
                print("Invalid choice. Please try again.")

# Run the app
if _name_ == "_main_":
    app = ParshikshanApp()
    app.run()
