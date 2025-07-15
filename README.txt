#  lookUpProfile Function (JavaScript Contact Lookup)

##  What It Does

The `lookUpProfile` function allows you to search through a list of contacts (JavaScript objects in an array) and return a specific piece of information (like their phone number or interests) **based on their first name**.

It checks two things:
1. Does the contact with the given first name exist?
2. Does that contact have the requested property?

Depending on what it finds, it returns:
- The **value** of the property if both are valid
- `"No such property"` if the contact exists but the property doesn't
- `"No such contact"` if no contact with that name is found

---

##  Function Definition

```javascript
function lookUpProfile(name, prop) {
  for (let i = 0; i < contacts.length; i++) {
    if (contacts[i].firstName === name) {
      if (contacts[i].hasOwnProperty(prop)) {
        return contacts[i][prop];
      } else {
        return "No such property";
      }
    }
  }
  return "No such contact";
}
