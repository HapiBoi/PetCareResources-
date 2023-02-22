# PetCareResources-
Pet care resources - users can access articles and resources on pet care, including tips on nutrition, exercise, and health.
class PetCareResource:
    def __init__(self, resource_id, title, description):
        self.resource_id = resource_id
        self.title = title
        self.description = description

class PetCareResources:
    def __init__(self):
        self.resources = []

    def add_resource(self, resource):
        self.resources.append(resource)

    def search(self, query):
        results = []
        for resource in self.resources:
            if query.lower() in resource.title.lower() or query.lower() in resource.description.lower():
                results.append(resource)
        return results

    def view(self, id):
        for resource in self.resources:
            if resource.resource_id == id:
                return resource
        return None

def main():
    # Initialize PetCareResources object
    pet_care_resources = PetCareResources()

    # Add some sample resources
    pet_care_resources.add_resource(PetCareResource(1, "How to Groom Your Dog", "Learn how to groom your dog like a pro."))
    pet_care_resources.add_resource(PetCareResource(2, "Top 10 Tips for Training Your Cat", "Get your cat to do what you want with these simple training tips."))
    pet_care_resources.add_resource(PetCareResource(3, "Feeding Your Rabbit: What You Need to Know", "Everything you need to know about feeding your rabbit a healthy diet."))

    # Loop to prompt user for input and display results
    while True:
        print("Welcome to the Pet Care Resources app!")
        print("Please choose an option:")
        print("1. Search for resources")
        print("2. View a resource")
        print("3. Add a resource")
        print("4. Quit")
        choice = input("> ")

        if choice == "1":
            query = input("Enter a search query: ")
            results = pet_care_resources.search(query)
            if results:
                print("Search results:")
                for result in results:
                    print(f"{result.resource_id}: {result.title}")
            else:
                print("No results found.")

        elif choice == "2":
            resource_id = input("Enter a resource ID: ")
            resource = pet_care_resources.view(int(resource_id))
            if resource:
                print(f"{resource.title}: {resource.description}")
            else:
                print("Resource not found.")

        elif choice == "3":
            resource_id = input("Enter a resource ID: ")
            title = input("Enter a title: ")
            description = input("Enter a description: ")
            pet_care_resources.add_resource(PetCareResource(int(resource_id), title, description))
            print("Resource added.")

        elif choice == "4":
            print("Goodbye!")
            break

        else:
            print("Invalid choice. Please try again.")

if __name__ == "__main__":
    main()
