<script>
    import Field from "./Field.Svelte";
    let attendee = {
        "username": "Test",
        "civility":"M",
        "login":"gwenael@captusite.fr"
    }
    let otherAttendee = {
        "username":"Doe",
        "civility":"Mme",
        "login":"test@captusite.fr"
    }
    const switchAttendee = () => {
        attendee = {...otherAttendee}
    }

</script>


<table>
    <tr>
        <td>{otherAttendee['username']}</td>
        <td>{otherAttendee['civility']}</td>
        <td>
            <button type="button" 
                on:click={switchAttendee}>
                Edit
            </button>
        </td>
    </tr>
</table>

<form id="setData">
    <Field type="text" name="civility"  value={attendee['civility']} />
    <Field type="text" name="username"  value={attendee['username']} />
    <Field type="email" name="login"    value={attendee['login']} />
    <button type="submit">Envoyer</button>
</form>