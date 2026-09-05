<template>
    <main>
        <!-- HERO SECTION -->
        <section class="hero" aria-labelledby="hero-heading">
            <div class="hero-container">
                <img src="@/assets/images/image-mockups.png"
                    alt="Digitalbank mobile app showing dashboard with accounts and transactions">
                <div class="hero-desc">
                    <h1 id="hero-heading">Next generation digital banking</h1>
                    <p>
                        Take your financial life online. Your Digitalbank account will be a
                        one-stop-shop for spending, saving, budgeting, investing, and much
                        more.
                    </p>
                    <button type="button" class="btn">Request Invite</button>
                </div>
            </div>

            <!-- Desktop mockup - decorative only -->
            <div class="desktop-img" aria-hidden="true"></div>
        </section>

        <!-- FEATURES SECTION -->
        <section class="features" aria-labelledby="features-heading">
            <div class="features-container">
                <div class="why-choose">
                    <h2 id="features-heading">Why choose Digitalbank?</h2>
                    <p>
                        We leverage Open Banking to turn your bank account into your
                        financial hub. Control your finances like never before.
                    </p>
                </div>

                <ul>
                    <li>
                        <img src="@/assets/icons/icon-online.svg" aria-hidden="true" alt="">
                        <div>
                            <h3>Online Banking</h3>
                            <p>
                                Our modern web and mobile applications allow you to keep track
                                of your finances wherever you are in the world.
                            </p>
                        </div>
                    </li>
                    <li>
                        <img src="@/assets/icons/icon-budgeting.svg" aria-hidden="true" alt="">
                        <div>
                            <h3>Simple Budgeting</h3>
                            <p>
                                See exactly where your money goes each month. Receive
                                notifications when you&rsquo;re close to hitting your limits.
                            </p>
                        </div>
                    </li>
                    <li>
                        <img src="@/assets/icons/icon-onboarding.svg" aria-hidden="true" alt="">
                        <div>
                            <h3>Fast Onboarding</h3>
                            <p>
                                We don&rsquo;t do branches. Open your account in minutes online
                                and start taking control of your finances right away.
                            </p>
                        </div>
                    </li>
                    <li>
                        <img src="@/assets/icons/icon-api.svg" aria-hidden="true" alt="">
                        <div>
                            <h3>Open API</h3>
                            <p>
                                Manage your savings, investments, pension, and much more from
                                one account. Tracking your money has never been easier.
                            </p>
                        </div>
                    </li>
                </ul>
            </div>
        </section>

        <!-- ARTICLES SECTION -->
        <section class="article" aria-labelledby="articles-heading">
            <div class="article-container">
                <h2 id="articles-heading">Latest Articles</h2>
                <div class="article-lists">
                    <article class="card">
                        <img src="@/assets/images/image-currency.jpg"
                            alt="Fanned out foreign banknotes including US dollars and euros">
                        <div class="content">
                            <p class="publisher">By Claire Robinson</p>
                            <div class="info">
                                <h3>Receive money in any currency with no fees</h3>
                                <p>
                                    The world is getting smaller and we&rsquo;re becoming more
                                    mobile. So why should you be forced to only receive money in a
                                    single …
                                </p>
                            </div>
                        </div>
                    </article>

                    <article class="card">
                        <img src="@/assets/images/image-restaurant.jpg"
                            alt="Plated restaurant dish being enjoyed at a table setting">
                        <div class="content">
                            <p class="publisher">By Wilson Hutton</p>
                            <div class="info">
                                <h3>Treat yourself without worrying about money</h3>
                                <p>
                                    Our simple budgeting feature allows you to separate out your
                                    spending and set realistic limits each month. That means you …
                                </p>
                            </div>
                        </div>
                    </article>

                    <article class="card">
                        <img src="@/assets/images/image-plane.jpg"
                            alt="View from an airplane window showing the wing above clouds">
                        <div class="content">
                            <p class="publisher">By Wilson Hutton</p>
                            <div class="info">
                                <h3>Take your Digitalbank card wherever you go</h3>
                                <p>
                                    We want you to enjoy your travels. This is why we don&rsquo;t
                                    charge any fees on purchases while you&rsquo;re abroad.
                                    We&rsquo;ll even ...
                                </p>
                            </div>
                        </div>
                    </article>

                    <article class="card">
                        <img src="@/assets/images/image-confetti.jpg"
                            alt="Colorful confetti falling against a blue background">
                        <div class="content">
                            <p class="publisher">By Claire Robinson</p>
                            <div class="info">
                                <h3>Our invite-only Beta accounts are now live!</h3>
                                <p>
                                    After a lot of hard work by the whole team, we&rsquo;re
                                    excited to launch our closed beta. It&rsquo;s easy to request
                                    an invite through ...
                                </p>
                            </div>
                        </div>
                    </article>
                </div>
            </div>
        </section>
    </main>
</template>