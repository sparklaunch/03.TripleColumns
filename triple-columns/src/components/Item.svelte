<script lang="ts">
    export let data;
    let isHovered: boolean = false;
    const mouseenterHandler: () => void = () => {
        isHovered = true;
    };
    const mouseleaveHandler: () => void = () => {
        isHovered = false;
    };
</script>

<div class="item" style="background-color: {data.color}">
    <div class="item-icon">
        <img src="/assets/{data.icon}" alt={data.title} />
    </div>
    <div class="item-title">
        <p>{data.title}</p>
    </div>
    <div class="item-description">
        <p>{data.description}</p>
    </div>
    <div class="item-button">
        <button
            style="color: {isHovered
                ? 'white'
                : data.color}; background-color: {isHovered
                ? data.color
                : 'white'}"
            on:mouseenter={mouseenterHandler}
            on:mouseleave={mouseleaveHandler}>Learn More</button
        >
    </div>
</div>

<style>
    .item {
        padding: 36px;
        display: flex;
        flex-direction: column;
        height: 500px;
        min-width: 300px;
    }
    .item-icon {
        margin-bottom: 20px;
    }
    .item-title {
        margin-bottom: 20px;
    }
    .item-title > p {
        font-family: "Big Shoulders Display", sans-serif;
        color: white;
        font-size: 36px;
    }
    .item-description {
        flex-grow: 1;
    }
    .item-description > p {
        font-family: "Lexend Deca", sans-serif;
        color: white;
        line-height: 1.5;
    }
    .item-button > button {
        border-radius: 30px;
        border: 2px solid white;
        font-family: "Lexend Deca", sans-serif;
        padding: 18px 30px;
        font-size: 18px;
        cursor: pointer;
        transition: color 0.3s, background-color 0.3s;
    }
    @media screen and (max-width: 1440px) {
        .item {
            height: 400px;
        }
    }
</style>
