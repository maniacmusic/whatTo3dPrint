<template>
  <div class="layout container mx-auto">
    <Header />
    <div class="w-full max-w-8xl mx-auto">
      <div class="lg:flex">
        <div
          id="sidebar"
          class="fixed z-40 inset-0 flex-none h-full bg-black bg-opacity-25 w-full lg:bg-white lg:static lg:h-auto lg:overflow-y-visible lg:pt-0 lg:w-64 lg:block hidden"
        >
          <div
            id="navWrapper"
            class="h-full overflow-y-auto scrolling-touch lg:h-auto lg:block lg:relative lg:sticky lg:bg-transparent overflow-hidden lg:top-18 bg-white mr-24 lg:mr-0"
          >
            <div
              class="hidden lg:block h-12 pointer-events-none absolute inset-x-0 z-10"
            ></div>
            <nav
              id="nav"
              class="px-1 pt-6 overflow-hidden text-base sm:px-3 xl:px-5 lg:text-sm pb-10 lg:pt-2 lg:pb-14 sticky?lg:h-(screen-18)"
            >
              <ul>
                <li class="hidden">
                  <div class="mr-3">
                    <svg
                      version="1.1"
                      id="Capa_1"
                      xmlns="http://www.w3.org/2000/svg"
                      xmlns:xlink="http://www.w3.org/1999/xlink"
                      x="0px"
                      y="0px"
                      viewBox="0 0 512 512"
                      style="enable-background: new 0 0 512 512"
                      xml:space="preserve"
                      class="h-10 w-10 p-1"
                    >
                      <g>
                        <g>
                          <path
                            d="M308.905,88.694c-11.965-11.964-25.646-21.816-40.663-29.282c-3.797-1.887-8.402-0.34-10.289,3.456
			c-1.887,3.796-0.34,8.402,3.456,10.289c13.527,6.724,25.855,15.603,36.641,26.391c54.54,54.54,54.54,143.284,0,197.824
			c-26.42,26.421-61.548,40.971-98.911,40.971c-37.365,0-72.492-14.55-98.912-40.971c-26.421-26.42-40.971-61.548-40.971-98.912
			c0-37.364,14.55-72.492,40.971-98.912c15.939-15.939,34.827-27.48,56.137-34.303c20.339-6.511,42.287-8.288,63.466-5.139
			c4.198,0.625,8.099-2.27,8.721-6.463c0.622-4.193-2.27-8.097-6.463-8.72c-23.493-3.493-47.839-1.522-70.405,5.703
			c-23.328,7.468-44.876,20.632-62.312,38.068c-29.319,29.319-45.466,68.301-45.466,109.766c0,41.465,16.147,80.447,45.466,109.766
			c29.32,29.32,68.302,45.467,109.767,45.467c41.463,0,80.446-16.147,109.766-45.467C369.43,247.7,369.43,149.219,308.905,88.694z"
                          />
                        </g>
                      </g>
                      <g>
                        <g>
                          <path
                            d="M499.76,441.314L365.463,307.019c23.859-36.733,34.945-80.778,31.279-124.757c-3.891-46.686-24.299-90.672-57.463-123.856
			C301.646,20.751,251.744,0.008,198.765,0c-0.013,0-0.018,0-0.031,0C145.768,0,95.867,20.728,58.232,58.363
			c-77.472,77.473-77.471,203.53,0.001,281.002c33.183,33.183,77.174,53.605,123.871,57.504
			c43.996,3.672,88.044-7.409,124.785-31.276l134.296,134.295c8.075,8.075,18.68,12.112,29.287,12.112s21.213-4.037,29.288-12.112
			C515.908,483.739,515.908,457.463,499.76,441.314z M488.906,489.034c-10.166,10.165-26.704,10.164-36.868,0L313.275,350.27
			c-1.485-1.485-3.451-2.248-5.429-2.248c-1.526,0-3.061,0.454-4.388,1.38c-34.843,24.301-77.477,35.725-120.076,32.171
			c-43.084-3.598-83.674-22.442-114.293-53.062C-2.4,257.024-2.401,140.705,69.087,69.217
			c34.738-34.738,80.778-53.867,129.647-53.867c0.009,0,0.02,0,0.029,0c48.878,0.007,94.926,19.152,129.66,53.907
			c30.602,30.62,49.433,71.206,53.023,114.281c3.543,42.501-7.837,85.056-32.041,119.856c-5.209,6.443-19.6,23.681-26.66,29.802
			c-3.203,2.777-3.548,7.624-0.771,10.826c1.518,1.751,3.655,2.647,5.802,2.647c1.782,0,3.573-0.617,5.025-1.876
			c6.502-5.638,16.965-17.801,23.319-25.41l132.786,132.785C499.069,462.331,499.069,478.87,488.906,489.034z"
                          />
                        </g>
                      </g>
                      <g></g>
                      <g></g>
                      <g></g>
                      <g></g>
                      <g></g>
                      <g></g>
                      <g></g>
                      <g></g>
                      <g></g>
                      <g></g>
                      <g></g>
                      <g></g>
                      <g></g>
                      <g></g>
                      <g></g>
                    </svg>
                  </div>
                  <input
                    id="search"
                    v-model="searchTerm"
                    class="input text-2xl"
                    type="text"
                    placeholder="Search"
                  />
                  <g-link
                    v-for="result in searchResults"
                    :key="result.id"
                    :to="result.path"
                    class="navbar-item"
                  >
                    {{ result.title }}
                  </g-link>
                </li>
                <li>
                  <g-link
                    to="/lamps/"
                    class="flex text-2xl items-center px-3 hover:text-gray-900 transition-colors duration-200 mb-2 text-gray-900"
                  >
                    <div class="mr-3 rounded-md">
                      <svg
                        version="1.1"
                        id="Capa_1"
                        xmlns="http://www.w3.org/2000/svg"
                        xmlns:xlink="http://www.w3.org/1999/xlink"
                        x="0px"
                        y="0px"
                        viewBox="0 0 480.005 480.005"
                        style="enable-background: new 0 0 480.005 480.005"
                        xml:space="preserve"
                        class="h-10 w-10 p-1"
                      >
                        <g>
                          <g>
                            <g>
                              <path
                                d="M240.003,48c4.418,0,8-3.582,8-8V8c0-4.418-3.582-8-8-8s-8,3.582-8,8v32C232.003,44.418,235.584,48,240.003,48z"
                              />
                              <path
                                d="M141.075,36.656l16,27.704c2.184,3.841,7.068,5.184,10.909,3s5.184-7.068,3-10.909c-0.017-0.031-0.035-0.061-0.053-0.092
				l-16-27.704c-2.184-3.841-7.068-5.184-10.909-3c-3.841,2.184-5.184,7.068-3,10.909C141.039,36.595,141.057,36.626,141.075,36.656
				z"
                              />
                              <path
                                d="M76.567,106.875c0.03,0.018,0.061,0.035,0.092,0.053l27.704,16c3.812,2.234,8.713,0.956,10.947-2.856
				c2.234-3.812,0.956-8.713-2.856-10.947c-0.03-0.018-0.061-0.035-0.092-0.053l-27.704-16c-3.812-2.234-8.713-0.956-10.947,2.856
				C71.477,99.739,72.755,104.641,76.567,106.875z"
                              />
                              <path
                                d="M96.003,192c0-4.418-3.582-8-8-8h-32c-4.418,0-8,3.582-8,8s3.582,8,8,8h32C92.421,200,96.003,196.418,96.003,192z"
                              />
                              <path
                                d="M104.456,261.018c-0.031,0.018-0.062,0.036-0.093,0.054l-27.704,16c-3.841,2.183-5.185,7.067-3.002,10.908
				c2.183,3.841,7.067,5.185,10.908,3.002c0.031-0.018,0.062-0.036,0.093-0.054l27.704-16c3.841-2.183,5.185-7.067,3.002-10.908
				C113.181,260.179,108.297,258.835,104.456,261.018z"
                              />
                              <path
                                d="M403.44,277.126c-0.031-0.018-0.062-0.036-0.093-0.054l-27.704-16c-3.811-2.235-8.713-0.957-10.948,2.854
				c-2.235,3.811-0.957,8.713,2.854,10.948c0.031,0.018,0.062,0.036,0.093,0.054l27.704,16c3.811,2.235,8.713,0.957,10.948-2.854
				C408.529,284.262,407.251,279.361,403.44,277.126z"
                              />
                              <path
                                d="M424.003,184h-32c-4.418,0-8,3.582-8,8s3.582,8,8,8h32c4.418,0,8-3.582,8-8S428.421,184,424.003,184z"
                              />
                              <path
                                d="M371.651,124c1.404,0,2.784-0.37,4-1.072l27.704-16c3.841-2.184,5.184-7.068,3-10.909s-7.068-5.184-10.909-3
				c-0.031,0.017-0.061,0.035-0.092,0.053l-27.704,16c-3.826,2.209-5.137,7.102-2.928,10.928
				C366.152,122.475,368.793,124,371.651,124z"
                              />
                              <path
                                d="M311.993,67.291c0.003,0.002,0.006,0.004,0.009,0.005c3.827,2.207,8.72,0.894,10.927-2.934
				c0-0.001,0.001-0.002,0.001-0.002l16-27.704c2.235-3.811,0.957-8.713-2.854-10.948c-3.811-2.235-8.713-0.957-10.948,2.854
				c-0.018,0.031-0.036,0.062-0.054,0.093l-16,27.704C306.862,60.184,308.169,65.078,311.993,67.291z"
                              />
                              <path
                                d="M256.003,320c4.418,0,8-3.582,8-8v-88h16c17.673,0,32-14.327,32-32s-14.327-32-32-32c-17.673,0-32,14.327-32,32v16h-16
				v-16c0-17.673-14.327-32-32-32s-32,14.327-32,32s14.327,32,32,32h16v88c0,4.418,3.582,8,8,8s8-3.582,8-8v-88h16v88
				C248.003,316.418,251.584,320,256.003,320z M264.003,192c0-8.837,7.163-16,16-16s16,7.163,16,16s-7.163,16-16,16h-16V192z
				 M216.003,208h-16c-8.837,0-16-7.163-16-16s7.163-16,16-16s16,7.163,16,16V208z"
                              />
                              <path
                                d="M246.219,64.152c-70.611-3.392-130.603,51.099-133.995,121.71c-1.943,40.432,15.354,79.4,46.643,105.082
				c5.639,4.417,8.994,11.135,9.136,18.296V328c0.042,10.134,6.445,19.15,16,22.528V360c0.021,5.923,2.245,11.627,6.24,16
				c-8.32,9.044-8.32,22.956,0,32c-8.894,9.75-8.2,24.864,1.55,33.758c4.429,4.04,10.215,6.268,16.21,6.242
				c4.306,0.113,7.889-3.287,8.001-7.593c0.044-1.68-0.456-3.33-1.425-4.703c-0.253-0.489-0.553-0.953-0.896-1.384
				c-0.658-0.602-1.409-1.094-2.224-1.456c-0.232-0.12-0.464-0.216-0.704-0.312c-0.81-0.295-1.659-0.465-2.52-0.504
				c-0.08,0-0.152-0.048-0.232-0.048c-4.418,0-8-3.582-8-8s3.582-8,8-8h32c4.418,0,8-3.582,8-8s-3.582-8-8-8h-32
				c-4.418,0-8-3.582-8-8s3.582-8,8-8h32c4.418,0,8-3.582,8-8s-3.582-8-8-8h-32c-4.418,0-8-3.582-8-8v-8h40c4.418,0,8-3.582,8-8
				s-3.582-8-8-8h-48c-4.418,0-8-3.582-8-8v-18.76c-0.131-11.962-5.64-23.23-15-30.68c-47.788-39.274-54.689-109.852-15.415-157.64
				c22.466-27.336,56.528-42.448,91.871-40.76c59.107,3.516,105.536,51.957,106.544,111.16c0.287,34.052-15.024,66.363-41.56,87.704
				c-9.29,7.652-14.602,19.109-14.44,31.144V328c0,4.418-3.582,8-8,8h-24c-4.418,0-8,3.582-8,8s3.582,8,8,8h16v8
				c0,4.418-3.582,8-8,8h-8c-4.418,0-8,3.582-8,8s3.582,8,8,8h8c4.418,0,8,3.582,8,8s-3.582,8-8,8h-8c-4.418,0-8,3.582-8,8
				s3.582,8,8,8h8c4.418,0,8,3.582,8,8s-3.582,8-8,8h-40c-4.418,0-8,3.582-8,8s3.582,8,8,8h30.632
				c-4.417,12.497-18.129,19.047-30.626,14.63c-3.826-1.352-7.246-3.653-9.942-6.686c-2.938-3.3-7.996-3.594-11.296-0.656
				c-3.3,2.938-3.594,7.996-0.656,11.296c14.631,16.487,39.857,17.992,56.344,3.362c6.81-6.043,11.349-14.232,12.864-23.21
				c12.529-3.916,19.511-17.247,15.596-29.776c-1.04-3.329-2.801-6.388-5.156-8.96c8.32-9.044,8.32-22.956,0-32
				c3.995-4.373,6.219-10.077,6.24-16v-9.472c9.555-3.378,15.958-12.394,16-22.528v-17.832c-0.107-7.187,3.007-14.046,8.488-18.696
				c30.344-24.395,47.85-61.339,47.512-100.272C366.847,123.532,313.777,68.169,246.219,64.152z"
                              />
                            </g>
                          </g>
                        </g>
                        <g></g>
                        <g></g>
                        <g></g>
                        <g></g>
                        <g></g>
                        <g></g>
                        <g></g>
                        <g></g>
                        <g></g>
                        <g></g>
                        <g></g>
                        <g></g>
                        <g></g>
                        <g></g>
                        <g></g>
                      </svg>
                    </div>
                    Lights</g-link
                  >
                </li>

                <li>
                  <g-link
                    to="/tools/"
                    class="flex text-2xl items-center px-3 hover:text-gray-900 transition-colors duration-200 mb-2 text-gray-900"
                  >
                    <div class="mr-3 rounded-md">
                      <svg
                        version="1.1"
                        id="Capa_1"
                        xmlns="http://www.w3.org/2000/svg"
                        xmlns:xlink="http://www.w3.org/1999/xlink"
                        x="0px"
                        y="0px"
                        viewBox="0 0 512 512"
                        style="enable-background: new 0 0 512 512"
                        xml:space="preserve"
                        class="h-10 w-10 p-1"
                        width="auto"
                      >
                        <g>
                          <g>
                            <path
                              d="M438.973,411.718c-14.598,0-26.475,11.876-26.475,26.475c0,14.598,11.876,26.474,26.475,26.474
			c14.598,0,26.474-11.876,26.474-26.474C465.447,423.595,453.571,411.718,438.973,411.718z M438.972,448.977
			c-5.946,0-10.784-4.838-10.784-10.784c0-5.946,4.838-10.784,10.784-10.784c5.946,0,10.784,4.838,10.784,10.784
			S444.918,448.977,438.972,448.977z"
                            />
                          </g>
                        </g>
                        <g>
                          <g>
                            <path
                              d="M510.303,436.82c-0.5-19.383-8.704-37.211-23.102-50.198L329.249,244.157l139.658-139.658
			c0.918-0.274,1.825-0.615,2.7-1.077L501.85,87.46c4.178-2.206,6.98-6.152,7.685-10.823c0.706-4.672-0.805-9.268-4.146-12.612
			l-34.052-34.051c-3.342-3.341-7.935-4.852-12.611-4.146c-4.671,0.705-8.616,3.507-10.823,7.686L431.94,63.755
			c-0.466,0.883-0.824,1.796-1.099,2.723l-65.92,65.92c-3.064,3.065-3.064,8.031,0,11.096c3.065,3.062,8.031,3.062,11.096,0
			l60.492-60.493l15.853,15.853l-154.7,154.7l-15.853-15.853l67.525-67.524c3.064-3.065,3.064-8.031,0-11.096
			c-3.065-3.062-8.031-3.062-11.096,0l-48.994,48.994l-53.322-48.094c15.118-43.516,4.17-91.931-28.625-124.725
			C173.706,1.665,123.314-9.04,78.916,7.987c-2.481,0.952-4.312,3.094-4.864,5.693s0.247,5.301,2.126,7.18l61.592,61.593
			c1.822,1.822,2.827,4.245,2.827,6.822c0,2.577-1.004,5-2.827,6.823l-39.999,39.999c-1.822,1.823-4.245,2.827-6.822,2.827
			c-2.577,0-5-1.003-6.823-2.827L22.533,74.504c-1.88-1.879-4.58-2.678-7.18-2.126c-2.599,0.553-4.741,2.383-5.693,4.864
			c-17.027,44.396-6.322,94.788,27.27,128.381c31.991,31.99,79.468,43.253,122.299,29.414l41.227,45.083
			c-1.981,3.871-4.557,7.481-7.734,10.658c-11.884,11.884-29.695,15.628-45.38,9.54c-2.899-1.128-6.188-0.434-8.388,1.765
			l-96.059,96.059c-26.004,26.005-26.004,68.317,0,94.32C55.494,505.063,72.243,512,90.058,512c17.814,0,34.564-6.937,47.161-19.534
			l96.059-96.058c2.198-2.199,2.891-5.489,1.765-8.388c-6.089-15.684-2.345-33.497,9.538-45.381
			c11.886-11.884,29.698-15.628,45.382-9.54c2.901,1.128,6.188,0.432,8.388-1.765l18.12-18.12c5.456-5.456,8.46-12.711,8.46-20.426
			c0-7.715-3.004-14.97-8.46-20.426l-7.713-7.713l9.383-9.383l158.552,143.007c11.172,10.077,17.539,23.911,17.926,38.951
			c0.387,15.04-5.259,29.183-15.898,39.821c-10.588,10.59-24.695,16.226-39.636,15.903c-14.971-0.334-28.781-6.604-38.886-17.655
			L282.31,346.378c-2.927-3.199-7.887-3.419-11.084-0.495c-3.197,2.925-3.419,7.887-0.495,11.084l117.888,128.915
			c13.024,14.241,30.822,22.321,50.115,22.752c0.54,0.012,1.079,0.018,1.618,0.018c18.688,0,36.199-7.249,49.464-20.512
			C503.526,474.429,510.801,456.203,510.303,436.82z M446.149,70.45l15.019-28.454l32.199,32.199l-28.454,15.019L446.149,70.45z
			 M167.324,220.639c-2.16-2.36-5.534-3.174-8.532-2.056c-38.363,14.31-81.845,4.868-110.768-24.052
			c-26.262-26.263-36.438-64.337-27.471-99.815l52.477,52.477c4.787,4.786,11.15,7.421,17.918,7.421s13.131-2.635,17.917-7.421
			l39.999-39.999c4.786-4.787,7.421-11.15,7.421-17.918s-2.635-13.131-7.421-17.917L96.388,18.88
			c35.475-8.971,73.553,1.208,99.814,27.471c29.659,29.657,38.773,74.003,23.222,112.978c-1.217,3.049-0.407,6.534,2.032,8.733
			l56.679,51.122l-7.422,7.422L263,218.893c-5.456-5.456-12.711-8.46-20.426-8.46c-7.715,0-14.97,3.004-20.426,8.46l-18.12,18.12
			c-2.198,2.199-2.891,5.489-1.765,8.388c2.087,5.375,2.992,10.997,2.837,16.548L167.324,220.639z M305.374,302.119l-14.682,14.683
			c-20.192-5.821-42.164-0.299-57.205,14.741h-0.001c-15.04,15.041-20.563,37.01-14.74,57.206l-92.622,92.62
			c-9.634,9.634-22.442,14.94-36.065,14.94s-26.433-5.306-36.065-14.94c-19.887-19.886-19.887-52.244,0-72.131l92.621-92.621
			c20.194,5.824,42.163,0.298,57.205-14.742c15.04-15.041,20.564-37.01,14.741-57.205l14.683-14.682
			c5.144-5.146,13.517-5.146,18.661,0l13.261,13.261l26.947,26.947l13.261,13.261C310.52,288.603,310.52,296.975,305.374,302.119z"
                            />
                          </g>
                        </g>
                        <g>
                          <g>
                            <path
                              d="M162.326,346.249c-3.065-3.063-8.031-3.063-11.096,0l-74.318,74.318c-3.064,3.065-3.064,8.031,0,11.096
			c1.532,1.531,3.541,2.297,5.548,2.297c2.007,0,4.016-0.766,5.548-2.297l74.318-74.318
			C165.389,354.28,165.389,349.313,162.326,346.249z"
                            />
                          </g>
                        </g>
                        <g>
                          <g>
                            <path
                              d="M189.785,373.708c-3.064-3.063-8.031-3.063-11.096,0l-74.318,74.317c-3.064,3.065-3.064,8.031,0,11.096
			c1.532,1.531,3.54,2.297,5.548,2.297c2.007,0,4.016-0.766,5.548-2.297l74.318-74.317
			C192.849,381.739,192.849,376.773,189.785,373.708z"
                            />
                          </g>
                        </g>
                        <g></g>
                        <g></g>
                        <g></g>
                        <g></g>
                        <g></g>
                        <g></g>
                        <g></g>
                        <g></g>
                        <g></g>
                        <g></g>
                        <g></g>
                        <g></g>
                        <g></g>
                        <g></g>
                        <g></g>
                      </svg>
                    </div>
                    Tools</g-link
                  >
                </li>

                <li>
                  <g-link
                    to="/household/"
                    class="flex text-2xl items-center px-3 hover:text-gray-900 transition-colors duration-200 mb-2 text-gray-900"
                  >
                    <div class="mr-3 rounded-md">
                      <svg
                        viewBox="0 0 60 60"
                        class="h-10 w-10 p-1"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <g id="Page-1" fill="none" fill-rule="evenodd">
                          <g
                            id="001---House-Clean"
                            fill="rgb(0,0,0)"
                            fill-rule="nonzero"
                          >
                            <path
                              id="Shape"
                              d="m3 60h5c.84849384-.0026614 1.6557601-.3662948 2.22-1h25.08c1.4674156.0006138 2.9066743-.4027938 4.16-1.166l18.74-11.408c.8861698-.5351758 1.5101446-1.4144837 1.722716-2.4276587.2125715-1.0131749-.0053725-2.0691235-.601716-2.9153413-.0211838-.0347875-.0445646-.0681886-.07-.1-.9674494-1.285176-2.6463435-1.8108862-4.174-1.307l-7.077 2.353v-21.029h1.31c.83848.0044805 1.5907385-.51454 1.8841979-1.3000018s.0658102-1.6705896-.5701979-2.2169982l-2.624-2.265v-11.218c0-1.1045695-.8954305-2-2-2h-5c-1.1045695 0-2 .8954305-2 2v3.448l-7.7-6.648c-.7496818-.63682621-1.8503182-.63682621-2.6 0l-19.327 16.686c-.63404392.5472616-.85993036 1.4316354-.56599012 2.2159224.29394024.7842871 1.04544087 1.3023493 1.88299012 1.2980776h1.31v14h-1.184c-.4222546-1.1943509-1.54921457-1.9947486-2.816-2h-5c-1.65685425 0-3 1.3431458-3 3v21c0 1.6568542 1.34314575 3 3 3zm52.7-18.431c.6861666-.2253147 1.4402969-.0070139 1.9.55.0150636.02484.0314194.048873.049.072.2947436.3918849.4095617.8903409.3159627 1.3716795-.0935989.4813386-.3868419.9004449-.8069627 1.1533205l-18.738 11.41c-.9401696.5719432-2.0195283.8743021-3.12.874l-24.3.0000002v-20.0000002h1.8c1.845108.0020745 3.634951.6299473 5.077 1.781 1.7963064 1.4330224 4.0251194 2.2152043 6.323 2.219h5.23c1.394477.0037201 2.687363.7300223 3.416 1.919.011.025.023.048.033.066.6282519.9152462.600051 2.1298968-.07 3.015h-6.089c-1.9744471.0012643-3.9045319.5857168-5.548 1.68l-.73.49c-.4583963.3081749-.5801749.9296037-.272 1.388s.9296037.5801749 1.388.272l.724-.486c1.3144658-.875765 2.8585114-1.3433624 4.438-1.344h8.89c.5394129.0006918 1.0752548-.087489 1.586-.261zm-18.7 4.131-.444.148c-.3048656.1021956-.6244653.1535477-.946.152h-.545c.4410785-1.3276445.2826613-2.7815064-.434-3.983-.0159082-.0344212-.0339431-.0678191-.054-.1-1.0873635-1.8046689-3.0380713-2.9106386-5.145-2.917h-5.232c-.4019373-.0032901-.8030621-.0367172-1.2-.1v-1.9c0-3.8659932 3.1340068-7 7-7s7 3.1340068 7 7zm4-41.7h5v9.492l-5-4.317zm-25 17c.5522847 0 1-.4477153 1-1s-.4477153-1-1-1h-5.317l19.317-16.683 9.3 8.03 10.01 8.653h-13.31c-.5522847 0-1 .4477153-1 1s.4477153 1 1 1h10v21.7l-7 2.333v-8.033c0-4.9705627-4.0294373-9-9-9s-9 4.0294373-9 9v1.336c-.6727193-.2856669-1.3034921-.6614393-1.875-1.117-1.4768401-1.1744322-3.2513695-1.9147139-5.125-2.138v-14.081zm-14 15c0-.5522847.44771525-1 1-1h5c.55228475 0 1 .4477153 1 1v21c0 .5522847-.44771525 1-1 1h-5c-.55228475 0-1-.4477153-1-1z"
                            />
                            <path
                              id="Shape"
                              d="m12 5c.5522847 0 1-.44771525 1-1v-2c0-.55228475-.4477153-1-1-1s-1 .44771525-1 1v2c0 .55228475.4477153 1 1 1z"
                            />
                            <path
                              id="Shape"
                              d="m12 7c-.5522847 0-1 .44771525-1 1v2c0 .5522847.4477153 1 1 1s1-.4477153 1-1v-2c0-.55228475-.4477153-1-1-1z"
                            />
                            <path
                              id="Shape"
                              d="m14 7h2c.5522847 0 1-.44771525 1-1s-.4477153-1-1-1h-2c-.5522847 0-1 .44771525-1 1s.4477153 1 1 1z"
                            />
                            <path
                              id="Shape"
                              d="m8 7h2c.5522847 0 1-.44771525 1-1s-.4477153-1-1-1h-2c-.55228475 0-1 .44771525-1 1s.44771525 1 1 1z"
                            />
                            <path
                              id="Shape"
                              d="m55.5 29.5c.2651948-.0000566.5195073-.1054506.707-.293l1.5-1.5c.3789722-.3923789.3735524-1.0160848-.0121814-1.4018186s-1.0094397-.3911536-1.4018186-.0121814l-1.5 1.5c-.2859079.2859943-.3714219.7160366-.216678 1.0896546.1547439.3736179.5192821.6172591.923678.6173454z"
                            />
                            <path
                              id="Shape"
                              d="m51.793 30.793-1.5 1.5c-.2599566.2510745-.3642126.6228779-.2726972.9725073.0915155.3496295.3645604.6226744.7141899.7141899.3496294.0915154.7214328-.0127406.9725073-.2726972l1.5-1.5c.3789722-.3923789.3735524-1.0160848-.0121814-1.4018186s-1.0094397-.3911536-1.4018186-.0121814z"
                            />
                            <path
                              id="Shape"
                              d="m56.293 33.707c.3923789.3789722 1.0160848.3735524 1.4018186-.0121814s.3911536-1.0094397.0121814-1.4018186l-1.5-1.5c-.3923789-.3789722-1.0160848-.3735524-1.4018186.0121814s-.3911536 1.0094397-.0121814 1.4018186z"
                            />
                            <path
                              id="Shape"
                              d="m50.293 26.293c-.3903819.3904999-.3903819 1.0235001 0 1.414l1.5 1.5c.3923789.3789722 1.0160848.3735524 1.4018186-.0121814s.3911536-1.0094397.0121814-1.4018186l-1.5-1.5c-.3904999-.3903819-1.0235001-.3903819-1.414 0z"
                            />
                            <path
                              id="Shape"
                              d="m20 21c2.7600532.0033061 4.9966939 2.2399468 5 5 0 .5522847.4477153 1 1 1s1-.4477153 1-1c.0033061-2.7600532 2.2399468-4.9966939 5-5 .5522847 0 1-.4477153 1-1s-.4477153-1-1-1c-2.7600532-.0033061-4.9966939-2.2399468-5-5 0-.5522847-.4477153-1-1-1s-1 .4477153-1 1c-.0033061 2.7600532-2.2399468 4.9966939-5 5-.5522847 0-1 .4477153-1 1s.4477153 1 1 1zm6-3.4c.5931269.9831096 1.4168904 1.8068731 2.4 2.4-.9831096.5931269-1.8068731 1.4168904-2.4 2.4-.5931269-.9831096-1.4168904-1.8068731-2.4-2.4.9831096-.5931269 1.8068731-1.4168904 2.4-2.4z"
                            />
                          </g>
                        </g>
                      </svg>
                    </div>
                    Household</g-link
                  >
                </li>

                <li>
                  <g-link
                    to="/electronics/"
                    class="flex text-2xl items-center px-3 hover:text-gray-900 transition-colors duration-200 mb-2 text-gray-900"
                  >
                    <div class="mr-3 rounded-md">
                      <svg
                        xmlns="http://www.w3.org/2000/svg"
                        viewBox="0 0 128 128"
                        class="h-10 w-10 p-1"
                      >
                        <g>
                          <path
                            d="M94.5,59.71h19.594a4.751,4.751,0,1,0,0-3.5H94.5V47.62h12.63a1.751,1.751,0,0,0,1.75-1.75V34.34h5.214a4.751,4.751,0,1,0,0-3.5H107.13a1.751,1.751,0,0,0-1.75,1.75V44.12H94.5V35.25a1.751,1.751,0,0,0-1.75-1.75H83.88V22.62H95.41a1.751,1.751,0,0,0,1.75-1.75V13.906a4.749,4.749,0,1,0-3.5,0V19.12H82.13a1.751,1.751,0,0,0-1.75,1.75V33.5H71.79V13.907a4.749,4.749,0,1,0-3.5,0V33.5H59.71V13.906a4.751,4.751,0,1,0-3.5,0V33.5H47.62V20.87a1.751,1.751,0,0,0-1.75-1.75H34.34V13.906a4.751,4.751,0,1,0-3.5,0V20.87a1.751,1.751,0,0,0,1.75,1.75H44.12V33.5H35.25a1.751,1.751,0,0,0-1.75,1.75v8.87H22.62V32.59a1.751,1.751,0,0,0-1.75-1.75H13.907a4.75,4.75,0,1,0,0,3.5H19.12V45.87a1.751,1.751,0,0,0,1.75,1.75H33.5v8.59H13.907a4.749,4.749,0,1,0,0,3.5H33.5v8.58H13.906a4.751,4.751,0,1,0,0,3.5H33.5v8.59H20.87a1.751,1.751,0,0,0-1.75,1.75V93.66H13.906a4.751,4.751,0,1,0,0,3.5H20.87a1.751,1.751,0,0,0,1.75-1.75V83.88H33.5v8.87a1.751,1.751,0,0,0,1.75,1.75h8.87v10.88H32.59a1.751,1.751,0,0,0-1.75,1.75v6.964a4.749,4.749,0,1,0,3.5,0V108.88H45.87a1.751,1.751,0,0,0,1.75-1.75V94.5h8.59v19.593a4.749,4.749,0,1,0,3.5,0V94.5h8.58v19.594a4.751,4.751,0,1,0,3.5,0V94.5h8.59v12.63a1.751,1.751,0,0,0,1.75,1.75H93.66v5.214a4.75,4.75,0,1,0,3.5,0V107.13a1.751,1.751,0,0,0-1.75-1.75H83.88V94.5h8.87a1.751,1.751,0,0,0,1.75-1.75V83.88h10.88V95.41a1.751,1.751,0,0,0,1.75,1.75h6.964a4.749,4.749,0,1,0,0-3.5H108.88V82.13a1.751,1.751,0,0,0-1.75-1.75H94.5V71.79h19.593a4.749,4.749,0,1,0,0-3.5H94.5Zm24-3a1.25,1.25,0,1,1-1.25,1.25A1.252,1.252,0,0,1,118.5,56.708Zm0-25.369a1.25,1.25,0,1,1-1.25,1.25A1.252,1.252,0,0,1,118.5,31.339ZM95.411,8.25a1.25,1.25,0,1,1-1.25,1.25A1.252,1.252,0,0,1,95.411,8.25Zm-25.369,0a1.25,1.25,0,1,1-1.25,1.25A1.252,1.252,0,0,1,70.042,8.25Zm-12.084,0a1.25,1.25,0,1,1-1.25,1.25A1.251,1.251,0,0,1,57.958,8.25Zm-25.369,0a1.25,1.25,0,1,1-1.25,1.25A1.251,1.251,0,0,1,32.589,8.25ZM9.5,33.839a1.25,1.25,0,1,1,1.25-1.25A1.251,1.251,0,0,1,9.5,33.839Zm0,25.369a1.25,1.25,0,1,1,1.25-1.25A1.251,1.251,0,0,1,9.5,59.208Zm0,12.084a1.25,1.25,0,1,1,1.25-1.25A1.252,1.252,0,0,1,9.5,71.292Zm0,25.369a1.25,1.25,0,1,1,1.25-1.25A1.252,1.252,0,0,1,9.5,96.661ZM32.589,119.75a1.25,1.25,0,1,1,1.25-1.25A1.252,1.252,0,0,1,32.589,119.75Zm25.369,0a1.25,1.25,0,1,1,1.25-1.25A1.252,1.252,0,0,1,57.958,119.75Zm12.084,0a1.25,1.25,0,1,1,1.25-1.25A1.251,1.251,0,0,1,70.042,119.75Zm25.369,0a1.25,1.25,0,1,1,1.25-1.25A1.251,1.251,0,0,1,95.411,119.75ZM118.5,94.161a1.25,1.25,0,1,1-1.25,1.25A1.251,1.251,0,0,1,118.5,94.161Zm0-25.369a1.25,1.25,0,1,1-1.25,1.25A1.251,1.251,0,0,1,118.5,68.792ZM91,91H37V37H91Z"
                          />
                          <path
                            d="M83.75,42.5H44.25a1.751,1.751,0,0,0-1.75,1.75v39.5a1.751,1.751,0,0,0,1.75,1.75h39.5a1.751,1.751,0,0,0,1.75-1.75V44.25A1.751,1.751,0,0,0,83.75,42.5ZM82,82H46V46H82Z"
                          />
                          <path
                            d="M77.75,66.583a1.751,1.751,0,0,0,1.75-1.75V54.958a1.75,1.75,0,0,0-3.5,0v9.875A1.751,1.751,0,0,0,77.75,66.583Z"
                          />
                        </g>
                      </svg>
                    </div>
                    Electronics</g-link
                  >
                </li>
              </ul>
            </nav>
          </div>
        </div>
        <div
          id="content-wrapper"
          class="min-w-0 w-full flex-auto lg:static lg:max-h-full lg:overflow-visible"
        >
          <slot />
        </div>
      </div>
    </div>

    <Footer />
  </div>
</template>

<script>
import Header from "@/components/Header";
import Footer from "@/components/Footer";
import Search from "gridsome-plugin-flexsearch/SearchMixin";

export default {
  mixins: [Search],
  components: {
    Header,
    Footer,
  },
  data: () => ({
    searchTerm: "",
  }),
  computed: {
    searchResults() {
      const searchTerm = this.searchTerm;
      if (searchTerm.length < 3) return [];
      return this.$search.search({ query: searchTerm, limit: 5 });
    },
  },
};
</script>
<style>
@import url("https://fonts.googleapis.com/css2?family=Karma:wght@300;500;700&display=swap");
* {
  font-family: "Karma", serif;
}
.active--exact {
  font-weight: bold;
}
#content-wrapper {
  font-size: 21px;
  text-align: center;
  animation: fadein 0.3s;
  -moz-animation: fadein 0.3s; /* Firefox */
  -webkit-animation: fadein 0.3s; /* Safari and Chrome */
  -o-animation: fadein 0.3s; /* Opera */
}
@keyframes fadein {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-moz-keyframes fadein {
  /* Firefox */
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-webkit-keyframes fadein {
  /* Safari and Chrome */
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-o-keyframes fadein {
  /* Opera */
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>