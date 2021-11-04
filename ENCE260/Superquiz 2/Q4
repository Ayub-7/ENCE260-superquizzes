Agent* newAgent(AgentPool* agentPool)
{
    Agent* agent = NULL;
    if (agentPool->next < MAX_NUMBER_AGENTS) {
        agent = &agentPool->pool[agentPool->next];
        agentPool->next += 1;
    }
    return agent;
}