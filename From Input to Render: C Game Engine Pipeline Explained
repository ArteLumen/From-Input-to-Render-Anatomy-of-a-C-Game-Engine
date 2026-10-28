#include <stdio.h>
#include <stdbool.h>

typedef struct {
    float x, y; 
    float speed;   
} Player;

void processInput(bool *isRunning) {
    char command;
    printf("Enter command (q: Quit, w: Move forward): ");
    scanf(" %c", &command);
    
    if (command == 'q') {
        *isRunning = false; 
    }
}

void update(Player *player) {
    player->y += player->speed; 
    printf("[UPDATE] Physics computed. New Position -> Y: %.1f\n", player->y);
}

void render(Player *player) {
    printf("[RENDER] Screen updated. Drawing player at (%.1f, %.1f).\n", player->x, player->y);
    printf("----------------------------------------\n");
}

int main() {
    bool isRunning = true;
    
    Player player = { 0.0f, 0.0f, 1.5f };

    printf("=== C Game Engine Initialized ===\n");

    while (isRunning) {
        processInput(&isRunning); // Read user inputs
        
        if (!isRunning) {
            break;
        }
        
        update(&player);          
        render(&player);        
    }

    printf("=== Game Engine Shutdown ===\n");
    return 0;
}
