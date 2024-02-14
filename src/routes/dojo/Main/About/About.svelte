<div class="root">
	<div class="leftBlock">
		<div class="title break-words">we are futur ists</div>
	</div>
	<div class="rightBlock">
		<div class="item">
			<div class="title">Team of experts</div>
			<div class="text">
				Our diverse team consists of seasoned digital marketers, social media wizards, content
				creators, SEO specialists, and designers, all united by a common goal: to elevate your brand
				to new heights.
			</div>
		</div>
		<div class="item">
			<div class="title">Data driven precision and futuristic vision</div>
			<div class="text">
				Where digital marketing converges with creative innovation. we forge futuristic growth
				odysseys for businesses and organizations. We harness cutting-edge strategies to propel your
				brand into tomorrow, guiding it through an evolving digital landscape with
				<span class="mark"> data driven precision and futuristic vision. </span>
			</div>
		</div>
		<div class="item">
			<div class="title">All dots connected</div>
			<div class="text">
				It's our core approach to digital marketing. We understand that every aspect of your online
				presence, from SEO to social media, content to customer engagement, forms a cohesive and
				interconnected digital ecosystem.
			</div>
		</div>
	</div>
</div>

<style lang="scss">
	.root {
		padding: min(72px, 6.6vh) min(130px, 12.037vh) min(66px, 6.1vh) min(58px, 5.37vh);

		height: 100%;
		position: relative;

		display: flex;
		gap: 116px;

		font-family: Montserrat;
	}

	.leftBlock {
		height: 100%;
		border-radius: 37px;
		background: linear-gradient(180deg, #210056 0%, #ae47ff 100%);

		display: flex;
		flex-direction: column;
		justify-content: flex-end;
		position: relative;

		color: #fff;

		& .title {
			text-align: justify;
			font-size: var(--font-size-128);
			font-weight: 900;
			line-height: 78.125%;
			letter-spacing: -1.28px;
			text-transform: uppercase;

			left: -11px;
			bottom: -6px;
			position: relative;
		}
	}

	.rightBlock {
		display: flex;
		justify-content: space-between;
		flex-direction: column;

		width: 100%;
		max-width: 560px;

		@media (max-height: 980px) {
			width: 470px;
		}

		& .title {
			font-size: var(--font-size-48);
			font-weight: 800;
			line-height: 100%; /* 48px */
			background: linear-gradient(90deg, #210056 0.01%, #9747ff 94.35%);
			background-clip: text;
			-webkit-background-clip: text;
			-webkit-text-fill-color: transparent;

			margin-bottom: 13px;
		}

		& .text {
			color: #210056;
			text-align: justify;
			font-size: 20px;
			font-weight: 400;
			line-height: normal;
		}

		& .mark {
			background: linear-gradient(90deg, #210056 0.01%, #9747ff 94.35%);
			background-clip: text;
			-webkit-background-clip: text;
			-webkit-text-fill-color: transparent;

			font-weight: 600;
		}
	}

	.break-words {
		width: min-intrinsic;
		width: -moz-min-content;
		width: min-content;
		display: table-caption;
		word-break: initial;
	}

	@media (max-width: $mobile-viewport) {
        .root {
            --gap: 50px;
			flex-direction: column;
			padding: 6%;

			height: auto;

			gap: var(--gap);

            padding-bottom: 80px;
		}

		.rightBlock {
			width: unset;
            gap: 50px;
            align-items: center;

            & .title {
                text-align: center;
            }

            & .item {
                max-width: 90%;
            }
		}

		.leftBlock {
			background: linear-gradient(270deg, #210056 0%, #ae47ff 100%);
			border-radius: 5vw;
            padding-top: 6vw;

			& .title {
				left: -1vw;
				bottom: -1vw;
			}
		}
	}
</style>
