<svelte:head>
	<title>Enter Code - Lukas Weichselbraun</title>
</svelte:head>

<script>
	let code;

	function openCode() {
		location.href = window.location.origin + "/code/" + code;
  }
  
</script>

<div class="w-full">
  
  <div class="py-12 xl:py-24 text-center">
    <h1 class="text-lg lg:text-xl font-bold">Servus Agent!</h1>
    <p>You must be really smart to made it until here.<br/>Please click on the button below to view your next job.</p>
    <button class="mt-4 modal-open bg-transparent border border-blue-400 hover:border-blue-500 text-blue-400 hover:text-blue-500 font-bold py-2 px-4 rounded-full">Open Job</button>
  </div>

  <!--Modal-->
  <div class="modal opacity-0 pointer-events-none fixed w-full h-full top-0 left-0 flex items-center justify-center">
    <div class="modal-overlay absolute w-full h-full bg-gray-900 opacity-50"></div>
    
    <div class="modal-container bg-white w-11/12 mx-auto rounded shadow-lg z-50 overflow-y-auto">
      
      <div class="modal-close absolute top-0 right-0 cursor-pointer flex flex-col items-center mt-4 mr-4 text-white text-sm z-50">
        <svg class="fill-current text-white" xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 18 18">
          <path d="M14.53 4.53l-1.06-1.06L9 7.94 4.53 3.47 3.47 4.53 7.94 9l-4.47 4.47 1.06 1.06L9 10.06l4.47 4.47 1.06-1.06L10.06 9z"></path>
        </svg>
      </div>

      <!-- Add margin if you want to see some of the overlay behind the modal-->
      <div class="modal-content py-4 text-left px-6">
        <!--Title-->
        <div class="flex justify-between items-center pb-3">
          <p class="text-2xl font-bold">Write your own code page</p>
          <div class="modal-close cursor-pointer z-50">
            <svg class="fill-current text-black" xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 18 18">
              <path d="M14.53 4.53l-1.06-1.06L9 7.94 4.53 3.47 3.47 4.53 7.94 9l-4.47 4.47 1.06 1.06L9 10.06l4.47 4.47 1.06-1.06L10.06 9z"></path>
            </svg>
          </div>
        </div>

        <!--Body-->
        <div style="max-height: 450px;">
          <p>It is so easy to write your own dedicated job page like this!</p>
          <p>Please be aware that there are no authentication or authorization features.</p>
          <p>So, if someone knows the code or link to this page your information is revealed.</p>
          <br/>
          <p>Follow the next steps to create your custom code page:</p>
          <br/>
          <ol>
            <li>1. Copy the '007.svelte' file</li>
            <li>2. Rename the file to your custom code, e.g. rename to 'mi6.svelte'</li>
            <li>3. Change the html content to your needs</li>
            <li>4. Add a link to this new file in the hidden DIV in 'code.svelte' file so that it gets build when exported</li>
            <li>5. Rebuild & deploy your code</li>
            <li>6. Pass the link to this website and the code to your desired person</li>
            <li>7. Done</li>
          </ol>
        </div>
        <!--Footer-->
        <div class="flex justify-end pt-2">
          <button class="modal-close px-4 bg-blue-500 p-3 rounded-lg text-white hover:bg-blue-400">Close</button>
        </div>
        
      </div>
    </div>
  </div>

  <script>
    var openmodal = document.querySelectorAll('.modal-open')
    for (var i = 0; i < openmodal.length; i++) {
      openmodal[i].addEventListener('click', function(event){
    	event.preventDefault()
    	toggleModal()
      })
    }
    
    const overlay = document.querySelector('.modal-overlay')
    overlay.addEventListener('click', toggleModal)
    
    var closemodal = document.querySelectorAll('.modal-close')
    for (var i = 0; i < closemodal.length; i++) {
      closemodal[i].addEventListener('click', toggleModal)
    }
    
    document.onkeydown = function(evt) {
      evt = evt || window.event
      var isEscape = false
      if ("key" in evt) {
    	isEscape = (evt.key === "Escape" || evt.key === "Esc")
      } else {
    	isEscape = (evt.keyCode === 27)
      }
      if (isEscape && document.body.classList.contains('modal-active')) {
    	toggleModal()
      }
    };
    
    
    function toggleModal () {
      const body = document.querySelector('body')
      const modal = document.querySelector('.modal')
      modal.classList.toggle('opacity-0')
      modal.classList.toggle('pointer-events-none')
      body.classList.toggle('modal-active')
    }
    
     
  </script>
  
</div>
