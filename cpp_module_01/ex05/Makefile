#### ######## #### #### ######## #### #### ######## #### #### ######## #### #### ######## ####

NAME = karen

CC = clang++
CFLAGS = -Wall -Wextra -Werror -std=c++98

#### ######## #### #### ######## #### #### ######## #### #### ######## #### #### ######## ####

ROOT_SOURCES = main Karen

SRC = $(addsuffix .cpp, $(addprefix , $(ROOT_SOURCES)))

#### ######## #### #### ######## #### #### ######## #### #### ######## #### #### ######## ####

OBJ = $(SRC:cpp=o)

#### ######## #### #### ######## #### #### ######## #### #### ######## #### #### ######## ####

all: $(NAME)

$(NAME): $(OBJ)
	@echo "\n"
	@echo "\033[0;32mCompiling ${NAME}..."
	@$(CC) $(CFLAGS) -o $(NAME) $(OBJ)
	@echo "\n\033[0mDone !"

%.o: %.cpp
	@printf "\033[0;33mGenerating ${NAME} objects... %-33.33s\r" $@
	@${CC} ${CFLAGS} -c $< -o $@

clean:
	@echo "\nRemoving binaries..."
	@rm -f $(OBJ)
	@echo "\033[0m"

fclean:
	@echo "\nDeleting objects..."
	@rm -f $(OBJ)
	@echo "\nDeleting executable..."
	@rm -f $(NAME)
	@echo "\033[0m"

re: fclean all

cclean: all clean

#### ######## #### #### ######## #### #### ######## #### #### ######## #### #### ######## ####
