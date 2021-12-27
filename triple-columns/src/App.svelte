<script lang="ts">
    import Card from "./components/Card.svelte";
    interface Car {
        title: string;
        icon: string;
        description: string;
        color: string;
    }
    const data: Car[] = [
        {
            title: "SEDANS",
            icon: "icon-sedans.svg",
            description:
                "Choose a sedan for its affordability and excellent fuel economy. Ideal for cruising in the city or on your next road trip.",
            color: "rgb(222, 122, 33)"
        },
        {
            title: "SUVS",
            icon: "icon-suvs.svg",
            description:
                "Take an SUV for its spacious interior, power, and versatility. Perfect for your next family vacation and off-road adventures.",
            color: "rgb(0, 94, 103)"
        },
        {
            title: "LUXURY",
            icon: "icon-luxury.svg",
            description:
                "Cruise in the best car brands without the bloated prices. Enjoy the enhanced comfort of a luxury rental and arrive in style.",
            color: "rgb(0, 56, 55)"
        }
    ];
</script>

<svelte:head>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" />
    <link
        href="https://fonts.googleapis.com/css2?family=Big+Shoulders+Display:wght@700&family=Lexend+Deca&display=swap"
        rel="stylesheet"
    />
</svelte:head>
<main>
    <Card {data} />
</main>

<style>
    @media all and (max-width: 1440px) {
        main {
            padding: 50px 0;
        }
    }
</style>
