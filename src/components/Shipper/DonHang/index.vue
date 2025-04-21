<template>
	<div class="row">
		<div class="col-12">
			<div class="card border-0 shadow bg-primary">
				<div class="card-body ">
					<div class="d-flex justify-content-between align-items-center flex-wrap">
						<div class="d-flex align-items-center">
							<div>
								<h2 class="h3 text-white mb-1">Quản lý đơn hàng</h2>
							</div>
						</div>
						<div class="d-flex align-items-center gap-3 mt-md-0">
							<div class="text-end">
								<h3 class="mb-0 mt-1 text-white">Nguyễn Văn A</h3>
							</div>
							<div
								class="rounded-circle bg-white bg-opacity-25 d-flex align-items-center justify-content-center">
								<img style="width: 60px; height: 60px; object-fit: cover; border-radius: 50%;"
									class="img-fluid" src="https://cdn-icons-png.flaticon.com/512/4140/4140037.png"
									alt="">
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
	<div class="card">
		<div class="card-body">
			<ul class="nav nav-tabs mb-3" id="orderTabs">
				<li class="nav-item">
					<a class="nav-link active" id="available-tab" data-bs-toggle="tab" href="#available">
						<i class="bi bi-list-ul me-1"></i> Đơn có thể nhận
						<span class="badge bg-primary ms-1">3</span>
					</a>
				</li>
				<li class="nav-item">
					<a class="nav-link" id="accepted-tab" data-bs-toggle="tab" href="#accepted">
						<i class="bi bi-check-circle me-1"></i> Đơn đã nhận
						<span class="badge bg-success ms-1">3</span>
					</a>
				</li>
				<li class="nav-item">
					<a class="nav-link" id="completed-tab" data-bs-toggle="tab" href="#completed">
						<i class="bi bi-archive me-1"></i> Đơn đã hoàn thành
					</a>
				</li>
			</ul>
			<div class="row">
				<div class="col-lg-5 col-md-6 mb-3">
					<select class="form-select">
						<option selected>Khu vực</option>
						<option>Quận 1</option>
						<option>Quận 2</option>
						<option>Quận 3</option>
						<option>Quận Bình Thạnh</option>
					</select>
				</div>
				<div class="col-lg-5 col-md-6 mb-3">
					<select class="form-select">
						<option selected>Sắp xếp theo</option>
						<option>Thời gian gần nhất</option>
						<option>Khoảng cách gần nhất</option>
						<option>Giá trị cao nhất</option>
					</select>
				</div>
				<div class="col-lg-2 col-md-12 mb-3">
					<button class="btn btn-primary w-100 ">
						Lọc
					</button>
				</div>
			</div>
			<div class="tab-content">
				<div class="tab-pane fade show active" id="available">
					<div class="row d-flex">
						<template v-for="(value, index) in list_don_hang_co_the_nhan" :key="index">
							<div class="col-xl-4 col-lg-6 col-md-6 col-12 d-flex">
								<div class="card w-100">
									<div
										class="card-header bg-warning d-flex justify-content-between align-items-center">
										<span class="fw-bold text-white">#{{ value.ma_don_hang }}</span>
										<span class="text-light small"><b>10 phút trước</b></span>
									</div>
									<div class="card-body">
										<div class="row mb-3">
											<div class="col-lg-6 col-md-12 d-flex">
												<div class="d-flex">
													<div class="me-3" style="align-content: center;">
														<img style="width: 80px; height: 60px;" class="img-fluid"
															:src="value.hinh_anh" alt="">
													</div>
													<div>
														<h6>{{ value.ten_quan_an }}</h6>
														<p class="text-muted mb-0 small">{{ value.dia_chi_quan }}, {{
															value.ten_quan_huyen_quan }}</p>
														<div class="small text-success">2.5km từ vị trí của bạn</div>
													</div>
												</div>
											</div>
											<div class="col-lg-6 col-md-12 d-flex">
												<div class="d-flex">
													<div class="me-3" style="align-content: center;">
														<img style="width: 60px; height: 60px; border-radius: 50%;"
															class="img-fluid" :src="value.avatar">
													</div>
													<div>
														<h6>{{ value.ten_nguoi_nhan }}</h6>
														<p class="text-muted mb-0 small">{{ value.dia_chi_khach }}, {{
															value.ten_quan_huyen_khach }}</p>
														<div class="small text-muted">5.2km • ~15 phút</div>
													</div>
												</div>
											</div>
										</div>
										<div class="d-flex justify-content-between border-top pt-3">
											<div>
												<span class="d-block">Giá trị đơn hàng:</span>
												<span class="fw-bold text-success">{{ formatVND(value.tong_tien)
												}}</span>
											</div>
											<div>
												<span class="d-block">Phí vận chuyển:</span>
												<span class="fw-bold text-primary">{{ formatVND(value.phi_ship)
												}}</span>
											</div>
											<div>
												<span class="d-block">Thanh toán:</span>
												<span class="fw-bold">COD</span>
											</div>
										</div>
									</div>
									<div class="card-footer">
										<div class="row">
											<div class="col-lg-6 col-md-12">
												<button class="btn btn-primary w-100">Chi tiết</button>
											</div>
											<div class="col-lg-6 col-md-12">
												<button v-on:click="Object.assign(don_hang, value)"
													data-bs-toggle="modal" data-bs-target="#exampleModal"
													class="btn btn-success w-100">Nhận
													đơn</button>
											</div>
										</div>
									</div>
								</div>
							</div>
						</template>
					</div>
				</div>
				<div class="tab-pane fade" id="accepted">
					<div class="row g-3">
						<template v-for="(value, index) in list_don_dang_giao" :key="index">
							<div class="col-xl-4 col-lg-6 col-md-6 col-12 d-flex">
								<div class="card border-warning w-100">
									<div
										class="card-header bg-warning d-flex justify-content-between align-items-center">
										<span class="fw-bold text-white">#ORD-5823</span>
										<span class="badge bg-secondary text-white">Đang lấy hàng</span>
									</div>
									<div class="card-body">
										<div class="d-flex mb-3">
											<div class="me-3">
												<img style="width: 100px; height: 100px; object-fit: cover; border-radius: 50%;"
													class="img-fluid"
													src="https://cdn.vntrip.vn/cam-nang/wp-content/uploads/2017/09/bun-dau-mam-tom-2-e1505460520519.jpg"
													alt="">
											</div>
											<div>
												<h6 class="mt-3">Bún Đậu Mắm Tôm A Chảnh</h6>
												<p class="text-muted mb-0 small">94 Nguyễn Du, Quận 1</p>
												<div class="small text-warning"><i
														class="bi bi-hourglass-split me-1"></i>
													Đang lấy hàng</div>
											</div>
										</div>
										<div class="d-flex mb-3">
											<div class="me-3">
												<img style="width: 100px; height: 100px; object-fit: cover; border-radius: 50%;"
													class="img-fluid"
													src="https://cdn-icons-png.flaticon.com/512/4140/4140037.png"
													alt="">
											</div>
											<div>
												<h6 class="mt-3">Trân Văn A</h6>
												<p class="text-muted mb-0 small">35 Trần Hưng Đạo, Quận 5</p>
												<div class="small text-muted"><i class="bi bi-clock-history me-1"></i>
													Chờ lấy hàng</div>
											</div>
										</div>
										<div class="progress mb-3" style="height: 8px;">
											<div class="progress-bar bg-success" role="progressbar" style="width: 40%;"
												aria-valuenow="40" aria-valuemin="0" aria-valuemax="100"></div>
										</div>
										<div class="d-flex justify-content-between mb-3">
											<div class="text-center">
												<i class="bi bi-check-circle-fill text-success"></i>
												<div class="small">Nhận đơn</div>
											</div>
											<div class="text-center">
												<i class="bi bi-circle-fill text-warning"></i>
												<div class="small">Lấy hàng</div>
											</div>
											<div class="text-center">
												<i class="bi bi-circle text-muted"></i>
												<div class="small">Giao hàng</div>
											</div>
											<div class="text-center">
												<i class="bi bi-circle text-muted"></i>
												<div class="small">Hoàn thành</div>
											</div>
										</div>

										<div class="d-flex justify-content-between border-top pt-3">
											<div>
												<span class="d-block">Giá trị đơn hàng:</span>
												<span class="fw-bold text-success">180.000đ</span>
											</div>
											<div>
												<span class="d-block">Phí vận chuyển:</span>
												<span class="fw-bold text-primary">35.000đ</span>
											</div>
											<div>
												<span class="d-block">Thanh toán:</span>
												<span class="fw-bold">Đã thanh toán</span>
											</div>
										</div>
									</div>
									<div class="card-footer bg-white">
										<div class="d-flex justify-content-between">
											<span class="text-muted small"><i class="bi bi-clock me-1"></i> Nhận đơn 20
												phút trước</span>
											<div>
												<button v-if="value.tinh_trang == 1" disabled
													class="btn btn-outline-warning ">Quán đang chế biến</button>
												<button v-else v-on:click="daGiao(value)"
													class="btn btn-outline-success ">Giao Hàng</button>
												<button class="btn btn-outline-danger ms-2">Gặp vấn đề</button>
											</div>
										</div>
									</div>
								</div>
							</div>
						</template>
					</div>
				</div>
				<div class="tab-pane fade" id="completed">
					<div class="completed-orders-header mb-4">
						<div class="card">
							<div class="card-body">
								<div class="d-flex justify-content-between align-items-center">
									<h4 class="mb-1">Lịch sử giao hàng</h4>
									<div class="d-flex gap-2">
										<div class="input-group">
											<input type="date" class="form-control" placeholder="Chọn ngày">
											<button class="btn btn-outline-primary">
												Lọc
											</button>
										</div>
										<button class="btn btn-outline-success text-nowrap">
											Xuất báo cáo
										</button>
									</div>
								</div>
							</div>
						</div>
					</div>
					<div class="row g-4">
						<template v-for="(value, index) in list_don_da_giao" :key="index">
							<div class="col-xl-4 col-lg-6 col-md-6 col-12 d-flex">
								<div class="card w-100">
									<div class="card-header bg-warning border-bottom-0">
										<div class="d-flex justify-content-between align-items-center">
											<div class="d-flex align-items-center gap-2">
												<i class="bi bi-check-circle-fill text-success fs-5"></i>
												<span class="fw-bold text-white">#{{ value.ma_don_hang }}</span>
											</div>

										</div>
									</div>
									<div class="card-body">
										<div class="restaurant-info d-flex align-items-center mb-4">
											<div class="restaurant-image me-3">
												<img :src="value.hinh_anh"
													class="rounded-3 shadow-sm"
													style="width: 100px; height: 100px; object-fit: cover;" alt="">
											</div>
											<div class="restaurant-details">
												<h5 class="mb-2">{{ value.ten_quan_an }}</h5>
												<p class="text-muted mb-1">
													<i class="bi bi-geo-alt me-1"></i>
													{{ value.dia_chi_quan }}
												</p>
												<div class="d-flex align-items-center gap-3">
													<span class="text-muted small">
														<i class="bi bi-clock-history me-1"></i>
														2 giờ trước
													</span>
												</div>
											</div>
										</div>
										<div class="delivery-info bg-light rounded-4 p-3 mb-4">
											<div class="d-flex align-items-center">
												<div class="customer-avatar me-3">
													<img :src="value.avatar"
														class="rounded-circle shadow-sm"
														style="width: 50px; height: 50px; object-fit: cover;" alt="">
												</div>
												<div class="customer-info">
													<h6 class="mb-1">{{ value.ten_nguoi_nhan }}</h6>
													<p class="text-muted mb-0 small">
														<i class="bi bi-geo-alt me-1"></i>
														{{ value.dia_chi_khach }}
													</p>
												</div>
											</div>
										</div>

										<div class="delivery-timeline mb-4">
											<div class="progress" style="height: 3px;">
												<div class="progress-bar bg-success" role="progressbar"
													style="width: 100%">
												</div>
											</div>
											<div class="d-flex justify-content-between mt-3">
												<div class="timeline-point completed">
													<div class="point-icon">
														<i class="bi bi-check-circle-fill"></i>
													</div>
													<div class="point-label">Nhận đơn</div>
												</div>
												<div class="timeline-point completed">
													<div class="point-icon">
														<i class="bi bi-check-circle-fill"></i>
													</div>
													<div class="point-label">Lấy hàng</div>
												</div>
												<div class="timeline-point completed">
													<div class="point-icon">
														<i class="bi bi-check-circle-fill"></i>
													</div>
													<div class="point-label">Giao hàng</div>
												</div>
												<div class="timeline-point completed">
													<div class="point-icon">
														<i class="bi bi-check-circle-fill"></i>
													</div>
													<div class="point-label">Hoàn thành</div>
												</div>
											</div>
										</div>
										<div class="order-summary bg-light rounded-4 p-3">
											<div class="row g-3">
												<div class="col-4">
													<div class="text-center">
														<div class="text-muted small mb-1">Giá trị đơn hàng</div>
														<div class="fw-bold text-success">85.000đ</div>
													</div>
												</div>
												<div class="col-4">
													<div class="text-center">
														<div class="text-muted small mb-1">Phí ship</div>
														<div class="fw-bold text-primary">25.000đ</div>
													</div>
												</div>
												<div class="col-4">
													<div class="text-center">
														<div class="text-muted small mb-1">Thanh toán</div>
														<div class="fw-bold">Đã thanh toán</div>
													</div>
												</div>
											</div>
										</div>
									</div>
									<div class="card-footer bg-white border-top-0 p-3">
										<button class="btn btn-outline-primary w-100">
											<i class="bi bi-eye me-2"></i>
											Xem chi tiết đơn hàng
										</button>
									</div>
								</div>
							</div>
						</template>
					</div>
				</div>
			</div>
		</div>
		<!-- Modal -->
		<div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
			<div class="modal-dialog">
				<div class="modal-content">
					<div class="modal-header">
						<h1 class="modal-title fs-5" id="exampleModalLabel">Nhận Đơn Hàng</h1>
						<button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
					</div>
					<div class="modal-body">
						<div class="alert alert-primary border-0 bg-primary alert-dismissible fade show py-2 mb-0">
							<div class="d-flex align-items-center">
								<div class="font-35 text-light"><i class="bx bx-info-circle"></i>
								</div>
								<div class="ms-3">
									<h6 class="mb-0 text-light">Cảnh Báo</h6>
									<div class="text-light">Bạn Có chắn chắc muốn nhận đơn hàng này không?</div>
								</div>
							</div>
						</div>
					</div>
					<div class="modal-footer">
						<button type="button" class="btn btn-danger" data-bs-dismiss="modal">Hủy</button>
						<button v-on:click="nhanDon()" type="button" data-bs-dismiss="modal" class="btn btn-primary">Xác
							Nhận</button>
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
			list_don_hang_co_the_nhan: [],
			list_don_dang_giao: [],
			list_don_da_giao: [],
			don_hang: {},
		}
	},
	mounted() {
		this.loadData();
		this.loadDonDangGiao();
	},
	methods: {
		formatVND(number) {
			return new Intl.NumberFormat('vi-VI', { style: 'currency', currency: 'VND' }).format(number,)
		},
		loadDonDangGiao() {
			axios
				.get("http://127.0.0.1:8000/api/shipper/don-hang/data-dang-giao", {
					headers: {
						Authorization: "Bearer " + localStorage.getItem("shipper_login"),
					},
				})
				.then((res) => {
					this.list_don_dang_giao = res.data.data;
					this.list_don_da_giao 	= res.data.list_don_hang_hoan_thanh;
				})
				.catch((res) => {
					const list = Object.values(res.response.data.errors);
					list.forEach((v, i) => {
						this.$toast.error(v[0]);
					});
				})
		},
		loadData() {
			axios
				.get("http://127.0.0.1:8000/api/shipper/don-hang/data", {
					headers: {
						Authorization: "Bearer " + localStorage.getItem("shipper_login"),
					},
				})
				.then((res) => {
					this.list_don_hang_co_the_nhan = res.data.list_don_hang_co_the_nhan;
				})
				.catch((res) => {
					const list = Object.values(res.response.data.errors);
					list.forEach((v, i) => {
						this.$toast.error(v[0]);
					});
				})
		},
		daGiao(payload) {
			axios
				.post("http://127.0.0.1:8000/api/shipper/don-hang/hoan-thanh", payload, {
					headers: {
						Authorization: "Bearer " + localStorage.getItem("shipper_login"),
					},
				})
				.then((res) => {
					if (res.data.status) {
						this.$toast.success(res.data.message);
						this.loadDonDangGiao();
					}
					else {
						this.$toast.error(res.data.message);
					}
				})
				.catch((res) => {
					const list = Object.values(res.response.data.errors);
					list.forEach((v, i) => {
						this.$toast.error(v[0]);
					});
				})
		},
		nhanDon() {
			axios
				.post("http://127.0.0.1:8000/api/shipper/don-hang/nhan-don", this.don_hang, {
					headers: {
						Authorization: "Bearer " + localStorage.getItem("shipper_login"),
					},
				})
				.then((res) => {
					if (res.data.status) {
						this.$toast.success(res.data.message);
						this.loadData();
						this.loadDonDangGiao();
					}
					else {
						this.$toast.error(res.data.message);
					}
				})
				.catch((res) => {
					const list = Object.values(res.response.data.errors);
					list.forEach((v, i) => {
						this.$toast.error(v[0]);
					});
				})
		}
	},
}	
</script>
<style></style>
