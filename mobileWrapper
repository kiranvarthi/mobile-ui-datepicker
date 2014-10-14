// Mobile Device Check
function MobileDeviceCheck() {
    var mobileFlag = false;
    var isMobile = window.matchMedia("only screen and (max-width: 768px)");
    if ($(window).innerWidth() < 768 || (/Android|webOS|iPhone|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent))) {
        mobileFlag = true;
    }
    return mobileFlag;
}

// Device Specific Configurations
function datepickerWrapper(id) {

    // Check the Client Device
    var mobileFlag = MobileDeviceCheck();
    var numberOfMonths = 2;
    var showButtonPanel = false;
    var showOn = "both";

    // Load Device Specific Date Pickers
    if (mobileFlag == true) {
        numberOfMonths = [12, 1];
        showButtonPanel = true;
        showOn = "both";
        $("#" + id).prop("readonly", true);
    }

    // Configure Datepicker Default
    var dtPickerDefaultSettings = {
           showButtonPanel: showButtonPanel,
           showOn: showOn,
           numberOfMonths: numberOfMonths,
           buttonText: "Select",
           buttonImageOnly: false,
    };

    // Load Datepicker
    if ($("#" + id).length > 0) { $("#" + id).datepicker(
        dtPickerDefaultSettings
    );}

}
