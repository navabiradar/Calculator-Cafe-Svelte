<script>
	import { Finance } from 'financejs';
	import { currency } from '../Currency';

	let cur = currency;

	let finance = new Finance();

	let formValues = {
		currency: 'USD',
		initialAmount: 0,
		rate: 0,
		timePeriod: 0,
		periods: 'Years',
		compoundInterest: 'Quaterly',
		interestEarned: 0,
		numOfCompounding: 0,
		numOfPeriods: 0,
		result: 0,
		words: '',
		currencyIcon: '',
		localeCode: 'en-US'
	};

	function Result() {
		switch (formValues.periods) {
			case 'Years':
				formValues.numOfPeriods = formValues.timePeriod;
				break;
			case 'Months':
				formValues.numOfPeriods = (formValues.timePeriod / 12).toFixed(2);
				break;
			case 'Days':
				formValues.numOfPeriods = (formValues.timePeriod / 365).toFixed(2);
				break;
		}

		switch (formValues.compoundInterest) {
			case 'Daily':
				formValues.numOfCompounding = 365;
				break;
			case 'Weekly':
				formValues.numOfCompounding = 52;
				break;
			case 'Monthly':
				formValues.numOfCompounding = 12;
				break;
			case 'Quaterly':
				formValues.numOfCompounding = 4;
				break;
			case 'Yearly':
				formValues.numOfCompounding = 1;
				break;
		}

		formValues.result = finance.CI(
			formValues.rate,
			formValues.numOfCompounding,
			formValues.initialAmount,
			formValues.numOfPeriods
		);
		formValues.interestEarned = (formValues.result - formValues.initialAmount).toFixed(2);
	}
</script>

<svelte:head>
	<title>Discover Your FD Interest with Our Free Calculator</title>
	<meta
		name="description"
		content="Calculate your fixed deposit returns easily with our user-friendly Fixed Deposit Calculator. Start planning your savings today and watch your money grow!"
	/>
</svelte:head>

<div class="container-xl">
	<div class="row">
		<div class="col-md-4">
			<div class="card border-primary rounded-0">
				<div class="card-header rounded-0 bg-blue">
					<h3 class="card-title text-uppercase text-white">Fixed Deposit Calculator</h3>
				</div>
				<div class="card-body">
					<div class="mb-3">
						<label class="form-label" for="">Select Currency</label>
						<div class="form-selectgroup">
							{#each cur as item}
								<label class="form-selectgroup-item">
									<input
										type="radio"
										bind:group={formValues.currency}
										class="form-selectgroup-input"
										value={item.shortName}
									/>
									<span class="form-selectgroup-label"
										><!-- Download SVG icon from http://tabler-icons.io/i/sun -->
										{@html item.icon}
									</span>
								</label>
							{/each}
						</div>
					</div>

					<div class="mb-3">
						<div class="col-12">
							<label class="form-label" for="">Initial Investment / Starting Amount</label>
							<div class="input-group mb-2">
								<input
									type="number"
									min="0"
									bind:value={formValues.initialAmount}
									class="form-control"
									placeholder="Enter Amount"
									autocomplete="off"
								/>
							</div>
						</div>
					</div>

					<div class="row">
						<div class="col-6">
							<label class="form-label" for="interest">Interest Rate</label>
							<div class="input-icon mb-3">
								<input
									type="number"
									bind:value={formValues.rate}
									min="0"
									class="form-control"
									placeholder="Interest Rate"
								/>
								<span class="input-icon-addon">
									<svg
										xmlns="http://www.w3.org/2000/svg"
										width="24"
										height="24"
										viewBox="0 0 24 24"
										fill="none"
										stroke="currentColor"
										stroke-width="2"
										stroke-linecap="round"
										stroke-linejoin="round"
										class="icon icon-tabler icons-tabler-outline icon-tabler-percentage"
										><path stroke="none" d="M0 0h24v24H0z" fill="none" /><path
											d="M17 17m-1 0a1 1 0 1 0 2 0a1 1 0 1 0 -2 0"
										/><path d="M7 7m-1 0a1 1 0 1 0 2 0a1 1 0 1 0 -2 0" /><path
											d="M6 18l12 -12"
										/></svg
									>
								</span>
							</div>
						</div>
						<div class="col-6">
							<label class="form-label" for="compound">Compound</label>
							<select name="user" bind:value={formValues.compoundInterest} class="form-select">
								<option value="Daily">Daily</option>
								<option value="Weekly">Weekly</option>
								<option value="Monthly">Monthly</option>
								<option selected value="Quaterly">Quaterly</option>
								<option value="Yearly">Yearly</option>
							</select>
						</div>
					</div>

					<div class="mb-3">
						<div class="col-12">
							<div class="row">
								<div class="col-6">
									<label class="form-label" for="time">Time Period</label>
									<div class="input-icon mb-3">
										<input
											type="number"
											bind:value={formValues.timePeriod}
											min="0"
											class="form-control"
											placeholder=""
										/>
										<span class="input-icon-addon">
											<!-- Download SVG icon from http://tabler-icons.io/i/search -->
										</span>
									</div>
								</div>
								<div class="col-6">
									<label class="form-label" for="type">Type</label>
									<select name="type" bind:value={formValues.periods} class="form-select">
										<option value="Years">Years</option>
										<option selected value="Months">Months</option>
										<option value="Days">Days</option>
									</select>
								</div>
							</div>
						</div>
					</div>
				</div>
				<div class="card-footer rounded-0 border-primary text-end">
					<button type="submit" class="btn btn-danger">Clear</button>
					<button
						type="submit"
						on:click={() => {
							Result();
						}}
						class="btn btn-primary">Submit</button
					>
				</div>
			</div>
		</div>

		<div class="col-md-8">
			<div class="card h-100 border-primary rounded-0">
				<div class="card-header rounded-0 bg-blue">
					<h3 class="card-title text-white text-uppercase">Result:</h3>
				</div>
				<div class="card-body">
					<div class="row">
						<div class="col-4">
							<label class="form-label page-title text-uppercase" for="">Intial Investment</label>
							<div class="input-group mb-2">
								<p class="page-title">{formValues.initialAmount}</p>
							</div>
						</div>
						<div class="col-4">
							<label class="form-label page-title text-uppercase" for="">Interest Earned</label>
							<div class="input-group mb-2">
								<p class="page-title">{formValues.result - formValues.initialAmount}</p>
							</div>
						</div>
						<div class="col-4">
							<label class="form-label page-title text-uppercase" for="">End Balance</label>
							<div class="input-group mb-2">
								<p class="page-title">{formValues.result}</p>
							</div>
						</div>
					</div>

					<div class="row">
						<div class="col-3">
							<label class="form-label text-uppercase" for="">Starting Amount</label>
							<div class="input-group mb-2">
								<p class="">{formValues.initialAmount}</p>
							</div>
						</div>
						<div class="col-3">
							<label class="form-label text-uppercase" for="">Interest Rate</label>
							<div class="input-group mb-2">
								<p class="">@ &nbsp;{formValues.rate} &nbsp; %</p>
							</div>
						</div>
						<div class="col-3">
							<label class="form-label text-uppercase" for="">Compound Type</label>
							<div class="input-group mb-2">
								<p class="">{formValues.compoundInterest}</p>
							</div>
						</div>
						<div class="col-3">
							<label class="form-label text-uppercase" for="">For a Period</label>
							<div class="input-group mb-2">
								<p class="">{formValues.timePeriod} &nbsp;{formValues.periods}</p>
							</div>
						</div>
					</div>
				</div>
				<div class="card-footer border-primary text-end">
					<a href="#" class="btn btn-facebook w-20">
						<!-- Download SVG icon from http://tabler-icons.io/i/brand-facebook -->
						<svg
							xmlns="http://www.w3.org/2000/svg"
							width="24"
							height="24"
							viewBox="0 0 24 24"
							fill="none"
							stroke="currentColor"
							stroke-width="2"
							stroke-linecap="round"
							stroke-linejoin="round"
							class="icon icon-tabler icons-tabler-outline icon-tabler-printer"
							><path stroke="none" d="M0 0h24v24H0z" fill="none" /><path
								d="M17 17h2a2 2 0 0 0 2 -2v-4a2 2 0 0 0 -2 -2h-14a2 2 0 0 0 -2 2v4a2 2 0 0 0 2 2h2"
							/><path d="M17 9v-4a2 2 0 0 0 -2 -2h-6a2 2 0 0 0 -2 2v4" /><path
								d="M7 13m0 2a2 2 0 0 1 2 -2h6a2 2 0 0 1 2 2v4a2 2 0 0 1 -2 2h-6a2 2 0 0 1 -2 -2z"
							/></svg
						>
						Print
					</a>
				</div>
			</div>
		</div>
	</div>
</div>

<div class="container-xl">
	<div class="col-md-12 pt-1 col-lg-12">
		<div class="card rounded-0 border-primary">
			<div class="card-body rounded-0 bg-blue">
				<h2 class="text-white">
					Simplify Your Investment: A Step-by-Step Guide to Fixed Deposit Calculators
				</h2>
			</div>
			<div class="card-body">
				<section>
					<h2><strong>Introduction</strong></h2>
					<p>
						Fixed Deposits (FDs) have long been a favorite among conservative investors. Offering
						security, guaranteed returns, and simplicity, FDs are a go-to for those looking to grow
						their wealth with minimal risk. But, how do you determine the best FD option for your
						needs? The answer lies in using a <strong>Fixed Deposit Calculator</strong>. This guide
						will walk you through how to use this tool to simplify your investment decisions and
						maximize your returns.
					</p>
				</section>

				<section>
					<h2><strong>What is a Fixed Deposit?</strong></h2>
					<p>
						A Fixed Deposit is a financial instrument offered by banks and financial institutions
						where you invest a lump sum for a fixed tenure at a predetermined interest rate. Once
						the tenure ends, you receive your principal along with the accumulated interest. FDs are
						known for their safety and stable returns, making them one of the most popular
						investment options.
					</p>
				</section>

				<section>
					<h2><strong>Understanding the Need for a Fixed Deposit Calculator</strong></h2>
					<p>
						In an age where financial tools are at our fingertips, the <strong
							>Fixed Deposit Calculator</strong
						> plays an essential role in simplifying investment decisions. It allows you to estimate
						the returns on your FD investment based on various factors such as the principal amount,
						interest rate, and tenure. No more manual calculations or guesswork; you can accurately predict
						your earnings with a few clicks.
					</p>
				</section>

				<section>
					<h2><strong>How Does a Fixed Deposit Calculator Work?</strong></h2>
					<p>
						A Fixed Deposit Calculator functions by taking inputs like the principal amount, tenure,
						and interest rate, and calculating the maturity amount based on the compounding
						frequency. The calculator considers whether the interest is compounded monthly,
						quarterly, or annually, providing you with the final maturity value and total interest
						earned.
					</p>
				</section>

				<section>
					<h2><strong>Benefits of Using a Fixed Deposit Calculator</strong></h2>
					<ul>
						<li>
							<strong>Accurate Calculations</strong>: Get precise interest and maturity amounts.
						</li>
						<li><strong>Time-Saving</strong>: Compare multiple FD options quickly.</li>
						<li>
							<strong>Financial Planning</strong>: Helps you set clear financial goals and plan
							accordingly.
						</li>
					</ul>
				</section>

				<section>
					<h2><strong>Step-by-Step Guide to Using a Fixed Deposit Calculator</strong></h2>
					<h3><strong>Step 1: Gathering Essential Information</strong></h3>
					<p>
						Start by collecting the basic details: the principal amount you wish to invest, the
						interest rate offered by the bank, and the tenure of the FD.
					</p>

					<h3><strong>Step 2: Inputting Principal Amount</strong></h3>
					<p>
						Enter the amount you want to invest as the principal. This is the lump sum you will
						deposit into the Fixed Deposit.
					</p>

					<h3><strong>Step 3: Selecting the Tenure of the FD</strong></h3>
					<p>
						Choose the duration for which you wish to keep your money invested. FD tenures can range
						from a few months to several years.
					</p>

					<h3><strong>Step 4: Choosing the Interest Rate</strong></h3>
					<p>
						Select the interest rate provided by the bank. Interest rates vary based on the bank,
						tenure, and market conditions.
					</p>

					<h3><strong>Step 5: Choosing Between Compound and Simple Interest</strong></h3>
					<p>
						Decide whether your interest will be compounded or kept simple. Compounded interest
						typically yields higher returns, especially over longer tenures.
					</p>

					<h3><strong>Step 6: Getting the Results</strong></h3>
					<p>
						Once you've input all the details, hit 'Calculate' to see the maturity amount and total
						interest earned on your FD.
					</p>
				</section>

				<section>
					<h2><strong>Key Parameters to Enter in a Fixed Deposit Calculator</strong></h2>
					<ul>
						<li><strong>Principal Amount</strong>: The amount of money you plan to invest.</li>
						<li><strong>Interest Rate</strong>: The rate of interest the bank offers.</li>
						<li><strong>FD Tenure</strong>: The period for which your money will stay invested.</li>
						<li>
							<strong>Interest Compounding Frequency</strong>: Monthly, quarterly, or yearly
							compounding options.
						</li>
						<li>
							<strong>Tax Implications</strong>: Applicable taxes can affect your final return.
						</li>
					</ul>
				</section>

				<section>
					<h2><strong>Why Should You Use a Fixed Deposit Calculator Before Investing?</strong></h2>
					<p>
						Using a Fixed Deposit Calculator ensures you make informed decisions. You can see how
						different interest rates and tenures impact your returns, helping you optimize your
						investment strategy for the best possible outcome.
					</p>
				</section>

				<section>
					<h2><strong>Fixed Deposit Calculator vs. Manual Calculation</strong></h2>
					<p>
						While manual calculations can be time-consuming and prone to errors, a Fixed Deposit
						Calculator provides instant, accurate results. The automation eliminates guesswork and
						allows you to experiment with various scenarios effortlessly.
					</p>
				</section>

				<section>
					<h2><strong>Factors That Can Affect Your Fixed Deposit Returns</strong></h2>
					<p>
						Several factors can influence your FD returns, including the prevailing market interest
						rates, tax liabilities, and penalties for early withdrawals. It’s essential to consider
						these before making any investment decision.
					</p>
				</section>

				<section>
					<h2><strong>Top Features to Look for in a Good Fixed Deposit Calculator</strong></h2>
					<ul>
						<li>User-friendly interface</li>
						<li>Flexibility to compare multiple FDs</li>
						<li>Precision in calculations</li>
						<li>Real-time updates with changing interest rates</li>
					</ul>
				</section>

				<section>
					<h2><strong>Fixed Deposit Alternatives</strong></h2>
					<p>
						If you're looking for other low-risk investments, consider options like recurring
						deposits, bonds, or mutual funds. These provide varied returns and can complement your
						FD strategy.
					</p>
				</section>

				<section>
					<h2><strong>Conclusion</strong></h2>
					<p>
						A Fixed Deposit Calculator is a simple yet powerful tool that can help you make smarter
						investment choices. By understanding the returns on your FD and comparing different
						options, you can ensure that your money works harder for you. So, before making your
						next FD investment, be sure to use a Fixed Deposit Calculator to plan your financial
						future effectively.
					</p>
				</section>

				<section>
					<h2><strong>FAQs</strong></h2>
					<h3><strong>What is the best interest rate for an FD?</strong></h3>
					<p>
						Interest rates vary by bank and tenure. It’s essential to shop around and use an FD
						calculator to compare different rates.
					</p>

					<h3><strong>How frequently do banks update FD interest rates?</strong></h3>
					<p>
						Banks may update their FD interest rates monthly or based on changes in the Reserve Bank
						of India's policies.
					</p>

					<h3><strong>Can I use the FD calculator for tax-saving FDs?</strong></h3>
					<p>
						Yes, you can use the FD calculator to determine the returns on tax-saving FDs, typically
						locked in for 5 years.
					</p>

					<h3><strong>Are FD calculators accurate for long-term deposits?</strong></h3>
					<p>
						FD calculators are highly accurate, even for long-term deposits, provided you enter the
						correct inputs for principal, tenure, and interest rate.
					</p>

					<h3><strong>What should I do if I need to withdraw my FD early?</strong></h3>
					<p>
						If you need to withdraw early, be aware of any penalties and reduced interest rates. The
						FD calculator can help you estimate your returns even with premature withdrawals.
					</p>
				</section>
			</div>
		</div>
	</div>
</div>

<style>
	input::-webkit-outer-spin-button,
	input::-webkit-inner-spin-button {
		-webkit-appearance: none;
		margin: 0;
	}

	input[type='number'] {
		-moz-appearance: textfield;
	}
</style>
