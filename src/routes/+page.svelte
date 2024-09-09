<script>
	import { urlsLists } from "$lib/ListUrls";
</script>

<svelte:head>
	
</svelte:head>

<section>
	<div class="container-xl">
        
            <div class="col-md-3 col-lg-3">

                <div class="card border-primary  bg-azure-lt rounded-0">
                    <div class="card-header   bg-blue rounded-0">
                        <input class="form-control rounded-0 w-100 p-2 h-100 border-0 shadow-none bg-blue-lt" type="number" readonly name="" id="">
                    </div>
                    <div class="card-body mx-auto bg-azure-lt">
                        
                        <div class="">
                            <a href="#" class="btn btn- btn-lg btn-icon mx-2 p-2" aria-label="Button">
                                
                                <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-letter-c"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M18 9a5 5 0 0 0 -5 -5h-2a5 5 0 0 0 -5 5v6a5 5 0 0 0 5 5h2a5 5 0 0 0 5 -5" /></svg>
                            </a>
                            <a href="#" class="btn btn- btn-lg btn-icon mx-2 p-2" aria-label="Button">
                                
                                <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-backspace"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M20 6a1 1 0 0 1 1 1v10a1 1 0 0 1 -1 1h-11l-5 -5a1.5 1.5 0 0 1 0 -2l5 -5z" /><path d="M12 10l4 4m0 -4l-4 4" /></svg>
                            </a>
                            <a href="#" class="btn btn- btn-lg btn-icon mx-2 p-2" aria-label="Button">
                                
                                <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-percentage"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M17 17m-1 0a1 1 0 1 0 2 0a1 1 0 1 0 -2 0" /><path d="M7 7m-1 0a1 1 0 1 0 2 0a1 1 0 1 0 -2 0" /><path d="M6 18l12 -12" /></svg>
                            </a>
                            <a href="#" class="btn btn-yellow btn-lg btn-icon mx-2 p-2" aria-label="Button">
                                
                                <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-divide"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><circle cx="12" cy="6" r="1" fill="currentColor" /><circle cx="12" cy="18" r="1" fill="currentColor" /><path d="M5 12l14 0" /></svg>
                            </a>
                        </div>
                        <div class="pt-2">
                            <a href="#" class="btn btn-blue btn-lg btn-icon mx-2 p-2" aria-label="Button">
                                
                                <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-number-7"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M8 4h8l-4 16" /></svg>
                            </a>
                            <a href="#" class="btn btn-blue btn-lg btn-icon mx-2 p-2" aria-label="Button">
                                
                                <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-number-8"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M12 8m-4 0a4 4 0 1 0 8 0a4 4 0 1 0 -8 0" /><path d="M12 16m-4 0a4 4 0 1 0 8 0a4 4 0 1 0 -8 0" /></svg>
                            </a>
                            <a href="#" class="btn btn-blue btn-lg btn-icon mx-2 p-2" aria-label="Button">
                                
                                <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-number-9"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M16 8a4 4 0 1 0 -8 0v1a4 4 0 1 0 8 0" /><path d="M8 16a4 4 0 1 0 8 0v-8" /></svg>
                            </a>
                            <a href="#" class="btn btn-yellow btn-lg btn-icon mx-2 p-2" aria-label="Button">
                                
                                <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-x"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M18 6l-12 12" /><path d="M6 6l12 12" /></svg>
                            </a>
                        </div>
                        <div class="pt-2">
                            <a href="#" class="btn btn-blue btn-lg btn-icon mx-2 p-2" aria-label="Button">
                                
                                <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-number-4"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M15 20v-15l-8 11h10" /></svg>
                            </a>
                            <a href="#" class="btn btn-blue btn-lg btn-icon mx-2 p-2" aria-label="Button">
                                
                                <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-number-5"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M8 20h4a4 4 0 1 0 0 -8h-4v-8h8" /></svg>
                            </a>
                            <a href="#" class="btn btn-blue btn-lg btn-icon mx-2 p-2" aria-label="Button">
                                
                                <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-number-6"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M8 16a4 4 0 1 0 8 0v-1a4 4 0 1 0 -8 0" /><path d="M16 8a4 4 0 1 0 -8 0v8" /></svg>
                            </a>
                            <a href="#" class="btn btn-yellow btn-lg btn-icon mx-2 p-2" aria-label="Button">
                                
                                <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-minus"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M5 12l14 0" /></svg>
                            </a>
                        </div>
                        <div class="pt-2">
                            <a href="#" class="btn btn-blue btn-lg btn-icon mx-2 p-2" aria-label="Button">
                                
                                <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-number-1"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M13 20v-16l-5 5" /></svg>
                            </a>
                            <a href="#" class="btn btn-blue btn-lg btn-icon mx-2 p-2" aria-label="Button">
                                
                                <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-number-2"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M8 8a4 4 0 1 1 8 0c0 1.098 -.564 2.025 -1.159 2.815l-6.841 9.185h8" /></svg>
                            </a>
                            <a href="#" class="btn btn-blue btn-lg btn-icon mx-2 p-2" aria-label="Button">
                                
                                <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-number-3"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M12 12a4 4 0 1 0 -4 -4" /><path d="M8 16a4 4 0 1 0 4 -4" /></svg>
                            </a>
                            <a href="#" class="btn btn-yellow btn-lg btn-icon mx-2 p-2" aria-label="Button">
                                
                                <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-plus"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M12 5l0 14" /><path d="M5 12l14 0" /></svg>
                            </a>
                        </div>
                        <div class="pt-2">
                            <a href="#" class="btn btn-blue btn-lg btn-icon mx-2 p-2" aria-label="Button">
                                
                                <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-number-0"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M16 16v-8" /><path d="M12 20a4 4 0 0 0 4 -4v-8a4 4 0 1 0 -8 0v8a4 4 0 0 0 4 4z" /></svg>
                            </a>
                            <a href="#" class="btn btn-blue btn-lg btn-icon mx-2 p-2" aria-label="Button">
                                
                                <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="currentColor"  class="icon icon-tabler icons-tabler-filled icon-tabler-point"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M12 7a5 5 0 1 1 -4.995 5.217l-.005 -.217l.005 -.217a5 5 0 0 1 4.995 -4.783z" /></svg>
                            </a>
                            <a href="#" class="btn btn-blue btn-lg btn-icon mx-2 p-2" aria-label="Button">
                                
                                <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-plus-minus"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M4 7h6" /><path d="M7 4v6" /><path d="M20 18h-6" /><path d="M5 19l14 -14" /></svg>
                            </a>
                            <a href="#" class="btn btn-yellow btn-lg btn-icon mx-2 p-2" aria-label="Button">
                                
                                <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-equal"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M5 10h14" /><path d="M5 14h14" /></svg>
                            </a>
                        </div>
                        
                    </div>
                </div>
            </div>
            
            
        
        
    </div>
    <div class="container-xl pt-2">
        <div class="row row-cards">
            <div class="col-md-3 col-lg-4">
                <div class="card rounded-0 border-primary ">
                    <div class="card-body bg-blue rounded-0">
                        <h2 class="text-center  text-white">Finance Calculator</h2>
                    </div>
                    <div class="card-body">
                      
                      
                      
                      {#each urlsLists['finance'] as urls }
              
                          <h4>
                            {#if urls.status === true}
                                  <a href={urls.url}
                                  ><span>
                                    <svg
                                      xmlns="http://www.w3.org/2000/svg"
                                      width="24"
                                      height="24"
                                      viewBox="0 0 24 24"
                                      fill="none"
                                      stroke="#0054a6"
                                      stroke-width="2"
                                      stroke-linecap="round"
                                      stroke-linejoin="round"
                                      class="icon icon-tabler icons-tabler-outline icon-tabler-coffee"
                                      ><path stroke="none" d="M0 0h24v24H0z" fill="none"
                                      ></path><path
                                        d="M3 14c.83 .642 2.077 1.017 3.5 1c1.423 .017 2.67 -.358 3.5 -1c.83 -.642 2.077 -1.017 3.5 -1c1.423 -.017 2.67 .358 3.5 1"
                                      ></path><path d="M8 3a2.4 2.4 0 0 0 -1 2a2.4 2.4 0 0 0 1 2"
                                      ></path><path d="M12 3a2.4 2.4 0 0 0 -1 2a2.4 2.4 0 0 0 1 2"
                                      ></path><path
                                        d="M3 10h14v5a6 6 0 0 1 -6 6h-2a6 6 0 0 1 -6 -6v-5z"
                                      ></path><path d="M16.746 16.726a3 3 0 1 0 .252 -5.555"
                                      ></path></svg
                                    >
                                  </span>&nbsp;{ urls.name }&nbsp;</a>
                            
                                  <span class="badge badge-sm text-uppercase bg-green-lt ms-auto">Ready</span>
                            {:else}
                                  <a href="/coming-soon"
                                  ><span>
                                  <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="#ef4444"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-grill"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M19 8h-14a6 6 0 0 0 6 6h2a6 6 0 0 0 6 -5.775l0 -.225z" /><path d="M17 20a2 2 0 1 1 0 -4a2 2 0 0 1 0 4z" /><path d="M15 14l1 2" /><path d="M9 14l-3 6" /><path d="M15 18h-8" /><path d="M15 5v-1" /><path d="M12 5v-1" /><path d="M9 5v-1" /></svg>
                                  </span>&nbsp;{ urls.name }&nbsp;</a>
                                  <span class="badge badge-sm text-uppercase bg-red-lt ms-auto">Cooking</span>
                            {/if}
                          </h4>
                        
                      {/each}
                    </div>
                  </div>
            </div>
           
            <div class="col-md-3 col-lg-4">
                <div class="card rounded-0 border-primary">
                    <div class="card-body bg-blue rounded-0">
                        <h2 class="text-center  text-white">Health Calculator</h2>
                    </div>
                    <div class="card-body">
                      
                      
                      
                      {#each urlsLists['health'] as urls }
            
                          <h4>
                            {#if urls.status === true}
                                  <a href={urls.url}
                                  ><span>
                                    <svg
                                      xmlns="http://www.w3.org/2000/svg"
                                      width="24"
                                      height="24"
                                      viewBox="0 0 24 24"
                                      fill="none"
                                      stroke="#0054a6"
                                      stroke-width="2"
                                      stroke-linecap="round"
                                      stroke-linejoin="round"
                                      class="icon icon-tabler icons-tabler-outline icon-tabler-coffee"
                                      ><path stroke="none" d="M0 0h24v24H0z" fill="none"
                                      ></path><path
                                        d="M3 14c.83 .642 2.077 1.017 3.5 1c1.423 .017 2.67 -.358 3.5 -1c.83 -.642 2.077 -1.017 3.5 -1c1.423 -.017 2.67 .358 3.5 1"
                                      ></path><path d="M8 3a2.4 2.4 0 0 0 -1 2a2.4 2.4 0 0 0 1 2"
                                      ></path><path d="M12 3a2.4 2.4 0 0 0 -1 2a2.4 2.4 0 0 0 1 2"
                                      ></path><path
                                        d="M3 10h14v5a6 6 0 0 1 -6 6h-2a6 6 0 0 1 -6 -6v-5z"
                                      ></path><path d="M16.746 16.726a3 3 0 1 0 .252 -5.555"
                                      ></path></svg
                                    >
                                  </span>&nbsp;{ urls.name }&nbsp;</a>
                            
                                  <span class="badge bg-green-lt">Ready</span>
                            {:else}
                                  <a href="/coming-soon"
                                  ><span>
                                  <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="#ef4444"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-grill"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M19 8h-14a6 6 0 0 0 6 6h2a6 6 0 0 0 6 -5.775l0 -.225z" /><path d="M17 20a2 2 0 1 1 0 -4a2 2 0 0 1 0 4z" /><path d="M15 14l1 2" /><path d="M9 14l-3 6" /><path d="M15 18h-8" /><path d="M15 5v-1" /><path d="M12 5v-1" /><path d="M9 5v-1" /></svg>
                                  </span>&nbsp;{ urls.name }&nbsp;</a>
                                  <span class="badge bg-red-lt">Cooking</span>
                            {/if}
                          </h4>
                        
                      {/each}
            
                      <h2 class="card-title text-uppercase">&nbsp;<u>Date & Time</u></h2>
                      
                      
                      {#each urlsLists['dateTime'] as urls }
            
                          <h4>
                            {#if urls.status === true}
                                  <a href={urls.url}
                                  ><span>
                                    <svg
                                      xmlns="http://www.w3.org/2000/svg"
                                      width="24"
                                      height="24"
                                      viewBox="0 0 24 24"
                                      fill="none"
                                      stroke="#0054a6"
                                      stroke-width="2"
                                      stroke-linecap="round"
                                      stroke-linejoin="round"
                                      class="icon icon-tabler icons-tabler-outline icon-tabler-coffee"
                                      ><path stroke="none" d="M0 0h24v24H0z" fill="none"
                                      ></path><path
                                        d="M3 14c.83 .642 2.077 1.017 3.5 1c1.423 .017 2.67 -.358 3.5 -1c.83 -.642 2.077 -1.017 3.5 -1c1.423 -.017 2.67 .358 3.5 1"
                                      ></path><path d="M8 3a2.4 2.4 0 0 0 -1 2a2.4 2.4 0 0 0 1 2"
                                      ></path><path d="M12 3a2.4 2.4 0 0 0 -1 2a2.4 2.4 0 0 0 1 2"
                                      ></path><path
                                        d="M3 10h14v5a6 6 0 0 1 -6 6h-2a6 6 0 0 1 -6 -6v-5z"
                                      ></path><path d="M16.746 16.726a3 3 0 1 0 .252 -5.555"
                                      ></path></svg
                                    >
                                  </span>&nbsp;{ urls.name }&nbsp;</a>
                            
                                  <span class="badge bg-green-lt">Ready</span>
                            {:else}
                                  <a href="/coming-soon"
                                  ><span>
                                  <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="#ef4444"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-grill"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M19 8h-14a6 6 0 0 0 6 6h2a6 6 0 0 0 6 -5.775l0 -.225z" /><path d="M17 20a2 2 0 1 1 0 -4a2 2 0 0 1 0 4z" /><path d="M15 14l1 2" /><path d="M9 14l-3 6" /><path d="M15 18h-8" /><path d="M15 5v-1" /><path d="M12 5v-1" /><path d="M9 5v-1" /></svg>
                                  </span>&nbsp;{ urls.name }&nbsp;</a>
                                  <span class="badge bg-red-lt">Cooking</span>
                            {/if}
                          </h4>
                        
                      {/each}
                    </div>
                </div>
            </div>
             
        </div>
    </div>


	
</section>


