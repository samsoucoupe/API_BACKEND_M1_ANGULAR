# API_BACKEND_M1_ANGULAR

This project is an API backend for the M1 Angular application.

## Important Notes

- This project uses `_id` instead of `id` for identifying documents.

## Purge Function

To clean all assignments in the backend, the following function is used:

```typescript
function purge(req, res) {
    Assignment.deleteMany({}, (err) => {
        if(err){
            res.send(err);
        }
        res.json({message: 'All assignments deleted'});
    });
}
```

This function deletes all assignments from the database and returns a message indicating the deletion was successful.