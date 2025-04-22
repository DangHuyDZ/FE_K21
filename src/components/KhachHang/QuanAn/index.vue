<template>
    <div class="row">
        <div class="col-12">
            <div class="card">
                <div class="card-body">
                    <div class="row align-items-center">
                        <div class="col-lg-3 col-xl-2">
                            <div class="position-relative"><input type="text" class="form-control ps-5"
                                    placeholder="Tìm kiếm quán ăn..."> <span
                                    class="position-absolute top-50 product-show translate-middle-y"><i
                                        class="bx bx-search"></i></span></div>
                        </div>
                        <div class="col-lg-9 col-xl-10">
                            <form class="float-lg-end">
                                <div class="row row-cols-lg-2 row-cols-xl-auto g-2">
                                    <div class="col">
                                        <div class="btn-group" role="group"><button type="button"
                                                class="btn btn-white">159 Kết quả</button>
                                            <div class="btn-group" role="group"><button id="btnGroupDrop1" type="button"
                                                    class="btn btn-white dropdown-toggle dropdown-toggle-nocaret px-1"
                                                    data-bs-toggle="dropdown" aria-expanded="false"><i
                                                        class="bx bx-slider"></i></button>
                                                <ul class="dropdown-menu dropdown-menu-start"
                                                    aria-labelledby="btnGroupDrop1">
                                                    <li><a class="dropdown-item" href="#">Đúng nhất</a></li>
                                                    <li><a class="dropdown-item" href="#">Gần tôi</a></li>
                                                </ul>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </form>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="row product-grid">
        <template v-for="(v, k) in list_quan_an" :key="k">
            <div class="col-xl-4 col-lg-6 col-md-6 col-12 d-flex">
                <div class="card flex-fill">
                    <router-link :to="'/khach-hang/quan-an/' + v.id">
                        <div class="card-body text-dark">
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
                                            v.gia_min }} <i class="fa-solid fa-circle-dollar-to-slot ms-3 me-1"></i>
                                            Giá
                                            {{ v.gia_max }}</p>
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
    </div>
</template>
<script>
import axios from 'axios';

export default {
    data() {
        return {
            list_quan_an: [],
        }
    },
    mounted() {
        this.loadData();
    },
    methods: {
        formatVND(number) {
            return new Intl.NumberFormat('vi-VI', { style: 'currency', currency: 'VND' }).format(number,)
        },
        loadData() {
            axios
                .get('http://127.0.0.1:8000/api/khach-hang/quan-an/data', {
                    headers: {
                        Authorization: "Bearer " + localStorage.getItem("khach_hang_login"),
                    },
                })
                .then((res) => {
                    this.list_quan_an = res.data.data;
                })
                .catch((res) => {
                    const list = Object.values(res.response.data.errors);
                    list.forEach((v, i) => {
                        this.$toast.error(v[0]);
                    });
                })
        },
    },
}
</script>
<style></style>