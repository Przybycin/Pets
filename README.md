# Pets
Cats and badgers

cat_image = "=^_^="
badger_image = "^._.^"

class Animal:
    __name = ""
    __species = ""
    __height = 0
    __weight = 0
    __colour = 0
    __sound = ""


    def __init__(self, name, species, height, weight, colour, sound, cuteness):
        self.__name = name
        self.__species = species
        self.__height = height
        self.__weight = weight
        self.__colour = colour
        self.__sound = sound
        self.__cuteness = cuteness

    def set_name(self, name):
        self.__name = name

    def set_species(self, species):
        self.__species = species

    def set_height(self, height):
        self.__height = height

    def set_weight(self, weight):
        self.__weight = weight

    def set_colour(self, colour):
        self.__colour = colour

    def set_sound(self, sound):
        self.__sound = sound

    def set_cuteness(self, cuteness):
        self.__cuteness = cuteness

    def get_name(self):
        return self.__name

    def get_species(self):
        return self.__species

    def get_height(self):
        return self.__height

    def get_weight(self):
        return self.__weight

    def get_colour(self):
        return self.__colour

    def get_sound(self):
        return self.__sound

    def get_cuteness(self):
        return self.__cuteness

    def get_type(self):
        print("Animal")

    def toString(self):
        return "{} is a {} {}. He is {}cm tall, weighs {}kg and says {}." \
               " He has a cuteness rating of {} out of 10    ".format(self.__name,
                                                                     self.__colour,
                                                                       self.__species,
                                                                       self.__height,
                                                                    self.__weight,
                                                                 self.__sound,
                                                                 self.__cuteness)

cat = Animal('Mr.Meows', 'cat', 20, 11, 'black', 'meow', 7)


print(cat.toString()+cat_image)




class Badger(Animal):
    __owner = ""

    def __init__(self, name, species, height, weight, colour, sound, cuteness, owner):
        self.__owner = owner
        super(Badger, self).__init__(name, species, height, weight, colour, sound, cuteness)

    def set_owner(self, owner):
        self.__owner = owner

    def get_owner(self):
        return self.__owner

    def get_type(self):
        print("Badger")


    def toString(self):
        return "{} is a {} {}. He is {}cm tall, weighs {}kg and says {}." \
               " He has a cuteness rating of {} out of 10. {} is his owner.    ".format(self.__name,
                                                                                        self.__colour,
                                                                                        self.__species,
                                                                                        self.__height,
                                                                                        self.__weight,
                                                                                        self.__sound,
                                                                                        self.__cuteness,
                                                                                        self.__owner)



    def multiple_sounds(self, how_many = None):
        if how_many is None:
            print(self.get_sound())
        else:
            print(self.get_sound() * how_many)


stripes = Badger('Mr.Stripes', 'badger', 40, 75, 'black and white', 'Earghhhaah', 6, 'Dave' )

print(stripes.toString()+badger_image)


class AnimalTest:
    def get_type(self, animal):
        animal.get_type()


test_animals = AnimalTesting

test_animals.get_type(cat)
test_animal.get_type(stripes)

stripes.multiple_sounds(1)
stripes.multiple_sounds()
