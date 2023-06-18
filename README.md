<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Random User Generator</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.1/dist/css/bootstrap.min.css" rel="stylesheet">
    <style>
      @import url('https://fonts.googleapis.com/css2?family=Bad+Script&family=Montserrat:wght@400;500;600;700;800&display=swap');

body {
    font-family: "Montserrat";
}

.header-inner-div {
    padding-bottom: 10rem !important;
}


#randomUserDisplaySection {
    margin-top: -12rem;
}

.user-rounded-image {
    border-radius: 100%;
    margin-bottom: -4rem;
    border: 4px solid gainsboro;
}


#displayUserInfo {
    vertical-align: middle;

}
  </style>

<body>
    <header class="bg-dark text-white py-5">
        <div class="container">
            <div class="row pb-5">
                <div class="header-inner-div col-md-12 text-center pb-5">
                    <h2 class="fs-1 fw-normal text-uppercase">ANKIT YADAV
                  </h2>
                    <p class="fw-lighter">
                      Hi This is ANKIT  YADAV This Website is made by me  by this Websit you can generate a Random person  tool website  and
                        bootstrap  By this website you can<br> generate a random person info and use anywhere.</p>
                    <button type="button" class="btn btn-primary py-3 px-5 rounded-2 fw-semibold"
                        onclick="getNewUserInfo()">Generate New User</button>
                </div>
            </div>
        </div>
    </header>
    <main>
        <div class="container mb-5">
            <div class="row">
                <div class="col-md-2"></div>
                <div class="col-md-8" id="randomUserDisplaySection">
                    <div class="card text-center shadow-lg">
                        <div class="card-header pt-5 shadow-sm">
                            <img src="" class="user-rounded-image img-fluid" id="displayUserPhoto">
                        </div>
                        <div class="card-body mb-4 mt-5">
                            <h3 class="card-title pt-2 fs-2" id="displayUserName"></h3>
                            <table class="table table-bordered mt-4">
                                <tbody class="text-start" id="displayUserInfo">
                                    <tr class="">
                                        <td class="col-1 text-center"><i class="fa-solid fa-user fs-4 text-muted"></i>
                                        </td>
                                        <th scope="col-2">Full Name: </th>
                                        <td class="col-6" id="displayUserFullName"></td>
                                        <td class="col-2 text-center"><button type="button"
                                                class="btn btn-outline-secondary" id="copyUserFullName"><i
                                                    class="fa-regular fa-clipboard me-2"></i>Copy</button></td>
                                    </tr>
                                    <tr>
                                        <td class="col-1 text-center"><i
                                                class="fa-solid fa-envelope fs-4 text-muted"></i></td>
                                        <th scope="col-2">Email Address: </th>
                                        <td class="col-6" id="displayUserEmail"></td>
                                        <td class="col-2 text-center"><button type="button"
                                                class="btn btn-outline-secondary" id="copyUserEmail"><i
                                                    class="fa-regular fa-clipboard me-2"></i>Copy</button></td>
                                    </tr>
                                    <tr>
                                        <td class="col-1 text-center"><i class="fa-solid fa-phone fs-4 text-muted"></i>
                                        </td>
                                        <th scope="col-2">Phone Number: </th>
                                        <td class="col-6" id="displayUserPhoneNumber"></td>
                                        <td class="col-2 text-center"><button type="button"
                                                class="btn btn-outline-secondary" id="copyUserPhoneNumber"><i
                                                    class="fa-regular fa-clipboard me-2"></i>Copy</button></td>
                                    </tr>
                                    <tr>
                                        <td class="col-1 text-center"><i class="fa-solid fa-user fs-4 text-muted"></i>
                                        </td>
                                        <th scope="col-2">Gander: </th>
                                        <td class="col-6 text-capitalize" id="displayUserGander"></td>
                                        <td class="col-2 text-center"><button type="button"
                                                class="btn btn-outline-secondary" id="copyUserGander"><i
                                                    class="fa-regular fa-clipboard me-2"></i>Copy</button></td>
                                    </tr>
                                    <tr>
                                        <td class="col-1 text-center"><i
                                                class="fa-regular fa-calendar fs-4 text-muted"></i></td>
                                        <th scope="col-2">Date of Birth: </th>
                                        <td class="col-6" id="displayUserDOB"></td>
                                        <td class="col-2 text-center"><button type="button"
                                                class="btn btn-outline-secondary" id="copyUserDOB"><i
                                                    class="fa-regular fa-clipboard me-2"></i>Copy</button></td>
                                    </tr>
                                    <tr>
                                        <td class="col-1 text-center"><i
                                                class="fa-solid fa-location-dot fs-4 text-muted"></i></td>
                                        <th scope="col-2">Address: </th>
                                        <td class="col-6" id="displayUserAddress"></td>
                                        <td class="col-2 text-center"><button type="button"
                                                class="btn btn-outline-secondary" id="copyUserAddress"><i
                                                    class="fa-regular fa-clipboard me-2"></i>Copy</button></td>
                                    </tr>
                                    <tr>
                                        <td class="col-1 text-center"><i
                                                class="fa-solid fa-map-location-dot fs-4 text-muted"></i></td>
                                        <th scope="col-2">Post Code: </th>
                                        <td class="col-6" id="displayUserPostcode"></td>
                                        <td class="col-2 text-center"><button type="button"
                                                class="btn btn-outline-secondary" id="copyUserPostcode"><i
                                                    class="fa-regular fa-clipboard me-2"></i>Copy</button></td>
                                    </tr>
                                    <tr>
                                        <td class="col-1 text-center"><i
                                                class="fa-solid fa-id-card fs-4 text-muted"></i></td>
                                        <th scope="col-2">SSN Number: </th>
                                        <td class="col-6" id="displayUserSSNNumber"></td>
                                        <td class="col-2 text-center"><button type="button"
                                                class="btn btn-outline-secondary" id="copyUserSSNNumber"><i
                                                    class="fa-regular fa-clipboard me-2"></i>Copy</button></td>
                                    </tr>
                                </tbody>
                            </table>
                            <button type="button" class="btn btn-primary py-3 px-5 mt-3 rounded-2 fw-semibold"
                                onclick="getNewUserInfo()">Generate New User</button>
                        </div>
                    </div>
                </div>
                <div class="col-md-2"></div>
            </div>
        </div>
    </main>

    <footer class="bg-dark py-5">
        <p class="text-white text-center mb-0">Copyright @ 2022. All Right Reserved Developed by Azhar Anowar</p>
    </footer>



    <div class="toast-container position-fixed bottom-0 end-0 p-3">
        <div id="copiedToClipboardToast" class="toast" role="alert" aria-live="assertive" aria-atomic="true">
            <div class="toast-header">
                <strong class="me-auto text-success"><i class="fa-regular fa-clipboard me-2"></i>Copied to clipboard!</strong>
                <button type="button" class="btn-close" data-bs-dismiss="toast" aria-label="Close"></button>
            </div>
            <div class="toast-body text-secondary fw-normal" id="copiedToClipboardMessage">
                <!-- Here will load dynamic toast message... -->>
            </div>
        </div>
    </div>

    <script src="https://kit.fontawesome.com/cdf319e764.js" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.1/dist/js/bootstrap.bundle.min.js"></script>
  <script>const getNewUserInfo = () => {
    fetch('https://randomuser.me/api')
        .then(response => response.json())
        .then(data => displayUserInfo(data))
}


const displayUserInfo = (data) => {
    
    const userInfo = data.results[0];

    document.getElementById("displayUserPhoto").src = userInfo.picture.large;

    const userName = `${userInfo.name.first} ${userInfo.name.last}`;
    document.getElementById("displayUserName").innerText = userName;

    const userFullName = `${userInfo.name.title}. ${userInfo.name.first} ${userInfo.name.last}`;
    document.getElementById("displayUserFullName").innerText = userFullName;

    const userEmailAddress = userInfo.email;
    document.getElementById("displayUserEmail").innerText = userEmailAddress;

    const userPhoneNumber = userInfo.phone;
    document.getElementById("displayUserPhoneNumber").innerText = userPhoneNumber;

    const userGender = userInfo.gender;
    document.getElementById("displayUserGander").innerText = userGender;

    let userDOB = new Date(userInfo.dob.date);
    userDOB = `${userDOB.getDate()}/${userDOB.getMonth() + 1}/${userDOB.getFullYear()} (${userInfo.dob.age} years old)`
    document.getElementById("displayUserDOB").innerText = userDOB;

    const userAddress = `Street: ${userInfo.location.street.number} ${userInfo.location.street.name}, City: ${userInfo.location.city}, State: ${userInfo.location.state}, ${userInfo.location.country}.`;
    document.getElementById("displayUserAddress").innerText = userAddress;

    const userPostCode = userInfo.location.postcode;
    document.getElementById("displayUserPostcode").innerText = userPostCode;

    const userSSNNumber = userInfo.id.value;
    document.getElementById("displayUserSSNNumber").innerText = userSSNNumber;
}


getNewUserInfo();


document.getElementById("copyUserFullName").addEventListener('click', () => {
    copyUserInfoToClipboard("displayUserFullName");
});

document.getElementById("copyUserEmail").addEventListener('click', () => {
    copyUserInfoToClipboard("displayUserEmail");
});

document.getElementById("copyUserPhoneNumber").addEventListener('click', () => {
    copyUserInfoToClipboard("displayUserPhoneNumber");
});

document.getElementById("copyUserGander").addEventListener('click', () => {
    copyUserInfoToClipboard("displayUserGander");
});

document.getElementById("copyUserDOB").addEventListener('click', () => {
    copyUserInfoToClipboard("displayUserDOB");
});

document.getElementById("copyUserAddress").addEventListener('click', () => {
    copyUserInfoToClipboard("displayUserAddress");
});

document.getElementById("copyUserPostcode").addEventListener('click', () => {
    copyUserInfoToClipboard("displayUserPostcode");
});

document.getElementById("copyUserSSNNumber").addEventListener('click', () => {
    copyUserInfoToClipboard("displayUserSSNNumber");
});


const copyUserInfoToClipboard = id => {
    const copyText = document.getElementById(id).innerText;
    if(copyText) {
        navigator.clipboard.writeText(copyText).then(() => {
        });
    
        document.getElementById("copiedToClipboardMessage").innerText = `Copied: "${copyText}"`;
    
        const copiedToClipboardToastTrigged = document.getElementById('copiedToClipboardToast')
        const toast = new bootstrap.Toast(copiedToClipboardToastTrigged)
        toast.show()
    }
}</script>
</body>

</html>
