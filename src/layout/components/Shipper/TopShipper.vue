<template>
	<div class="topbar d-flex align-items-center">
		<nav class="navbar navbar-expand">
			<div class="topbar-logo-header">
				<div class="">
					<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS8Qs5Fh70n2MpVMZYjJy5R3DuZusdWCzAckA&s"
						class="logo-icon" alt="logo icon">
				</div>
				<div class="">
					<h4 class="logo-text text-danger">FoodZone</h4>
				</div>
			</div>
			<div class="mobile-toggle-menu"><i class='bx bx-menu'></i></div>
			<div class="search-bar flex-grow-1">
				<div class="position-relative search-bar-box">
					<input type="text" class="form-control search-control" placeholder="Tìm Kiếm?">
					<span class="position-absolute top-50 search-show translate-middle-y"><i
							class='bx bx-search'></i></span>
					<span class="position-absolute top-50 search-close translate-middle-y"><i
							class='bx bx-x'></i></span>
				</div>
			</div>
			<div class="top-menu ms-auto">
				<ul class="navbar-nav align-items-center">
					<li class="nav-item mobile-search-icon">
						<a class="nav-link" href="#"> <i class='bx bx-search'></i>
						</a>
					</li>
					<li class="nav-item dropdown dropdown-large">
						<a class="nav-link dropdown-toggle dropdown-toggle-nocaret" href="#" role="button"
							data-bs-toggle="dropdown" aria-expanded="false"> <i class='bx bx-category'></i>
						</a>
						<div class="dropdown-menu dropdown-menu-end">
							<div class="row row-cols-3 g-3 p-3">
								<div class="col text-center">
									<div class="app-box mx-auto bg-gradient-cosmic text-white"><i
											class='bx bx-group'></i>
									</div>
									<div class="app-title">Teams</div>
								</div>
								<div class="col text-center">
									<div class="app-box mx-auto bg-gradient-burning text-white"><i
											class='bx bx-atom'></i>
									</div>
									<div class="app-title">Projects</div>
								</div>
								<div class="col text-center">
									<div class="app-box mx-auto bg-gradient-lush text-white"><i
											class='bx bx-shield'></i>
									</div>
									<div class="app-title">Tasks</div>
								</div>
								<div class="col text-center">
									<div class="app-box mx-auto bg-gradient-kyoto text-dark"><i
											class='bx bx-notification'></i>
									</div>
									<div class="app-title">Feeds</div>
								</div>
								<div class="col text-center">
									<div class="app-box mx-auto bg-gradient-blues text-dark"><i class='bx bx-file'></i>
									</div>
									<div class="app-title">Files</div>
								</div>
								<div class="col text-center">
									<div class="app-box mx-auto bg-gradient-moonlit text-white"><i
											class='bx bx-filter-alt'></i>
									</div>
									<div class="app-title">Alerts</div>
								</div>
							</div>
						</div>
					</li>
				</ul>
			</div>
			<div class="user-box dropdown">
				<a class="d-flex align-items-center nav-link dropdown-toggle dropdown-toggle-nocaret" href="#"
					role="button" data-bs-toggle="dropdown" aria-expanded="false">
					<img src="https://cdn.iconscout.com/icon/free/png-256/free-avatar-icon-download-in-svg-png-gif-file-formats--user-boy-avatars-flat-icons-pack-people-456322.png"
						class="user-img" alt="user avatar">
					<div class="user-info ps-3">
						<p class="user-name mb-0">{{ ho_ten }}</p>
						<p class="designattion mb-0">Shipper</p>
					</div>
				</a>
				<ul class="dropdown-menu dropdown-menu-end">
					<li>
						<router-link to="/shipper/profile">
							<a class="dropdown-item" href="/shipper/profile"><i
									class="bx bx-user"></i><span>Profile</span></a>
						</router-link>
					</li>
					<li><a v-on:click="logout()" class="dropdown-item" href="javascript:;"><i
								class='bx bx-log-out-circle'></i><span>Logout</span></a>
					</li>
					<li><a v-on:click="logoutAll()" class="dropdown-item" href="javascript:;"><i
								class='bx bx-log-out-circle'></i><span>Logout All</span></a>
					</li>
				</ul>
			</div>
		</nav>
	</div>
</template>
<script>
import axios from 'axios';

export default {
	data() {
		return {
			ho_ten: localStorage.getItem('ho_ten_shipper')
		}
	},
	methods: {
		logout() {
			axios
				.get('http://127.0.0.1:8000/api/shipper/dang-xuat', {
					headers: {
						Authorization: "Bearer " + localStorage.getItem("shipper_login"),
					},
				})
				.then(res => {
					if (res.data.status) {
						this.$toast.success(res.data.message);
						localStorage.removeItem('shipper_login');
						this.$router.push('/shipper/dang-nhap');
					} else {
						this.$toast.error(res.data.message);
					}
				})
				.catch(res => {
					const list = Object.values(res.res.data.errors);
					list.forEach((v, i) => {
						this.$toast.error(v[0]);
					});
				});
		},
		logoutAll() {
			axios
				.get('http://127.0.0.1:8000/api/shipper/dang-xuat-tat-ca', {
					headers: {
						Authorization: "Bearer " + localStorage.getItem("shipper_login"),
					},
				})
				.then(res => {
					if (res.data.status) {
						this.$toast.success(res.data.message);
						localStorage.removeItem('shipper_login');
						this.$router.push('/shipper/dang-nhap');
					} else {
						this.$toast.error(res.data.message);
					}
				})
				.catch(res => {
					const list = Object.values(res.res.data.errors);
					list.forEach((v, i) => {
						this.$toast.error(v[0]);
					});
				});
		},
	}
}
</script>
<style></style>