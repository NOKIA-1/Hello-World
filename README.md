# World
•readme-edits•


const client = new StreamrClient({
    auth: {
        privateKey: 'your-private-key'
    }
})

const sub = await client.subscribe({
    stream: 'streamId',
    partition: 0, // Optional, defaults to zero. Use for partitioned streams to select partition.
    // optional resend options here
}, (message, metadata) => {
    // This is the message handler which gets called for every incoming message in the stream.
    // Do something with the message here!
})

