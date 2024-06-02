<script lang="ts">
    import Icon from "@iconify/svelte";
    type Schedule = {
        [key: string]: { start: string; end: string };
    };
    const schedule = {
        Monday: { start: "17:00", end: "21:00" },
        Tuesday: { start: "00:00", end: "23:59" },
        Wednesday: { start: "17:00", end: "21:00" },
        Thursday: { start: "17:00", end: "21:00" },
        Friday: { start: "17:00", end: "21:00" },
        Saturday: { start: "17:00", end: "21:00" },
        Sunday: { start: "00:00", end: "00:00" },
    };
    const daysOfWeek = Object.keys(schedule);

    function isAvailable(day: string): boolean {
        const now = new Date();
        const currentTime = now.toLocaleTimeString([], {
            hour: "2-digit",
            minute: "2-digit",
            hour12: false,
        });
        console.log(currentTime);

        if (day === "Sunday") return false;

        const { start, end } = schedule[day as keyof typeof schedule];
        return currentTime >= start && currentTime <= end;
    }

    function getDay(day: string) {
        //tailwind class
        return isAvailable(day) ? "text-success" : "text-error";
    }
    function getText(day: string) {
        //text
        return isAvailable(day) ? "Available" : "Closed";
    }

    //dynamically get day from date
    //get day from date

    const currentDay = new Date().toLocaleDateString("en-US", {
        weekday: "long",
    });
    console.log(currentDay);
</script>

<div class="mx-auto container p-2">
    <div class="py-2">
        <h1 class="text-4xl font-bold mb-2">Interested?</h1>
        <h2 class="text-2xl font-light">Get in touch today!</h2>
    </div>

    <!-- map showing location available -->
    <div class="container mx-auto md:p-5">
        <div class="card bg-base-100 shadow-xl">
            <div class="card-body">
                <h2 class="card-title">Area available for car repair</h2>
                <p class="mb-4">Charlotte, NC</p>
                <iframe
                    src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d208648.51845835603!2d-80.83982894999997!3d35.203153450000016!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x88541fc4fc381a81%3A0x884650e6bf43d164!2sCharlotte%2C%20NC!5e0!3m2!1sen!2sus!4v1709590417525!5m2!1sen!2sus"
                    width="600"
                    height="450"
                    style="border:0;"
                    allowfullscreen
                    loading="lazy"
                    referrerpolicy="no-referrer-when-downgrade"
                    title="Area available for car repair map"
                    class="border border-primary rounded-lg w-full h-96 md:h-96 map"
                ></iframe>
                <p class="mt-4 text-sm italic">
                    Note: service is only available in Charlotte, NC
                </p>
            </div>
        </div>
    </div>

    <!-- row displaying phone number and hours available -->
    <div class="container mx-auto md:p-5">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
            <div class="card bg-base-100 shadow-xl">
                <div class="card-body">
                    <h2 class="card-title">
                        <Icon icon="mdi:phone" class="mr-2" />
                        Phone
                    </h2>
                    <p class="text-xl">704-995-9486</p>
                </div>
            </div>
            <div class="card bg-base-100 shadow-xl"></div>
        </div>
    </div>

    <!-- Nextdoor link -->
    <div class="container mx-auto md:p-5">
        <div class="card bg-base-100 shadow-xl">
            <div class="card-body">
                <h2 class="card-title">On Nextdoor?</h2>
                <p>Get in contact with me on Nextdoor</p>
                <div class="card-actions">
                    <a
                        class="btn btn-primary"
                        href="https://nextdoor.com/profile/01L3TtYWhd547HkmK"
                        target="_blank"
                    >
                        <Icon icon="ph:door-bold" class="mr-2 text-3xl" />
                        Nextdoor
                    </a>
                </div>
            </div>
        </div>
    </div>
</div>

<style>
    :global(.map) {
        height: 500px;
    }
</style>
