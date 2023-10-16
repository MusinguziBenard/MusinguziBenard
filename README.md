import pygame

# Initialize Pygame
pygame.init()

# Set up the display
screen = pygame.display.set_mode((400, 300))
pygame.display.set_caption("Enhanced Graphics Game")

# Load images
player_image = pygame.image.load('player.png')  # Replace 'player.png' with your image file

# Set up the game clock
clock = pygame.time.Clock()

# Game loop
running = True
while running:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

    # Fill the screen with white color
    screen.fill((255, 255, 255))

    # Display the player image
    screen.blit(player_image, (150, 100))  # Adjust the position as needed

    # Update the display
    pygame.display.flip()

    # Control the frame rate
    clock.tick(60)  # Set the desired frame rate

# Quit Pygame
pygame.quit()
