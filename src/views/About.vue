<template>
  <main class="col-md-9 ms-sm-auto col-lg-10 px-md-4">
    <br>
    <div class="container">

      <h1 class="mt-3 green">About</h1>
      <br>
      <div class="column">
        <h3>Overview</h3>
        <p> Our dashboard tries to provide a live-update platform for the investors which visualizes the stock market by
          analyzing global and domestic indices and sector data. The price data we used is directly yahoo finance. In
          addition, we offer SPY index price prediction.
          Therefore, investors can make a macro-overview of the equity market and make further investment decisions.
        </p>
      </div>

      <div class="column">
        <h3>Market Index</h3>
        <p>We set the domestic market summary info as the main page and
          plot candle charts of three representative indices(SPY, QQQ, IWM) to display price and
          volume information. In addition, we also provide intra-day price line charts for the three indices, which
          allow users to access minute-tick data. Moreover, users can select a different date using the
          date picker component to get historical intraday price information.</p>
        <p>As for the intraday part, because of the unstable API of Alpha Academy from
          which we get the real-time data, we can not get the data frequently, so Market Index Page
          can not been refresh too frequently.</p>
      </div>

      <div class="column">
        <h3>Sector Overview</h3>
        <p>we provide four types of charts show daily sector information, includes Multiline
          Graph, Bar Chart, Pie Chart, Treemap. Most of these chart support the function of real-time update, the data
          can update every 10 seconds in trade time. Users can select the time period and index by using buttons and
          time
          sliders. they also can search the histroy data by using data packer.</p>
      </div>

      <div class="column">
        <h3>Global Market</h3>
        <p>World map on this page shows the real-time index value and the
          rise and fall of the stock indices of 18 countries. In addition to getting real-time updates
          on the same day, users can also select a date to get historical information.</p>
      </div>

      <div class="column">
        <h3>Forecast</h3>
        <p>We use an auto-regression model with time series to predict the stock market based on the strong
          auto-correlation and high Pearson Correlation Coefficient. The prediction from the regression model has
          continuity and hysteresis,
          specifically, the regression model retains the direction of the prices trend well, but most of
          the time lags behind the rapid change of the price direction.</p>
      </div>

      <br><br>
      <footer class="footer navbar-fixed-bottom ">
        <!-- <h6 class="text-center text-muted">Support</h6> -->
        <ul class="nav justify-content-center border-bottom pb-3 mb-3">
          <li class="nav-item nav-link px-2" style="color: black;">Support</li>
          <li class="nav-item nav-link px-2 text-muted">Yidan Wang <a
              href="mailto:shaozhen@usc.edu">yidanwan@usc.edu</a> </li>
          <li class="nav-item nav-link px-2 text-muted">Shaozhen Lu <a
              href="mailto:shaozhen@usc.edu">shaozhen@usc.edu</a></li>
          <li class="nav-item nav-link px-2 text-muted">Shu Wang: <a href="mailto:shaozhen@usc.edu">swang780@usc.edu</a>
          </li>
          <li class="nav-item nav-link px-2 text-muted">Peng Rui: <a href="mailto:shaozhen@usc.edu">prui@usc.edu</a>
          </li>

        </ul>
        <p class="text-center text-muted"><a href="#" class="text-center text-muted">Video Link</a> </p>
      </footer>
    </div>
  </main>
</template>