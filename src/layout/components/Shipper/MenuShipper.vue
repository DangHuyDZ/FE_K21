<template>
	<div class="nav-container primary-menu">
		<div class="mobile-topbar-header">
			<div>
				<img src="../../../assets/images/logo-icon.png" class="logo-icon" alt="logo icon" />
			</div>
			<div>
				<h4 class="logo-text">Rukada</h4>
			</div>
			<div class="toggle-icon ms-auto"><i class="bx bx-arrow-to-left"></i></div>
		</div>
		<nav class="navbar navbar-expand-xl w-100">
			<ul class="navbar-nav justify-content-start flex-grow-1 gap-1">
				<li class="nav-item">
					<router-link to="/shipper/don-hang">
						<a class="nav-link" href="/shipper/don-hang">
							<div class="parent-icon">
								<i class="fa-regular fa-rectangle-list"></i>
							</div>
							<div class="menu-title">Đơn Hàng</div>
						</a>
					</router-link>
				</li>
				<li class="nav-item">
					<router-link to="/shipper/vi-tri-hien-tai">
						<a class="nav-link" href="/shipper/vi-tri-hien-tai">
							<div class="parent-icon">
								<i class="fa-solid fa-location-dot"></i>
							</div>
							<div class="menu-title">Vị Trí Hiện Tại</div>
						</a>
					</router-link>
				</li>
				<!-- <li class="nav-item">
					<router-link to="/shipper/vi-tien">
						<a class="nav-link" href="/shipper/vi-tien">
							<div class="parent-icon">
								<i class="fa-solid fa-wallet"></i>
							</div>
							<div class="menu-title">Quản Lý Ví</div>
						</a>
					</router-link>
				</li> -->
				<li class="nav-item">
					<router-link to="/shipper/thong-ke">
						<a class="nav-link" href="/shipper/thong-ke">
							<div class="parent-icon">
								<i class="fa-solid fa-wallet"></i>
							</div>
							<div class="menu-title">Thống Kê</div>
						</a>
					</router-link>
				</li>
			</ul>
		</nav>
	</div>
</template>
<script>
export default {};
</script>
<style></style>
