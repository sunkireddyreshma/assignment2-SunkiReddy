# assignment2-SunkiReddy
markdown repo
# Sunkireddy Reshmareddy
#### Location:Charminar
 Located at Old City of **Hyderabad**.Charminar is a **square-shaped structure** built out of granite and lime mortar.Charminar is at its best when it lights up at night in the lively neighborhood of colorful bazaar and shops.

 ---

 # Travelling Spot

 1. Reaching to kansas airport from maryville.
 2. Kansas to our city Hyderabad through flight.
 3. After landing book a cab to charminar and  at the west lies the Laad Bazaar, and to the southwest lies the richly ornamented granite Makkah Masjid.

 * It is flanked by four minarets on every corner which are 48.7 meters high.
 * The mosque is located on the top floor, and visitors can enjoy a short climb of the 149 steps to get there.
 * Charminar is at its best when it lights up at night in the lively neighborhood of colorful bazaar and shops

---

# Creating Table

| Food/Drink | Location | Amount |
| --- | --- | ---: |
| birayani | tankbund| 500 |
| pizza | pizzahut| 350|
| icecrean | creamstone | 200 |
| samosa| bakery | 50 |

---

# Quotation
> Unity is strength .when there is teamwork and collaboration, wonderful things can be achieved - ***Mattie Stepanek***
> You only live once, but if you do it right, once is enough. - ***Mae West***

---

# Algorithms
> Graham's Scan Algorithm is an efficient algorithm for finding the convex hull of a finite set of points in the plane with time complexity O(N log N). The algorithm finds all vertices of the convex hull ordered along its boundary. It uses a stack to detect and remove concavities in the boundary efficiently.
Link: <https://iq.opengenus.org/graham-scan-convex-hull/>
Link to Source Code: <https://cp-algorithms.com/geometry/grahams-scan-convex-hull.html>
~~~
struct pt {
    double x, y;
};

bool cmp(pt a, pt b) {
    return a.x < b.x || (a.x == b.x && a.y < b.y);
}

bool cw(pt a, pt b, pt c) {
    return a.x*(b.y-c.y)+b.x*(c.y-a.y)+c.x*(a.y-b.y) < 0;
}

bool ccw(pt a, pt b, pt c) {
    return a.x*(b.y-c.y)+b.x*(c.y-a.y)+c.x*(a.y-b.y) > 0;
}

void convex_hull(vector<pt>& a) {
    if (a.size() == 1)
        return;

    sort(a.begin(), a.end(), &cmp);
    pt p1 = a[0], p2 = a.back();
    vector<pt> up, down;
    up.push_back(p1);
    down.push_back(p1);
    for (int i = 1; i < (int)a.size(); i++) {
        if (i == a.size() - 1 || cw(p1, a[i], p2)) {
            while (up.size() >= 2 && !cw(up[up.size()-2], up[up.size()-1], a[i]))
                up.pop_back();
            up.push_back(a[i]);
        }
        if (i == a.size() - 1 || ccw(p1, a[i], p2)) {
            while(down.size() >= 2 && !ccw(down[down.size()-2], down[down.size()-1], a[i]))
                down.pop_back();
            down.push_back(a[i]);
        }
    }

    a.clear();
    for (int i = 0; i < (int)up.size(); i++)
        a.push_back(up[i]);
    for (int i = down.size() - 2; i > 0; i--)
        a.push_back(down[i]);
}
~~~

[Click Here to know More about Me](https://github.com/sunkireddyreshma/assignment2-SunkiReddy/blob/main/AboutMe.md)