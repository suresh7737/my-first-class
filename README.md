# my-first-class <br>
hello suresh takhar
@extends('user.include.link')
@section('content')
    <div id="carouselExampleControls" class="carousel slide" data-bs-ride="carousel">
        <div class="carousel-inner">
            @foreach ($data as $key => $banner1)
                @if ($banner1->status != 0)
                    <div class="carousel-item @if ($key == 1) . active @endif">

                        <img src="{{ asset('assets/img/' . $banner1->image) }}" class="d-block w-100" alt="...">
                    </div>
                @endif
            @endforeach
            {{-- <div class="carousel-item">
                <img src="{{asset('image/1682923238.jpg')  }}" class="d-block w-100" alt="...">
            </div>
            <div class="carousel-item">
                <img src="{{ asset('image/1682923238.jpg') }}" class="d-block w-100" alt="...">
            </div> --}}
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Next</span>
        </button>
    </div>

    <div class="container">
        <div class="row justify-content-evenly">
            <div class="col-10 mt-5">
                <h4 class="text-xs text-center sm:text-base md:text-xl text-secondary" style="font-weight: 300;">
                    <span class="text-secondary fw-bolder">Seen Unseen</span> creates meaningful designs using natural
                    materials and traditional techniques, showcasing the beauty and richness of nature. Our artisans weave
                    together a story with every piece, honoring their craft and bringing it to life for others to enjoy.
                </h4>
            </div>
        </div>
    </div>


    <div class="container mt-4">
        <div class="row d-flex justify-content-between ">
            @foreach ($product as $data)
                @if ($data->Status != 0)
                    <div class="col-md-4 ">

                        <div class=" a5" style="height: 410px; margin-top: 50px">
                            <a href="{{ route('product_details', $data->id) }}" class="text-dark" style="text-decoration: none">
                                <img src="{{ asset('assets/img/' . $data->image) }}" alt="" width="100%">
                                <div class=" ms-3">
                                    <p> {{ $data->Name }}</p>
                                    
                                    ₹ {{ $data->MRP }}
                                    <br>

                                    <p class="mt-3"><s> ₹ 5999</s></p>
                                    <p style="margin-left: 70px;margin-top:-60px;">{{ $data->Offer }}</p>

                                </div>
                            </a>
                        </div>
                    </div>
                @endif
            @endforeach
        </div>
    </div>



    {{-- <div class="col-md-2 a5" style="height: 400px">
                    <img src="{{ asset('image/2.jpg') }}" alt="" width="100%">
                    <div class="">
                        <p>Daboo Print Co-ord Set</p>
                        ₹ 3600
                        <br>

                        <p class="mt-3"> ₹ 5999</p>
                        <p style="margin-left: 70px;margin-top:-60px;">40% OFF</p>

                    </div>
                </div>
                <div class="col-md-2 a5" style="height: 400px">
                    <img src="{{ asset('image/3.jpg') }}" alt="" width="100%">
                    <div class="">
                        <p>Crayola Summer Long Dress
                        </p>
                        ₹ 3600
                        <br>

                        <p class="mt-3"> ₹ 5999</p>
                        <p style="margin-left: 70px;margin-top:-60px;">40% OFF</p>

                    </div>
                </div>
                <div class="col-md-2 a5" style="height: 400px">
                    <img src="{{ asset('image/4.jpg') }}" alt="" width="100%">
                    <div class="">
                        <p>Teal Vivid Short Dress</p>
                        ₹ 3600
                        <br>

                        <p class="mt-3"> ₹ 5999</p>
                        <p style="margin-left: 70px;margin-top:-60px;">40% OFF</p>

                    </div>
                </div> --}}


    {{-- <div class="row a6 mt-5"> --}}
    {{-- <div class="col-md-2 a5" style="height: 400px">
                        <img src="{{ asset('image/5.jpg') }}" alt="" width="100%">
                        <div class="">
                            <p>Pistachio Dino Teeth Co-ord Set</p>
                            ₹ 3600
                            <br>

                            <p class="mt-3"> ₹ 5999</p>
                            <p style="margin-left: 70px;margin-top:-60px;">40% OFF</p>

                        </div>
                    </div>
                    <div class="col-md-2 a5" style="height: 400px">
                        <img src="{{ asset('image/6.jpg') }}" alt="" width="100%">
                        <div class="">
                            <p>Sand Ruffled up Co-ord
                            </p>
                            ₹ 3600
                            <br>

                            <p class="mt-3"> ₹ 5999</p>
                            <p style="margin-left: 70px;margin-top:-60px;">40% OFF</p>

                        </div>
                    </div>
                    <div class="col-md-2 a5" style="height: 400px">
                        <img src="{{ asset('image/7.jpg') }}" alt="" width="100%">
                        <div class="">
                            <p>Code Blue Co-ord Set</p>
                            ₹ 3600
                            <br>

                            <p class="mt-3"> ₹ 5999</p>
                            <p style="margin-left: 70px;margin-top:-60px;">40% OFF</p>

                        </div>
                    </div>
                    <div class="col-md-2 a5" style="height: 400px">
                        <img src="{{ asset('image/8.jpg') }}" alt="" width="100%">
                        <div class="">
                            <p>Flared Tunic and Pants with hand Embroidery</p>
                            ₹ 3600
                            <br>

                            <p class="mt-3"> ₹ 5999</p>
                            <p style="margin-left: 70px;margin-top:-60px; font-weight: 50;">40% OFF</p>

                        </div>
                    </div> --}}
    {{-- </div> --}}
    </div>
    </div>




    <div class="container">
        <div class="row my-5">
            <h1 style="font-weight: 200;margin:auto;padding: 22px 0px 51px 0px; text-align:center">Shop by category
            </h1>
            <!-- // Catageoyr insert -->



            <div class="col-md-2">
                <a href=""> <img style="width: 100%; border-radius: 10px; height:260px;"
                        src="{{ asset('image/a.jpg') }}" alt=""></a>
                <h6 style="font-weight: 100; text-align: center;" class="mt-4">OFFICE WEAR </h6>
            </div>

            <div class="col-md-2">
                <img style="width: 100%; border-radius: 10px; height:260px;" src="{{ asset('image/b.jpg') }}"
                    alt="">
                <h6 style="font-weight: 100; text-align: center;" class="mt-4">SHIRTS</h6>
            </div>


            <div class="col-md-2">
                <img style="width: 100%; border-radius: 10px; height:260px;" src="{{ asset('image/c.jpg') }}"
                    alt="">
                <h6 style="font-weight: 100; text-align: center;" class="mt-4">CO-ORDS</h6>
            </div>


            <div class="col-md-2">
                <img style="width: 100%; border-radius: 10px; height:260px;" src="{{ asset('image/d.jpg') }}"
                    alt="">
                <h6 style="font-weight: 100; text-align: center;" class="mt-4">JUMPSUITS</h6>
            </div>


            <div class="col-md-2">
                <img style="width: 100%; border-radius: 10px; height:260px;" src="{{ asset('image/e.jpg') }}"
                    alt="">
                <h6 style="font-weight: 100; text-align: center;" class="mt-4">DRESSES</h6>
            </div>

            <div class="col-md-2">
                <img style="width: 100%; border-radius: 10px; height:260px;" src="{{ asset('image/f.jpg') }}"
                    alt="">
                <h6 style="font-weight: 100; text-align: center;" class="mt-4">FESTIVE WEAR</h6>
            </div>

        </div>
    </div>
    <div class="text-center">
        <h1 style="font-weight:200;">#seenunseensustainability</h1>
    </div>

    <style>
        * {
            box-sizing: border-box;
        }

        body {
            font-family: Verdana, sans-serif;
        }

        .mySlides {
            display: none;
        }

        img {
            vertical-align: middle;
        }

        .numbertext {
            color: #f2f2f2;
            font-size: 12px;
            padding: 8px 12px;
            position: absolute;
            top: 0;
        }

        /* The dots/bullets/indicators */
        .dot {
            height: 15px;
            width: 15px;
            margin: 0 2px;
            background-color: #bbb;
            border-radius: 50%;
            display: inline-block;
            transition: background-color 0.6s ease;
        }

        .active {
            background-color: #717171;
        }

        /* Fading animation */
        .fade {
            animation-name: fade;
            animation-duration: 1.5s;
        }

        @keyframes fade {
            from {
                opacity: .4
            }

            to {
                opacity: 1
            }
        }

        /* On smaller screens, decrease text size */
        @media only screen and (max-width: 300px) {
            .text {
                font-size: 11px
            }
        }
    </style>


    <div class="text-center mt-4">
        @foreach ($data1 as $num => $banner2)
            <div class="mySlides fade">
                <div class="numbertext">2 / 5</div>
                <img src="{{ asset('assets/img/' . $banner2->image) }}" alt="" class="w-75">

            </div>
        @endforeach
        {{-- 
        <div class="mySlides fade">
            <div class="numbertext">3 / 5</div>
            <img src="https://ubgot.co.in/seen_unseen/images/banners/1678537072.png" alt="" class="w-75">

        </div>
        <div class="mySlides fade">
            <div class="numbertext">4 / 5</div>
            <img src="https://ubgot.co.in/seen_unseen/images/banners/1678965695.jpg" alt="" class="w-75">

        </div>

        <div class="mySlides fade">
            <div class="numbertext">5 / 5</div>
            <img src="https://ubgot.co.in/seen_unseen/images/banners/1678537072.png" alt="" class="w-75">

        </div> --}}

    </div>
    <br>

    <div style="text-align:center">
        <span class="dot"></span>
        <span class="dot"></span>
        <span class="dot"></span>
        <span class="dot"></span>
        <span class="dot"></span>
    </div>

    <script>
        let slideIndex = 0;
        showSlides();

        function showSlides() {
            let i;
            let slides = document.getElementsByClassName("mySlides");
            let dots = document.getElementsByClassName("dot");
            for (i = 0; i < slides.length; i++) {
                slides[i].style.display = "none";
            }
            slideIndex++;
            if (slideIndex > slides.length) {
                slideIndex = 1
            }
            for (i = 0; i < dots.length; i++) {
                dots[i].className = dots[i].className.replace(" active", "");
            }
            slides[slideIndex - 1].style.display = "block";
            dots[slideIndex - 1].className += " active";
            setTimeout(showSlides, 1400); // Change image every 2 seconds
        }
    </script>
    <div class="container text-center">
        <div class="my-4" style="width: 88%;margin-left: 66px;">

            <div style="font-weight: 100;color:#868686; font-size:23px;">
                <u>SeenUnseen</u> is dedicated to sustainability, using eco-friendly materials, and reducing water
                usage and waste. We prioritize partnering with like-minded suppliers and strive to minimize our
                environmental impact, ensuring that choosing our brand is a responsible choice for your wardrobe and
                the planet.
            </div>
        </div>
    </div>
@endsection
