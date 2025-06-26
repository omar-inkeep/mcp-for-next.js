## Usage

This sample app uses the [Vercel MCP Adapter](https://www.npmjs.com/package/@vercel/mcp-adapter) that allows you to drop in an MCP server on a group of routes in any Next.js project.

Update `app/[transport]/route.ts` with your tools, prompts, and resources following the [MCP TypeScript SDK documentation](https://github.com/modelcontextprotocol/typescript-sdk/tree/main?tab=readme-ov-file#server).

## Using Inkeep Analytics

This sample app logs the user question and the assistant respond to Inkeep analytics using the [inkeep-analytics-typescript sdk](https://github.com/inkeep/inkeep-analytics-typescript)

## Environment variables

- You need to set INKEEP_API_KEY. If you don't have one, create one in your Inkeep portal. See more info related to this in [our documentation](https://docs.inkeep.com/analytics-api/authentication#get-an-api-key)
- You can optionally set INKEEP_API_BASE_URL (defaults to 'https://api.inkeep.com/v1')

## Notes for running on Vercel

- Make sure you have [Fluid compute](https://vercel.com/docs/functions/fluid-compute) enabled for efficient execution
- After enabling Fluid compute, open `app/route.ts` and adjust `maxDuration` to 800 if you using a Vercel Pro or Enterprise account
- [Deploy the Next.js MCP template](https://vercel.com/templates/next.js/model-context-protocol-mcp-with-next-js)
