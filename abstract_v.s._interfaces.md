# `abstrac`
what you want to generalize behaviours
# `interface`
what you want to make a standart behaviours


# e.g.
```cpp
// interface 1
class ableEat {
public:
    virtual void eatfood() = 0;
};
// interface 1
class ableSleeping {
public:
    virtual void sleeping() = 0;
};

// abstract class 1
class Human: public ableEat, ableSleeping {
    virtual void eatfood() = 0;
    virtual void sleeping() = 0;
public:
    void work() {
        cout << "get money!" << endl;
    };
};

// abstract class 2
class Animal : public ableEat, ableSleeping {
    virtual void eatfood() = 0;
    virtual void sleeping() = 0;
public:
    void work() {
        cout << "use money :)" << endl;
    };
};

// class 1
class Girls : public Human{
public:
    virtual void eatfood()
    {
        cout << "A girl is eating Pizza." << endl;
    };
    virtual void sleeping()
    {
        cout << "A girl is sleeping." << endl;
    };
};

// class 2
class Cat : public Animal {
public:

    virtual void eatfood()
    {
        cout << "A cat is eating a fish." << endl;
    };
    virtual void sleeping()
    {
        cout << "A cat is sleeping." << endl;
    };
};

int main()
{
    Girls* g1 = new Girls();
    g1->eatfood();
    g1->sleeping();
    g1->work();

    Cat* c1 = new Cat();
    c1->eatfood();
    c1->sleeping();
    c1->work();

}
```