<template>
    <div>
        <Menu/>
        <div class="container">
            <h1 class="m0">Voucher</h1>
            <div class="row">
                <div class="col">
                    <p class="mt5 mb20 tc-green">Manage your voucher promotion</p>
                </div>
                <div class="col flex">
                    <router-link to="/add-voucher">
                        <button class="bt-green">+ Add Voucher</button>
                    </router-link>
                </div>
            </div>
            <div class="row bg-blue mt10 p10">
                <div class="col">
                    <input
                        class="search-field"
                        type="text"
                        id="deskripsi"
                        placeholder="Tambah deskripsi..."
                    />
                </div>
                <div class="col flex">
                    <button class="bt-blue">Filter</button>
                </div>
            </div>
            <div class="mt50">
                <table>
                    <thead>
                        <tr>
                            <th>CODE VOUCHER</th>
                            <th>VOUCHER NAME</th>
                            <th>VALID FROM</th>
                            <th>VALID UNTILL</th>
                            <th>VOUCHER STATUS</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr v-for="item of list_voucher" :key="item.id">
                            <td class="center">{{ item.code_voucher }}</td>
                            <td class="center">{{ item.voucher_name }}</td>
                            <td class="center">{{ item.valid_from }}</td>
                            <td class="center">{{ item.valid_until }}</td>
                            <td class="center">
                                <div v-if="item.isVoucherInactive">
                                 <label class="label-green">Active</label>
                                </div>
                                <div v-else>
                                <label class="label-blue">Inactive</label>
                                </div>
                            </td>
                            <td class="center">
                                <div class="mt5">
                                    <router-link to="/add-voucher">
                                        <img src="../../assets/icons/detail.svg">
                                    </router-link>
                                </div>
                                <div class="mt5">
                                    <router-link to="/edit-voucher">
                                        <img src="../../assets/icons/edit.svg">
                                    </router-link>
                                </div>
                                <div class="mt5">
                                    <img src="../../assets/icons/delete.svg">
                                </div>
                            </td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
    </div>
</template>

<script>
import Menu from "../../components/menu.vue"

export default {
	name: 'list-voucher',
	components: {
		Menu
	},
    data(){
        return {
            list_voucher: [
                {
                    id: "1",
                    code_voucher: "CERIA1",
                    voucher_name: "PROMO",
                    valid_from: "2020-06-01",
                    valid_until: "2021-06-01",
                    isVoucherInactive: " ",
                   // role: 1
                },
                {
                    id: "2",
                    code_voucher: "CERIA2",
                    voucher_name: "PROMO",
                    valid_from: "2021-06-21",
                    valid_until: "2026-06-22",
                    isVoucherInactive: " ",
                    //role: 2
                },
            ]
        }
    },
    computed:{
        list_voucher_with_status() {
      const currentDate = new Date();
      return this.list_voucher.map((item) => {
        const validFrom = new Date(item.valid_from);
        const validUntil = new Date(item.valid_until);
        const isVoucherInactive= currentDate < validFrom || currentDate > validUntil;
        return {
            item,
          isVoucherInactive: isVoucherInactive,
        };
    });
},
},
};
</script>