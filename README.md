<?php
session_start();
include('includes/header.php'); 

?>



<div class="container">

<!-- Outer Row -->
<div class="row justify-content-center">

  <div class="col-xl-6 col-lg-6 col-md-6">

    <div class="card o-hidden border-0 shadow-lg my-5">
      <div class="card-body p-0">
        <!-- Nested Row within Card Body -->
        <div class="row">
          <div class="col-lg-12">
            <div class="p-5">
              <div class="text-center">
                
                <h1 class="h3 text-gray-900 mb-4"><a href="/SYSTEM/admin/"><img src="img/logo-wide-icon1.png"></a>
     
 <?php

                    if(isset($_SESSION['status']) && $_SESSION['status'] !='') 
                    {
                        echo '<h6 class="bg-danger text-white"> '.$_SESSION['status'].' </h6>';
                        unset($_SESSION['status']);
                    }
                ?>
                <form class="user" action="code.php" method="POST">

              
              </div>

                    <div class="form-group">

    
                    <input type="text" name="username" class="form-control form-control-user" placeholder="Username" required>
                    </div>
                    <div class="form-group">
                    <input type="password" name="password" class="form-control form-control-user" placeholder="Password" required>
                    </div>
            
                    <button type="submit" name="login_btn" class="btn btn-primary btn-user btn-block"> Login </button>
                    <hr>
                </form>


            </div>
          </div>
        </div>
      </div>
    </div>

  </div>

</div>

</div>


<?php
include('includes/scripts.php'); 
?>
