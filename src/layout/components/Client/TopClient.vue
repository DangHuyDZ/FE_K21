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
					<input @keyup="timKiem()"  v-model="noi_dung_tim" type="text" class="form-control search-control" placeholder="Tìm Kiếm?">
					<span class="position-absolute top-50 search-show translate-middle-y"><i
							class='bx bx-search'></i></span>
					<span class="position-absolute top-50 search-close translate-middle-y"><i
							class='bx bx-x'></i></span>
				</div>
			</div>

			<div class="user-box dropdown">
				<a class="d-flex align-items-center nav-link dropdown-toggle dropdown-toggle-nocaret" href="#"
					role="button" data-bs-toggle="dropdown" aria-expanded="false">
					<img :src="avatar ? avatar : 'https://cdn.iconscout.com/icon/free/png-256/free-avatar-icon-download-in-svg-png-gif-file-formats--user-boy-avatars-flat-icons-pack-people-456322.png'"
						class="user-img" alt="user avatar">
					<div class="user-info ps-3">
						<p class="user-name mb-0">{{ ho_ten }}</p>
						<p class="designattion mb-0">Khách Hàng</p>
					</div>
				</a>
				<ul class="dropdown-menu dropdown-menu-end">
					<li>
						<router-link to="/khach-hang/profile">
							<a class="dropdown-item" href="/khach-hang/profile"><i
									class="bx bx-user"></i><span>Profile</span></a>
						</router-link>
					</li>
					<li>
						<a v-on:click="logout()" class="dropdown-item" href="javascript:;"><i
								class='bx bx-log-out-circle'></i><span>Logout</span></a>
					</li>
					<li>
						<a v-on:click="logoutAll()" class="dropdown-item" href="javascript:;"><i
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
			ho_ten: localStorage.getItem('ho_ten_khach_hang'),
			avatar: localStorage.getItem('avatar'),
			noi_dung_tim: '',
			
		}
	},
	methods: {
		timKiem() {
            this.$router.push({
                name: 'name_tim_kiem',
                params: {
                    thong_tin: this.noi_dung_tim,
                }
            });
        },
		logout() {
			axios.get('http://127.0.0.1:8000/api/khach-hang/dang-xuat', {
				headers: {
					Authorization: "Bearer " + localStorage.getItem("khach_hang_login"),
				},
			})
				.then(res => {
					if (res.data.status) {
						this.$toast.success(res.data.message);
						localStorage.removeItem('khach_hang_login');
						this.$router.push('/khach-hang/dang-nhap');
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
			axios.get('http://127.0.0.1:8000/api/khach-hang/dang-xuat-tat-ca', {
				headers: {
					Authorization: "Bearer " + localStorage.getItem("khach_hang_login"),
				},
			})
				.then(res => {
					if (res.data.status) {
						this.$toast.success(res.data.message);
						localStorage.removeItem('khach_hang_login');
						this.$router.push('/khach-hang/dang-nhap');
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