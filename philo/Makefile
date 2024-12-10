CC = cc
CFLAG = -Wall -Wextra -Werror
FFLAG = -fsanitize=thread
NAME = philosopher
HEAD = ./includes/php.h
SRCS = srcs/main.c \
		srcs/process.c \
		srcs/src1.c \
		srcs/src2.c \
		srcs/src3.c \
		srcs/src4.c \
		srcs/thread1.c \
		srcs/action.c \
		
OBJS = $(SRCS:.c=.o)

all : $(NAME)

$(NAME) : $(OBJS) $(HAED)
	$(CC) $(CFLAG) -I $(HEAD) -o $(NAME) $(OBJS)

.c.o :
	$(CC) $(CFLAG) -I $(HEAD) -c $< -o $@

clean : 
	rm -rf *.o

fclean : clean
	rm -rf $(NAME)

re : fclean all

.PHONY : all re clean fclean
