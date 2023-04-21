
BIN      = wrf2017
BIN_DIFF = diffwrf

CC      = cc -Ofast
FC      = ftn -Ofast #-O3 -hfp3
FFLAGS	= -hbyteswapio -dy -hgnu_abi=nf_strerror
# For a faster Fortran compilation on some select routines.
#FAST_COMPILE = -O0
CFLAGS  =
OMP_FLAGS = -DSPEC_SUPPRESS_OPENMP

# LFLAGS	= -hbyteswapio
EXTRA_FLAGS = -I src -I src/netcdf/include -I src/inc -DSPEC -DNDEBUG -DSPEC_LP64 -DSTUBMPI -DSPEC_SUPPRESS_OPENMP
EXTRA_FFLAGS = $(EXTRA_FLAGS) -DDM_PARALLEL -DEM_CORE=1 -DNMM_CORE=0 -DNMM_MAX_DIM=2600 -DCOAMPS_CORE=0 -DDA_CORE=0 -DEXP_CORE=0 -DIWORDSIZE=4 -DDWORDSIZE=8 -DRWORDSIZE=4 -DLWORDSIZE=4 -DNETCDF -DINTIO -DCONFIG_BUF_LEN=32768 -DMAX_DOMAINS_F=21 -DNMM_NEST=0 -DMAX_HISTORY=25 -DNMM_NEST=0 -DMAX_HISTORY=25
EXTRA_CFLAGS = $(EXTRA_FLAGS) -DSPEC_CASE_FLAG -DSPEC_AUTO_BYTEORDER=0x12345678

# CCE   FFLAGS=-hbyteswapio -dy -hgnu_abi=nf_strerror
# CCE     -hbyteswapio is LINK TIME option to handle IO from Big Endian files
# CCE     -dy          compile option so can later link with he missing .o files for diffwrf
# CCE     -gnu_abi=nf_strerror  compile time option to handle Cray Fortran to C argument mismatch
# GNU   FFLAGS=-fconvert=big-endian
# Intel FFLAGS=-convert big_endian

#-w -m literal.pm -DSPEC_AUTO_SUPPRESS_OPENMP

# rate -DSPEC_SUPPRESS_OPENMP
# speed -DSPEC_OPENMP


# For WRF
SOURCES = \
        ESMF_Alarm.F90 \
        ESMF_AlarmClock.F90 \
        ESMF_Base.F90 \
        ESMF_BaseTime.F90 \
        ESMF_Calendar.F90 \
        ESMF_Clock.F90 \
        ESMF_Fraction.F90 \
        ESMF_Mod.F90 \
        ESMF_Stubs.F90 \
        ESMF_Time.F90 \
        ESMF_TimeInterval.F90 \
        Meat.F90 \
        adapt_timestep_em.F90 \
        alloc_2d.c \
        apply_bitmap.c \
        bobrand.c \
        c1f2kb.F90 \
        c1f2kf.F90 \
        c1f3kb.F90 \
        c1f3kf.F90 \
        c1f4kb.F90 \
        c1f4kf.F90 \
        c1f5kb.F90 \
        c1f5kf.F90 \
        c1fgkb.F90 \
        c1fgkf.F90 \
        c1fm1b.F90 \
        c1fm1f.F90 \
        c_code.c \
        cfft1b.F90 \
        cfft1i.F90 \
        cfftmb.F90 \
        cfftmf.F90 \
        cfftmi.F90 \
        cmf2kb.F90 \
        cmf2kf.F90 \
        cmf3kb.F90 \
        cmf3kf.F90 \
        cmf4kb.F90 \
        cmf4kf.F90 \
        cmf5kb.F90 \
        cmf5kf.F90 \
        cmfgkb.F90 \
        cmfgkf.F90 \
        cmfm1b.F90 \
        cmfm1f.F90 \
        collect_on_comm.c \
        cosq1b.F90 \
        cosq1f.F90 \
        cosq1i.F90 \
        cosqb1.F90 \
        cosqf1.F90 \
        cosqmb.F90 \
        cosqmf.F90 \
        cosqmi.F90 \
        couple_or_uncouple_em.F90 \
        d1f2kb.F90 \
        d1f2kf.F90 \
        d1f3kb.F90 \
        d1f3kf.F90 \
        d1f4kb.F90 \
        d1f4kf.F90 \
        d1f5kb.F90 \
        d1f5kf.F90 \
        d1fgkb.F90 \
        d1fgkf.F90 \
        data.c \
        dfft1b.F90 \
        dfft1f.F90 \
        dfft1i.F90 \
        dfftb1.F90 \
        dfftf1.F90 \
        dffti1.F90 \
        dfi.F90 \
        field_routines.F90 \
        flt2ieee.c \
        gbyte.c \
        get_region_center.c \
        grib1_routines.c \
        grib_dec.c \
        grib_enc.c \
        grib_seek.c \
        grib_uthin.c \
        gribgetbds.c \
        gribgetbms.c \
        gribgetgds.c \
        gribgetpds.c \
        gribhdr2file.c \
        gribmap.c \
        gribputbds.c \
        gribputgds.c \
        gribputpds.c \
        gridnav.c \
        hires_timer.c \
        init_dec_struct.c \
        init_gribhdr.c \
        init_modules.F90 \
        init_modules_em.F90 \
        input_wrf.F90 \
        interp_fcn.F90 \
        io_int.F90 \
        io_int_idx.c \
        landread.c \
        ld_dec_lookup.c \
        ld_grib_origctrs.c \
        libmassv.F90 \
        mcsqb1.F90 \
        mcsqf1.F90 \
        mediation_feedback_domain.F90 \
        mediation_force_domain.F90 \
        mediation_integrate.F90 \
        mediation_interp_domain.F90 \
        mediation_wrfmain.F90 \
        misc.c \
        module_advect_em.F90 \
        module_after_all_rk_steps.F90 \
        module_alloc_space_0.F90 \
        module_alloc_space_1.F90 \
        module_alloc_space_2.F90 \
        module_alloc_space_3.F90 \
        module_alloc_space_4.F90 \
        module_alloc_space_5.F90 \
        module_alloc_space_6.F90 \
        module_alloc_space_7.F90 \
        module_alloc_space_8.F90 \
        module_alloc_space_9.F90 \
        module_avgflx_em.F90 \
        module_bc.F90 \
        module_bc_em.F90 \
        module_bc_time_utilities.F90 \
        module_big_step_utilities_em.F90 \
        module_bl_acm.F90 \
        module_bl_boulac.F90 \
        module_bl_camuwpbl_driver.F90 \
        module_bl_fogdes.F90 \
        module_bl_gbmpbl.F90 \
        module_bl_gfs.F90 \
        module_bl_gfs2011.F90 \
        module_bl_gwdo.F90 \
        module_bl_mfshconvpbl.F90 \
        module_bl_mrf.F90 \
        module_bl_myjpbl.F90 \
        module_bl_myjurb.F90 \
        module_bl_mynn.F90 \
        module_bl_qnsepbl.F90 \
        module_bl_qnsepbl09.F90 \
        module_bl_temf.F90 \
        module_bl_ysu.F90 \
        module_cam_bl_diffusion_solver.F90 \
        module_cam_bl_eddy_diff.F90 \
        module_cam_cldwat.F90 \
        module_cam_constituents.F90 \
        module_cam_error_function.F90 \
        module_cam_esinti.F90 \
        module_cam_gffgch.F90 \
        module_cam_molec_diff.F90 \
        module_cam_mp_cldwat2m_micro.F90 \
        module_cam_mp_conv_water.F90 \
        module_cam_mp_microp_aero.F90 \
        module_cam_mp_modal_aero_initialize_data_phys.F90 \
        module_cam_mp_ndrop.F90 \
        module_cam_mp_qneg3.F90 \
        module_cam_mp_radconstants.F90 \
        module_cam_physconst.F90 \
        module_cam_shr_const_mod.F90 \
        module_cam_shr_kind_mod.F90 \
        module_cam_support.F90 \
        module_cam_trb_mtn_stress.F90 \
        module_cam_upper_bc.F90 \
        module_cam_wv_saturation.F90 \
        module_check_a_mundo.F90 \
        module_comm_dm.F90 \
        module_comm_dm_0.F90 \
        module_comm_dm_1.F90 \
        module_comm_dm_2.F90 \
        module_comm_dm_3.F90 \
        module_comm_dm_4.F90 \
        module_comm_nesting_dm.F90 \
        module_configure.F90 \
        module_convtrans_prep.F90 \
        module_cpl.F90 \
        module_cpl_oasis3.F90 \
        module_cu_bmj.F90 \
        module_cu_camzm.F90 \
        module_cu_camzm_driver.F90 \
        module_cu_g3.F90 \
        module_cu_gd.F90 \
        module_cu_gf.F90 \
        module_cu_kf.F90 \
        module_cu_kfeta.F90 \
        module_cu_mesosas.F90 \
        module_cu_nsas.F90 \
        module_cu_osas.F90 \
        module_cu_sas.F90 \
        module_cu_tiedtke.F90 \
        module_cumulus_driver.F90 \
        module_damping_em.F90 \
        module_data_cam_mam_aero.F90 \
        module_data_cam_mam_asect.F90 \
        module_data_gocart_dust.F90 \
        module_date_time.F90 \
        module_diag_afwa.F90 \
        module_diag_afwa_hail.F90 \
        module_diag_cl.F90 \
        module_diag_misc.F90 \
        module_diag_pld.F90 \
        module_diagnostics_driver.F90 \
        module_diffusion_em.F90 \
        module_dm.F90 \
        module_domain.F90 \
        module_domain_type.F90 \
        module_driver_constants.F90 \
        module_em.F90 \
        module_fdda_psufddagd.F90 \
        module_fdda_spnudging.F90 \
        module_fddagd_driver.F90 \
        module_fddaobs_driver.F90 \
        module_fddaobs_rtfdda.F90 \
        module_first_rk_step_part1.F90 \
        module_first_rk_step_part2.F90 \
        module_force_scm.F90 \
        module_fr_fire_atm.F90 \
        module_fr_fire_core.F90 \
        module_fr_fire_driver.F90 \
        module_fr_fire_driver_wrf.F90 \
        module_fr_fire_model.F90 \
        module_fr_fire_phys.F90 \
        module_fr_fire_util.F90 \
        module_gfs_funcphys.F90 \
        module_gfs_machine.F90 \
        module_gfs_physcons.F90 \
        module_init_utilities.F90 \
        module_integrate.F90 \
        module_intermediate_nmm.F90 \
        module_internal_header_util.F90 \
        module_interp_store.F90 \
        module_io.F90 \
        module_io_domain.F90 \
        module_io_quilt.F90 \
        module_io_wrf.F90 \
        module_lightning_driver.F90 \
        module_llxy.F90 \
        module_ltng_cpmpr92z.F90 \
        module_ltng_crmpr92.F90 \
        module_ltng_iccg.F90 \
        module_ltng_lpi.F90 \
        module_machine.F90 \
        module_microphysics_driver.F90 \
        module_microphysics_zero_out.F90 \
        module_mixactivate.F90 \
        module_model_constants.F90 \
        module_mp_HWRF.F90 \
        module_mp_cammgmp_driver.F90 \
        module_mp_etanew.F90 \
        module_mp_etaold.F90 \
        module_mp_fast_sbm.F90 \
        module_mp_full_sbm.F90 \
        module_mp_gsfcgce.F90 \
        module_mp_kessler.F90 \
        module_mp_lin.F90 \
        module_mp_milbrandt2mom.F90 \
        module_mp_morr_two_moment.F90 \
        module_mp_nssl_2mom.F90 \
        module_mp_radar.F90 \
        module_mp_sbu_ylin.F90 \
        module_mp_thompson.F90 \
        module_mp_wdm5.F90 \
        module_mp_wdm6.F90 \
        module_mp_wsm3.F90 \
        module_mp_wsm5.F90 \
        module_mp_wsm6.F90 \
        module_nesting.F90 \
        module_optional_input.F90 \
        module_pbl_driver.F90 \
        module_physics_addtendc.F90 \
        module_physics_init.F90 \
        module_polarfft.F90 \
        module_progtm.F90 \
        module_quilt_outbuf_ops.F90 \
        module_ra_HWRF.F90 \
        module_ra_aerosol.F90 \
        module_ra_cam.F90 \
        module_ra_cam_support.F90 \
        module_ra_clWRF_support.F90 \
        module_ra_flg.F90 \
        module_ra_gfdleta.F90 \
        module_ra_goddard.F90 \
        module_ra_gsfcsw.F90 \
        module_ra_hs.F90 \
        module_ra_rrtm.F90 \
        module_ra_sw.F90 \
        module_radiation_driver.F90 \
        module_sf_3dpwp.F90 \
        module_sf_bem.F90 \
        module_sf_bep.F90 \
        module_sf_bep_bem.F90 \
        module_sf_clm.F90 \
        module_sf_fogdes.F90 \
        module_sf_gfdl.F90 \
        module_sf_gfs.F90 \
        module_sf_idealscmsfclay.F90 \
        module_sf_lake.F90 \
        module_sf_myjsfc.F90 \
        module_sf_mynn.F90 \
        module_sf_noah_seaice.F90 \
        module_sf_noah_seaice_drv.F90 \
        module_sf_noahdrv.F90 \
        module_sf_noahlsm.F90 \
        module_sf_noahlsm_glacial_only.F90 \
        module_sf_noahmp_glacier.F90 \
        module_sf_noahmp_groundwater.F90 \
        module_sf_noahmpdrv.F90 \
        module_sf_noahmplsm.F90 \
        module_sf_ocean_driver.F90 \
        module_sf_oml.F90 \
        module_sf_pxlsm.F90 \
        module_sf_pxlsm_data.F90 \
        module_sf_pxsfclay.F90 \
        module_sf_qnsesfc.F90 \
        module_sf_ruclsm.F90 \
        module_sf_scmflux.F90 \
        module_sf_scmskintemp.F90 \
        module_sf_sfcdiags.F90 \
        module_sf_sfcdiags_ruclsm.F90 \
        module_sf_sfclay.F90 \
        module_sf_sfclayrev.F90 \
        module_sf_slab.F90 \
        module_sf_ssib.F90 \
        module_sf_sstskin.F90 \
        module_sf_temfsfclay.F90 \
        module_sf_tmnupdate.F90 \
        module_sf_urban.F90 \
        module_shallowcu_driver.F90 \
        module_shcu_camuwshcu.F90 \
        module_shcu_camuwshcu_driver.F90 \
        module_shcu_grims.F90 \
        module_small_step_em.F90 \
        module_soil_pre.F90 \
        module_solvedebug_em.F90 \
        module_state_description.F90 \
        module_stoch.F90 \
        module_streams.F90 \
        module_surface_driver.F90 \
        module_symbols_util.F90 \
        module_tiles.F90 \
        module_timing.F90 \
        module_utility.F90 \
        module_wind_fitch.F90 \
        module_wrf_error.F90 \
        module_wrf_top.F90 \
        mradb2.F90 \
        mradb3.F90 \
        mradb4.F90 \
        mradb5.F90 \
        mradbg.F90 \
        mradf2.F90 \
        mradf3.F90 \
        mradf4.F90 \
        mradf5.F90 \
        mradfg.F90 \
        mrftb1.F90 \
        mrftf1.F90 \
        mrfti1.F90 \
        msntb1.F90 \
        msntf1.F90 \
        my_strtok.c \
        nest_init_utils.F90 \
        attr.c \
        dim.c \
        error.c \
        fort-attio.c \
        fort-control.c \
        fort-dim.c \
        fort-genatt.c \
        fort-geninq.c \
        fort-genvar.c \
        fort-lib.c \
        fort-misc.c \
        fort-varaio.c \
        libvers.c \
        nc.c \
        ncio.c \
        ncx.c \
        putget.c \
        string.c \
        v1hpg.c \
        v2i.c \
        var.c \
        nl_get_0_routines.F90 \
        nl_get_1_routines.F90 \
        nl_get_2_routines.F90 \
        nl_get_3_routines.F90 \
        nl_get_4_routines.F90 \
        nl_get_5_routines.F90 \
        nl_get_6_routines.F90 \
        nl_get_7_routines.F90 \
        nl_set_0_routines.F90 \
        nl_set_1_routines.F90 \
        nl_set_2_routines.F90 \
        nl_set_6_routines.F90 \
        nl_set_7_routines.F90 \
        output_wrf.F90 \
        pack_spatial.c \
        pack_utils.c \
        period.c \
        r1f2kb.F90 \
        r1f2kf.F90 \
        r1f3kb.F90 \
        r1f3kf.F90 \
        r1f4kb.F90 \
        r1f4kf.F90 \
        r1f5kb.F90 \
        r1f5kf.F90 \
        r1fgkb.F90 \
        r1fgkf.F90 \
        r4_factor.F90 \
        r4_mcfti1.F90 \
        r4_tables.F90 \
        r8_factor.F90 \
        r8_mcfti1.F90 \
        r8_tables.F90 \
        read_grib.c \
        reg_parse.c \
        rfft1b.F90 \
        rfft1f.F90 \
        rfft1i.F90 \
        rfftb1.F90 \
        rfftf1.F90 \
        rffti1.F90 \
        rfftmb.F90 \
        rfftmf.F90 \
        rfftmi.F90 \
        rsl_bcast.c \
        set_bytes.c \
        set_timekeeping.F90 \
        setfeenv.c \
        sint.F90 \
        solve_em.F90 \
        solve_interface.F90 \
        start_domain.F90 \
        start_em.F90 \
        symtab_gen.c \
        task_for_point.c \
        track_driver.F90 \
        track_input.F90 \
        trim.c \
        type.c \
        upd_child_errmsg.c \
        wrf.F90 \
        wrf_bdyin.F90 \
        wrf_bdyout.F90 \
        wrf_debug.F90 \
        wrf_ext_read_field.F90 \
        wrf_ext_write_field.F90 \
        wrf_fddaobs_in.F90 \
        wrf_io.F90 \
        wrf_num_bytes_between.c \
        wrf_shutdown.F90 \
        wrf_timeseries.F90 \
        wrf_tsin.F90 \
        xercon.F90 \
        xerfft.F90 \
        z1f2kb.F90 \
        z1f2kf.F90 \
        z1f3kb.F90 \
        z1f3kf.F90 \
        z1f4kb.F90 \
        z1f4kf.F90 \
        z1f5kb.F90 \
        z1f5kf.F90 \
        z1fgkb.F90 \
        z1fgkf.F90 \
        z1fm1b.F90 \
        z1fm1f.F90 \
        zmf2kb.F90 \
        zmf2kf.F90 \
        zmf3kb.F90 \
        zmf3kf.F90 \
        zmf4kb.F90 \
        zmf4kf.F90 \
        zmf5kb.F90 \
        zmf5kf.F90 \
        zmfgkb.F90 \
        zmfgkf.F90

# For DIFFWRF, not complete, does not include .o's for USE of PARAMETERS only, so not used.
#SOURCES_DIFF_orig = \  #   
SOURCES_DIFF = \
        ESMF_Alarm.F90 \
        ESMF_AlarmClock.F90 \
        ESMF_Base.F90 \
        ESMF_BaseTime.F90 \
        ESMF_Calendar.F90 \
        ESMF_Clock.F90 \
        ESMF_Mod.F90 \
        ESMF_Stubs.F90 \
        ESMF_Time.F90 \
        ESMF_TimeInterval.F90 \
        Meat.F90 \
        adapt_timestep_em.F90 \
        c1f2kb.F90 \
        c1f3kb.F90 \
        c1f4kb.F90 \
        c1f5kb.F90 \
        c1fgkb.F90 \
        c1fm1b.F90 \
        c_code.c \
        cfft1b.F90 \
        cfft1i.F90 \
        collect_on_comm.c \
        couple_or_uncouple_em.F90 \
        data.c \
        diffwrf.F90 \
        field_routines.F90 \
        hires_timer.c \
        input_wrf.F90 \
        interp_fcn.F90 \
        io_int.F90 \
        libmassv.F90 \
        mediation_wrfmain.F90 \
        misc.c \
        module_alloc_space_0.F90 \
        module_alloc_space_1.F90 \
        module_alloc_space_2.F90 \
        module_alloc_space_3.F90 \
        module_alloc_space_4.F90 \
        module_alloc_space_5.F90 \
        module_alloc_space_6.F90 \
        module_alloc_space_7.F90 \
        module_alloc_space_8.F90 \
        module_alloc_space_9.F90 \
        module_avgflx_em.F90 \
        module_bc.F90 \
        module_bc_em.F90 \
        module_bc_time_utilities.F90 \
        module_bl_acm.F90 \
        module_bl_boulac.F90 \
        module_bl_camuwpbl_driver.F90 \
        module_bl_gbmpbl.F90 \
        module_bl_gfs.F90 \
        module_bl_gfs2011.F90 \
        module_bl_mfshconvpbl.F90 \
        module_bl_mrf.F90 \
        module_bl_myjpbl.F90 \
        module_bl_myjurb.F90 \
        module_bl_mynn.F90 \
        module_bl_qnsepbl.F90 \
        module_bl_qnsepbl09.F90 \
        module_bl_temf.F90 \
        module_bl_ysu.F90 \
        module_cam_bl_diffusion_solver.F90 \
        module_cam_bl_eddy_diff.F90 \
        module_cam_cldwat.F90 \
        module_cam_constituents.F90 \
        module_cam_error_function.F90 \
        module_cam_esinti.F90 \
        module_cam_gffgch.F90 \
        module_cam_molec_diff.F90 \
        module_cam_mp_cldwat2m_micro.F90 \
        module_cam_mp_conv_water.F90 \
        module_cam_mp_microp_aero.F90 \
        module_cam_mp_modal_aero_initialize_data_phys.F90 \
        module_cam_mp_ndrop.F90 \
        module_cam_mp_qneg3.F90 \
        module_cam_mp_radconstants.F90 \
        module_cam_physconst.F90 \
        module_cam_support.F90 \
        module_cam_trb_mtn_stress.F90 \
        module_cam_upper_bc.F90 \
        module_cam_wv_saturation.F90 \
        module_comm_dm.F90 \
        module_comm_dm_0.F90 \
        module_comm_dm_1.F90 \
        module_comm_dm_2.F90 \
        module_comm_dm_3.F90 \
        module_comm_dm_4.F90 \
        module_comm_nesting_dm.F90 \
        module_configure.F90 \
        module_cpl.F90 \
        module_cpl_oasis3.F90 \
        module_cu_bmj.F90 \
        module_cu_camzm.F90 \
        module_cu_camzm_driver.F90 \
        module_cu_g3.F90 \
        module_cu_gd.F90 \
        module_cu_kf.F90 \
        module_cu_kfeta.F90 \
        module_cu_mesosas.F90 \
        module_cu_nsas.F90 \
        module_cu_osas.F90 \
        module_cu_sas.F90 \
        module_cu_tiedtke.F90 \
        module_data_cam_mam_aero.F90 \
        module_date_time.F90 \
        module_diag_pld.F90 \
        module_dm.F90 \
        module_domain.F90 \
        module_domain_type.F90 \
        module_driver_constants.F90 \
        module_fdda_psufddagd.F90 \
        module_fdda_spnudging.F90 \
        module_fddaobs_rtfdda.F90 \
        module_fr_fire_atm.F90 \
        module_fr_fire_core.F90 \
        module_fr_fire_driver.F90 \
        module_fr_fire_driver_wrf.F90 \
        module_fr_fire_model.F90 \
        module_fr_fire_phys.F90 \
        module_fr_fire_util.F90 \
        module_gfs_funcphys.F90 \
        module_internal_header_util.F90 \
        module_io.F90 \
        module_io_domain.F90 \
        module_io_quilt.F90 \
        module_io_wrf.F90 \
        module_lightning_driver.F90 \
        module_llxy.F90 \
        module_ltng_cpmpr92z.F90 \
        module_ltng_crmpr92.F90 \
        module_ltng_iccg.F90 \
        module_ltng_lpi.F90 \
        module_machine.F90 \
        module_model_constants.F90 \
        module_mp_cammgmp_driver.F90 \
        module_mp_etanew.F90 \
        module_mp_etaold.F90 \
        module_mp_fast_sbm.F90 \
        module_mp_full_sbm.F90 \
        module_mp_milbrandt2mom.F90 \
        module_mp_morr_two_moment.F90 \
        module_mp_nssl_2mom.F90 \
        module_mp_radar.F90 \
        module_mp_thompson.F90 \
        module_mp_wdm5.F90 \
        module_mp_wdm6.F90 \
        module_mp_wsm3.F90 \
        module_mp_wsm5.F90 \
        module_mp_wsm6.F90 \
        module_physics_init.F90 \
        module_ra_cam.F90 \
        module_ra_cam_support.F90 \
        module_ra_clWRF_support.F90 \
        module_ra_gfdleta.F90 \
        module_ra_gsfcsw.F90 \
        module_ra_hs.F90 \
        module_ra_rrtm.F90 \
        module_ra_sw.F90 \
        module_sf_bem.F90 \
        module_sf_bep.F90 \
        module_sf_bep_bem.F90 \
        module_sf_lake.F90 \
        module_sf_myjsfc.F90 \
        module_sf_mynn.F90 \
        module_sf_noah_seaice.F90 \
        module_sf_noahdrv.F90 \
        module_sf_noahlsm.F90 \
        module_sf_noahlsm_glacial_only.F90 \
        module_sf_noahmp_glacier.F90 \
        module_sf_noahmp_groundwater.F90 \
        module_sf_noahmpdrv.F90 \
        module_sf_noahmplsm.F90 \
        module_sf_oml.F90 \
        module_sf_pxlsm.F90 \
        module_sf_pxlsm_data.F90 \
        module_sf_pxsfclay.F90 \
        module_sf_qnsesfc.F90 \
        module_sf_ruclsm.F90 \
        module_sf_sfclay.F90 \
        module_sf_sfclayrev.F90 \
        module_sf_slab.F90 \
        module_sf_temfsfclay.F90 \
        module_sf_urban.F90 \
        module_shcu_camuwshcu.F90 \
        module_shcu_grims.F90 \
        module_state_description.F90 \
        module_stoch.F90 \
        module_streams.F90 \
        module_symbols_util.F90 \
        module_tiles.F90 \
        module_timing.F90 \
        module_utility.F90 \
        module_wind_fitch.F90 \
        module_wrf_error.F90 \
        mradb2.F90 \
        mradb3.F90 \
        mradb4.F90 \
        mradb5.F90 \
        mradbg.F90 \
        mradf2.F90 \
        mradf3.F90 \
        mradf4.F90 \
        mradf5.F90 \
        mradfg.F90 \
        mrftb1.F90 \
        mrftf1.F90 \
        mrfti1.F90 \
        my_strtok.c \
        attr.c \
        dim.c \
        error.c \
        fort-attio.c \
        fort-control.c \
        fort-dim.c \
        fort-genatt.c \
        fort-geninq.c \
        fort-genvar.c \
        fort-lib.c \
        fort-misc.c \
        fort-varaio.c \
        libvers.c \
        nc.c \
        ncio.c \
        ncx.c \
        putget.c \
        string.c \
        v1hpg.c \
        v2i.c \
        var.c \
        nl_get_0_routines.F90 \
        nl_get_1_routines.F90 \
        nl_get_2_routines.F90 \
        nl_get_3_routines.F90 \
        nl_get_4_routines.F90 \
        nl_get_5_routines.F90 \
        nl_get_6_routines.F90 \
        nl_get_7_routines.F90 \
        nl_set_0_routines.F90 \
        nl_set_1_routines.F90 \
        nl_set_2_routines.F90 \
        nl_set_7_routines.F90 \
        output_wrf.F90 \
        pack_utils.c \
        period.c \
        r4_factor.F90 \
        r4_mcfti1.F90 \
        r4_tables.F90 \
        reg_parse.c \
        rfftmb.F90 \
        rfftmf.F90 \
        rfftmi.F90 \
        rsl_bcast.c \
        sint.F90 \
        start_domain.F90 \
        start_em.F90 \
        symtab_gen.c \
        task_for_point.c \
        track_driver.F90 \
        track_input.F90 \
        type.c \
        wrf_bdyin.F90 \
        wrf_bdyout.F90 \
        wrf_debug.F90 \
        wrf_ext_read_field.F90 \
        wrf_ext_write_field.F90 \
        wrf_io.F90 \
        wrf_num_bytes_between.c \
        wrf_timeseries.F90 \
        wrf_tsin.F90 \
        xercon.F90 \
        xerfft.F90

# Full source list for DIFFWRF.
#SOURCES_DIFF = \  #
SOURCES_DIFF_FULL = \
        ESMF_Alarm.F90 \
        ESMF_AlarmClock.F90 \
        ESMF_Base.F90 \
        ESMF_BaseTime.F90 \
        ESMF_Calendar.F90 \
        ESMF_Clock.F90 \
        ESMF_Fraction.F90 \
        ESMF_Mod.F90 \
        ESMF_Stubs.F90 \
        ESMF_Time.F90 \
        ESMF_TimeInterval.F90 \
        Meat.F90 \
        adapt_timestep_em.F90 \
        alloc_2d.c \
        apply_bitmap.c \
        bobrand.c \
        c1f2kb.F90 \
        c1f2kf.F90 \
        c1f3kb.F90 \
        c1f3kf.F90 \
        c1f4kb.F90 \
        c1f4kf.F90 \
        c1f5kb.F90 \
        c1f5kf.F90 \
        c1fgkb.F90 \
        c1fgkf.F90 \
        c1fm1b.F90 \
        c1fm1f.F90 \
        c_code.c \
        cfft1b.F90 \
        cfft1i.F90 \
        cfftmb.F90 \
        cfftmf.F90 \
        cfftmi.F90 \
        cmf2kb.F90 \
        cmf2kf.F90 \
        cmf3kb.F90 \
        cmf3kf.F90 \
        cmf4kb.F90 \
        cmf4kf.F90 \
        cmf5kb.F90 \
        cmf5kf.F90 \
        cmfgkb.F90 \
        cmfgkf.F90 \
        cmfm1b.F90 \
        cmfm1f.F90 \
        collect_on_comm.c \
        cosq1b.F90 \
        cosq1f.F90 \
        cosq1i.F90 \
        cosqb1.F90 \
        cosqf1.F90 \
        cosqmb.F90 \
        cosqmf.F90 \
        cosqmi.F90 \
        couple_or_uncouple_em.F90 \
        d1f2kb.F90 \
        d1f2kf.F90 \
        d1f3kb.F90 \
        d1f3kf.F90 \
        d1f4kb.F90 \
        d1f4kf.F90 \
        d1f5kb.F90 \
        d1f5kf.F90 \
        d1fgkb.F90 \
        d1fgkf.F90 \
        data.c \
        diffwrf.F90 \
        dfft1b.F90 \
        dfft1f.F90 \
        dfft1i.F90 \
        dfftb1.F90 \
        dfftf1.F90 \
        dffti1.F90 \
        dfi.F90 \
        field_routines.F90 \
        flt2ieee.c \
        gbyte.c \
        get_region_center.c \
        grib1_routines.c \
        grib_dec.c \
        grib_enc.c \
        grib_seek.c \
        grib_uthin.c \
        gribgetbds.c \
        gribgetbms.c \
        gribgetgds.c \
        gribgetpds.c \
        gribhdr2file.c \
        gribmap.c \
        gribputbds.c \
        gribputgds.c \
        gribputpds.c \
        gridnav.c \
        hires_timer.c \
        init_dec_struct.c \
        init_gribhdr.c \
        init_modules.F90 \
        init_modules_em.F90 \
        input_wrf.F90 \
        interp_fcn.F90 \
        io_int.F90 \
        io_int_idx.c \
        landread.c \
        ld_dec_lookup.c \
        ld_grib_origctrs.c \
        libmassv.F90 \
        mcsqb1.F90 \
        mcsqf1.F90 \
        mediation_feedback_domain.F90 \
        mediation_force_domain.F90 \
        mediation_integrate.F90 \
        mediation_interp_domain.F90 \
        mediation_wrfmain.F90 \
        misc.c \
        module_advect_em.F90 \
        module_after_all_rk_steps.F90 \
        module_alloc_space_0.F90 \
        module_alloc_space_1.F90 \
        module_alloc_space_2.F90 \
        module_alloc_space_3.F90 \
        module_alloc_space_4.F90 \
        module_alloc_space_5.F90 \
        module_alloc_space_6.F90 \
        module_alloc_space_7.F90 \
        module_alloc_space_8.F90 \
        module_alloc_space_9.F90 \
        module_avgflx_em.F90 \
        module_bc.F90 \
        module_bc_em.F90 \
        module_bc_time_utilities.F90 \
        module_big_step_utilities_em.F90 \
        module_bl_acm.F90 \
        module_bl_boulac.F90 \
        module_bl_camuwpbl_driver.F90 \
        module_bl_fogdes.F90 \
        module_bl_gbmpbl.F90 \
        module_bl_gfs.F90 \
        module_bl_gfs2011.F90 \
        module_bl_gwdo.F90 \
        module_bl_mfshconvpbl.F90 \
        module_bl_mrf.F90 \
        module_bl_myjpbl.F90 \
        module_bl_myjurb.F90 \
        module_bl_mynn.F90 \
        module_bl_qnsepbl.F90 \
        module_bl_qnsepbl09.F90 \
        module_bl_temf.F90 \
        module_bl_ysu.F90 \
        module_cam_bl_diffusion_solver.F90 \
        module_cam_bl_eddy_diff.F90 \
        module_cam_cldwat.F90 \
        module_cam_constituents.F90 \
        module_cam_error_function.F90 \
        module_cam_esinti.F90 \
        module_cam_gffgch.F90 \
        module_cam_molec_diff.F90 \
        module_cam_mp_cldwat2m_micro.F90 \
        module_cam_mp_conv_water.F90 \
        module_cam_mp_microp_aero.F90 \
        module_cam_mp_modal_aero_initialize_data_phys.F90 \
        module_cam_mp_ndrop.F90 \
        module_cam_mp_qneg3.F90 \
        module_cam_mp_radconstants.F90 \
        module_cam_physconst.F90 \
        module_cam_shr_const_mod.F90 \
        module_cam_shr_kind_mod.F90 \
        module_cam_support.F90 \
        module_cam_trb_mtn_stress.F90 \
        module_cam_upper_bc.F90 \
        module_cam_wv_saturation.F90 \
        module_check_a_mundo.F90 \
        module_comm_dm.F90 \
        module_comm_dm_0.F90 \
        module_comm_dm_1.F90 \
        module_comm_dm_2.F90 \
        module_comm_dm_3.F90 \
        module_comm_dm_4.F90 \
        module_comm_nesting_dm.F90 \
        module_configure.F90 \
        module_convtrans_prep.F90 \
        module_cpl.F90 \
        module_cpl_oasis3.F90 \
        module_cu_bmj.F90 \
        module_cu_camzm.F90 \
        module_cu_camzm_driver.F90 \
        module_cu_g3.F90 \
        module_cu_gd.F90 \
        module_cu_gf.F90 \
        module_cu_kf.F90 \
        module_cu_kfeta.F90 \
        module_cu_mesosas.F90 \
        module_cu_nsas.F90 \
        module_cu_osas.F90 \
        module_cu_sas.F90 \
        module_cu_tiedtke.F90 \
        module_cumulus_driver.F90 \
        module_damping_em.F90 \
        module_data_cam_mam_aero.F90 \
        module_data_cam_mam_asect.F90 \
        module_data_gocart_dust.F90 \
        module_date_time.F90 \
        module_diag_afwa.F90 \
        module_diag_afwa_hail.F90 \
        module_diag_cl.F90 \
        module_diag_misc.F90 \
        module_diag_pld.F90 \
        module_diagnostics_driver.F90 \
        module_diffusion_em.F90 \
        module_dm.F90 \
        module_domain.F90 \
        module_domain_type.F90 \
        module_driver_constants.F90 \
        module_em.F90 \
        module_fdda_psufddagd.F90 \
        module_fdda_spnudging.F90 \
        module_fddagd_driver.F90 \
        module_fddaobs_driver.F90 \
        module_fddaobs_rtfdda.F90 \
        module_first_rk_step_part1.F90 \
        module_first_rk_step_part2.F90 \
        module_force_scm.F90 \
        module_fr_fire_atm.F90 \
        module_fr_fire_core.F90 \
        module_fr_fire_driver.F90 \
        module_fr_fire_driver_wrf.F90 \
        module_fr_fire_model.F90 \
        module_fr_fire_phys.F90 \
        module_fr_fire_util.F90 \
        module_gfs_funcphys.F90 \
        module_gfs_machine.F90 \
        module_gfs_physcons.F90 \
        module_init_utilities.F90 \
        module_integrate.F90 \
        module_intermediate_nmm.F90 \
        module_internal_header_util.F90 \
        module_interp_store.F90 \
        module_io.F90 \
        module_io_domain.F90 \
        module_io_quilt.F90 \
        module_io_wrf.F90 \
        module_lightning_driver.F90 \
        module_llxy.F90 \
        module_ltng_cpmpr92z.F90 \
        module_ltng_crmpr92.F90 \
        module_ltng_iccg.F90 \
        module_ltng_lpi.F90 \
        module_machine.F90 \
        module_microphysics_driver.F90 \
        module_microphysics_zero_out.F90 \
        module_mixactivate.F90 \
        module_model_constants.F90 \
        module_mp_HWRF.F90 \
        module_mp_cammgmp_driver.F90 \
        module_mp_etanew.F90 \
        module_mp_etaold.F90 \
        module_mp_fast_sbm.F90 \
        module_mp_full_sbm.F90 \
        module_mp_gsfcgce.F90 \
        module_mp_kessler.F90 \
        module_mp_lin.F90 \
        module_mp_milbrandt2mom.F90 \
        module_mp_morr_two_moment.F90 \
        module_mp_nssl_2mom.F90 \
        module_mp_radar.F90 \
        module_mp_sbu_ylin.F90 \
        module_mp_thompson.F90 \
        module_mp_wdm5.F90 \
        module_mp_wdm6.F90 \
        module_mp_wsm3.F90 \
        module_mp_wsm5.F90 \
        module_mp_wsm6.F90 \
        module_nesting.F90 \
        module_optional_input.F90 \
        module_pbl_driver.F90 \
        module_physics_addtendc.F90 \
        module_physics_init.F90 \
        module_polarfft.F90 \
        module_progtm.F90 \
        module_quilt_outbuf_ops.F90 \
        module_ra_HWRF.F90 \
        module_ra_aerosol.F90 \
        module_ra_cam.F90 \
        module_ra_cam_support.F90 \
        module_ra_clWRF_support.F90 \
        module_ra_flg.F90 \
        module_ra_gfdleta.F90 \
        module_ra_goddard.F90 \
        module_ra_gsfcsw.F90 \
        module_ra_hs.F90 \
        module_ra_rrtm.F90 \
        module_ra_sw.F90 \
        module_radiation_driver.F90 \
        module_sf_3dpwp.F90 \
        module_sf_bem.F90 \
        module_sf_bep.F90 \
        module_sf_bep_bem.F90 \
        module_sf_clm.F90 \
        module_sf_fogdes.F90 \
        module_sf_gfdl.F90 \
        module_sf_gfs.F90 \
        module_sf_idealscmsfclay.F90 \
        module_sf_lake.F90 \
        module_sf_myjsfc.F90 \
        module_sf_mynn.F90 \
        module_sf_noah_seaice.F90 \
        module_sf_noah_seaice_drv.F90 \
        module_sf_noahdrv.F90 \
        module_sf_noahlsm.F90 \
        module_sf_noahlsm_glacial_only.F90 \
        module_sf_noahmp_glacier.F90 \
        module_sf_noahmp_groundwater.F90 \
        module_sf_noahmpdrv.F90 \
        module_sf_noahmplsm.F90 \
        module_sf_ocean_driver.F90 \
        module_sf_oml.F90 \
        module_sf_pxlsm.F90 \
        module_sf_pxlsm_data.F90 \
        module_sf_pxsfclay.F90 \
        module_sf_qnsesfc.F90 \
        module_sf_ruclsm.F90 \
        module_sf_scmflux.F90 \
        module_sf_scmskintemp.F90 \
        module_sf_sfcdiags.F90 \
        module_sf_sfcdiags_ruclsm.F90 \
        module_sf_sfclay.F90 \
        module_sf_sfclayrev.F90 \
        module_sf_slab.F90 \
        module_sf_ssib.F90 \
        module_sf_sstskin.F90 \
        module_sf_temfsfclay.F90 \
        module_sf_tmnupdate.F90 \
        module_sf_urban.F90 \
        module_shallowcu_driver.F90 \
        module_shcu_camuwshcu.F90 \
        module_shcu_camuwshcu_driver.F90 \
        module_shcu_grims.F90 \
        module_small_step_em.F90 \
        module_soil_pre.F90 \
        module_solvedebug_em.F90 \
        module_state_description.F90 \
        module_stoch.F90 \
        module_streams.F90 \
        module_surface_driver.F90 \
        module_symbols_util.F90 \
        module_tiles.F90 \
        module_timing.F90 \
        module_utility.F90 \
        module_wind_fitch.F90 \
        module_wrf_error.F90 \
        module_wrf_top.F90 \
        mradb2.F90 \
        mradb3.F90 \
        mradb4.F90 \
        mradb5.F90 \
        mradbg.F90 \
        mradf2.F90 \
        mradf3.F90 \
        mradf4.F90 \
        mradf5.F90 \
        mradfg.F90 \
        mrftb1.F90 \
        mrftf1.F90 \
        mrfti1.F90 \
        msntb1.F90 \
        msntf1.F90 \
        my_strtok.c \
        nest_init_utils.F90 \
        attr.c \
        dim.c \
        error.c \
        fort-attio.c \
        fort-control.c \
        fort-dim.c \
        fort-genatt.c \
        fort-geninq.c \
        fort-genvar.c \
        fort-lib.c \
        fort-misc.c \
        fort-varaio.c \
        libvers.c \
        nc.c \
        ncio.c \
        ncx.c \
        putget.c \
        string.c \
        v1hpg.c \
        v2i.c \
        var.c \
        nl_get_0_routines.F90 \
        nl_get_1_routines.F90 \
        nl_get_2_routines.F90 \
        nl_get_3_routines.F90 \
        nl_get_4_routines.F90 \
        nl_get_5_routines.F90 \
        nl_get_6_routines.F90 \
        nl_get_7_routines.F90 \
        nl_set_0_routines.F90 \
        nl_set_1_routines.F90 \
        nl_set_2_routines.F90 \
        nl_set_6_routines.F90 \
        nl_set_7_routines.F90 \
        output_wrf.F90 \
        pack_spatial.c \
        pack_utils.c \
        period.c \
        r1f2kb.F90 \
        r1f2kf.F90 \
        r1f3kb.F90 \
        r1f3kf.F90 \
        r1f4kb.F90 \
        r1f4kf.F90 \
        r1f5kb.F90 \
        r1f5kf.F90 \
        r1fgkb.F90 \
        r1fgkf.F90 \
        r4_factor.F90 \
        r4_mcfti1.F90 \
        r4_tables.F90 \
        r8_factor.F90 \
        r8_mcfti1.F90 \
        r8_tables.F90 \
        read_grib.c \
        reg_parse.c \
        rfft1b.F90 \
        rfft1f.F90 \
        rfft1i.F90 \
        rfftb1.F90 \
        rfftf1.F90 \
        rffti1.F90 \
        rfftmb.F90 \
        rfftmf.F90 \
        rfftmi.F90 \
        rsl_bcast.c \
        set_bytes.c \
        set_timekeeping.F90 \
        setfeenv.c \
        sint.F90 \
        solve_em.F90 \
        solve_interface.F90 \
        start_domain.F90 \
        start_em.F90 \
        symtab_gen.c \
        task_for_point.c \
        track_driver.F90 \
        track_input.F90 \
        trim.c \
        type.c \
        upd_child_errmsg.c \
        wrf_bdyin.F90 \
        wrf_bdyout.F90 \
        wrf_debug.F90 \
        wrf_ext_read_field.F90 \
        wrf_ext_write_field.F90 \
        wrf_fddaobs_in.F90 \
        wrf_io.F90 \
        wrf_num_bytes_between.c \
        wrf_shutdown.F90 \
        wrf_timeseries.F90 \
        wrf_tsin.F90 \
        xercon.F90 \
        xerfft.F90 \
        z1f2kb.F90 \
        z1f2kf.F90 \
        z1f3kb.F90 \
        z1f3kf.F90 \
        z1f4kb.F90 \
        z1f4kf.F90 \
        z1f5kb.F90 \
        z1f5kf.F90 \
        z1fgkb.F90 \
        z1fgkf.F90 \
        z1fm1b.F90 \
        z1fm1f.F90 \
        zmf2kb.F90 \
        zmf2kf.F90 \
        zmf3kb.F90 \
        zmf3kf.F90 \
        zmf4kb.F90 \
        zmf4kf.F90 \
        zmf5kb.F90 \
        zmf5kf.F90 \
        zmfgkb.F90 \
        zmfgkf.F90

TMPOBJ  = $(SOURCES:.c=.o)
TMPOBJ2 = $(TMPOBJ:.f90=.o)
OBJ     = $(TMPOBJ2:.F90=.o)

TMPOBJ_DIFF  = $(SOURCES_DIFF:.c=.o)
TMPOBJ2_DIFF = $(TMPOBJ_DIFF:.f90=.o)
OBJ_DIFF     = $(TMPOBJ2_DIFF:.F90=.o)

VPATH	= src:src/netcdf
.SUFFIXES: .f90 .F90 .c

ifeq ($(MAKECMDGOALS),wrf2017_omp)
BIN       = wrf2017_omp
OMP_FLAGS = -DSPEC_OPENMP
endif


$(BIN):	x$(BIN) $(BIN).execute.script $(BIN_DIFF)
	cp $(BIN).execute.script $(BIN)
x$(BIN): $(OBJ)
	$(FC) $(FFLAGS) -o x$(BIN) $(OBJ) $(LDFLAGS) $(LIBS)

$(BIN_DIFF): $(OBJ_DIFF)
	$(FC) $(FFLAGS) -o $(BIN_DIFF) $(OBJ_DIFF) $(LDFLAGS) $(LIBS)

.c.o:
	$(CC) -c -o $@ $(EXTRA_CFLAGS) $(OMP_FLAGS) $(CFLAGS) $<

.f.o:
	$(FC) -c -o $@ $(EXTRA_FFLAGS) $(OMP_FLAGS) $(FFLAGS) $<

.f90.o:
	$(FC) -c -o $@ $(EXTRA_FFLAGS) $(OMP_FLAGS) $(FFLAGS) $<

.F90.o:
	$(FC) -c -o $@ $(EXTRA_FFLAGS) $(OMP_FLAGS) $(FFLAGS) $<

module_alloc_space_0.o: module_alloc_space_0.F90
	$(FC) -c -o $@ $(EXTRA_FFLAGS) $(OMP_FLAGS) $(FFLAGS) $(FAST_COMPILE) $<

module_alloc_space_1.o: module_alloc_space_1.F90
	$(FC) -c -o $@ $(EXTRA_FFLAGS) $(OMP_FLAGS) $(FFLAGS) $(FAST_COMPILE) $<

module_alloc_space_2.o: module_alloc_space_2.F90
	$(FC) -c -o $@ $(EXTRA_FFLAGS) $(OMP_FLAGS) $(FFLAGS) $(FAST_COMPILE) $<

module_alloc_space_3.o: module_alloc_space_3.F90
	$(FC) -c -o $@ $(EXTRA_FFLAGS) $(OMP_FLAGS) $(FFLAGS) $(FAST_COMPILE) $<

module_alloc_space_4.o: module_alloc_space_4.F90
	$(FC) -c -o $@ $(EXTRA_FFLAGS) $(OMP_FLAGS) $(FFLAGS) $(FAST_COMPILE) $<

module_alloc_space_5.o: module_alloc_space_5.F90
	$(FC) -c -o $@ $(EXTRA_FFLAGS) $(OMP_FLAGS) $(FFLAGS) $(FAST_COMPILE) $<

module_alloc_space_6.o: module_alloc_space_6.F90
	$(FC) -c -o $@ $(EXTRA_FFLAGS) $(OMP_FLAGS) $(FFLAGS) $(FAST_COMPILE) $<

module_alloc_space_7.o: module_alloc_space_7.F90
	$(FC) -c -o $@ $(EXTRA_FFLAGS) $(OMP_FLAGS) $(FFLAGS) $(FAST_COMPILE) $<

module_alloc_space_8.o: module_alloc_space_8.F90
	$(FC) -c -o $@ $(EXTRA_FFLAGS) $(OMP_FLAGS) $(FFLAGS) $(FAST_COMPILE) $<

module_alloc_space_9.o: module_alloc_space_9.F90
	$(FC) -c -o $@ $(EXTRA_FFLAGS) $(OMP_FLAGS) $(FFLAGS) $(FAST_COMPILE) $<

module_dm.o: module_dm.F90
	$(FC) -c -o $@ $(EXTRA_FFLAGS) $(OMP_FLAGS) $(FFLAGS) $(FAST_COMPILE) $<

module_configure.o: module_configure.F90
	$(FC) -c -o $@ $(EXTRA_FFLAGS) $(OMP_FLAGS) $(FFLAGS) $(FAST_COMPILE) $<

module_domain.o: module_domain.F90
	$(FC) -c -o $@ $(EXTRA_FFLAGS) $(OMP_FLAGS) $(FFLAGS) $(FAST_COMPILE) $<

module_first_rk_step_part1.o: module_first_rk_step_part1.F90
	$(FC) -c -o $@ $(EXTRA_FFLAGS) $(OMP_FLAGS) $(FFLAGS) $(FAST_COMPILE) $<

clean:
	-rm -f core
	-rm -f $(OBJ) $(OBJ_DIFF) *.mod

clobber: clean
	-rm -f $(BIN) x$(BIN) $(BIN)_omp x$(BIN)_omp $(BIN_DIFF)
	-rm -f control namelist.input namelist.output *_DATA *.TBL *.TBLa OBS_DOMAIN* co2_trans
	-rm -f ozone*formatted grib* tr49* tr67* wrf*_d01 wrfout_d01* wrf.out

ESMF_Alarm.o: \
   ESMF_Base.o \
   ESMF_Time.o \
   ESMF_TimeInterval.o 

ESMF_AlarmClock.o: \
   ESMF_Alarm.o \
   ESMF_Clock.o \
   ESMF_Time.o \
   ESMF_TimeInterval.o 

ESMF_BaseTime.o: \
   ESMF_Base.o 

ESMF_Calendar.o: \
   ESMF_Base.o  \
   ESMF_BaseTime.o 

ESMF_Clock.o: \
   ESMF_Alarm.o \
   ESMF_Base.o \
   ESMF_Time.o \
   ESMF_TimeInterval.o 

ESMF_Mod.o: \
    ESMF_Alarm.o \
    ESMF_AlarmClock.o \
    ESMF_Base.o \
    ESMF_BaseTime.o \
    ESMF_Calendar.o \
    ESMF_Clock.o \
    ESMF_Fraction.o \
    ESMF_Stubs.o \
    ESMF_Time.o \
    ESMF_TimeInterval.o 

ESMF_Stubs.o: \
    ESMF_Base.o \
    ESMF_Calendar.o 

ESMF_Time.o: \
    ESMF_Base.o \
    ESMF_BaseTime.o \
    ESMF_Calendar.o \
    ESMF_Stubs.o \
    ESMF_TimeInterval.o 

ESMF_TimeInterval.o: \
    ESMF_Base.o \
    ESMF_BaseTime.o \
    ESMF_Calendar.o \
    ESMF_Fraction.o 

Meat.o: \
    ESMF_Alarm.o \
    ESMF_Base.o \
    ESMF_BaseTime.o \
    ESMF_Calendar.o \
    ESMF_Clock.o \
    ESMF_Fraction.o \
    ESMF_Time.o \
    ESMF_TimeInterval.o 

adapt_timestep_em.o: \
    module_bc_em.o \
    module_configure.o \
    module_dm.o \
    module_domain.o 

couple_or_uncouple_em.o: \
    module_bc.o \
    module_comm_dm.o \
    module_configure.o \
    module_dm.o \
    module_domain.o \
    module_driver_constants.o \
    module_machine.o \
    module_state_description.o \
    module_tiles.o 

dfi.o: \
    module_comm_dm.o \
    module_configure.o \
    module_dm.o \
    module_domain.o \
    module_driver_constants.o \
    module_io_domain.o \
    module_machine.o \
    module_model_constants.o \
    module_state_description.o \
    module_utility.o 

diffwrf.o: \
    wrf_io.o 

f_xpose.o: \
    f_pack.o 

field_routines.o: \
    wrf_io.o 

init_modules.o: \
    io_int.o \
    module_bc.o \
    module_configure.o \
    module_dm.o \
    module_domain.o \
    module_driver_constants.o \
    module_io.o \
    module_io_quilt.o \
    module_io_wrf.o \
    module_machine.o \
    module_model_constants.o \
    module_nesting.o \
    module_tiles.o \
    module_timing.o \
    module_wrf_error.o 

input_wrf.o: \
    module_bc_time_utilities.o \
    module_configure.o \
    module_date_time.o \
    module_domain.o \
    module_io.o \
    module_io_wrf.o \
    module_state_description.o \
    module_utility.o 

interp_domain_em.o: \
    module_configure.o \
    module_domain.o \
    module_state_description.o 

interp_fcn.o: \
    module_configure.o \
    module_dm.o \
    module_interp_store.o \
    module_model_constants.o \
    module_state_description.o \
    module_timing.o \
    module_wrf_error.o 

io_int.o: \
    module_internal_header_util.o 

mediation_feedback_domain.o: \
    module_configure.o \
    module_dm.o \
    module_domain.o \
    module_intermediate_nmm.o \
    module_timing.o 

mediation_force_domain.o: \
    module_configure.o \
    module_domain.o \
    module_intermediate_nmm.o \
    module_timing.o 

mediation_integrate.o: \
    module_bc_time_utilities.o \
    module_configure.o \
    module_date_time.o \
    module_dm.o \
    module_domain.o \
    module_io_domain.o \
    module_model_constants.o \
    module_state_description.o \
    module_streams.o \
    module_timing.o \
    module_utility.o 

mediation_interp_domain.o: \
    module_configure.o \
    module_domain.o \
    module_timing.o 

mediation_nest_move.o: \
    module_compute_geop.o \
    module_configure.o \
    module_dm.o \
    module_domain.o \
    module_driver_constants.o \
    module_model_constants.o \
    module_state_description.o \
    module_streams.o \
    module_timing.o \
    module_utility.o 

mediation_wrfmain.o: \
    module_bc_time_utilities.o \
    module_configure.o \
    module_domain.o \
    module_io.o \
    module_io_domain.o \
    module_timing.o \
    module_utility.o 

module_advect_em.o: \
    module_bc.o \
    module_model_constants.o \
    module_wrf_error.o 

module_after_all_rk_steps.o: \
    module_comm_dm.o \
    module_configure.o \
    module_diagnostics_driver.o \
    module_dm.o \
    module_domain.o \
    module_state_description.o 

module_alloc_space_0.o: \
    module_configure.o \
    module_domain_type.o 

module_alloc_space_1.o: \
    module_configure.o \
    module_domain_type.o 

module_alloc_space_2.o: \
    module_configure.o \
    module_domain_type.o 

module_alloc_space_3.o: \
    module_configure.o \
    module_domain_type.o 

module_alloc_space_4.o: \
    module_configure.o \
    module_domain_type.o 

module_alloc_space_5.o: \
    module_configure.o \
    module_domain_type.o 

module_alloc_space_6.o: \
    module_configure.o \
    module_domain_type.o 

module_alloc_space_7.o: \
    module_configure.o \
    module_domain_type.o 

module_alloc_space_8.o: \
    module_configure.o \
    module_domain_type.o 

module_alloc_space_9.o: \
    module_configure.o \
    module_domain_type.o 

module_avgflx_em.o: \
    module_bc.o \
    module_model_constants.o \
    module_wrf_error.o 

module_bc.o: \
    module_configure.o \
    module_model_constants.o \
    module_state_description.o \
    module_wrf_error.o 

module_bc_em.o: \
    module_bc.o \
    module_configure.o \
    module_wrf_error.o 

module_bc_time_utilities.o: \
    module_utility.o 

module_big_step_utilities_em.o: \
    module_configure.o \
    module_llxy.o \
    module_model_constants.o \
    module_state_description.o \
    module_wrf_error.o 

module_bl_camuwpbl_driver.o: \
    module_cam_bl_diffusion_solver.o \
    module_cam_bl_eddy_diff.o \
    module_cam_constituents.o \
    module_cam_molec_diff.o \
    module_cam_physconst.o \
    module_cam_shr_kind_mod.o \
    module_cam_support.o \
    module_cam_trb_mtn_stress.o \
    module_cam_wv_saturation.o \
    module_data_cam_mam_aero.o \
    module_model_constants.o 

module_bl_fogdes.o: \
    module_bl_mynn.o \
    module_model_constants.o 

module_bl_gbmpbl.o: \
    module_model_constants.o 

module_bl_gfs.o: \
    module_gfs_machine.o \
    module_gfs_physcons.o 

module_bl_gfs2011.o: \
    module_gfs_machine.o \
    module_gfs_physcons.o 

module_bl_mfshconvpbl.o: \
    module_model_constants.o 

module_bl_myjpbl.o: \
    module_model_constants.o 

module_bl_myjurb.o: \
    module_model_constants.o 

module_bl_mynn.o: \
    module_model_constants.o \
    module_state_description.o 

module_bl_qnsepbl.o: \
    module_model_constants.o 

module_bl_qnsepbl09.o: \
    module_model_constants.o 

module_cam_bl_diffusion_solver.o: \
    module_cam_support.o 

module_cam_bl_eddy_diff.o: \
    module_cam_bl_diffusion_solver.o \
    module_cam_support.o 

module_cam_cldwat.o: \
    module_cam_physconst.o \
    module_cam_shr_kind_mod.o \
    module_cam_support.o \
    module_cam_wv_saturation.o 

module_cam_constituents.o: \
    module_cam_physconst.o \
    module_cam_shr_kind_mod.o \
    module_cam_support.o 

module_cam_esinti.o: \
    module_cam_shr_kind_mod.o \
    module_cam_wv_saturation.o 

module_cam_gffgch.o: \
    module_cam_physconst.o \
    module_cam_shr_kind_mod.o \
    module_cam_support.o 

module_cam_infnan.o: \
    module_cam_shr_kind_mod.o 

module_cam_molec_diff.o: \
    module_cam_constituents.o \
    module_cam_support.o \
    module_cam_upper_bc.o 

module_cam_mp_cldwat2m_micro.o: \
    module_cam_physconst.o \
    module_cam_shr_kind_mod.o \
    module_cam_support.o \
    module_cam_wv_saturation.o 

module_cam_mp_conv_water.o: \
    module_cam_constituents.o \
    module_cam_physconst.o \
    module_cam_shr_kind_mod.o \
    module_cam_support.o 

module_cam_mp_microp_aero.o: \
    module_cam_constituents.o \
    module_cam_error_function.o \
    module_cam_mp_ndrop.o \
    module_cam_physconst.o \
    module_cam_shr_kind_mod.o \
    module_cam_support.o \
    module_cam_wv_saturation.o \
    module_data_cam_mam_aero.o 

module_cam_mp_modal_aero_initialize_data_phys.o: \
    module_data_cam_mam_aero.o 

module_cam_mp_ndrop.o: \
    module_cam_constituents.o \
    module_cam_error_function.o \
    module_cam_physconst.o \
    module_cam_shr_kind_mod.o \
    module_cam_support.o \
    module_cam_wv_saturation.o \
    module_data_cam_mam_aero.o 

module_cam_mp_qneg3.o: \
    module_cam_shr_kind_mod.o \
    module_cam_support.o 

module_cam_mp_radconstants.o: \
    module_cam_shr_kind_mod.o \
    module_cam_support.o 

module_cam_physconst.o: \
    module_cam_shr_const_mod.o \
    module_cam_shr_kind_mod.o 

module_cam_shr_const_mod.o: \
    module_cam_shr_kind_mod.o 

module_cam_support.o: \
    module_cam_shr_kind_mod.o \
    module_state_description.o \
    module_wrf_error.o 

module_cam_trb_mtn_stress.o: \
    module_cam_shr_kind_mod.o \
    module_cam_support.o 

module_cam_upper_bc.o: \
    module_cam_constituents.o \
    module_cam_shr_kind_mod.o \
    module_cam_support.o 

module_cam_wv_saturation.o: \
    module_cam_gffgch.o \
    module_cam_shr_kind_mod.o \
    module_cam_support.o \
    module_wrf_error.o 

module_check_a_mundo.o: \
    module_configure.o \
    module_state_description.o \
    module_wrf_error.o 

module_comm_dm.o: \
    module_comm_dm_0.o \
    module_comm_dm_1.o \
    module_comm_dm_2.o \
    module_comm_dm_3.o \
    module_comm_dm_4.o \
    module_configure.o \
    module_domain.o \
    module_driver_constants.o \
    module_state_description.o 

module_comm_dm_0.o: \
    module_configure.o \
    module_domain.o \
    module_driver_constants.o \
    module_state_description.o 

module_comm_dm_1.o: \
    module_configure.o \
    module_domain.o \
    module_driver_constants.o \
    module_state_description.o 

module_comm_dm_2.o: \
    module_configure.o \
    module_domain.o \
    module_driver_constants.o \
    module_state_description.o 

module_comm_dm_3.o: \
    module_configure.o \
    module_domain.o \
    module_driver_constants.o \
    module_state_description.o 

module_comm_dm_4.o: \
    module_configure.o \
    module_domain.o \
    module_driver_constants.o \
    module_state_description.o 

module_comm_nesting_dm.o: \
    module_configure.o \
    module_domain.o \
    module_driver_constants.o \
    module_state_description.o 

module_configure.o: \
    module_domain_type.o \
    module_driver_constants.o \
    module_state_description.o \
    module_wrf_error.o 

module_cpl.o: \
    module_configure.o \
    module_cpl_oasis3.o \
    module_domain.o \
    module_driver_constants.o \
    module_model_constants.o 

module_cpl_oasis3.o: \
    module_domain.o \
    module_driver_constants.o 

module_cu_bmj.o: \
    module_model_constants.o 

module_cu_camzm.o: \
    module_cam_cldwat.o \
    module_cam_constituents.o \
    module_cam_physconst.o \
    module_cam_shr_kind_mod.o \
    module_cam_support.o \
    module_cam_wv_saturation.o 

module_cu_camzm_driver.o: \
    module_cam_constituents.o \
    module_cam_physconst.o \
    module_cam_shr_kind_mod.o \
    module_cam_support.o \
    module_cam_wv_saturation.o \
    module_cu_camzm.o \
    module_data_cam_mam_asect.o \
    module_model_constants.o \
    module_mp_cammgmp_driver.o \
    module_state_description.o 

module_cu_kf.o: \
    module_wrf_error.o 

module_cu_kfeta.o: \
    module_wrf_error.o 

module_cu_mesosas.o: \
    module_gfs_funcphys.o \
    module_gfs_machine.o \
    module_gfs_physcons.o 

module_cu_osas.o: \
    module_gfs_funcphys.o \
    module_gfs_machine.o \
    module_gfs_physcons.o 

module_cu_sas.o: \
    module_gfs_funcphys.o \
    module_gfs_machine.o \
    module_gfs_physcons.o 

module_cumulus_driver.o: \
    module_comm_dm.o \
    module_cu_bmj.o \
    module_cu_camzm_driver.o \
    module_cu_g3.o \
    module_cu_gd.o \
    module_cu_gf.o \
    module_cu_kf.o \
    module_cu_kfeta.o \
    module_cu_mesosas.o \
    module_cu_nsas.o \
    module_cu_osas.o \
    module_cu_sas.o \
    module_cu_tiedtke.o \
    module_dm.o \
    module_domain.o \
    module_model_constants.o \
    module_state_description.o \
    module_wrf_error.o 

module_damping_em.o: \
    module_wrf_error.o 

module_data_cam_mam_aero.o: \
    module_cam_constituents.o \
    module_cam_mp_radconstants.o \
    module_cam_shr_kind_mod.o \
    module_cam_support.o 

module_data_cam_mam_asect.o: \
    module_cam_shr_kind_mod.o \
    module_data_cam_mam_aero.o 

module_date_time.o: \
    module_configure.o \
    module_model_constants.o \
    module_utility.o \
    module_wrf_error.o 

module_diag_afwa.o: \
    module_configure.o \
    module_diag_afwa_hail.o \
    module_dm.o \
    module_domain.o \
    module_model_constants.o \
    module_state_description.o \
    module_streams.o \
    module_utility.o 

module_diag_cl.o: \
    module_configure.o \
    module_dm.o 

module_diag_misc.o: \
    module_dm.o 

module_diag_pld.o: \
    module_model_constants.o 

module_diagnostics_driver.o: \
    module_configure.o \
    module_diag_afwa.o \
    module_diag_cl.o \
    module_diag_misc.o \
    module_diag_pld.o \
    module_domain.o \
    module_driver_constants.o \
    module_lightning_driver.o \
    module_model_constants.o \
    module_state_description.o 

module_diffusion_em.o: \
    module_bc.o \
    module_big_step_utilities_em.o \
    module_model_constants.o \
    module_state_description.o 

module_dm.o: \
    module_comm_dm.o \
    module_comm_dm_3.o \
    module_comm_nesting_dm.o \
    module_configure.o \
    module_cpl.o \
    module_domain.o \
    module_driver_constants.o \
    module_machine.o \
    module_state_description.o \
    module_timing.o \
    module_utility.o \
    module_wrf_error.o 

module_domain.o: \
    module_alloc_space_0.o \
    module_alloc_space_1.o \
    module_alloc_space_2.o \
    module_alloc_space_3.o \
    module_alloc_space_4.o \
    module_alloc_space_5.o \
    module_alloc_space_6.o \
    module_alloc_space_7.o \
    module_alloc_space_8.o \
    module_alloc_space_9.o \
    module_configure.o \
    module_domain_type.o \
    module_driver_constants.o \
    module_machine.o \
    module_utility.o \
    module_wrf_error.o 

module_domain_type.o: \
    module_driver_constants.o \
    module_streams.o \
    module_utility.o 

module_em.o: \
    module_advect_em.o \
    module_big_step_utilities_em.o \
    module_configure.o \
    module_damping_em.o \
    module_dm.o \
    module_domain.o \
    module_llxy.o \
    module_model_constants.o \
    module_state_description.o 

module_fdda_psufddagd.o: \
    module_model_constants.o 

module_fdda_spnudging.o: \
    module_dm.o \
    module_domain.o \
    module_state_description.o \
    module_wrf_error.o 

module_fddagd_driver.o: \
    module_configure.o \
    module_domain.o \
    module_fdda_psufddagd.o \
    module_fdda_spnudging.o \
    module_model_constants.o \
    module_state_description.o 

module_fddaobs_driver.o: \
    module_domain.o \
    module_fddaobs_rtfdda.o \
    module_model_constants.o 

module_fddaobs_rtfdda.o: \
    module_dm.o \
    module_domain.o \
    module_model_constants.o 

module_first_rk_step_part1.o: \
    module_big_step_utilities_em.o \
    module_comm_dm.o \
    module_configure.o \
    module_convtrans_prep.o \
    module_cumulus_driver.o \
    module_dm.o \
    module_domain.o \
    module_em.o \
    module_fddagd_driver.o \
    module_force_scm.o \
    module_fr_fire_driver_wrf.o \
    module_model_constants.o \
    module_pbl_driver.o \
    module_radiation_driver.o \
    module_shallowcu_driver.o \
    module_state_description.o \
    module_surface_driver.o \
    module_utility.o 

module_first_rk_step_part2.o: \
    module_bc.o \
    module_comm_dm.o \
    module_configure.o \
    module_diffusion_em.o \
    module_dm.o \
    module_domain.o \
    module_driver_constants.o \
    module_em.o \
    module_fddaobs_driver.o \
    module_model_constants.o \
    module_physics_addtendc.o \
    module_state_description.o \
    module_stoch.o 

module_force_scm.o: \
    module_init_utilities.o 

module_fr_fire_atm.o: \
    module_fr_fire_util.o \
    module_model_constants.o 

module_fr_fire_core.o: \
    module_fr_fire_phys.o \
    module_fr_fire_util.o 

module_fr_fire_driver.o: \
    module_comm_dm.o \
    module_configure.o \
    module_dm.o \
    module_domain.o \
    module_fr_fire_core.o \
    module_fr_fire_model.o \
    module_fr_fire_phys.o \
    module_fr_fire_util.o \
    module_model_constants.o 

module_fr_fire_driver_wrf.o: \
    module_configure.o \
    module_domain.o \
    module_fr_fire_atm.o \
    module_fr_fire_driver.o \
    module_fr_fire_util.o 

module_fr_fire_model.o: \
    module_fr_fire_core.o \
    module_fr_fire_phys.o \
    module_fr_fire_util.o 

module_fr_fire_phys.o: \
    module_fr_fire_util.o \
    module_model_constants.o 

module_fr_fire_util.o: \
    module_dm.o \
    module_wrf_error.o 

module_gfs_funcphys.o: \
    module_gfs_machine.o \
    module_gfs_physcons.o 

module_gfs_physcons.o: \
    module_gfs_machine.o 

module_initialize_real.o: \
    module_bc.o \
    module_comm_dm.o \
    module_configure.o \
    module_date_time.o \
    module_dm.o \
    module_domain.o \
    module_io_domain.o \
    module_llxy.o \
    module_model_constants.o \
    module_optional_input.o \
    module_polarfft.o \
    module_soil_pre.o \
    module_state_description.o \
    module_timing.o 

module_integrate.o: \
    module_configure.o \
    module_cpl.o \
    module_domain.o \
    module_driver_constants.o \
    module_nesting.o \
    module_timing.o \
    module_utility.o 

module_intermediate_nmm.o: \
    module_comm_dm.o \
    module_configure.o \
    module_dm.o \
    module_domain.o \
    module_state_description.o \
    module_timing.o 

module_interp_store.o: \
    module_domain_type.o 

module_io.o: \
    module_configure.o \
    module_dm.o \
    module_driver_constants.o \
    module_state_description.o \
    module_streams.o 

module_io_domain.o: \
    module_configure.o \
    module_domain.o \
    module_io.o \
    module_io_wrf.o \
    module_state_description.o \
    module_utility.o 

module_io_quilt.o: \
    module_configure.o \
    module_cpl.o \
    module_dm.o \
    module_internal_header_util.o \
    module_quilt_outbuf_ops.o \
    module_state_description.o \
    module_timing.o \
    module_wrf_error.o 

module_io_wrf.o: \
    module_date_time.o \
    module_streams.o \
    module_wrf_error.o 

module_lightning_driver.o: \
    module_dm.o \
    module_ltng_cpmpr92z.o \
    module_ltng_crmpr92.o \
    module_ltng_iccg.o \
    module_ltng_lpi.o \
    module_model_constants.o \
    module_state_description.o \
    module_utility.o \
    module_wrf_error.o 

module_llxy.o: \
    module_wrf_error.o 

module_ltng_cpmpr92z.o: \
    module_model_constants.o \
    module_state_description.o \
    module_wrf_error.o 

module_ltng_crmpr92.o: \
    module_dm.o \
    module_model_constants.o \
    module_state_description.o \
    module_wrf_error.o 

module_ltng_iccg.o: \
    module_utility.o 

module_machine.o: \
    module_driver_constants.o 

module_microphysics_driver.o: \
    module_configure.o \
    module_data_cam_mam_aero.o \
    module_domain.o \
    module_mixactivate.o \
    module_model_constants.o \
    module_mp_HWRF.o \
    module_mp_cammgmp_driver.o \
    module_mp_etanew.o \
    module_mp_etaold.o \
    module_mp_fast_sbm.o \
    module_mp_full_sbm.o \
    module_mp_gsfcgce.o \
    module_mp_kessler.o \
    module_mp_lin.o \
    module_mp_milbrandt2mom.o \
    module_mp_morr_two_moment.o \
    module_mp_nssl_2mom.o \
    module_mp_sbu_ylin.o \
    module_mp_thompson.o \
    module_mp_wdm5.o \
    module_mp_wdm6.o \
    module_mp_wsm3.o \
    module_mp_wsm5.o \
    module_mp_wsm6.o \
    module_state_description.o \
    module_utility.o \
    module_wrf_error.o 

module_microphysics_zero_out.o: \
    module_configure.o \
    module_state_description.o \
    module_wrf_error.o 

module_mixactivate.o: \
    module_model_constants.o \
    module_radiation_driver.o 

module_mp_cammgmp_driver.o: \
    module_cam_cldwat.o \
    module_cam_constituents.o \
    module_cam_mp_cldwat2m_micro.o \
    module_cam_mp_conv_water.o \
    module_cam_mp_microp_aero.o \
    module_cam_mp_ndrop.o \
    module_cam_physconst.o \
    module_cam_shr_kind_mod.o \
    module_cam_support.o \
    module_cam_wv_saturation.o \
    module_configure.o \
    module_data_cam_mam_aero.o \
    module_data_cam_mam_asect.o \
    module_state_description.o 

module_mp_fast_sbm.o: \
    module_mp_radar.o 

module_mp_full_sbm.o: \
    module_mp_radar.o 

module_mp_gsfcgce.o: \
    module_domain.o \
    module_mp_radar.o \
    module_utility.o 

module_mp_lin.o: \
    module_domain.o \
    module_mp_radar.o \
    module_utility.o 

module_mp_milbrandt2mom.o: \
    module_model_constants.o \
    module_wrf_error.o 

module_mp_morr_two_moment.o: \
    module_domain.o \
    module_model_constants.o \
    module_mp_radar.o \
    module_utility.o 

module_mp_radar.o: \
    module_wrf_error.o 

module_mp_thompson.o: \
    module_dm.o \
    module_domain.o \
    module_mp_radar.o \
    module_wrf_error.o 

module_mp_wdm5.o: \
    module_domain.o \
    module_mp_radar.o \
    module_utility.o 

module_mp_wdm6.o: \
    module_domain.o \
    module_mp_radar.o \
    module_utility.o 

module_mp_wsm5.o: \
    module_domain.o \
    module_mp_radar.o \
    module_utility.o 

module_mp_wsm6.o: \
    module_domain.o \
    module_mp_radar.o \
    module_utility.o 

module_nesting.o: \
    module_configure.o \
    module_domain.o \
    module_driver_constants.o \
    module_machine.o \
    module_utility.o 

module_optional_input.o: \
    module_configure.o \
    module_domain.o \
    module_io_domain.o \
    module_io_wrf.o 

module_pbl_driver.o: \
    module_bl_acm.o \
    module_bl_boulac.o \
    module_bl_camuwpbl_driver.o \
    module_bl_fogdes.o \
    module_bl_gbmpbl.o \
    module_bl_gfs.o \
    module_bl_gfs2011.o \
    module_bl_gwdo.o \
    module_bl_mfshconvpbl.o \
    module_bl_mrf.o \
    module_bl_myjpbl.o \
    module_bl_myjurb.o \
    module_bl_mynn.o \
    module_bl_qnsepbl.o \
    module_bl_qnsepbl09.o \
    module_bl_temf.o \
    module_bl_ysu.o \
    module_model_constants.o \
    module_state_description.o \
    module_wind_fitch.o 

module_physics_addtendc.o: \
    module_configure.o \
    module_cu_kf.o \
    module_cu_kfeta.o \
    module_state_description.o 

module_physics_init.o: \
    module_bl_acm.o \
    module_bl_boulac.o \
    module_bl_camuwpbl_driver.o \
    module_bl_gbmpbl.o \
    module_bl_gfs.o \
    module_bl_gfs2011.o \
    module_bl_mfshconvpbl.o \
    module_bl_mrf.o \
    module_bl_myjpbl.o \
    module_bl_myjurb.o \
    module_bl_mynn.o \
    module_bl_qnsepbl.o \
    module_bl_qnsepbl09.o \
    module_bl_temf.o \
    module_bl_ysu.o \
    module_cam_constituents.o \
    module_cam_esinti.o \
    module_cam_mp_modal_aero_initialize_data_phys.o \
    module_cam_physconst.o \
    module_cam_shr_kind_mod.o \
    module_cam_support.o \
    module_configure.o \
    module_cu_bmj.o \
    module_cu_camzm_driver.o \
    module_cu_g3.o \
    module_cu_gd.o \
    module_cu_kf.o \
    module_cu_kfeta.o \
    module_cu_mesosas.o \
    module_cu_nsas.o \
    module_cu_osas.o \
    module_cu_sas.o \
    module_cu_tiedtke.o \
    module_data_cam_mam_aero.o \
    module_domain.o \
    module_fdda_psufddagd.o \
    module_fdda_spnudging.o \
    module_fddaobs_rtfdda.o \
    module_llxy.o \
    module_model_constants.o \
    module_mp_HWRF.o \
    module_mp_cammgmp_driver.o \
    module_mp_etanew.o \
    module_mp_etaold.o \
    module_mp_fast_sbm.o \
    module_mp_full_sbm.o \
    module_mp_milbrandt2mom.o \
    module_mp_morr_two_moment.o \
    module_mp_nssl_2mom.o \
    module_mp_thompson.o \
    module_mp_wdm5.o \
    module_mp_wdm6.o \
    module_mp_wsm3.o \
    module_mp_wsm5.o \
    module_mp_wsm6.o \
    module_ra_HWRF.o \
    module_ra_cam.o \
    module_ra_cam_support.o \
    module_ra_gfdleta.o \
    module_ra_gsfcsw.o \
    module_ra_hs.o \
    module_ra_rrtm.o \
    module_ra_sw.o \
    module_sf_bep.o \
    module_sf_bep_bem.o \
    module_sf_clm.o \
    module_sf_gfdl.o \
    module_sf_lake.o \
    module_sf_myjsfc.o \
    module_sf_mynn.o \
    module_sf_noahdrv.o \
    module_sf_noahmpdrv.o \
    module_sf_oml.o \
    module_sf_pxlsm.o \
    module_sf_pxsfclay.o \
    module_sf_qnsesfc.o \
    module_sf_ruclsm.o \
    module_sf_sfclay.o \
    module_sf_sfclayrev.o \
    module_sf_slab.o \
    module_sf_temfsfclay.o \
    module_sf_urban.o \
    module_shcu_camuwshcu.o \
    module_shcu_grims.o \
    module_state_description.o \
    module_wind_fitch.o \
    module_wrf_error.o 

module_polarfft.o: \
    module_comm_dm.o \
    module_dm.o \
    module_domain.o \
    module_driver_constants.o \
    module_model_constants.o \
    module_state_description.o \
    module_wrf_error.o 

module_progtm.o: \
    module_gfs_machine.o 

module_quilt_outbuf_ops.o: \
    module_state_description.o \
    module_timing.o 

module_ra_HWRF.o: \
    module_configure.o \
    module_model_constants.o \
    module_mp_HWRF.o 

module_ra_aerosol.o: \
    module_wrf_error.o 

module_ra_cam.o: \
    module_cam_constituents.o \
    module_cam_support.o \
    module_ra_cam_support.o \
    module_ra_clWRF_support.o \
    module_state_description.o \
    module_wrf_error.o 

module_ra_cam_support.o: \
    module_cam_support.o \
    module_wrf_error.o 

module_ra_clWRF_support.o: \
    module_wrf_error.o 

module_ra_gfdleta.o: \
    module_configure.o \
    module_model_constants.o \
    module_mp_etanew.o 

module_ra_rrtm.o: \
    module_ra_clWRF_support.o \
    module_wrf_error.o 

module_radiation_driver.o: \
    module_bc.o \
    module_comm_dm.o \
    module_dm.o \
    module_domain.o \
    module_model_constants.o \
    module_ra_HWRF.o \
    module_ra_aerosol.o \
    module_ra_cam.o \
    module_ra_flg.o \
    module_ra_gfdleta.o \
    module_ra_goddard.o \
    module_ra_gsfcsw.o \
    module_ra_hs.o \
    module_ra_rrtm.o \
    module_ra_sw.o \
    module_state_description.o \
    module_wrf_error.o 

module_sf_bep.o: \
    module_sf_urban.o 

module_sf_bep_bem.o: \
    module_sf_bem.o \
    module_sf_urban.o 

module_sf_clm.o: \
    module_cam_shr_const_mod.o \
    module_cam_shr_kind_mod.o \
    module_cam_support.o \
    module_configure.o \
    module_date_time.o \
    module_sf_urban.o \
    module_wrf_error.o 

module_sf_fogdes.o: \
    module_bl_mynn.o \
    module_model_constants.o 

module_sf_gfdl.o: \
    module_gfs_funcphys.o \
    module_gfs_machine.o \
    module_gfs_physcons.o 

module_sf_gfs.o: \
    module_gfs_funcphys.o \
    module_gfs_machine.o \
    module_gfs_physcons.o \
    module_progtm.o 

module_sf_lake.o: \
    module_model_constants.o \
    module_wrf_error.o 

module_sf_myjsfc.o: \
    module_dm.o \
    module_model_constants.o 

module_sf_mynn.o: \
    module_bl_mynn.o \
    module_model_constants.o \
    module_sf_sfclay.o 

module_sf_noah_seaice.o: \
    module_model_constants.o \
    module_sf_noahlsm.o 

module_sf_noah_seaice_drv.o: \
    module_sf_noah_seaice.o \
    module_state_description.o 

module_sf_noahdrv.o: \
    module_data_gocart_dust.o \
    module_sf_bep.o \
    module_sf_bep_bem.o \
    module_sf_noahlsm.o \
    module_sf_noahlsm_glacial_only.o \
    module_sf_urban.o \
    module_wrf_error.o 

module_sf_noahlsm.o: \
    module_model_constants.o 

module_sf_noahlsm_glacial_only.o: \
    module_model_constants.o \
    module_sf_noahlsm.o 

module_sf_noahmp_groundwater.o: \
    module_sf_noahlsm.o 

module_sf_noahmpdrv.o: \
    module_data_gocart_dust.o \
    module_ra_gfdleta.o \
    module_sf_noah_seaice.o \
    module_sf_noahdrv.o \
    module_sf_noahmp_glacier.o \
    module_sf_noahmp_groundwater.o \
    module_sf_noahmplsm.o \
    module_sf_urban.o 

module_sf_noahmplsm.o: \
    module_model_constants.o \
    module_sf_myjsfc.o \
    module_sf_noahlsm.o \
    module_sf_sfclay.o 

module_sf_ocean_driver.o: \
    module_sf_3dpwp.o \
    module_sf_oml.o \
    module_state_description.o 

module_sf_pxlsm.o: \
    module_model_constants.o \
    module_sf_pxlsm_data.o 

module_sf_qnsesfc.o: \
    module_dm.o \
    module_model_constants.o 

module_sf_ruclsm.o: \
    module_data_gocart_dust.o \
    module_model_constants.o \
    module_wrf_error.o 

module_sf_sstskin.o: \
    module_wrf_error.o 

module_shallowcu_driver.o: \
    module_dm.o \
    module_domain.o \
    module_model_constants.o \
    module_shcu_camuwshcu_driver.o \
    module_shcu_grims.o \
    module_state_description.o 

module_shcu_camuwshcu.o: \
    module_cam_constituents.o \
    module_cam_error_function.o \
    module_cam_support.o \
    module_cam_wv_saturation.o \
    module_data_cam_mam_aero.o \
    module_state_description.o 

module_shcu_camuwshcu_driver.o: \
    module_cam_constituents.o \
    module_cam_physconst.o \
    module_cam_shr_kind_mod.o \
    module_cam_support.o \
    module_cam_wv_saturation.o \
    module_data_cam_mam_asect.o \
    module_mp_cammgmp_driver.o \
    module_shcu_camuwshcu.o \
    module_state_description.o 

module_small_step_em.o: \
    module_configure.o \
    module_model_constants.o 

module_soil_pre.o: \
    module_date_time.o \
    module_state_description.o 

module_stoch.o: \
    module_configure.o 

module_surface_driver.o: \
    module_cpl.o \
    module_model_constants.o \
    module_sf_clm.o \
    module_sf_fogdes.o \
    module_sf_gfdl.o \
    module_sf_gfs.o \
    module_sf_idealscmsfclay.o \
    module_sf_lake.o \
    module_sf_myjsfc.o \
    module_sf_mynn.o \
    module_sf_noah_seaice_drv.o \
    module_sf_noahdrv.o \
    module_sf_noahmp_groundwater.o \
    module_sf_noahmpdrv.o \
    module_sf_ocean_driver.o \
    module_sf_pxlsm.o \
    module_sf_pxsfclay.o \
    module_sf_qnsesfc.o \
    module_sf_ruclsm.o \
    module_sf_scmflux.o \
    module_sf_scmskintemp.o \
    module_sf_sfcdiags.o \
    module_sf_sfcdiags_ruclsm.o \
    module_sf_sfclay.o \
    module_sf_sfclayrev.o \
    module_sf_slab.o \
    module_sf_ssib.o \
    module_sf_sstskin.o \
    module_sf_temfsfclay.o \
    module_sf_tmnupdate.o \
    module_state_description.o 

module_symbols_util.o: \
    ESMF_Mod.o 

module_tiles.o: \
    module_configure.o \
    module_domain.o \
    module_driver_constants.o \
    module_machine.o \
    module_wrf_error.o 

module_timing.o: \
    module_wrf_error.o 

module_utility.o: \
    module_symbols_util.o 

module_wind_fitch.o: \
    module_configure.o \
    module_dm.o \
    module_driver_constants.o \
    module_llxy.o \
    module_model_constants.o 

module_wps_io_arw.o: \
    module_domain.o \
    module_internal_header_util.o \
    module_optional_input.o \
    module_soil_pre.o 

module_wrf_top.o: \
    module_check_a_mundo.o \
    module_configure.o \
    module_cpl.o \
    module_dm.o \
    module_domain.o \
    module_driver_constants.o \
    module_integrate.o \
    module_machine.o \
    module_nesting.o \
    module_timing.o \
    module_wrf_error.o 

ndown_em.o: \
    module_bc.o \
    module_big_step_utilities_em.o \
    module_check_a_mundo.o \
    module_configure.o \
    module_dm.o \
    module_domain.o \
    module_domain_type.o \
    module_driver_constants.o \
    module_get_file_names.o \
    module_initialize_real.o \
    module_integrate.o \
    module_io_domain.o \
    module_machine.o \
    module_optional_input.o \
    module_soil_pre.o \
    module_timing.o \
    module_utility.o \
    module_wrf_error.o 

nest_init_utils.o: \
    module_bc.o \
    module_comm_dm.o \
    module_configure.o \
    module_dm.o \
    module_domain.o \
    module_driver_constants.o \
    module_machine.o \
    module_model_constants.o \
    module_state_description.o \
    module_tiles.o 

netcdfnetcdf.f90: \
    netcdftypeSizes.o

netcdfnetcdf_test.f90: \
    netcdfnetcdf.o \
    netcdftypeSizes.o

nl_get_0_routines.o: \
    module_configure.o 

nl_get_1_routines.o: \
    module_configure.o 

nl_get_2_routines.o: \
    module_configure.o 

nl_get_3_routines.o: \
    module_configure.o 

nl_get_4_routines.o: \
    module_configure.o 

nl_get_5_routines.o: \
    module_configure.o 

nl_get_6_routines.o: \
    module_configure.o 

nl_get_7_routines.o: \
    module_configure.o 

nl_set_0_routines.o: \
    module_configure.o 

nl_set_1_routines.o: \
    module_configure.o 

nl_set_2_routines.o: \
    module_configure.o 

nl_set_3_routines.o: \
    module_configure.o 

nl_set_4_routines.o: \
    module_configure.o 

nl_set_5_routines.o: \
    module_configure.o 

nl_set_6_routines.o: \
    module_configure.o 

nl_set_7_routines.o: \
    module_configure.o 

nup_em.o: \
    module_bc.o \
    module_big_step_utilities_em.o \
    module_configure.o \
    module_dm.o \
    module_domain.o \
    module_domain_type.o \
    module_driver_constants.o \
    module_get_file_names.o \
    module_initialize_real.o \
    module_integrate.o \
    module_io_domain.o \
    module_machine.o \
    module_optional_input.o \
    module_soil_pre.o \
    module_streams.o \
    module_timing.o \
    module_utility.o \
    module_wrf_error.o 

output_wrf.o: \
    module_configure.o \
    module_domain.o \
    module_domain_type.o \
    module_io.o \
    module_io_wrf.o \
    module_model_constants.o \
    module_state_description.o \
    module_utility.o \
    module_wrf_error.o 

real_em.o: \
    module_bc.o \
    module_bc_time_utilities.o \
    module_big_step_utilities_em.o \
    module_check_a_mundo.o \
    module_configure.o \
    module_date_time.o \
    module_dm.o \
    module_domain.o \
    module_driver_constants.o \
    module_initialize_real.o \
    module_io_domain.o \
    module_machine.o \
    module_optional_input.o \
    module_state_description.o \
    module_symbols_util.o \
    module_timing.o \
    module_utility.o \
    module_wps_io_arw.o 

set_timekeeping.o: \
    module_configure.o \
    module_domain.o \
    module_utility.o 

shift_domain_em.o: \
    module_comm_dm.o \
    module_configure.o \
    module_dm.o \
    module_domain.o \
    module_domain_type.o \
    module_state_description.o \
    module_timing.o 

solve_em.o: \
    module_after_all_rk_steps.o \
    module_avgflx_em.o \
    module_bc.o \
    module_bc_em.o \
    module_big_step_utilities_em.o \
    module_comm_dm.o \
    module_configure.o \
    module_cpl.o \
    module_diffusion_em.o \
    module_dm.o \
    module_domain.o \
    module_domain_type.o \
    module_driver_constants.o \
    module_em.o \
    module_fddaobs_driver.o \
    module_first_rk_step_part1.o \
    module_first_rk_step_part2.o \
    module_llxy.o \
    module_machine.o \
    module_microphysics_driver.o \
    module_microphysics_zero_out.o \
    module_model_constants.o \
    module_physics_addtendc.o \
    module_polarfft.o \
    module_small_step_em.o \
    module_solvedebug_em.o \
    module_state_description.o \
    module_tiles.o \
    module_utility.o 

solve_interface.o: \
    module_configure.o \
    module_domain.o \
    module_driver_constants.o \
    module_timing.o \
    module_wrf_error.o 

start_domain.o: \
    module_configure.o \
    module_domain.o \
    module_driver_constants.o 

start_em.o: \
    module_avgflx_em.o \
    module_bc.o \
    module_bc_em.o \
    module_comm_dm.o \
    module_configure.o \
    module_diag_pld.o \
    module_dm.o \
    module_domain.o \
    module_fr_fire_driver_wrf.o \
    module_lightning_driver.o \
    module_model_constants.o \
    module_physics_init.o \
    module_state_description.o \
    module_stoch.o \
    module_tiles.o 

tc_em.o: \
    module_bc.o \
    module_bc_time_utilities.o \
    module_big_step_utilities_em.o \
    module_configure.o \
    module_date_time.o \
    module_dm.o \
    module_domain.o \
    module_driver_constants.o \
    module_initialize_real.o \
    module_io_domain.o \
    module_llxy.o \
    module_machine.o \
    module_optional_input.o \
    module_state_description.o \
    module_symbols_util.o \
    module_timing.o \
    module_utility.o 

track_driver.o: \
    module_configure.o \
    module_date_time.o \
    module_dm.o \
    module_domain.o \
    module_llxy.o \
    module_model_constants.o \
    module_state_description.o 

track_input.o: \
    module_domain.o \
    module_utility.o 

wrf.o: \
    module_wrf_top.o 

wrf_bdyin.o: \
    module_bc_time_utilities.o \
    module_configure.o \
    module_date_time.o \
    module_domain.o \
    module_io.o \
    module_io_wrf.o \
    module_state_description.o \
    module_utility.o 

wrf_bdyout.o: \
    module_configure.o \
    module_domain.o \
    module_io.o \
    module_io_wrf.o \
    module_state_description.o \
    module_utility.o \
    module_wrf_error.o 

wrf_debug.o: \
    module_wrf_error.o 

wrf_ext_read_field.o: \
    module_io.o \
    module_state_description.o \
    module_timing.o \
    module_wrf_error.o 

wrf_ext_write_field.o: \
    module_io.o \
    module_state_description.o \
    module_timing.o \
    module_wrf_error.o 

wrf_fddaobs_in.o: \
    module_configure.o \
    module_date_time.o \
    module_domain.o \
    module_llxy.o \
    module_model_constants.o 

wrf_timeseries.o: \
    module_configure.o \
    module_dm.o \
    module_domain.o \
    module_llxy.o \
    module_model_constants.o \
    module_state_description.o 

wrf_tsin.o: \
    module_domain.o \
    module_utility.o 

