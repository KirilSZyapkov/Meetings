# Meetings

function meetings(input) {
    let schedule = {};
    input.forEach(element => {
        let [day, name] = element.split(` `);
        if (schedule.hasOwnProperty(day)) {
            console.log(`Conflict on ${day}!`);
        } else {
            console.log(`Scheduled for ${day}`);
            schedule[day] = name;

        }
    })
    let keys = Object.keys(schedule);
    for (let inputElement of keys) {
        console.log(`${inputElement} -> ${schedule[inputElement]}`);
    }
}
