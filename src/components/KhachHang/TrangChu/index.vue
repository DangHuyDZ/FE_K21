<template>
    <div class="row">
        <div id="carouselExampleControls" class="carousel slide pointer-event" data-bs-ride="carousel">
            <ol class="carousel-indicators">
                <li data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class=""></li>
                <li data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1" class=""></li>
                <li data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2" class="active" aria-current="true">
                </li>
            </ol>
            <div class="carousel-inner">
                <div class="carousel-item rounded-4" data-bs-interval="2000" style="background-color: #1C2331;">
                    <div class="row">
                        <div class="col-6 d-flex align-items-center">
                            <div class="container ms-5">
                                <h2 class="text-white mb-4">Món ngon đến tay bạn chỉ trong vài phút!
                                    <i class="fa-brands fa-square-web-awesome-stroke text-warning"></i>
                                </h2>
                                <span class="text-white">
                                    FoodZone cam kết giao đồ ăn nóng hổi, tươi ngon, đúng giờ đến tận cửa nhà bạn.
                                    Thỏa mãn cơn đói bất kỳ lúc nào, ở bất kỳ đâu!
                                </span>
                                <p class="mt-4"><button class="btn btn-outline-light rounded-4"> <b>TRẢI NGHIỆM
                                            NGAY</b> </button></p>
                            </div>
                        </div>
                        <div class="col-6">
                            <img src="https://png.pngtree.com/png-clipart/20241112/original/pngtree-food-delivery-by-scooters-free-download-png-image_16940462.png"
                                class="d-block w-100 rounded-4" alt="..."
                                style="width: 400px; height: 500px; object-fit: cover;">
                        </div>
                    </div>
                </div>
                <div class="carousel-item active rounded-4" data-bs-interval="10000" style="background-color: #1C2331;">
                    <div class="row">
                        <div class="col-6 d-flex align-items-center">
                            <div class="container ms-5">
                                <h2 class="text-white mb-4">Ưu đãi hấp dẫn - Đặt ngay hôm nay!
                                    <i class="fa-brands fa-square-web-awesome-stroke text-warning"></i>
                                </h2>
                                <span class="text-white">
                                    Giảm đến 50% cho lần đặt hàng đầu tiên. Hàng ngàn món ăn ngon đang chờ bạn khám
                                    phá! Nhanh tay đặt ngay để không bỏ lỡ!
                                </span>
                                <p class="mt-4"><button class="btn btn-outline-light rounded-4"> <b>ĐẶT HÀNG
                                            NGAY</b> </button></p>
                            </div>
                        </div>
                        <div class="col-6">
                            <img src="https://alltop.vn/backend/media/images/posts/695/Dominos_Pizza-196049.jpg"
                                class="d-block w-100 rounded-4" alt="..."
                                style="width: 450px; height: 500px; object-fit: cover;">
                        </div>
                    </div>
                </div>
                <div class="carousel-item rounded-4" style="background-color: #1C2331;">
                    <div class="row">
                        <div class="col-6 d-flex align-items-center">
                            <div class="container ms-5">
                                <h2 class="text-white mb-4">Khám phá thế giới ẩm thực ngay tại nhà!
                                </h2>
                                <span class="text-white">
                                    Hàng ngàn món ăn từ Việt Nam, Âu, Á, Fusion đang sẵn sàng phục vụ bạn. Chỉ cần vài
                                    cú nhấp chuột, tất cả ẩm thực sẽ đến ngay trước cửa nhà!
                                </span>
                                <p class="mt-4"><button class="btn btn-outline-light rounded-4"> <b>THỬ NGAY</b>
                                    </button></p>
                            </div>
                        </div>
                        <div class="col-6">
                            <img src="https://vj-prod-website-cms.s3.ap-southeast-1.amazonaws.com/shutterstock371955106huge-1675245432977.jpg"
                                class="d-block w-100 rounded-4" alt="..."
                                style="width: 450px; height: 500px; object-fit: cover;">
                        </div>
                    </div>
                </div>

            </div>
            <a class="carousel-control-prev" href="#carouselExampleControls" role="button" data-bs-slide="prev">
                <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                <span class="visually-hidden">Previous</span>
            </a>
            <a class="carousel-control-next" href="#carouselExampleControls" role="button" data-bs-slide="next">
                <span class="carousel-control-next-icon" aria-hidden="true"></span>
                <span class="visually-hidden">Next</span>
            </a>
        </div>
    </div>
    <div class="row mt-5">
        <div class="col-lg-12 text-center mb-2">
            <div class="d-inline-block">
                <h2><b>ĐẶT ĐỒ ĂN DỄ DÀNG TIỆN LỢI</b></h2>
                <div class="text-center">
                    <hr class="bg-secondary mb-3" style="width: 100%; height: 3px; border: none; border-radius: 5px" />
                </div>
            </div>
        </div>
        <div class="col-lg-12">
            <div class="row row-cols-1 row-cols-md-3 row-cols-xl-5 product-grid">
                <!-- Card 1: Đặt món ăn nhanh -->
                <div class="col">
                    <div class="card border-info border-start border-5 border-1 radius-10">
                        <div class="card-body">
                            <div class="text-center">
                                <div class="widgets-icons rounded-circle mx-auto bg-light-primary mb-3">
                                    <img src="https://hattimayukle.com/wp-content/uploads/2020/05/post-thumb-dat-do-an.jpg"
                                        alt="Fast Food" class="rounded-circle" style="width: 50px; height: 50px" />
                                </div>
                                <h5 class="my-1">Đặt Món Nhanh</h5>
                                <p class="mb-0 text-secondary">
                                    Nhận đồ ăn chỉ trong 30 phút
                                </p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Card 2: Giao hàng tận nơi -->
                <div class="col">
                    <div class="card border-primary border-start border-5 border-1 radius-10">
                        <div class="card-body">
                            <div class="text-center">
                                <div class="widgets-icons rounded-circle mx-auto bg-light-danger mb-3">
                                    <img src="https://kamereo.vn/blog/wp-content/uploads/2019/05/freepik_featured_delivery.jpg"
                                        alt="Delivery" class="rounded-circle" style="width: 50px; height: 50px" />
                                </div>
                                <h5 class="my-1">Giao Tận Nơi</h5>
                                <p class="mb-0 text-secondary">Giao đến bất cứ đâu</p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Card 3: Ẩm thực đa dạng -->
                <div class="col">
                    <div class="card border-warning border-start border-5 border-1 radius-10">
                        <div class="card-body">
                            <div class="text-center">
                                <div class="widgets-icons rounded-circle mx-auto bg-light-info mb-3">
                                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT9H5dbXlZ5W7DFkFi3f4aedpIkbEOPmLTH6w&s"
                                        alt="Diverse Cuisine" class="rounded-circle"
                                        style="width: 50px; height: 50px" />
                                </div>
                                <h5 class="my-1">Ẩm Thực Đa Dạng</h5>
                                <p class="mb-0 text-secondary">Từ món Việt đến quốc tế</p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Card 4: Combo tiết kiệm -->
                <div class="col">
                    <div class="card border-danger border-start border-5 border-1 radius-10">
                        <div class="card-body">
                            <div class="text-center">
                                <div class="widgets-icons rounded-circle mx-auto bg-light-success mb-3">
                                    <img src="https://www.gosell.vn/blog/wp-content/uploads/2023/03/combo-01.jpg"
                                        alt="Combo" class="rounded-circle" style="width: 50px; height: 50px" />
                                </div>
                                <h5 class="my-1">Combo Tiết Kiệm</h5>
                                <p class="mb-0 text-secondary">Ưu đãi lớn mỗi ngày</p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Card 5: Đồ ăn lành mạnh -->
                <div class="col">
                    <div class="card border-success border-start border-5 border-1 radius-10">
                        <div class="card-body">
                            <div class="text-center">
                                <div class="widgets-icons rounded-circle mx-auto bg-light-warning mb-3">
                                    <img src="https://img.lovepik.com/photo/50088/5320.jpg_wh860.jpg" alt="Healthy Food"
                                        class="rounded-circle" style="width: 50px; height: 50px" />
                                </div>
                                <h5 class="my-1">Đồ Ăn Lành Mạnh</h5>
                                <p class="mb-0 text-secondary">Dinh dưỡng cho cả gia đình</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <div class="row mt-4">
        <div class="col-lg-12">
            <div class="card">
                <div class="card-header">
                    <div class="row">
                        <div class="col-lg-8">
                            <h5 class="mt-2 text-danger">
                                Danh Mục Các Món Ăn <i class="fa-solid fa-bowl-food ms-1"></i>
                            </h5>
                        </div>
                        <div class="col-lg-2">
                            <div class="dropdown">
                                <button class="btn btn-white dropdown-toggle w-100" type="button" id="dropdownDanhMuc"
                                    data-bs-toggle="dropdown" aria-expanded="false">
                                    Danh Mục Món Ăn
                                </button>
                                <ul class="dropdown-menu" style="max-height: 250px; overflow-y: auto;"
                                    aria-labelledby="dropdownDanhMuc">
                                    <li v-for="(v, k) in phanLoai" :key="k">
                                        <a class="dropdown-item" href="#" @click.prevent="chonDanhMuc(v.id)">
                                            {{ v.ten_danh_muc }}
                                        </a>
                                    </li>
                                </ul>
                            </div>
                        </div>
                        <div class="col-lg-2">
                            <div class="btn-group w-100" role="group">
                                <button type="button" class="btn btn-white w-100">Chọn Mức Giá</button>
                                <div class="btn-group" role="group">
                                    <button id="btnGroupDrop1" type="button"
                                        class="btn btn-white dropdown-toggle dropdown-toggle-nocaret px-1"
                                        data-bs-toggle="dropdown" aria-expanded="false">
                                        <i class="bx bx-slider ms-1"></i>
                                    </button>
                                    <ul class="dropdown-menu dropdown-menu-start" aria-labelledby="btnGroupDrop1">
                                        <li><a class="dropdown-item" href="#"
                                                @click.prevent="filterByPrice('under50')">Dưới 50.000 VNĐ</a></li>
                                        <li><a class="dropdown-item" href="#"
                                                @click.prevent="filterByPrice('50to100')">50.000 - 100.000 VNĐ</a>
                                        </li>
                                        <li><a class="dropdown-item" href="#"
                                                @click.prevent="filterByPrice('100to200')">100.000 - 200.000
                                                VNĐ</a></li>
                                        <li><a class="dropdown-item" href="#"
                                                @click.prevent="filterByPrice('200to300')">200.000 - 300.000
                                                VNĐ</a></li>
                                        <li><a class="dropdown-item" href="#"
                                                @click.prevent="filterByPrice('above300')">Trên 300.000 VNĐ</a>
                                        </li>
                                    </ul>
                                </div>
                            </div>

                        </div>
                    </div>
                </div>
                <div class="card-body">
                    <div class="row product-grid">
                        <template v-for="(v, k) in monAnData" :key="k">
                            <div class="col-lg-2 d-flex">
                                <div class="card flex-fill">
                                    <router-link :to="'/khach-hang/don-dat-hang/' + v.id_quan_an">
                                        <img :src="v.hinh_anh" class="card-img-top"
                                            style="height: 200px; width: 100%;" />
                                        <div class="card-body">
                                            <h6 class="card-title cursor-pointer">
                                                {{ v.ten_mon_an }}
                                            </h6>
                                            <div class="clearfix">
                                                <p class="mb-0 float-start">{{ v.ten_quan_an }}</p>
                                            </div>
                                            <p class="mt-2">
                                                <del>{{ v.gia_ban }}đ</del>
                                                <strong class="ms-2">{{ v.gia_khuyen_mai }}đ</strong>
                                            </p>
                                            <div class="d-flex align-items-center mt-auto">
                                                <i class="fa-solid fa-tag text-danger me-2"></i>
                                                <span class="text-primary">-30%</span>
                                            </div>
                                        </div>
                                    </router-link>
                                </div>
                            </div>
                        </template>
                        <div class="col-lg-12 text-center">
                            <button type="button" class="btn btn-lg btn-outline-success" style="width: 30%;"><i
                                    class="fa-regular fa-hand-point-up"></i>Xem Thêm</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="row mt-4">
        <div class="col-lg-12 text-center">
            <div class="d-inline-block">
                <h4><b>QUÁN ĂN ĐƯỢC YÊU THÍCH NHIỀU NHẤT</b></h4>
                <div class="text-center">
                    <hr class="bg-primary my-2" style="width: 100%; height: 3px; border: none; border-radius: 5px" />
                </div>
            </div>
        </div>
        <div class="card">
            <div class="card-body">
                <div class="row product-grid">
                    <template v-for="(v, k) in quanAn" :key="k">
                        <div class="col-xl-4 col-lg-6 col-md-6 col-12 d-flex" v-if="k < 6">
                            <div class="card flex-fill">
                                <router-link :to="'/khach-hang/quan-an/' + v.id">
                                    <div class="card-body">
                                        <div class="row g-0">
                                            <div class="col-md-5">
                                                <img v-bind:src="v.hinh_anh" class="img-fluid rounded-start" alt="..."
                                                    style="width: 100%;height: 100%;">
                                            </div>
                                            <div class="col-md-7">
                                                <div class="card-body">
                                                    <h5 class="card-title"><b>
                                                            {{ v.ten_quan_an }}</b></h5>
                                                    <p>{{ v.dia_chi }}
                                                    </p>
                                                    <p><i class="fa-solid fa-tags me-1"></i> Tối thiểu {{
                                                        v.toi_thieu }} <i
                                                            class="fa-solid fa-circle-dollar-to-slot ms-3 me-1"></i>
                                                        Giá
                                                        {{ v.gia }}</p>
                                                    <div class="d-flex align-items-center mt-3">
                                                        <i class="fa-solid fa-tag text-danger me-2"></i> <span
                                                            class="text-primary"><b>Giảm hết {{ v.giam_gia
                                                            }}</b></span>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </router-link>
                            </div>
                        </div>
                    </template>
                    <div class="col-lg-12 text-center">
                        <button type="button" class="btn btn-lg btn-outline-success" style="width: 30%;"><i
                                class="fa-regular fa-hand-point-up"></i>Xem Thêm</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="row mt-4">
        <div class="col-lg-12">
            <div class="card">
                <div class="card-header">
                    <h5 class="mt-3"><b class="">VOUCHER HẤP DẪN KHI ĐẶT MÓN</b></h5>
                </div>
                <div class="card-body">
                    <div class="row product-grid">
                        <template v-for="(v, k) in list_voucher" :key="k">
                            <div class="col-lg-2 d-flex">
                                <div class="card flex-fill">
                                    <img :src="v.hinh_anh" class="card-img-top" >
                                    <div class="card-body">
                                        <h6 class="card-title cursor-pointer">{{ v.ten_voucher }}</h6>
                                        <div class="clearfix">
                                            <p class="mb-0 float-start text-danger">{{ v.ten_quan_an }}</p>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </template>
                        <div class="col-lg-12 text-center">
                            <button type="button" class="btn btn-lg btn-outline-success" style="width: 30%;"><i
                                    class="fa-regular fa-hand-point-up"></i>Xem Thêm</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import axios from 'axios';

export default {
    data() {
        return {
            phanLoai: [],
            quanAn: [],
            monAnData: [],
            originalMonAnData: [],
            list_voucher: [],
        };
    },
    created() {
        this.loadData();
    },
    methods: {
        loadData() {
            axios
                .get('http://127.0.0.1:8000/api/khach-hang/trang-chu/data')
                .then((res) => {
                    this.monAnData = res.data.mon_an;
                    this.originalMonAnData = res.data.mon_an;
                    this.quanAn = res.data.quan_an_yeu_thich;
                    this.list_voucher = res.data.voucher;
                    this.phanLoai = res.data.phan_loai;
                })
                .catch((res) => {
                    const list = Object.values(res.response.data.errors);
                    list.forEach((v, i) => {
                        this.$toast.error(v[0]);
                    });
                })
        },
        filterByPrice(range) {
            switch (range) {
                case "under50":
                    this.monAnData = this.originalMonAnData.filter(
                        (item) => item.gia_khuyen_mai < 50000
                    );
                    break;
                case "50to100":
                    this.monAnData = this.originalMonAnData.filter(
                        (item) => item.gia_khuyen_mai >= 50000 && item.gia_khuyen_mai <= 100000
                    );
                    break;
                case "100to200":
                    this.monAnData = this.originalMonAnData.filter(
                        (item) => item.gia_khuyen_mai > 100000 && item.gia_khuyen_mai <= 200000
                    );
                    break;
                case "200to300":
                    this.monAnData = this.originalMonAnData.filter(
                        (item) => item.gia_khuyen_mai > 200000 && item.gia_khuyen_mai <= 300000
                    );
                    break;
                case "above300":
                    this.monAnData = this.originalMonAnData.filter(
                        (item) => item.gia_khuyen_mai > 300000
                    );
                    break;
                default:
                    this.monAnData = this.originalMonAnData; // Hiển thị tất cả nếu không có bộ lọc
                    break;
            }
        }
    },

};
</script>
<style>
.dropdown-menu {
    max-height: 250px;
    width: 100%;
    overflow-y: auto;
}
</style>
