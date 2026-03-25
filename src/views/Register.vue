<template>
    <div class="container my-5">
        <div class="d-flex justify-content-center align-items-center vh-100">
        <div class="card shadow p-4" style="width: 500px; border-radius: 15px;">
            <h3 class="text-center mb-4">Register</h3>
            <form>
                <div class="mb-3">
                    <label for="firstname" class="form-label">FirstName</label>
                    <input type="text" class="form-control" id="firstname" placeholder="Enter firstname" required>
                </div>
                <div class="mb-3">
                    <label for="lastName" class="form-label">LastName</label>
                    <input type="text" class="form-control" id="lastName" placeholder="Enter lastName" required>
                </div>
                <div class="mb-3">
                    <label for="Phone" class="form-label">Phone</label>
                    <input type="password" class="form-control" id="Phone" placeholder="Enter Phone" required>
                </div>
                <div class="mb-3">
                    <label for="usename" class="form-label">Usename</label>
                    <input type="text" class="form-control" id="usename" placeholder="Enter usename" required>
                </div>
                <div class="mb-3">
                    <label for="password" class="form-label">Password</label>
                    <input type="password" class="form-control" id="password" placeholder="Enter password" required>
                </div>
                <button type="submit" class="btn btn-primary w-100">Login</button>
                
            </form>
        </div>
    </div>
</div>
</template>