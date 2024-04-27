#include <graphics.h>
#include <conio.h>

int main() {
    int gd = DETECT, gm;
    initgraph(&gd, &gm, "C:\\TC\\BGI");

    // اللون الأسود
    setfillstyle(SOLID_FILL, BLACK);
    bar(0, 0, getmaxx(), getmaxy() / 3);

    // اللون الأبيض
    setfillstyle(SOLID_FILL, WHITE);
    bar(0, getmaxy() / 3, getmaxx(), 2 * getmaxy() / 3);

    // اللون الأخضر
    setfillstyle(SOLID_FILL, GREEN);
    bar(0, 2 * getmaxy() / 3, getmaxx(), getmaxy());

    // المثلث الأحمر
    setfillstyle(SOLID_FILL, RED);
    int points[] = {0, getmaxy() / 3, getmaxx() / 4, getmaxy() / 2, 0, 2 * getmaxy() / 3, 0, getmaxy() / 3};
    fillpoly(4, points);

    getch();
    closegraph();
    return 0;
}
