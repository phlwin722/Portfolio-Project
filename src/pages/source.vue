<template>
  <div class="code-container">
    <h2>Provided Code Snippets</h2>

    <h3>Permissions</h3>
    <pre><code>{{ permissionsCode }}</code></pre>

    <h3>React Router</h3>
    <pre><code>{{ routerCode }}</code></pre>

    <h3>ContextProvider</h3>
    <pre><code>{{ contextProviderCode }}</code></pre>

    <h3>.env</h3>
    <pre><code>{{ envCode }}</code></pre>

    <h3>Axios Client</h3>
    <pre><code>{{ axiosClientCode }}</code></pre>

    <h3>Handle Change Function</h3>
    <pre><code>{{ handleChangeCode }}</code></pre>

    <h3>Sidebar Component</h3>
    <pre><code>{{ sidebarCode }}</code></pre>

    <h3>Laravel Backend Setup</h3>
    <pre><code>{{ laravelBackendCode }}</code></pre>

    <h3>User Component</h3>
    <pre><code>{{ userComponentCode }}</code></pre>

    <h3>CRUD Controller (Laravel)</h3>
    <pre><code>{{ crudControllerCode }}</code></pre>

    <h3>Main Application</h3>
    <pre><code>{{ mainCode }}</code></pre>

    <h3>Postman</h3>
    <pre><code>{{ postMan }}</code></pre>
  </div>
</template>

<script setup>
const permissionsCode = `
sudo chmod -R $USER:$USER /var/www/folder_name
sudo chmod -R 775 /var/www/folder_name

sudo npm install axios
sudo npm install react-router-dom -S
`;

const routerCode = `
import { createBrowserRouter, Navigate } from "react-router-dom";
import Signin from "../pages/DefaultLayout/Signin";
import Signup from "../pages/DefaultLayout/Signup";
import Notfound from "../Notfound";
import MainLayout from "../layout/MainLayout";
import GuestLayout from "../layout/GuestLayout";

const router = createBrowserRouter([
  {
    path: "/",
    element: <GuestLayout />,
    children: [
      {
        path: '/',
        element: <Navigate to='/signin' />
      },
      {
        path: "/signin",
        element: <Signin />,
      },
      {
        path: "/signup",
        element: <Signup />,
      },
    ],
  },
  {
    path: '',
    element: <MainLayout />,
    children: [
      {

      }
    ],
  },
  {
    path: "*",
    element: <Notfound />,
  },
]);

export default router;
`;

const contextProviderCode = `
import { createContext, useState, useContext } from "react";

const StateContext = createContext({
  user: null,
  token: null,
  setUser: () => {},
  setToken: () => {},
}); 

export const ContextProvider = ({ children }) => {
  // load user information from localstorage if available
  const [user, _setUser] = useState(() => {
    const storedUser = localStorage.getItem('USER');
    return storedUser ? JSON.parse(storedUser) : null;
  });

  // load token from localstorage if available
  const [token, _setToken] = useState(localStorage.getItem('ACCESS_TOKEN'));

  const setUser = (user_info) => {{
    _setUser(user_info)
    if (user) {
      localStorage.setItem('USER', JSON.stringify(user))
    } else {
      localStorage.removeItem('USER');
    }
  }}

  const setToken = (token) => {
    _setToken(token);
    if (token) {
      localStorage.setItem('ACCESS_TOKEN',token)
    } else {
      localStorage.removeItem('ACCESS_TOKEN')
    }
  }

  return (
    <StateContext.Provider
      value={{
        user,
        token,
        setToken,
        setUser,
      }}
    >
      {children}
    </StateContext.Provider>
  )
}

export const useStateContext = () => useContext(StateContext)
`;

const envCode = `
.env VITE_API_BASE_URL=http://127.0.0.1:8000/api
`;

const axiosClientCode = `
import axios from 'axios'

const axiosClient = axios.create({
  baseURL: import.meta.env.VITE_API_BASE_URL,
})

axiosClient.interceptors.request.use((config) => {
  const token = localStorage.getItem('ACCESS_TOKEN');
  
  if (token) {
    config.headers.Authorization = \`Bearer \${token}\`;
  }

  return config;
});

axiosClient.interceptors.response.use((response) => {
  return response;
},
(error) => {
  try {
    if (error.response.status && error.response.status === 401) {
      localStorage.removeItem('ACCESS_TOKEN')
      // handle unauthorized access
      window.location.href= '/signin'
    }
  } catch (error) {
    console.log('error', error)
  }
  throw error;
});

export default axiosClient;
`;

const handleChangeCode = `
const handleChange = (event) => {
  const { name, value } = event.target;
  setFormData((prev) => ({
    ...prev,
    [name]: value
  }))
}
`;

const sidebarCode = `
import { NavLink } from "react-router-dom";

const SectionBar = () => {
  return (
    <div className="h-full">
      <ul className="px-3 py-4 space-y-2">
        <li>
          <NavLink 
            to='/dashboard'
            className={({isActive}) => 
              \`block p-2 rounded cursor-pointer \${
                isActive ? 'bg-gray-700 text-white': 'hover:bg-gray-500 hover:text-white'
              }\`
            }
            >
              Dashboard
          </NavLink>
        </li>
        <li>
          <NavLink 
            to='/user'
            className={({isActive}) => 
              \`block p-2 rounded cursor-pointer \${
                isActive ? 'bg-gray-700 text-white' : 'hover:bg-gray-500 hover:text-white'
              }\`
            }
            >
              User
          </NavLink>
        </li>
      </ul>
    </div>
  );
};

export default SectionBar;
`;

const laravelBackendCode = `
composer global config bin-dir --absolute
/home/system32/.config/composer/vendor/bin
export PATH="$PATH:$HOME/.config/composer/vendor/bin"
source ~/.bashrc 
laravel --version

create database junior_fullstack

touch routes/api.php

// Laravel’s app/Providers/RouteServiceProvider.php
use Illuminate\Support\Facades\Route;

public function boot(): void
{
    Route::middleware('api')
        ->prefix('api')
        ->group(base_path('routes/api.php'));
}

// Install Laravel Sanctum (Recommended for simple API tokens)
composer require laravel/sanctum
php artisan vendor:publish --provider="Laravel\Sanctum\SanctumServiceProvider"
php artisan migrate

// Add HasApiTokens trait to your User model:
use Laravel\Sanctum\HasApiTokens;

class User extends Authenticatable
{
    use HasApiTokens, Notifiable, ...;
}

// route/api.php
<?php 
use Illuminate\Support\Facades\Route;
use Illuminate\Http\Request;
use App\Http\Controllers\UserController;

Route::get('/user', function (Request $request) {
  return $request->user();
})->middleware('auth:sanctum');

Route::prefix('auth')->controller(UserController::class)->group(function () {
  Route::post('/signin', 'Create');
  Route::post('/signup', 'Login');
  Route::middleware('auth:sanctum')->post('/logout', 'Logout');
});

// Password validation
use Illuminate\Validation\Rules\Password;
'password' => [
    'required',
    Password::min(8)
        ->mixedCase()
        ->symbols()
        ->letters()
        ->numbers()
],

use Illuminate\Support\Facades\DB;
use Illuminate\Support\Facades\Auth;

public function Login (SigninRequest $signinRequest) {
    try {
        $data = $signinRequest->validated();
        if (!Auth::attempt($data)) {
            return response()->json([
                'errors' => 'Invalid email address or password, please try again.'
            ],423);
        }

        $user = Auth::user();
        $token = $user->createToken('access_token')->plainTextToken;

        return response()->json([
            'user' => $user,
            'token' => $token
        ]);
    } catch (\Exception $e)  {
        return response()->json([
            'error' => $e->getMessage()
        ]);
    }
}

public function Logout (Request $request) {
    try {
        $user = $request->user();
        $user->currentAccessToken()->delete();

        return response()->json([
            'message' => 'Logout successfully' 
        ],200);
    } catch(\Exception $e) {
        return response()->json([
            'error' => $e->getMessage()
        ]);
    }
}
`;

const userComponentCode = `
import { NavLink, useNavigate } from "react-router-dom";
import { useEffect, useState } from "react";
import axiosClient from "../../axiosClient";

const User = () => {
  const URL = "/product";
  const navigate = useNavigate();

  const [rows, setRows] = useState([]);

  const handleEdit = (id) => {
    navigate(\`/user/form/\${id}\`);
  };

  const handleDelete = async (id) => {
    try {
      const confirm = window.confirm("Are you sure you want to delete this product?");

      if (confirm) {
        const deleteData = new FormData();
        deleteData.append("id", id);
        const response = await axiosClient.post(\`\${URL}/delete\`, deleteData);

        if (response.data.message) {
          fetch();
          alert('Deleted successfully')
        }
      } else {
      }
    } catch (error) {
      console.log(error);
    }
  };

  const fetch = async () => {
    try {
      const response = await axiosClient.post(\`\${URL}/index\`);
      setRows(response.data.product);
    } catch (error) {
      console.log(error);
    }
  };

  useEffect(() => {
    fetch();
  }, []);

  useEffect(() => {
    console.log("rows updated", rows);
  }, [rows]);

  return (
    <>
      <div className="w-full bg-white p-3 rounded-lg">
        <p className="text-[20px]">Product</p>
      </div>

      <div className="w-full bg-white p-3 rounded-lg mt-4 flex items-end justify-end">
        <button className="bg-blue-500 p-2 rounded-lg text-white">
          <NavLink to="/user/form">Add</NavLink>
        </button>
      </div>

      <div className="w-full bg-white p-3 rounded-lg mt-4">
        <table className="table-auto w-full border border-gray-300">
          <thead>
            <tr className="bg-gray-200">
              <th className="py-2">Product name</th>
              <th className="py-2">Price</th>
              <th className="py-2">Quantity</th>
              <th className="py-2">Actions</th>
            </tr>
          </thead>
          <tbody>
            {rows.length > 0 ? (
              rows.map((product) => (
                <tr
                  key={product.id}
                  className="hover:bg-gray-200 cursor-pointer"
                >
                  <td className="py-2 text-center">{product.product_name}</td>
                  <td className="py-2 text-center">{product.price}</td>
                  <td className="py-2 text-center">{product.quantity}</td>
                  <td className="py-2 flex gap-2 items-center justify-center">
                    <button
                      className="bg-green-500 text-white p-1 rounded-lg cursor-pointer"
                      onClick={() => handleEdit(product.id)}
                    >
                      Edit
                    </button>
                    <button
                      onClick={() => handleDelete(product.id)}
                      className="bg-red-500 text-white rounded-lg p-1 cursor-pointer"
                    >
                      Delete
                    </button>
                  </td>
                </tr>
              ))
            ) : (
              <tr>
                <td colSpan="4" className="text-center p-4">
                  No Product found
                </td>
              </tr>
            )}
          </tbody>
        </table>
      </div>
    </>
  );
};

export default User;
`;

const crudControllerCode = `
<?php

namespace App\Http\Controllers;

use Illuminate\Http\Request;
use App\Http\Requests\ProductRequest;
use App\Models\Product;
use Illuminate\Support\Facades\DB;

class ProductController extends Controller
{
    public function Index()
    {
        try {
            $product = Product::all();

            return response()->json([
                'product' => $product
            ]);
        } catch (\Exception $e) {
            return response()->json([
                'error' => $e->getMessage()
            ]);
        }
    }
    public function Create(ProductRequest $productRequest)
    {
        try {
            $data = $productRequest->validated();
            $product = Product::create($data);

            return response()->json([
                'message' => 'Created successfully',
                'product' => $product
            ]);
        } catch (\Exception $e) {
            return response()->json([
                'error' => $e->getMessage()
            ]);
        }
    }

    public function update(Request $request)
    {
        try {
            $product = Product::findOrFail($request->id);
            
            $data = $request->only(['first_name', 'last_name']);

            if (!empty($request->password)) {
              $data['password'] = bcrypt($request->password);
            }
            $product->update($data);
            return response()->json([
              'user' => $user 
            ]);
        } catch (\Exception $E) {
            return response()->json([
                'error' => $E->getMessage()
            ]);
        }
    }

    public function delete(Request $request)
    {
        try {
            $product = Product::findOrFail($request->id);
            $product->delete();

            return response()->json([
                'message' => 'Product deleted successfully'
            ]);
        } catch (\Exception $e) {
            return response()->json(
                [
                    'error' => $e->getMessage()
                ]
            );
        }
    }

    public function ProductInfo(Request $request)
    {
        try {
            $product = DB::table('products')
                        ->where('id', $request->id)
                        ->get();

            return response()->json([
                'product' => $product,
                'message' => 'Fetch successfully'
            ]);
        } catch (\Exception $e) {
            return response()->json([
                'error' => $e->getMessage()
            ]);
        }
    }
}
`;

const mainCode = `
import { StrictMode } from "react";
import { createRoot } from "react-dom/client";
import "./index.css";
import { RouterProvider } from "react-router-dom";
import router from "./routes/router";
import { ContextProvider } from "./contexts/ContextProvider";

createRoot(document.getElementById("root")).render(
  <StrictMode>
    <ContextProvider>
      <RouterProvider router={router} />
    </ContextProvider>
  </StrictMode>
);
`;

const postMan = `
  postman checking
  http://127.0.0.1:8000/api/crud/create
  headers:
  Accept: application/json
  Content-Type: application/json
  Authorization: Bearer 2|asda
`
</script>

<style scoped>
.code-container {
  padding: 20px;
  max-width: 100%;
  overflow-x: auto;
}

h2,
h3 {
  color: #333;
  margin-top: 20px;
  margin-bottom: 10px;
}

pre {
  background: #f4f4f4;
  padding: 15px;
  border-radius: 5px;
  overflow-x: auto;
}

code {
  font-family: "Courier New", Courier, monospace;
  font-size: 14px;
  color: #333;
}
</style>
