NAME			= gnl.a

SRCS			= src/get_next_line.c \
			  src/get_next_line_utils.c

OBJS			= $(SRCS:%.c=%.o)

FLAGS			= -Wall -Wextra -Werror

$(NAME):		$(OBJS)
			ar rc $(NAME) $(OBJS)
			ranlib $(NAME)

all:			$(NAME)

%.o: %.c
			gcc $(FLAGS) -I includes -c $< -o $@

clean:
			rm -f $(OBJS)

fclean:			clean
			rm -f $(NAME)

re:			fclean all

.PHONY:			all clean fclean re