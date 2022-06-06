Simulator sim = new();
sim.MasterSim(1000);

class Simulator
{
    public int[] checks = new int[45];
    public int count = 0;
    Random random = new();

    public void MasterSim(int runs)
    {
        int[] finalcount = new int[runs];
        int rand1 = 0;
        int rand2 = 0;
        int rand3 = 0;
        int rand4 = 0;
        int rand5 = 0;
        int rand6 = 0;
        int[] ArrayofRandom = { rand1, rand2, rand3, rand4, rand5, rand6 };
        int max = 3444848;
        for (int j = 0; j < runs; j++)
        {
            this.count = 0;
            Array.Clear(this.checks, 0, this.checks.Length);
            int[] casketArray = new int[6];
            for (int i = 0; this.count < 45; i++)
            {
                casketArray = generateArray(casketArray, max);
                foreach (int roll in casketArray)
                {
                    if (roll < 253) //this is the 1/313168 chance times 23 items times the 11 chances because of the increased max
                    {
                        int current = random.Next(23);
                        newItem(current);
                    }
                    else if (roll <= 505) //this is the 1/149776 chance times 11 items times the 23 chances because of the increased max
                    {
                        int current = 23 + random.Next(11);
                        newItem(current);
                    }
                    else if (roll <= 3288) //this is the 1/13616 chance times 11 items times 253 chances because of the increased max
                    {
                        int current = 34 + random.Next(11);
                        newItem(current);
                    }
                }
                MimicTry();
                finalcount[j] = i + 1;
            }
            Console.WriteLine(finalcount[j]);
        }
    }

    int[] generateArray(int[] testArray, int max)
    {
        for (int i = 0; i < testArray.Length; i++)
        {
            testArray[i] = random.Next(max);
        }
        return testArray;
    }

    void MimicTry()
    {
        int roll = random.Next(228);
        if (roll == 0)
        {
            int item = random.Next(23);
            if (this.checks[item] == 0)
            {
                newItem(item);
            }
        }
    }

    void newItem(int itemIndex)
    {
        this.checks[itemIndex] = 1;
        this.count += 1;
    }
}
