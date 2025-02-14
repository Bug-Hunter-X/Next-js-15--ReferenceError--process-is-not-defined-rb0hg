# Next.js 15: ReferenceError: process is not defined
This repository demonstrates a common error in Next.js 15 applications where accessing environment variables directly in client-side code results in a `ReferenceError: process is not defined` error.

## Bug Description
The bug occurs when attempting to access environment variables (e.g., `process.env.MY_VARIABLE`) within a client-side component.  Since the browser environment does not have a `process` object, this leads to the error.

## Solution
The solution involves using the `getServerSideProps` or `getStaticProps` methods to fetch the environment variables on the server-side before rendering the component.  These fetched variables can then be passed as props to the component.