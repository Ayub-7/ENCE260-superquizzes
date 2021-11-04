Agent* findAgent(char name[], AgentPool* agentPool)
{
    Agent* agent = NULL;
    int i = 0;
    while (i < agentPool->next && agent->name != name) {
        agent = &agentPool->pool[i];
        if (strcmp(agent->name, name) == 0) {
            name = agent->name;
            return agent;

        }
        i++;

    }
    return NULL;
}