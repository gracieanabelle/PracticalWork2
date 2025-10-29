# PracticalWork2
GRACIE ANABELLE JAMIRIN
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Bloom College - Student Registration Form</title>
  <!-- Bootstrap CSS -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body class="bg-light">
  <div class="container mt-5">
    <div class="card shadow">
      <div class="card-body">
        <h3 class="text-center mb-4">BLOOM COLLEGE</h3>
        <h5 class="text-center mb-4">Student Registration Form</h5>

        <form id="studentForm">
          <!-- Image Upload -->
          <div class="mb-3 text-center">
            <label for="studentImage" class="form-label">Student Image</label>
            <input class="form-control w-50 mx-auto" type="file" id="studentImage" accept="image/*">
            <small class="text-muted">(less than 5Mb)</small>
          </div>

          <!-- Text Fields -->
          <div class="mb-3">
            <label for="studentName" class="form-label">Student Name</label>
            <input type="text" class="form-control" id="studentName" placeholder="Full name" onchange="toUpperCaseField(this)">
          </div>

          <div class="mb-3">
            <label for="fatherName" class="form-label">Father's Name</label>
            <input type="text" class="form-control" id="fatherName" placeholder="Father's full name" onchange="toUpperCaseField(this)">
          </div>

          <div class="mb-3">
            <label for="motherName" class="form-label">Mother's Name</label>
            <input type="text" class="form-control" id="motherName" placeholder="Mother's full name" onchange="toUpperCaseField(this)">
          </div>

          <!-- Gender -->
          <div class="mb-3">
            <label class="form-label">Gender</label><br>
            <input type="radio" name="gender" value="Male"> Male
            <input type="radio" name="gender" value="Female" class="ms-3"> Female
          </div>

          <!-- Date of Birth -->
          <div class="mb-3">
            <label for="dob" class="form-label">Date of Birth</label>
            <input type="date" class="form-control" id="dob">
          </div>

          <!-- Email -->
          <div class="mb-3">
            <label for="email" class="form-label">Email</label>
            <input type="email" class="form-control" id="email" placeholder="email@xyz.com"
                   onfocus="highlightField(this)" onblur="removeHighlight(this)">
          </div>

          <!-- Level & Department -->
          <div class="row mb-3">
            <div class="col-md-6">
              <label for="level" class="form-label">Level</label>
              <select class="form-select" id="level">
                <option>Diploma</option>
                <option>Degree</option>
                <option>Master</option>
                <option>PhD</option>
              </select>
            </div>
            <div class="col-md-6">
              <label for="department" class="form-label">Department</label>
              <select class="form-select" id="department">
                <option>Computer Engineering</option>
                <option>Information Technology</option>
                <option>Electrical Engineering</option>
                <option>Mechanical Engineering</option>
              </select>
            </div>
          </div>

          <!-- Telephone -->
          <div class="mb-3">
            <label for="tel" class="form-label">Tel/Mobile</label>
            <input type="tel" class="form-control" id="tel" placeholder="01X-XXX XXXX">
          </div>

          <!-- Address -->
          <h5 class="mt-4">Address</h5>
          <div class="mb-3">
            <label for="state" class="form-label">State</label>
            <input type="text" class="form-control" id="state">
          </div>
          <div class="mb-3">
            <label for="city" class="form-label">City</label>
            <input type="text" class="form-control" id="city">
          </div>
          <div class="mb-3">
            <label for="postcode" class="form-label">Postcode</label>
            <input type="text" class="form-control" id="postcode">
          </div>

          <!-- Buttons -->
          <div class="text-center mt-4">
            <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#successModal">
              Register
            </button>
            <button type="reset" class="btn btn-secondary ms-3">Reset</button>
          </div>
        </form>
      </div>
    </div>
  </div>

  <!-- Success Modal -->
  <div class="modal fade" id="successModal" tabindex="-1" aria-labelledby="successModalLabel" aria-hidden="true">
    <div class="modal-dialog modal-dialog-centered">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="successModalLabel">Success</h5>
          <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
        </div>
        <div class="modal-body">
          Your details have been saved!
        </div>
        <div class="modal-footer">
          <button type="button" class="btn btn-success" data-bs-dismiss="modal">OK</button>
        </div>
      </div>
    </div>
  </div>

  <!-- Bootstrap JS -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>

  <!-- JavaScript Events -->
  <script>
    //onChange
    function toUpperCaseField(field) {
      field.value = field.value.toUpperCase();
    }

    //onFocus
    function highlightField(field) {
      field.style.backgroundColor = "#e0f7fa";
    }

    //onBlur
    function removeHighlight(field) {
      field.style.backgroundColor = "white";
    }
  </script>
</body>
</html>
