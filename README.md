### Messages broadcaster
Our system is a Rails app that will receive and process messages that are related to different topics.

   1. Create a new rails app `rails new --api APP_NAME`
   2. Create a `topics` table with a column `name` not null. Topics must be unique.
   3. Create a `messages` table with a not null `body` column, a `status` column, and an association to `topics`. The possible values for `status` are `received` and `processed`, being `received` the initial value.
   4. Add the proper model associations and constraints.
   5. We need an endpoint to create new messages.
   6. Every new message needs to be processed with a background job. It's going to be heavy processing, but for now, we only want to mark the message status as `processed`.
   7. Create some basic tests for the API and message processing.
  