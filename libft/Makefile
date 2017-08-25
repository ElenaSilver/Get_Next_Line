# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: eserebry <eserebry@student.42.fr>          +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2017/04/11 21:47:23 by eserebry          #+#    #+#              #
#    Updated: 2017/06/22 18:03:09 by eserebry         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = libft.a

FLAGS = -Wall -Wextra -Werror -c -I -fsanitize=address

INCLUDES =	"includes"

FUNCTION = memalloc memdel memcpy memmove memset strchr strdup strjoin strlen \
strsub strnew strcat strcpy

FT_FUNCTION = $(addprefix ft_, $(FUNCTION))
SRC = $(addsuffix .c, $(FT_FUNCTION))

OBJ = $(SRC:.c=.o)

RM = rm -f

.PHONY: all clean fclean re

all: $(NAME)

$(NAME): $(OBJ)
		ar rc $(NAME) $(OBJ)
		ranlib $(NAME)

$(COMPILED): %.o: %.c
	$(CC) $(FLAGS) $< -o $@ -I $(INCLUDES)

clean:
		$(RM) $(OBJ)

fclean: clean
		$(RM) $(NAME)

re: fclean all
