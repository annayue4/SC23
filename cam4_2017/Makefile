
BIN           = cam4_2017
BIN_VALIDATE  = cam4_validate

CC      = cc -Ofast
FC      = ftn -Ofast #-O3 -hfp3
FFLAGS	= 
CFLAGS  = 
EXTRA_FLAGS = -I src -I src/include -I src/netcdf/include \
              -DSPEC -DNDEBUG -DSPEC_LP64 \
              -DNO_SHR_VMATH -DCO2A -DPERGRO -DPLON=144 -DPLAT=96 -DPLEV=26 -DPCNST=3 \
              -DPCOLS=4 -DPTRM=1 -DPTRN=1 -DPTRK=1 -DSTAGGERED -D_NETCDF -DNO_R16
EXTRA_FFLAGS = $(EXTRA_FLAGS) -DHIDE_MPI -D_MPISERIAL -DNO_MPI2
EXTRA_CFLAGS = $(EXTRA_FLAGS) -DSPEC_CASE_FLAG -DSPEC_AUTO_BYTEORDER=0x12345678
OMP_FLAGS = -DSPEC_SUPPRESS_OPENMP
LIBS = -static

# rate -DSPEC_SUPPRESS_OPENMP
# speed -DSPEC_OPENMP -DUSE_COSP


SOURCES = \
        ESMF_BaseMod.F90 \
        ESMF_BaseTimeMod.F90 \
        ESMF_FractionMod.F90 \
        ESMF_CalendarMod.F90 \
        ESMF_TimeIntervalMod.F90 \
        ESMF_Stubs.F90 \
        ESMF_TimeMod.F90 \
        ESMF_AlarmMod.F90 \
        ESMF_ClockMod.F90 \
        ESMF_AlarmClockMod.F90 \
        ESMF_Mod.F90 \
        cam_logfile.F90 \
        debugutilitiesmodule.F90 \
        decompmodule.F90 \
        shr_kind_mod.F90 \
        ghostmodule.F90 \
        perf_utils.F90 \
        shr_log_mod.F90 \
        shr_mpi_mod.F90 \
        shr_sys_mod.F90 \
        shr_file_mod.F90 \
        string_utils.F90 \
        namelist_utils.F90 \
        perf_mod.F90 \
        mod_comm.F90 \
        parutilitiesmodule.F90 \
        mpishorthand.F90 \
        abortutils.F90 \
        units.F90 \
        spmd_utils.F90 \
        fv_control_mod.F90 \
        pft_module.F90 \
        dynamics_vars.F90 \
        FVperf_module.F90 \
        GPTLget_memusage.c \
        GPTLprint_memusage.c \
        GPTLutil.c \
        MISR_simulator.F90 \
        Meat.F90 \
        pmgrid.F90 \
        dycore.F90 \
        pio_kinds.F90 \
        pio_support.F90 \
        pio_types.F90 \
        pio_msg_mod.F90 \
        alloc_mod.F90 \
        pio_utils.F90 \
        nf_mod.F90 \
        pionfput_mod.F90 \
        pionfatt_mod.F90 \
        pio_spmd_utils.F90 \
        calcdisplace_mod.F90 \
        box_rearrange.F90 \
        rearrange.F90 \
        pionfread_mod.F90 \
        iompi_mod.F90 \
        pionfwrite_mod.F90 \
        piodarray.F90 \
        ionf_mod.F90 \
        calcdecomp.F90 \
        pio_mpi_utils.F90 \
        piolib_mod.F90 \
        pionfget_mod.F90 \
        pio.F90 \
        shr_timer_mod.F90 \
        shr_string_mod.F90 \
        shr_const_mod.F90 \
        shr_cal_mod.F90 \
        time_manager.F90 \
        ppgrid.F90 \
        physconst.F90 \
        constituents.F90 \
        commap.F90 \
        infnan.F90 \
        pspect.F90 \
        rgrid.F90 \
        spmd_dyn.F90 \
        hycoef.F90 \
        dyn_grid.F90 \
        m_chars.F90 \
        m_flow.F90 \
        m_stdio.F90 \
        m_mpif.F90 \
        m_realkinds.F90 \
        m_mpif90.F90 \
        m_dropdead.F90 \
        m_ioutil.F90 \
        m_mpout.F90 \
        m_die.F90 \
        m_MergeSorts.F90 \
        phys_grid.F90 \
        ioFileMod.F90 \
        cam_history_support.F90 \
        cam_control_mod.F90 \
        m_mall.F90 \
        m_String.F90 \
        m_rankMerge.F90 \
        m_IndexBin_logical.F90 \
        m_Permuter.F90 \
        m_IndexBin_char.F90 \
        m_IndexBin_integer.F90 \
        m_SortingTools.F90 \
        m_List.F90 \
        m_TraceBack.F90 \
        m_AttrVect.F90 \
        m_GlobalMap.F90 \
        m_FcComms.F90 \
        m_MCTWorld.F90 \
        m_GlobalSegMap.F90 \
        m_AttrVectComms.F90 \
        m_SparseMatrix.F90 \
        m_SparseMatrixDecomp.F90 \
        m_SparseMatrixComms.F90 \
        m_Navigator.F90 \
        m_GlobalToLocal.F90 \
        m_SparseMatrixToMaps.F90 \
        m_ConvertMaps.F90 \
        m_ExchangeMaps.F90 \
        m_Router.F90 \
        m_Rearranger.F90 \
        m_SparseMatrixPlus.F90 \
        m_GeneralGrid.F90 \
        m_Transfer.F90 \
        m_inpak90.F90 \
        m_GlobalSegMapComms.F90 \
        m_Accumulator.F90 \
        m_MatAttrVectMul.F90 \
        m_GeneralGridComms.F90 \
        mct_mod.F90 \
        seq_comm_mct.F90 \
        seq_drydep_mod.F90 \
        seq_flds_mod.F90 \
        seq_io_mod.F90 \
        cam_pio_utils.F90 \
        sat_hist.F90 \
        solar_data.F90 \
        shr_orb_mod.F90 \
        shr_tInterp_mod.F90 \
        shr_stream_mod.F90 \
        shr_pcdf_mod.F90 \
        shr_mct_mod.F90 \
        shr_map_mod.F90 \
        shr_ncread_mod.F90 \
        shr_dmodel_mod.F90 \
        shr_strdata_mod.F90 \
        shr_scam_mod.F90 \
        wrap_nf.F90 \
        scamMod.F90 \
        error_messages.F90 \
        interpolate_data.F90 \
        geopotential.F90 \
        ref_pres.F90 \
        phys_control.F90 \
        physics_types.F90 \
        time_utils.F90 \
        repro_sum_mod.F90 \
        phys_gmean.F90 \
        mo_constants.F90 \
        m_types.F90 \
        mo_flbc.F90 \
        chem_surfvals.F90 \
        cam_history_buffers.F90 \
        filenames.F90 \
        cosp_share.F90 \
        interp_mod.F90 \
        cam_history.F90 \
        advect_tend.F90 \
        phys_buffer.F90 \
        ghg_data.F90 \
        radconstants.F90 \
        radae.F90 \
        quicksort.F90 \
        radlw.F90 \
        pkg_cldoptics.F90 \
        phys_debug_util.F90 \
        conv_water.F90 \
        param_cldoptics.F90 \
        mo_util.F90 \
        rad_solar_var.F90 \
        cmparray_mod.F90 \
        radsw.F90 \
        phys_prop.F90 \
        rad_constituents.F90 \
        wv_saturation.F90 \
        modal_aer_opt.F90 \
        aer_rad_props.F90 \
        camsrfexch_types.F90 \
        radiation_data.F90 \
        cosp_constants.F90 \
        cosp_utils.F90 \
        radar_simulator_types.f90 \
        cosp_types.F90 \
        modis_simulator.F90 \
        cosp_modis_simulator.F90 \
        cosp_lidar.F90 \
        cosp_misr_simulator.F90 \
        llnl_stats.F90 \
        lmd_ipsl_stats.F90 \
        cosp_stats.F90 \
        atmos_lib.f90 \
        mrgrnk.f90 \
        array_lib.f90 \
        format_input.f90 \
        math_lib.f90 \
        optics_lib.f90 \
        cosp_radar.F90 \
        cosp_isccp_simulator.F90 \
        cosp_simulator.F90 \
        cosp.F90 \
        cospsimulator_intr.F90 \
        chemistry.F90 \
        radheat.F90 \
        radiation.F90 \
        horizontal_interpolate.F90 \
        polar_avg.F90 \
        tracer_data.F90 \
        prescribed_ghg.F90 \
        prescribed_aero.F90 \
        trb_mtn_stress.F90 \
        phys_debug.F90 \
        hb_diff.F90 \
        upper_bc.F90 \
        molec_diff.F90 \
        diffusion_solver.F90 \
        eddy_diff.F90 \
        vertical_diffusion.F90 \
        boundarydata.F90 \
        cam3_ozone_data.F90 \
        aoa_tracers.F90 \
        iondrag.F90 \
        cam3_aero_data.F90 \
        tracers_suite.F90 \
        tracers.F90 \
        tropopause.F90 \
        prescribed_volcaero.F90 \
        prescribed_ozone.F90 \
        aircraft_emit.F90 \
        modal_aero_deposition.F90 \
        aerodep_flx.F90 \
        advnce.F90 \
        drydep_mod.F90 \
        wetdep.F90 \
        dust_sediment_mod.F90 \
        dust_intr.F90 \
        progseasalts_intr.F90 \
        scyc.F90 \
        aerosol_intr.F90 \
        history_scam.F90 \
        xpavg_mod.F90 \
        ncdio_atm.F90 \
        metdata.F90 \
        co2_data_flux.F90 \
        co2_cycle.F90 \
        buffer.F90 \
        comsrf.F90 \
        restart_physics.F90 \
        pfixer.F90 \
        ctem.F90 \
        diag_module.F90 \
        dyn_comp.F90 \
        dyn_internal_state.F90 \
        restart_dynamics.F90 \
        cam_restart.F90 \
        readinitial.F90 \
        history_defaults.F90 \
        error_function.F90 \
        uw_conv.F90 \
        uwshcu.F90 \
        cldwat.F90 \
        zm_conv.F90 \
        hk_conv.F90 \
        convect_shallow.F90 \
        cloud_fraction.F90 \
        cldwat2m_macro.F90 \
        ndrop.F90 \
        cldwat2m_micro.F90 \
        microp_aero.F90 \
        microp_driver.F90 \
        pkg_cld_sediment.F90 \
        stratiform.F90 \
        inidat.F90 \
        startup_initialconds.F90 \
        inital.F90 \
        check_energy.F90 \
        dp_coupling.F90 \
        fv_prints.F90 \
        stepon.F90 \
        ionosphere.F90 \
        cloud_diagnostics.F90 \
        cloud_rad_props.F90 \
        tidal_diag.F90 \
        constituent_burden.F90 \
        cam_diagnostics.F90 \
        flux_avg.F90 \
        macrop_driver.F90 \
        gw_drag.F90 \
        zm_conv_intr.F90 \
        convect_deep.F90 \
        rayleigh_friction.F90 \
        majorsp_diffusion.F90 \
        sslt_rebin.F90 \
        physpkg.F90 \
        cam_comp.F90 \
        seq_infodata_mod.F90 \
        seq_cdata_mod.F90 \
        runtime_opts.F90 \
        cam_cpl_indices.F90 \
        seq_timemgr_mod.F90 \
        atm_comp_mct.F90 \
        benergy.F90 \
        binary_io.F90 \
        bnddyi.F90 \
        seq_flds_indices.F90 \
        seq_diag_mct.F90 \
        seq_rearr_mod.F90 \
        map_ocnocn_mct.F90 \
        mrg_x2s_mct.F90 \
        ice_comp_mct.F90 \
        mrg_x2o_mct.F90 \
        seq_avdata_mod.F90 \
        seq_hist_mod.F90 \
        mrg_x2a_mct.F90 \
        map_iceocn_mct.F90 \
        seq_map_mod.F90 \
        map_atmlnd_mct.F90 \
        map_atmice_mct.F90 \
        map_snoglc_mct.F90 \
        map_atmocn_mct.F90 \
        seq_domain_mct.F90 \
        seq_rest_mod.F90 \
        mrg_x2l_mct.F90 \
        seq_frac_mct.F90 \
        shr_flux_mod.F90 \
        seq_flux_mct.F90 \
        map_lndlnd_mct.F90 \
        map_iceice_mct.F90 \
        map_glcglc_mct.F90 \
        lnd_comp_mct.F90 \
        ocn_types.F90 \
        ocn_comp.F90 \
        ocn_comp_mct.F90 \
        map_rofrof_mct.F90 \
        map_atmatm_mct.F90 \
        map_rofocn_mct.F90 \
        shr_mem_mod.F90 \
        map_snosno_mct.F90 \
        mrg_x2g_mct.F90 \
        mrg_x2i_mct.F90 \
        glc_comp_mct.F90 \
        ccsm_comp_mod.F90 \
        ccsm_driver.F90 \
        tp_core.F90 \
        sw_core.F90 \
        cd_core.F90 \
        cldsav.F90 \
        collective.c \
        comm.c \
        comspe.F90 \
        cpslec.F90 \
        d2a3dijk.F90 \
        d2a3dikj.F90 \
        dadadj.F90 \
        datetime.F90 \
        diag_dynvar_ic.F90 \
        mean_module.F90 \
        dryairm.F90 \
        dsd.f90 \
        mapz_module.F90 \
        epvd.F90 \
        esinti.F90 \
        f_wrappers.c \
        fft99.F90 \
        fill_module.F90 \
        fort.F90 \
        gases.f90 \
        gauaw_mod.F90 \
        geopk.F90 \
        get_zeits.c \
        gffgch.F90 \
        gptl.c \
        gptl_papi.c \
        group.c \
        handles.c \
        hirsbtpar.f90 \
        hirsbt.f90 \
        icarus.F90 \
        initcom.F90 \
        initindx.F90 \
        intp_util.F90 \
        iop_surf.F90 \
        lidar_simulator.F90 \
        list.c \
        load_hydrometeor_classes.f90 \
        m_AccumulatorComms.F90 \
        m_AttrVectReduce.F90 \
        m_StrTemplate.F90 \
        m_FileResolv.F90 \
        m_Filename.F90 \
        m_Merge.F90 \
        m_SpatialIntegralV.F90 \
        m_SpatialIntegral.F90 \
        m_zeit.F90 \
        marsaglia.F90 \
        mcshallow.F90 \
        pio_quicksort.F90 \
        mct_rearrange.F90 \
        miesubs.F90 \
        mo_msis_ubc.F90 \
        mo_regrider.F90 \
        mo_solar_parms.F90 \
        mpi.c \
        msise00.F90 \
        p_d_adjust.F90 \
        pack.c \
        par_vecsum.F90 \
        par_xsum.F90 \
        pf_to_mr.F90 \
        pio_msg_callbacks.F90 \
        pio_msg_getput_callbacks.F90 \
        pio_nf_utils.F90 \
        pkez.F90 \
        prec_scops.F90 \
        puminterfaces.F90 \
        qneg3.F90 \
        qneg4.F90 \
        radar_simulator.f90 \
        recv.c \
        redistributemodule.F90 \
        req.c \
        scops.F90 \
        send.c \
        sgexx.F90 \
        shr_jlcp.c \
        shr_msg_mod.F90 \
        shr_vmath_fwrap.c \
        shr_vmath_mod.F90 \
        srchutil.F90 \
        srfxfer.F90 \
        sulchem.F90 \
        te_map.F90 \
        threadutil.c \
        time.c \
        topology.c \
        tphysac.F90 \
        tphysbc.F90 \
        tphysidl.F90 \
        trac2d.F90 \
        trunc.F90 \
        tsinti.F90 \
        uv3s_update.F90 \
        virtem.F90 \
        vrtmap.F90 \
        wrap_mpi.F90 \
        wrf_error_fatal.F90 \
        wrf_message.F90 \
        zeff.f90 \
        zenith.F90 \
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
        fort-v2compat.c \
        fort-var1io.c \
        fort-varaio.c \
        fort-vario.c \
        fort-varmio.c \
        fort-varsio.c \
        libvers.c \
        nc.c \
        ncx.c \
        posixio.c \
        putget.c \
        string.c \
        v1hpg.c \
        v2i.c \
        var.c \
        typeSizes.f90 \
        netcdf.f90 \
        spec_qsort.c

SOURCES_VALIDATE = \
        validate-cam.f90 \
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
        fort-v2compat.c \
        fort-var1io.c \
        fort-varaio.c \
        fort-vario.c \
        fort-varmio.c \
        fort-varsio.c \
        libvers.c \
        nc.c \
        ncx.c \
        posixio.c \
        putget.c \
        string.c \
        v1hpg.c \
        v2i.c \
        var.c \
        typeSizes.f90 \
        netcdf.f90 \
        spec_qsort.c

TMPOBJ  = $(SOURCES:.c=.o)
TMPOBJ2 = $(TMPOBJ:.f90=.o)
TMPOBJ3 = $(TMPOBJ2:.F90=.o)
OBJ     = $(TMPOBJ3:.F=.o)

TMPOBJ_VALIDATE  = $(SOURCES_VALIDATE:.c=.o)
TMPOBJ2_VALIDATE = $(TMPOBJ_VALIDATE:.f90=.o)
OBJ_VALIDATE     = $(TMPOBJ2_VALIDATE:.F90=.o)

VPATH	= src:src/netcdf:src/spec_qsort
.SUFFIXES: .F .f90 .F90 .c

ifeq ($(MAKECMDGOALS),cam4_2017_omp)
BIN       = cam4_2017_omp
OMP_FLAGS = -DSPEC_OPENMP -DUSE_COSP
endif


$(BIN):	x$(BIN) $(BIN).execute.script $(BIN_VALIDATE)
	cp $(BIN).execute.script $(BIN)
x$(BIN): $(OBJ)
	$(FC) $(FFLAGS) -o x$(BIN) $(OBJ) $(LDFLAGS) $(LIBS)

$(BIN_VALIDATE): $(OBJ_VALIDATE)
	$(FC) $(FFLAGS) -o $(BIN_VALIDATE) $(OBJ_VALIDATE) $(LDFLAGS) $(LIBS)

.c.o:
	$(CC) -c $(EXTRA_CFLAGS) $(OMP_FLAGS) $(CFLAGS) $<

.f.o:
	$(FC) -c $(EXTRA_FFLAGS) $(OMP_FLAGS) $(FFLAGS) $<

.f90.o:
	$(FC) -c $(EXTRA_FFLAGS) $(OMP_FLAGS) $(FFLAGS) $<

.F90.o:
	$(FC) -c $(EXTRA_FFLAGS) $(OMP_FLAGS) $(FFLAGS) $<

clean:
	-rm -f core
	-rm -f $(OBJ) $(OBJ_VALIDATE) *.mod

clobber: clean
	-rm -f $(BIN) x$(BIN) $(BIN)_omp x$(BIN)_omp $(BIN_VALIDATE)
	-rm -f *_in ccsm_timing *.nc cam4.out cam4.err

ESMF_BaseTimeMod.o: \
    ESMF_BaseMod.o \

ESMF_CalendarMod.o: \
    ESMF_BaseMod.o \
    ESMF_BaseTimeMod.o \

ESMF_TimeIntervalMod.o: \
    ESMF_BaseTimeMod.o \
    ESMF_FractionMod.o \
    ESMF_BaseMod.o \
    ESMF_CalendarMod.o \

ESMF_Stubs.o: \
    ESMF_BaseMod.o \
    ESMF_CalendarMod.o \

ESMF_TimeMod.o: \
    ESMF_TimeIntervalMod.o \
    ESMF_BaseTimeMod.o \
    ESMF_BaseMod.o \
    ESMF_CalendarMod.o \
    ESMF_Stubs.o \

ESMF_AlarmMod.o: \
    ESMF_BaseMod.o \
    ESMF_TimeIntervalMod.o \
    ESMF_TimeMod.o \

ESMF_ClockMod.o: \
    ESMF_AlarmMod.o \
    ESMF_BaseMod.o \
    ESMF_TimeIntervalMod.o \
    ESMF_TimeMod.o \

ESMF_AlarmClockMod.o: \
    ESMF_AlarmMod.o \
    ESMF_ClockMod.o \
    ESMF_TimeIntervalMod.o \
    ESMF_TimeMod.o \

ESMF_Mod.o: \
    ESMF_TimeIntervalMod.o \
    ESMF_BaseTimeMod.o \
    ESMF_FractionMod.o \
    ESMF_TimeMod.o \
    ESMF_AlarmMod.o \
    ESMF_AlarmClockMod.o \
    ESMF_BaseMod.o \
    ESMF_ClockMod.o \
    ESMF_CalendarMod.o \
    ESMF_Stubs.o \

debugutilitiesmodule.o: \
    cam_logfile.o \

decompmodule.o: \
    cam_logfile.o \
    debugutilitiesmodule.o \

ghostmodule.o: \
    decompmodule.o \
    debugutilitiesmodule.o \

shr_log_mod.o: \
    shr_kind_mod.o \

shr_mpi_mod.o: \
    shr_log_mod.o \
    shr_kind_mod.o \

shr_sys_mod.o: \
    shr_log_mod.o \
    shr_kind_mod.o \
    shr_mpi_mod.o \

shr_file_mod.o: \
    shr_sys_mod.o \
    shr_log_mod.o \
    shr_kind_mod.o \

namelist_utils.o: \
    string_utils.o \

perf_mod.o: \
    perf_utils.o \
    shr_sys_mod.o \
    shr_file_mod.o \
    shr_kind_mod.o \
    namelist_utils.o \
    shr_mpi_mod.o \

mod_comm.o: \
    shr_kind_mod.o \
    perf_mod.o \
    cam_logfile.o \

parutilitiesmodule.o: \
    decompmodule.o \
    shr_kind_mod.o \
    cam_logfile.o \
    ghostmodule.o \
    mod_comm.o \
    debugutilitiesmodule.o \

abortutils.o: \
    shr_sys_mod.o \
    cam_logfile.o \
    mpishorthand.o \

units.o: \
    shr_file_mod.o \
    abortutils.o \

spmd_utils.o: \
    mpishorthand.o \
    units.o \
    abortutils.o \
    shr_kind_mod.o \
    perf_mod.o \
    cam_logfile.o \
    namelist_utils.o \

fv_control_mod.o: \
    spmd_utils.o \
    abortutils.o \
    mpishorthand.o \
    shr_kind_mod.o \
    cam_logfile.o \
    namelist_utils.o \
    units.o 

pft_module.o: \
    fv_control_mod.o \
    shr_kind_mod.o \

dynamics_vars.o: \
    parutilitiesmodule.o \
    fv_control_mod.o \
    decompmodule.o \
    mpishorthand.o \
    shr_kind_mod.o \
    pft_module.o \
    cam_logfile.o \
    ghostmodule.o \
    mod_comm.o \

FVperf_module.o: \
    dynamics_vars.o \
    perf_mod.o \
    mod_comm.o \

Meat.o: \
    ESMF_TimeIntervalMod.o \
    ESMF_BaseTimeMod.o \
    ESMF_FractionMod.o \
    ESMF_TimeMod.o \
    ESMF_AlarmMod.o \
    ESMF_ClockMod.o \
    ESMF_BaseMod.o \
    ESMF_CalendarMod.o \

pmgrid.o: \
    decompmodule.o \
    shr_kind_mod.o \

dycore.o: \
    pmgrid.o \

pio_kinds.o: \
    netcdf.o \

pio_support.o: \
    pio_kinds.o \

pio_types.o: \
    pio_kinds.o \

pio_msg_mod.o: \
    pio_support.o \
    pio_types.o \
    perf_mod.o \
    pio_kinds.o \

alloc_mod.o: \
    pio_kinds.o \
    pio_support.o \
    pio_types.o \

pio_utils.o: \
    pio_support.o \
    pio_types.o \
    pio_kinds.o \

nf_mod.o: \
    pio_msg_mod.o \
    alloc_mod.o \
    pio_support.o \
    perf_mod.o \
    pio_kinds.o \
    pio_utils.o \
    pio_types.o \

pionfput_mod.o: \
    pio_support.o \
    nf_mod.o \
    pio_types.o \
    pio_msg_mod.o \
    perf_mod.o \
    pio_kinds.o \
    pio_utils.o \

pionfatt_mod.o: \
    pio_support.o \
    pio_types.o \
    pio_msg_mod.o \
    pio_kinds.o \
    pio_utils.o \

pio_spmd_utils.o: \
    pio_support.o \
    pio_kinds.o \

calcdisplace_mod.o: \
    pio_support.o \
    pio_kinds.o \

box_rearrange.o: \
    pio_spmd_utils.o \
    alloc_mod.o \
    pio_support.o \
    calcdisplace_mod.o \
    pio_kinds.o \
    pio_types.o \

rearrange.o: \
    box_rearrange.o \
    pio_support.o \
    pio_types.o \
    perf_mod.o \
    pio_kinds.o \

pionfread_mod.o: \
    alloc_mod.o \
    pio_support.o \
    pio_types.o \
    perf_mod.o \
    pio_kinds.o \
    pio_utils.o \

iompi_mod.o: \
    alloc_mod.o \
    pio_support.o \
    perf_mod.o \
    pio_kinds.o \
    pio_types.o \

pionfwrite_mod.o: \
    alloc_mod.o \
    pio_support.o \
    nf_mod.o \
    pio_types.o \
    perf_mod.o \
    pio_kinds.o \
    pio_utils.o \

piodarray.o: \
    alloc_mod.o \
    pio_support.o \
    rearrange.o \
    pio_types.o \
    pio_msg_mod.o \
    pionfread_mod.o \
    perf_mod.o \
    iompi_mod.o \
    pio_kinds.o \
    pionfwrite_mod.o \

ionf_mod.o: \
    alloc_mod.o \
    pio_support.o \
    perf_mod.o \
    pio_kinds.o \
    pio_utils.o \
    pio_types.o \

calcdecomp.o: \
    pio_support.o \
    pio_kinds.o \
    pio_types.o \

pio_mpi_utils.o: \
    pio_support.o \
    pio_types.o \

piolib_mod.o: \
    alloc_mod.o \
    pio_support.o \
    rearrange.o \
    ionf_mod.o \
    calcdecomp.o \
    pio_types.o \
    pio_mpi_utils.o \
    pio_msg_mod.o \
    pionfread_mod.o \
    perf_mod.o \
    calcdisplace_mod.o \
    iompi_mod.o \
    pio_kinds.o \
    pionfwrite_mod.o \

pionfget_mod.o: \
    pio_support.o \
    pio_types.o \
    pio_msg_mod.o \
    perf_mod.o \
    pio_kinds.o \
    pio_utils.o \

pio.o: \
    pionfput_mod.o \
    pionfatt_mod.o \
    nf_mod.o \
    piodarray.o \
    piolib_mod.o \
    pio_types.o \
    pionfget_mod.o \
    pio_kinds.o \

shr_timer_mod.o: \
    shr_sys_mod.o \
    shr_log_mod.o \
    shr_kind_mod.o \

shr_string_mod.o: \
    shr_sys_mod.o \
    shr_log_mod.o \
    shr_kind_mod.o \
    shr_timer_mod.o \

shr_const_mod.o: \
    shr_kind_mod.o \

shr_cal_mod.o: \
    ESMF_Mod.o \
    shr_sys_mod.o \
    shr_log_mod.o \
    shr_string_mod.o \
    shr_kind_mod.o \
    shr_const_mod.o \

time_manager.o: \
    spmd_utils.o \
    ESMF_Mod.o \
    dycore.o \
    mpishorthand.o \
    pio.o \
    string_utils.o \
    abortutils.o \
    shr_kind_mod.o \
    cam_logfile.o \
    shr_cal_mod.o \

physconst.o: \
    spmd_utils.o \
    abortutils.o \
    mpishorthand.o \
    shr_kind_mod.o \
    cam_logfile.o \
    shr_const_mod.o \
    namelist_utils.o \
    ppgrid.o \
    units.o \

constituents.o: \
    physconst.o \
    spmd_utils.o \
    abortutils.o \
    shr_kind_mod.o \
    cam_logfile.o \

commap.o: \
    pmgrid.o \
    shr_kind_mod.o \

infnan.o: \
    shr_kind_mod.o \

rgrid.o: \
    infnan.o \
    pmgrid.o \
    pspect.o \

spmd_dyn.o: \
    spmd_utils.o \
    parutilitiesmodule.o \
    infnan.o \
    pmgrid.o \
    mpishorthand.o \
    units.o \
    fv_control_mod.o \
    abortutils.o \
    decompmodule.o \
    shr_kind_mod.o \
    cam_logfile.o \
    namelist_utils.o \
    ghostmodule.o \

hycoef.o: \
    pio.o \
    spmd_utils.o \
    abortutils.o \
    pmgrid.o \
    shr_kind_mod.o \
    cam_logfile.o \

dyn_grid.o: \
    physconst.o \
    spmd_utils.o \
    commap.o \
    rgrid.o \
    spmd_dyn.o \
    abortutils.o \
    pmgrid.o \
    shr_kind_mod.o \
    hycoef.o \
    cam_logfile.o \
    shr_const_mod.o \

m_flow.o: \
    m_chars.o \

m_mpif90.o: \
    m_stdio.o \
    m_mpif.o \
    m_realkinds.o \

m_dropdead.o: \
    m_stdio.o \
    m_mpif90.o \

m_ioutil.o: \
    m_stdio.o \

m_mpout.o: \
    m_ioutil.o \
    m_dropdead.o \
    m_stdio.o \
    m_mpif90.o \

m_die.o: \
    m_flow.o \
    m_dropdead.o \
    m_stdio.o \
    m_mpout.o \
    m_mpif90.o \

m_MergeSorts.o: \
    m_die.o \
    m_stdio.o \
    m_realkinds.o \

phys_grid.o: \
    dyn_grid.o \
    physconst.o \
    spmd_utils.o \
    spmd_dyn.o \
    abortutils.o \
    dycore.o \
    pmgrid.o \
    mpishorthand.o \
    shr_kind_mod.o \
    perf_mod.o \
    cam_logfile.o \
    ppgrid.o \
    mod_comm.o \
    m_MergeSorts.o \

ioFileMod.o: \
    spmd_utils.o \
    abortutils.o \
    shr_kind_mod.o \
    cam_logfile.o \

cam_history_support.o: \
    spmd_utils.o \
    pio.o \
    abortutils.o \
    shr_kind_mod.o \
    cam_logfile.o \

cam_control_mod.o: \
    shr_kind_mod.o \

m_mall.o: \
    m_ioutil.o \
    m_die.o \
    m_stdio.o \
    m_chars.o \
    m_realkinds.o \

m_String.o: \
    m_mall.o \
    m_die.o \
    m_mpif90.o \

m_rankMerge.o: \
    m_realkinds.o \

m_IndexBin_logical.o: \
    m_die.o \
    m_stdio.o \

m_Permuter.o: \
    m_die.o \
    m_realkinds.o \

m_IndexBin_char.o: \
    m_die.o \
    m_stdio.o \

m_IndexBin_integer.o: \
    m_die.o \
    m_stdio.o \

m_SortingTools.o: \
    m_rankMerge.o \
    m_IndexBin_logical.o \
    m_Permuter.o \
    m_IndexBin_char.o \
    m_MergeSorts.o \
    m_IndexBin_integer.o \

m_List.o: \
    m_String.o \
    m_mall.o \
    m_die.o \
    m_stdio.o \
    m_mpif90.o \

m_TraceBack.o: \
    m_String.o \
    m_die.o \
    m_stdio.o \

m_AttrVect.o: \
    m_String.o \
    m_SortingTools.o \
    m_List.o \
    m_mall.o \
    m_die.o \
    m_TraceBack.o \
    m_stdio.o \
    m_realkinds.o \

m_GlobalMap.o: \
    m_die.o \
    m_stdio.o \
    m_mpif90.o \

m_FcComms.o: \
    m_die.o \
    m_mpif90.o \
    m_realkinds.o \

m_MCTWorld.o: \
    m_List.o \
    m_die.o \
    m_stdio.o \
    m_mpif90.o \

m_GlobalSegMap.o: \
    m_SortingTools.o \
    m_die.o \
    m_stdio.o \
    m_FcComms.o \
    m_MCTWorld.o \
    m_mpif90.o \

m_AttrVectComms.o: \
    m_AttrVect.o \
    m_String.o \
    m_List.o \
    m_GlobalMap.o \
    m_die.o \
    m_stdio.o \
    m_FcComms.o \
    m_GlobalSegMap.o \
    m_mpif90.o \
    m_realkinds.o \

m_SparseMatrix.o: \
    m_AttrVect.o \
    m_String.o \
    m_List.o \
    m_die.o \
    m_TraceBack.o \
    m_stdio.o \
    m_mpif90.o \
    m_realkinds.o \

m_SparseMatrixDecomp.o: \
    m_AttrVect.o \
    m_List.o \
    m_GlobalMap.o \
    m_AttrVectComms.o \
    m_die.o \
    m_SparseMatrix.o \
    m_GlobalSegMap.o \

m_SparseMatrixComms.o: \
    m_List.o \
    m_GlobalMap.o \
    m_AttrVectComms.o \
    m_die.o \
    m_SparseMatrixDecomp.o \
    m_stdio.o \
    m_SparseMatrix.o \
    m_GlobalSegMap.o \
    m_mpif90.o \

m_Navigator.o: \
    m_mall.o \
    m_die.o \
    m_stdio.o \

m_GlobalToLocal.o: \
    m_GlobalMap.o \
    m_die.o \
    m_Navigator.o \
    m_stdio.o \
    m_SparseMatrix.o \
    m_GlobalSegMap.o \
    m_mpif90.o \

m_SparseMatrixToMaps.o: \
    m_List.o \
    m_die.o \
    m_stdio.o \
    m_SparseMatrix.o \
    m_GlobalSegMap.o \
    m_mpif90.o \

m_ConvertMaps.o: \
    m_SortingTools.o \
    m_GlobalMap.o \
    m_die.o \
    m_stdio.o \
    m_GlobalSegMap.o \
    m_MCTWorld.o \

m_ExchangeMaps.o: \
    m_GlobalMap.o \
    m_ConvertMaps.o \
    m_die.o \
    m_stdio.o \
    m_GlobalSegMap.o \
    m_MCTWorld.o \
    m_mpif90.o \

m_Router.o: \
    m_GlobalToLocal.o \
    m_ExchangeMaps.o \
    m_die.o \
    m_stdio.o \
    m_GlobalSegMap.o \
    m_MCTWorld.o \
    m_Permuter.o \
    m_MergeSorts.o \
    m_mpif90.o \
    m_realkinds.o \

m_Rearranger.o: \
    m_AttrVect.o \
    m_Router.o \
    m_die.o \
    m_stdio.o \
    m_GlobalSegMap.o \
    m_MCTWorld.o \
    m_mpif90.o \
    m_realkinds.o \

m_SparseMatrixPlus.o: \
    m_SparseMatrixComms.o \
    m_String.o \
    m_List.o \
    m_GlobalToLocal.o \
    m_SparseMatrixToMaps.o \
    m_die.o \
    m_stdio.o \
    m_SparseMatrix.o \
    m_GlobalSegMap.o \
    m_Rearranger.o \
    m_mpif90.o \

m_GeneralGrid.o: \
    m_AttrVect.o \
    m_String.o \
    m_List.o \
    m_die.o \
    m_TraceBack.o \
    m_stdio.o \
    m_realkinds.o \

m_Transfer.o: \
    m_AttrVect.o \
    m_Router.o \
    m_die.o \
    m_stdio.o \
    m_MCTWorld.o \
    m_mpif90.o \

m_inpak90.o: \
    m_ioutil.o \
    m_mall.o \
    m_die.o \
    m_stdio.o \
    m_mpif90.o \
    m_realkinds.o \

m_GlobalSegMapComms.o: \
    m_die.o \
    m_stdio.o \
    m_GlobalSegMap.o \
    m_MCTWorld.o \
    m_mpif90.o \

m_Accumulator.o: \
    m_AttrVect.o \
    m_String.o \
    m_List.o \
    m_mall.o \
    m_die.o \
    m_stdio.o \
    m_realkinds.o \

m_MatAttrVectMul.o: \
    m_AttrVect.o \
    m_SparseMatrixPlus.o \
    m_String.o \
    m_List.o \
    m_die.o \
    m_stdio.o \
    m_SparseMatrix.o \
    m_Rearranger.o \
    m_mpif90.o \
    m_realkinds.o \

m_GeneralGridComms.o: \
    m_List.o \
    m_GlobalMap.o \
    m_AttrVectComms.o \
    m_GeneralGrid.o \
    m_die.o \
    m_stdio.o \
    m_GlobalSegMap.o \
    m_MCTWorld.o \
    m_mpif90.o \

mct_mod.o: \
    m_AttrVect.o \
    m_SparseMatrixPlus.o \
    m_String.o \
    m_SparseMatrixComms.o \
    m_List.o \
    shr_sys_mod.o \
    m_AttrVectComms.o \
    m_GlobalToLocal.o \
    m_Router.o \
    m_GeneralGrid.o \
    m_SparseMatrixToMaps.o \
    m_die.o \
    m_Transfer.o \
    shr_kind_mod.o \
    m_stdio.o \
    m_SparseMatrix.o \
    m_Rearranger.o \
    m_GlobalSegMap.o \
    m_inpak90.o \
    shr_const_mod.o \
    m_GlobalSegMapComms.o \
    m_Accumulator.o \
    m_MatAttrVectMul.o \
    m_GeneralGridComms.o \
    shr_mpi_mod.o \
    m_MCTWorld.o \
    m_Permuter.o \
    shr_log_mod.o \
    m_MergeSorts.o \

seq_comm_mct.o: \
    shr_sys_mod.o \
    mct_mod.o \
    shr_file_mod.o \
    shr_mpi_mod.o \

seq_drydep_mod.o: \
    shr_sys_mod.o \
    shr_log_mod.o \
    shr_file_mod.o \
    shr_kind_mod.o \
    shr_const_mod.o \

seq_flds_mod.o: \
    shr_sys_mod.o \
    seq_drydep_mod.o \
    mct_mod.o \
    shr_string_mod.o \

seq_io_mod.o: \
    shr_sys_mod.o \
    mct_mod.o \
    pio.o \
    shr_string_mod.o \
    shr_file_mod.o \
    seq_comm_mct.o \
    shr_kind_mod.o \
    shr_mpi_mod.o \
    seq_flds_mod.o \
    shr_cal_mod.o \

cam_pio_utils.o: \
    dyn_grid.o \
    spmd_utils.o \
    pio.o \
    cam_history_support.o \
    shr_string_mod.o \
    phys_grid.o \
    pio_support.o \
    abortutils.o \
    dycore.o \
    cam_control_mod.o \
    shr_kind_mod.o \
    perf_mod.o \
    cam_logfile.o \
    seq_io_mod.o \
    ppgrid.o \

sat_hist.o: \
    dyn_grid.o \
    spmd_utils.o \
    phys_grid.o \
    mpishorthand.o \
    ioFileMod.o \
    ppgrid.o \
    cam_pio_utils.o \
    units.o \
    physconst.o \
    time_manager.o \
    pio.o \
    cam_history_support.o \
    string_utils.o \
    abortutils.o \
    shr_kind_mod.o \
    perf_mod.o \
    cam_logfile.o \
    namelist_utils.o \
    pionfwrite_mod.o \

solar_data.o: \
    spmd_utils.o \
    infnan.o \
    ioFileMod.o \
    units.o \
    cam_pio_utils.o \
    time_manager.o \
    physconst.o \
    pio.o \
    abortutils.o \
    shr_kind_mod.o \
    cam_logfile.o \
    namelist_utils.o \

shr_orb_mod.o: \
    shr_sys_mod.o \
    shr_log_mod.o \
    shr_kind_mod.o \
    shr_const_mod.o \

shr_tInterp_mod.o: \
    shr_sys_mod.o \
    shr_log_mod.o \
    shr_orb_mod.o \
    shr_kind_mod.o \
    shr_const_mod.o \
    shr_cal_mod.o \

shr_stream_mod.o: \
    shr_sys_mod.o \
    shr_log_mod.o \
    shr_string_mod.o \
    shr_file_mod.o \
    shr_kind_mod.o \
    perf_mod.o \
    shr_const_mod.o \
    shr_mpi_mod.o \
    shr_cal_mod.o \
    netcdf.o \

shr_pcdf_mod.o: \
    shr_sys_mod.o \
    mct_mod.o \
    shr_log_mod.o \
    pio.o \
    shr_kind_mod.o \
    shr_const_mod.o \

shr_mct_mod.o: \
    shr_pcdf_mod.o \
    shr_sys_mod.o \
    mct_mod.o \
    shr_log_mod.o \
    pio.o \
    shr_kind_mod.o \
    shr_const_mod.o \
    shr_mpi_mod.o \

shr_map_mod.o: \
    shr_sys_mod.o \
    shr_log_mod.o \
    shr_kind_mod.o \
    shr_const_mod.o \
    shr_timer_mod.o \

shr_ncread_mod.o: \
    netcdf.o \
    shr_sys_mod.o \
    shr_log_mod.o \
    shr_string_mod.o \
    shr_file_mod.o \
    shr_kind_mod.o \

shr_dmodel_mod.o: \
    shr_sys_mod.o \
    shr_stream_mod.o \
    mct_mod.o \
    shr_log_mod.o \
    pio.o \
    shr_map_mod.o \
    shr_string_mod.o \
    shr_file_mod.o \
    shr_kind_mod.o \
    perf_mod.o \
    shr_const_mod.o \
    shr_mpi_mod.o \
    seq_flds_mod.o \
    shr_ncread_mod.o \

shr_strdata_mod.o: \
    shr_tInterp_mod.o \
    shr_sys_mod.o \
    shr_stream_mod.o \
    shr_mct_mod.o \
    mct_mod.o \
    shr_log_mod.o \
    pio.o \
    shr_orb_mod.o \
    shr_map_mod.o \
    shr_string_mod.o \
    shr_file_mod.o \
    shr_kind_mod.o \
    perf_mod.o \
    shr_const_mod.o \
    shr_mpi_mod.o \
    shr_dmodel_mod.o \
    shr_cal_mod.o \

shr_scam_mod.o: \
    shr_sys_mod.o \
    mct_mod.o \
    shr_log_mod.o \
    pio.o \
    shr_strdata_mod.o \
    shr_file_mod.o \
    shr_kind_mod.o \
    shr_dmodel_mod.o \
    shr_ncread_mod.o \

wrap_nf.o: \
    abortutils.o \
    shr_kind_mod.o \
    cam_logfile.o \

scamMod.o: \
    pmgrid.o \
    shr_scam_mod.o \
    shr_kind_mod.o \
    cam_logfile.o \
    wrap_nf.o \
    constituents.o \

error_messages.o: \
    netcdf.o \
    abortutils.o \
    cam_logfile.o \

interpolate_data.o: \
    abortutils.o \
    scamMod.o \
    shr_kind_mod.o \
    cam_logfile.o \

geopotential.o: \
    dycore.o \
    shr_kind_mod.o \
    ppgrid.o \

ref_pres.o: \
    dyn_grid.o \
    ppgrid.o \
    shr_kind_mod.o \

phys_control.o: \
    spmd_utils.o \
    abortutils.o \
    mpishorthand.o \
    shr_kind_mod.o \
    ref_pres.o \
    cam_logfile.o \
    namelist_utils.o \
    ppgrid.o \
    units.o \

physics_types.o: \
    physconst.o \
    infnan.o \
    phys_grid.o \
    abortutils.o \
    dycore.o \
    pmgrid.o \
    geopotential.o \
    scamMod.o \
    phys_control.o \
    shr_kind_mod.o \
    cam_logfile.o \
    shr_const_mod.o \
    ppgrid.o \
    constituents.o \

time_utils.o: \
    time_manager.o \
    abortutils.o \
    shr_kind_mod.o \
    cam_logfile.o \

repro_sum_mod.o: \
    shr_sys_mod.o \
    shr_kind_mod.o \
    perf_mod.o \

phys_gmean.o: \
    dyn_grid.o \
    physconst.o \
    spmd_utils.o \
    repro_sum_mod.o \
    rgrid.o \
    phys_grid.o \
    dycore.o \
    mpishorthand.o \
    physics_types.o \
    shr_kind_mod.o \
    perf_mod.o \
    cam_logfile.o \
    ppgrid.o \
    constituents.o \

mo_constants.o: \
    physconst.o \
    shr_kind_mod.o \

mo_flbc.o: \
    time_manager.o \
    pio.o \
    spmd_utils.o \
    time_utils.o \
    commap.o \
    string_utils.o \
    phys_grid.o \
    abortutils.o \
    interpolate_data.o \
    physics_types.o \
    shr_kind_mod.o \
    phys_gmean.o \
    ioFileMod.o \
    cam_logfile.o \
    mo_constants.o \
    ppgrid.o \
    m_types.o \
    constituents.o \
    cam_pio_utils.o \

chem_surfvals.o: \
    physconst.o \
    time_manager.o \
    spmd_utils.o \
    infnan.o \
    abortutils.o \
    error_messages.o \
    interpolate_data.o \
    mpishorthand.o \
    physics_types.o \
    shr_kind_mod.o \
    ioFileMod.o \
    cam_logfile.o \
    namelist_utils.o \
    mo_flbc.o \
    ppgrid.o \
    m_types.o \
    constituents.o \
    units.o \

cam_history_buffers.o: \
    dyn_grid.o \
    physconst.o \
    time_manager.o \
    pio.o \
    cam_history_support.o \
    phys_grid.o \
    abortutils.o \
    shr_kind_mod.o \
    cam_pio_utils.o \

filenames.o: \
    time_manager.o \
    abortutils.o \
    shr_kind_mod.o \
    cam_logfile.o \

cosp_share.o: \
    shr_kind_mod.o \
    ppgrid.o \

interp_mod.o: \
    pio.o \
    abortutils.o \
    shr_kind_mod.o \

cam_history.o: \
    physconst.o \
    time_manager.o \
    sat_hist.o \
    dyn_grid.o \
    pio.o \
    spmd_utils.o \
    cam_history_support.o \
    string_utils.o \
    solar_data.o \
    rgrid.o \
    shr_sys_mod.o \
    phys_grid.o \
    abortutils.o \
    dycore.o \
    pmgrid.o \
    cam_control_mod.o \
    scamMod.o \
    shr_kind_mod.o \
    hycoef.o \
    perf_mod.o \
    ioFileMod.o \
    chem_surfvals.o \
    cam_logfile.o \
    cam_history_buffers.o \
    pspect.o \
    filenames.o \
    ppgrid.o \
    cosp_share.o \
    interp_mod.o \
    cam_pio_utils.o \
    units.o \

advect_tend.o: \
    time_manager.o \
    shr_kind_mod.o \
    dynamics_vars.o \
    constituents.o \
    cam_history.o \

phys_buffer.o: \
    dyn_grid.o \
    pio.o \
    spmd_utils.o \
    string_utils.o \
    infnan.o \
    phys_grid.o \
    abortutils.o \
    mpishorthand.o \
    shr_kind_mod.o \
    cam_logfile.o \
    ppgrid.o \
    cam_pio_utils.o \

ghg_data.o: \
    physconst.o \
    phys_buffer.o \
    abortutils.o \
    error_messages.o \
    physics_types.o \
    shr_kind_mod.o \
    chem_surfvals.o \
    ppgrid.o \

radconstants.o: \
    abortutils.o \
    shr_kind_mod.o \

radae.o: \
    spmd_utils.o \
    infnan.o \
    pmgrid.o \
    phys_control.o \
    ioFileMod.o \
    radconstants.o \
    ppgrid.o \
    cam_pio_utils.o \
    pio.o \
    abortutils.o \
    shr_kind_mod.o \
    ref_pres.o \
    cam_logfile.o \
    filenames.o \

quicksort.o: \
    shr_kind_mod.o \

radlw.o: \
    radae.o \
    cam_history.o \
    phys_control.o \
    radconstants.o \
    quicksort.o \
    ppgrid.o \
    abortutils.o \
    scamMod.o \
    shr_kind_mod.o \

pkg_cldoptics.o: \
    phys_control.o \
    ppgrid.o \
    physconst.o \
    shr_kind_mod.o \

phys_debug_util.o: \
    spmd_utils.o \
    phys_grid.o \
    abortutils.o \
    mpishorthand.o \
    shr_kind_mod.o \
    cam_logfile.o \
    namelist_utils.o \
    units.o \

conv_water.o: \
    physconst.o \
    phys_buffer.o \
    abortutils.o \
    cam_history.o \
    phys_control.o \
    shr_kind_mod.o \
    perf_mod.o \
    phys_debug_util.o \
    cam_logfile.o \
    ppgrid.o \
    constituents.o \

param_cldoptics.o: \
    physconst.o \
    pkg_cldoptics.o \
    phys_buffer.o \
    cam_history.o \
    conv_water.o \
    phys_control.o \
    physics_types.o \
    shr_kind_mod.o \
    ppgrid.o \
    constituents.o \

mo_util.o: \
    shr_kind_mod.o \

rad_solar_var.o: \
    solar_data.o \
    radconstants.o \
    mo_util.o \
    abortutils.o \
    shr_kind_mod.o \

cmparray_mod.o: \
    shr_kind_mod.o \

radsw.o: \
    rad_solar_var.o \
    solar_data.o \
    cam_history.o \
    cmparray_mod.o \
    phys_control.o \
    radconstants.o \
    quicksort.o \
    ppgrid.o \
    abortutils.o \
    scamMod.o \
    shr_kind_mod.o \
    cam_logfile.o \

phys_prop.o: \
    spmd_utils.o \
    pio.o \
    abortutils.o \
    shr_kind_mod.o \
    ioFileMod.o \
    radconstants.o \
    cam_logfile.o \
    cam_pio_utils.o \

rad_constituents.o: \
    spmd_utils.o \
    phys_buffer.o \
    cam_history.o \
    mpishorthand.o \
    radconstants.o \
    ppgrid.o \
    units.o \
    physconst.o \
    phys_prop.o \
    abortutils.o \
    error_messages.o \
    physics_types.o \
    shr_kind_mod.o \
    cam_logfile.o \
    namelist_utils.o \
    constituents.o \

wv_saturation.o: \
    spmd_utils.o \
    abortutils.o \
    shr_kind_mod.o \
    cam_logfile.o \

modal_aer_opt.o: \
    physconst.o \
    pio.o \
    spmd_utils.o \
    cam_history_support.o \
    phys_buffer.o \
    abortutils.o \
    cam_history.o \
    mpishorthand.o \
    phys_control.o \
    physics_types.o \
    shr_kind_mod.o \
    perf_mod.o \
    ioFileMod.o \
    radconstants.o \
    cam_logfile.o \
    rad_constituents.o \
    namelist_utils.o \
    ppgrid.o \
    constituents.o \
    units.o \
    cam_pio_utils.o \

aer_rad_props.o: \
    physconst.o \
    physics_types.o \
    shr_kind_mod.o \
    cam_history_support.o \
    radconstants.o \
    phys_buffer.o \
    rad_constituents.o \
    wv_saturation.o \
    ppgrid.o \
    constituents.o \
    abortutils.o \
    cam_history.o \
    modal_aer_opt.o \
    phys_control.o \

camsrfexch_types.o: \
    infnan.o \
    phys_grid.o \
    seq_drydep_mod.o \
    abortutils.o \
    shr_kind_mod.o \
    cam_logfile.o \
    ppgrid.o \
    constituents.o \

radiation_data.o: \
    spmd_utils.o \
    phys_buffer.o \
    cam_history.o \
    phys_control.o \
    mpishorthand.o \
    ppgrid.o \
    units.o \
    cam_history_support.o \
    abortutils.o \
    camsrfexch_types.o \
    physics_types.o \
    shr_kind_mod.o \
    rad_constituents.o \
    namelist_utils.o \
    constituents.o \

cosp_utils.o: \
    cosp_constants.o \

cosp_types.o: \
    cosp_constants.o \
    cosp_utils.o \
    radar_simulator_types.o \

modis_simulator.o: \
    cosp_constants.o \
    abortutils.o \

cosp_modis_simulator.o: \
    cosp_constants.o \
    cosp_types.o \
    modis_simulator.o \

cosp_lidar.o: \
    cosp_constants.o \
    cosp_types.o \

cosp_misr_simulator.o: \
    cosp_constants.o \
    cosp_types.o \

llnl_stats.o: \
    cosp_constants.o \

lmd_ipsl_stats.o: \
    llnl_stats.o \

cosp_stats.o: \
    cosp_constants.o \
    cosp_types.o \
    lmd_ipsl_stats.o \
    llnl_stats.o \

array_lib.o: \
    mrgrnk.o \

format_input.o: \
    array_lib.o \

math_lib.o: \
    mrgrnk.o \
    array_lib.o \

cosp_radar.o: \
    cosp_constants.o \
    atmos_lib.o \
    cosp_types.o \
    cosp_utils.o \
    mrgrnk.o \
    format_input.o \
    radar_simulator_types.o \
    array_lib.o \
    math_lib.o \
    optics_lib.o \

cosp_isccp_simulator.o: \
    cosp_constants.o \
    cosp_types.o \

cosp_simulator.o: \
    cosp_lidar.o \
    cosp_types.o \
    cosp_misr_simulator.o \
    cosp_stats.o \
    cosp_radar.o \
    cosp_modis_simulator.o \
    cosp_isccp_simulator.o \

cosp.o: \
    cosp_types.o \
    cosp_simulator.o \
    cosp_modis_simulator.o \

cospsimulator_intr.o: \
    time_manager.o \
    physconst.o \
    spmd_utils.o \
    cosp_constants.o \
    cosp_types.o \
    cam_history_support.o \
    phys_buffer.o \
    phys_grid.o \
    abortutils.o \
    cam_history.o \
    cmparray_mod.o \
    error_messages.o \
    interpolate_data.o \
    camsrfexch_types.o \
    mpishorthand.o \
    phys_control.o \
    physics_types.o \
    shr_kind_mod.o \
    perf_mod.o \
    rad_constituents.o \
    namelist_utils.o \
    wv_saturation.o \
    ppgrid.o \
    cosp_share.o \
    cosp_modis_simulator.o \
    constituents.o \
    units.o \
    cam_pio_utils.o \
    cosp.o \

chemistry.o: \
    pio.o \
    phys_buffer.o \
    camsrfexch_types.o \
    physics_types.o \
    shr_kind_mod.o \

radheat.o: \
    phys_buffer.o \
    pmgrid.o \
    chemistry.o \
    ppgrid.o \
    physics_types.o \
    shr_kind_mod.o \

radiation.o: \
    spmd_utils.o \
    phys_buffer.o \
    radae.o \
    phys_grid.o \
    cam_history.o \
    interpolate_data.o \
    phys_control.o \
    radconstants.o \
    pspect.o \
    radlw.o \
    param_cldoptics.o \
    ppgrid.o \
    radsw.o \
    time_manager.o \
    physconst.o \
    shr_orb_mod.o \
    cam_history_support.o \
    aer_rad_props.o \
    abortutils.o \
    error_messages.o \
    camsrfexch_types.o \
    cam_control_mod.o \
    scamMod.o \
    physics_types.o \
    shr_kind_mod.o \
    perf_mod.o \
    cam_logfile.o \
    rad_constituents.o \
    radiation_data.o \
    cospsimulator_intr.o \
    cosp_share.o \
    radheat.o \

horizontal_interpolate.o: \
    abortutils.o \
    scamMod.o \
    shr_kind_mod.o \
    cam_logfile.o \
    shr_const_mod.o \

polar_avg.o: \
    dyn_grid.o \
    repro_sum_mod.o \
    phys_grid.o \
    dycore.o \
    mpishorthand.o \
    ppgrid.o \
    shr_kind_mod.o \

tracer_data.o: \
    dyn_grid.o \
    spmd_utils.o \
    horizontal_interpolate.o \
    phys_buffer.o \
    shr_sys_mod.o \
    phys_grid.o \
    dycore.o \
    interpolate_data.o \
    mpishorthand.o \
    ioFileMod.o \
    mo_constants.o \
    ppgrid.o \
    polar_avg.o \
    cam_pio_utils.o \
    physconst.o \
    time_manager.o \
    pio.o \
    string_utils.o \
    mo_util.o \
    shr_file_mod.o \
    abortutils.o \
    cam_control_mod.o \
    physics_types.o \
    shr_kind_mod.o \
    perf_mod.o \
    ref_pres.o \
    cam_logfile.o \

prescribed_ghg.o: \
    spmd_utils.o \
    phys_buffer.o \
    cam_history.o \
    mpishorthand.o \
    ppgrid.o \
    tracer_data.o \
    units.o \
    physconst.o \
    pio.o \
    string_utils.o \
    abortutils.o \
    error_messages.o \
    physics_types.o \
    shr_kind_mod.o \
    cam_logfile.o \
    namelist_utils.o \

prescribed_aero.o: \
    spmd_utils.o \
    phys_buffer.o \
    cam_history.o \
    mpishorthand.o \
    ppgrid.o \
    tracer_data.o \
    units.o \
    pio.o \
    string_utils.o \
    abortutils.o \
    error_messages.o \
    physics_types.o \
    shr_kind_mod.o \
    cam_logfile.o \
    namelist_utils.o \

trb_mtn_stress.o: \
    shr_kind_mod.o \
    cam_logfile.o \

phys_debug.o: \
    camsrfexch_types.o \
    physics_types.o \
    shr_kind_mod.o \
    cam_logfile.o \
    phys_debug_util.o \
    ppgrid.o \
    constituents.o \

hb_diff.o: \
    spmd_utils.o \
    phys_debug.o \
    shr_kind_mod.o \
    cam_logfile.o \
    ppgrid.o \
    constituents.o \

upper_bc.o: \
    physics_types.o \
    shr_kind_mod.o \

molec_diff.o: \
    physconst.o \
    infnan.o \
    abortutils.o \
    phys_control.o \
    physics_types.o \
    perf_mod.o \
    cam_logfile.o \
    upper_bc.o \
    ppgrid.o \
    constituents.o \

diffusion_solver.o: \
    time_manager.o \
    phys_control.o \
    phys_debug_util.o \
    cam_logfile.o \

eddy_diff.o: \
    physconst.o \
    time_manager.o \
    abortutils.o \
    cam_history.o \
    phys_control.o \
    phys_debug_util.o \
    cam_logfile.o \
    diffusion_solver.o \
    ppgrid.o \

vertical_diffusion.o: \
    spmd_utils.o \
    phys_buffer.o \
    infnan.o \
    cam_history.o \
    phys_control.o \
    trb_mtn_stress.o \
    ppgrid.o \
    hb_diff.o \
    time_manager.o \
    physconst.o \
    molec_diff.o \
    abortutils.o \
    geopotential.o \
    physics_types.o \
    shr_kind_mod.o \
    perf_mod.o \
    ref_pres.o \
    cam_logfile.o \
    wv_saturation.o \
    diffusion_solver.o \
    eddy_diff.o \
    constituents.o \

boundarydata.o: \
    time_manager.o \
    physconst.o \
    spmd_utils.o \
    infnan.o \
    abortutils.o \
    error_messages.o \
    interpolate_data.o \
    mpishorthand.o \
    physics_types.o \
    shr_kind_mod.o \
    ioFileMod.o \
    ref_pres.o \
    cam_logfile.o \
    ppgrid.o \

cam3_ozone_data.o: \
    physconst.o \
    spmd_utils.o \
    boundarydata.o \
    phys_buffer.o \
    abortutils.o \
    cam_history.o \
    mpishorthand.o \
    physics_types.o \
    shr_kind_mod.o \
    cam_logfile.o \
    namelist_utils.o \
    ppgrid.o \
    units.o \

aoa_tracers.o: \
    dyn_grid.o \
    time_manager.o \
    physconst.o \
    physics_types.o \
    spmd_utils.o \
    shr_kind_mod.o \
    cam_logfile.o \
    namelist_utils.o \
    phys_grid.o \
    ppgrid.o \
    abortutils.o \
    constituents.o \
    cam_history.o \
    dycore.o \
    units.o \
    mpishorthand.o \

iondrag.o: \
    phys_buffer.o \
    abortutils.o \
    physics_types.o \
    shr_kind_mod.o \
    ppgrid.o \

cam3_aero_data.o: \
    physconst.o \
    time_manager.o \
    spmd_utils.o \
    boundarydata.o \
    phys_buffer.o \
    infnan.o \
    phys_grid.o \
    abortutils.o \
    error_messages.o \
    interpolate_data.o \
    mpishorthand.o \
    scamMod.o \
    physics_types.o \
    shr_kind_mod.o \
    perf_mod.o \
    ioFileMod.o \
    cam_logfile.o \
    namelist_utils.o \
    ppgrid.o \
    shr_scam_mod.o \
    units.o \

tracers_suite.o: \
    ppgrid.o \
    abortutils.o \
    shr_kind_mod.o \
    ref_pres.o \
    cam_logfile.o \

tracers.o: \
    cam_history.o \
    ppgrid.o \
    physconst.o \
    tracers_suite.o \
    physics_types.o \
    shr_kind_mod.o \
    cam_logfile.o \
    constituents.o \

tropopause.o: \
    dyn_grid.o \
    spmd_utils.o \
    phys_grid.o \
    cam_history.o \
    interpolate_data.o \
    mpishorthand.o \
    ioFileMod.o \
    ppgrid.o \
    cam_pio_utils.o \
    units.o \
    time_manager.o \
    physconst.o \
    pio.o \
    cam_history_support.o \
    abortutils.o \
    physics_types.o \
    shr_kind_mod.o \
    cam_logfile.o \
    namelist_utils.o \

prescribed_volcaero.o: \
    spmd_utils.o \
    phys_buffer.o \
    cam_history.o \
    mpishorthand.o \
    ppgrid.o \
    tracer_data.o \
    units.o \
    physconst.o \
    pio.o \
    tropopause.o \
    string_utils.o \
    abortutils.o \
    error_messages.o \
    physics_types.o \
    shr_kind_mod.o \
    cam_logfile.o \
    namelist_utils.o \

prescribed_ozone.o: \
    spmd_utils.o \
    phys_buffer.o \
    cam_history.o \
    phys_control.o \
    mpishorthand.o \
    ppgrid.o \
    tracer_data.o \
    units.o \
    physconst.o \
    pio.o \
    string_utils.o \
    abortutils.o \
    error_messages.o \
    cam_control_mod.o \
    physics_types.o \
    shr_kind_mod.o \
    cam_logfile.o \
    namelist_utils.o \

aircraft_emit.o: \
    physconst.o \
    physics_types.o \
    spmd_utils.o \
    shr_kind_mod.o \
    perf_mod.o \
    phys_buffer.o \
    cam_logfile.o \
    string_utils.o \
    namelist_utils.o \
    phys_grid.o \
    ppgrid.o \
    tracer_data.o \
    constituents.o \
    abortutils.o \
    cam_history.o \
    units.o \
    mpishorthand.o \

modal_aero_deposition.o: \
    abortutils.o \
    camsrfexch_types.o \
    shr_kind_mod.o \
    ppgrid.o \
    constituents.o \

aerodep_flx.o: \
    physics_types.o \
    spmd_utils.o \
    shr_kind_mod.o \
    cam_logfile.o \
    namelist_utils.o \
    ppgrid.o \
    modal_aero_deposition.o \
    tracer_data.o \
    abortutils.o \
    cam_history.o \
    camsrfexch_types.o \
    units.o \
    mpishorthand.o \

advnce.o: \
    ghg_data.o \
    physics_types.o \
    shr_kind_mod.o \
    radiation.o \
    chemistry.o \
    perf_mod.o \
    prescribed_ghg.o \
    chem_surfvals.o \
    prescribed_aero.o \
    phys_buffer.o \
    vertical_diffusion.o \
    cam3_ozone_data.o \
    solar_data.o \
    aoa_tracers.o \
    iondrag.o \
    cam3_aero_data.o \
    ppgrid.o \
    tracers.o \
    prescribed_volcaero.o \
    prescribed_ozone.o \
    aircraft_emit.o \
    aerodep_flx.o \
    camsrfexch_types.o \
    radheat.o \

drydep_mod.o: \
    shr_kind_mod.o \
    ppgrid.o \

wetdep.o: \
    phys_control.o \
    ppgrid.o \
    physconst.o \
    shr_kind_mod.o \
    cam_logfile.o \

dust_sediment_mod.o: \
    physconst.o \
    abortutils.o \
    shr_kind_mod.o \
    cam_logfile.o \
    ppgrid.o \

dust_intr.o: \
    error_function.o \
    physconst.o \
    pio.o \
    spmd_utils.o \
    phys_grid.o \
    abortutils.o \
    cam_history.o \
    interpolate_data.o \
    camsrfexch_types.o \
    phys_control.o \
    physics_types.o \
    shr_kind_mod.o \
    ioFileMod.o \
    drydep_mod.o \
    wetdep.o \
    cam_logfile.o \
    mo_constants.o \
    ppgrid.o \
    dust_sediment_mod.o \
    constituents.o \
    aerodep_flx.o \
    cam_pio_utils.o \

progseasalts_intr.o: \
    spmd_utils.o \
    phys_grid.o \
    cam_history.o \
    phys_control.o \
    drydep_mod.o \
    wetdep.o \
    mo_constants.o \
    ppgrid.o \
    dust_sediment_mod.o \
    time_manager.o \
    physconst.o \
    physics_types.o \
    shr_kind_mod.o \
    cam_logfile.o \
    wv_saturation.o \
    constituents.o \

scyc.o: \
    cam_logfile.o \

aerosol_intr.o: \
    time_manager.o \
    physconst.o \
    physics_types.o \
    spmd_utils.o \
    shr_kind_mod.o \
    perf_mod.o \
    dust_intr.o \
    drydep_mod.o \
    progseasalts_intr.o \
    wetdep.o \
    phys_buffer.o \
    cam_logfile.o \
    namelist_utils.o \
    phys_grid.o \
    ppgrid.o \
    abortutils.o \
    constituents.o \
    scyc.o \
    cam_history.o \
    units.o \
    camsrfexch_types.o \
    mpishorthand.o \
    phys_control.o \

history_scam.o: \
    cam_history.o \
    pmgrid.o \
    scamMod.o \
    shr_kind_mod.o \
    ppgrid.o \
    constituents.o \

xpavg_mod.o: \
    shr_kind_mod.o \

ncdio_atm.o: \
    dyn_grid.o \
    spmd_utils.o \
    pio.o \
    string_utils.o \
    xpavg_mod.o \
    shr_sys_mod.o \
    phys_grid.o \
    abortutils.o \
    dycore.o \
    scamMod.o \
    shr_kind_mod.o \
    cam_logfile.o \
    ppgrid.o \
    shr_scam_mod.o \
    constituents.o \
    cam_pio_utils.o \

metdata.o: \
    time_manager.o \
    pio.o \
    spmd_utils.o \
    string_utils.o \
    shr_sys_mod.o \
    infnan.o \
    dynamics_vars.o \
    phys_grid.o \
    ncdio_atm.o \
    shr_file_mod.o \
    abortutils.o \
    cam_history.o \
    pmgrid.o \
    camsrfexch_types.o \
    cam_control_mod.o \
    mpishorthand.o \
    physics_types.o \
    shr_kind_mod.o \
    hycoef.o \
    perf_mod.o \
    ioFileMod.o \
    cam_logfile.o \
    shr_const_mod.o \
    ppgrid.o \
    mod_comm.o \
    shr_cal_mod.o \
    cam_pio_utils.o \

co2_data_flux.o: \
    time_manager.o \
    spmd_utils.o \
    phys_grid.o \
    abortutils.o \
    error_messages.o \
    interpolate_data.o \
    mpishorthand.o \
    shr_kind_mod.o \
    ioFileMod.o \
    cam_logfile.o \
    ppgrid.o \

co2_cycle.o: \
    time_manager.o \
    physconst.o \
    spmd_utils.o \
    co2_data_flux.o \
    abortutils.o \
    cam_history.o \
    mpishorthand.o \
    physics_types.o \
    shr_kind_mod.o \
    chem_surfvals.o \
    namelist_utils.o \
    ppgrid.o \
    constituents.o \
    units.o \

buffer.o: \
    infnan.o \
    shr_kind_mod.o \
    ppgrid.o \
    constituents.o \

comsrf.o: \
    infnan.o \
    abortutils.o \
    cam_control_mod.o \
    shr_kind_mod.o \
    ppgrid.o \

restart_physics.o: \
    dyn_grid.o \
    spmd_utils.o \
    prescribed_ghg.o \
    phys_buffer.o \
    radae.o \
    phys_grid.o \
    chemistry.o \
    ioFileMod.o \
    ppgrid.o \
    prescribed_ozone.o \
    cam_pio_utils.o \
    units.o \
    pio.o \
    prescribed_aero.o \
    prescribed_volcaero.o \
    abortutils.o \
    co2_cycle.o \
    cam_control_mod.o \
    camsrfexch_types.o \
    shr_kind_mod.o \
    radiation.o \
    cam_logfile.o \
    cospsimulator_intr.o \
    buffer.o \
    comsrf.o \
    constituents.o \

pfixer.o: \
    time_manager.o \
    spmd_utils.o \
    parutilitiesmodule.o \
    commap.o \
    dynamics_vars.o \
    metdata.o \
    spmd_dyn.o \
    abortutils.o \
    mpishorthand.o \
    shr_kind_mod.o \
    hycoef.o \
    cam_logfile.o \
    mod_comm.o \

ctem.o: \
    physconst.o \
    spmd_utils.o \
    parutilitiesmodule.o \
    dynamics_vars.o \
    abortutils.o \
    cam_history.o \
    pmgrid.o \
    interpolate_data.o \
    mpishorthand.o \
    shr_kind_mod.o \
    hycoef.o \
    cam_logfile.o \
    namelist_utils.o \
    units.o \

diag_module.o: \
    dynamics_vars.o \
    shr_kind_mod.o \
    mod_comm.o \

dyn_comp.o: \
    physconst.o \
    time_manager.o \
    spmd_utils.o \
    pio.o \
    parutilitiesmodule.o \
    infnan.o \
    fv_control_mod.o \
    dynamics_vars.o \
    metdata.o \
    spmd_dyn.o \
    pfixer.o \
    abortutils.o \
    cam_history.o \
    dycore.o \
    pmgrid.o \
    phys_control.o \
    mpishorthand.o \
    shr_kind_mod.o \
    hycoef.o \
    perf_mod.o \
    ctem.o \
    cam_logfile.o \
    ppgrid.o \
    mod_comm.o \
    constituents.o \
    diag_module.o \

dyn_internal_state.o: \
    dynamics_vars.o \

restart_dynamics.o: \
    dyn_grid.o \
    dynamics_vars.o \
    pmgrid.o \
    hycoef.o \
    cam_pio_utils.o \
    time_manager.o \
    pio.o \
    fv_control_mod.o \
    metdata.o \
    abortutils.o \
    shr_kind_mod.o \
    cam_logfile.o \
    dyn_comp.o \
    dyn_internal_state.o \
    constituents.o \

cam_restart.o: \
    time_manager.o \
    pio.o \
    spmd_utils.o \
    rgrid.o \
    infnan.o \
    restart_physics.o \
    phys_grid.o \
    spmd_dyn.o \
    abortutils.o \
    cam_history.o \
    dycore.o \
    pmgrid.o \
    camsrfexch_types.o \
    mpishorthand.o \
    restart_dynamics.o \
    shr_kind_mod.o \
    radiation.o \
    ioFileMod.o \
    chem_surfvals.o \
    ref_pres.o \
    cam_logfile.o \
    dyn_comp.o \
    filenames.o \
    ppgrid.o \
    cam_pio_utils.o \
    units.o \

readinitial.o: \
    pmgrid.o \
    pio.o \
    abortutils.o \
    scamMod.o \
    shr_kind_mod.o \
    cam_logfile.o \

history_defaults.o: \
    cam_history.o \
    dycore.o \
    pmgrid.o \
    phys_control.o \
    shr_kind_mod.o \
    ppgrid.o \
    constituents.o \

uw_conv.o: \
    error_function.o \
    abortutils.o \
    cam_logfile.o \

uwshcu.o: \
    spmd_utils.o \
    cam_history.o \
    mpishorthand.o \
    ppgrid.o \
    units.o \
    abortutils.o \
    error_function.o \
    cam_logfile.o \
    namelist_utils.o \
    wv_saturation.o \
    constituents.o \

cldwat.o: \
    spmd_utils.o \
    phys_grid.o \
    abortutils.o \
    dycore.o \
    pmgrid.o \
    cam_control_mod.o \
    phys_control.o \
    mpishorthand.o \
    shr_kind_mod.o \
    ref_pres.o \
    cam_logfile.o \
    namelist_utils.o \
    wv_saturation.o \
    ppgrid.o \
    comsrf.o \
    units.o \

zm_conv.o: \
    spmd_utils.o \
    phys_grid.o \
    cldwat.o \
    dycore.o \
    phys_control.o \
    mpishorthand.o \
    ppgrid.o \
    units.o \
    physconst.o \
    abortutils.o \
    shr_kind_mod.o \
    cam_logfile.o \
    namelist_utils.o \
    wv_saturation.o \
    constituents.o \

hk_conv.o: \
    spmd_utils.o \
    phys_grid.o \
    abortutils.o \
    dycore.o \
    mpishorthand.o \
    shr_kind_mod.o \
    cam_logfile.o \
    namelist_utils.o \
    wv_saturation.o \
    ppgrid.o \
    constituents.o \
    units.o \

convect_shallow.o: \
    time_manager.o \
    uw_conv.o \
    physconst.o \
    spmd_utils.o \
    uwshcu.o \
    phys_buffer.o \
    abortutils.o \
    cam_history.o \
    pmgrid.o \
    phys_control.o \
    physics_types.o \
    shr_kind_mod.o \
    zm_conv.o \
    hk_conv.o \
    cam_logfile.o \
    wv_saturation.o \
    ppgrid.o \
    constituents.o \

cloud_fraction.o: \
    physconst.o \
    spmd_utils.o \
    phys_buffer.o \
    phys_grid.o \
    abortutils.o \
    dycore.o \
    phys_control.o \
    mpishorthand.o \
    shr_kind_mod.o \
    chemistry.o \
    ref_pres.o \
    cam_logfile.o \
    namelist_utils.o \
    wv_saturation.o \
    ppgrid.o \
    units.o \

cldwat2m_macro.o: \
    physconst.o \
    time_manager.o \
    spmd_utils.o \
    abortutils.o \
    cam_history.o \
    shr_kind_mod.o \
    cloud_fraction.o \
    phys_debug_util.o \
    cam_logfile.o \
    wv_saturation.o \
    ppgrid.o \
    constituents.o \

ndrop.o: \
    time_manager.o \
    physconst.o \
    phys_grid.o \
    error_function.o \
    abortutils.o \
    cam_history.o \
    physics_types.o \
    shr_kind_mod.o \
    cam_logfile.o \
    wv_saturation.o \
    ppgrid.o \
    constituents.o \

cldwat2m_micro.o: \
    physconst.o \
    spmd_utils.o \
    cam_history.o \
    phys_control.o \
    shr_kind_mod.o \
    cldwat2m_macro.o \
    cam_logfile.o \
    wv_saturation.o \
    ppgrid.o \

microp_aero.o: \
    physconst.o \
    spmd_utils.o \
    error_function.o \
    abortutils.o \
    cam_history.o \
    phys_control.o \
    shr_kind_mod.o \
    cldwat2m_macro.o \
    cam_logfile.o \
    rad_constituents.o \
    ndrop.o \
    wv_saturation.o \
    ppgrid.o \
    constituents.o \

microp_driver.o: \
    time_manager.o \
    physconst.o \
    phys_buffer.o \
    convect_shallow.o \
    abortutils.o \
    cam_history.o \
    cldwat.o \
    dycore.o \
    conv_water.o \
    phys_control.o \
    physics_types.o \
    shr_kind_mod.o \
    perf_mod.o \
    cldwat2m_macro.o \
    phys_debug_util.o \
    cam_logfile.o \
    rad_constituents.o \
    ndrop.o \
    cldwat2m_micro.o \
    microp_aero.o \
    ppgrid.o \
    constituents.o \

pkg_cld_sediment.o: \
    spmd_utils.o \
    pkg_cldoptics.o \
    cldwat.o \
    mpishorthand.o \
    ppgrid.o \
    units.o \
    physconst.o \
    abortutils.o \
    shr_kind_mod.o \
    cam_logfile.o \
    namelist_utils.o \

stratiform.o: \
    pkg_cldoptics.o \
    phys_buffer.o \
    convect_shallow.o \
    cldwat.o \
    cam_history.o \
    dycore.o \
    phys_control.o \
    chemistry.o \
    cldwat2m_macro.o \
    ppgrid.o \
    time_manager.o \
    physconst.o \
    pkg_cld_sediment.o \
    abortutils.o \
    physics_types.o \
    shr_kind_mod.o \
    cloud_fraction.o \
    perf_mod.o \
    phys_debug_util.o \
    cam_logfile.o \
    cldwat2m_micro.o \
    microp_aero.o \
    constituents.o \

inidat.o: \
    dyn_grid.o \
    physconst.o \
    pio.o \
    spmd_utils.o \
    cam_history_support.o \
    commap.o \
    aoa_tracers.o \
    aerosol_intr.o \
    fv_control_mod.o \
    dynamics_vars.o \
    phys_grid.o \
    spmd_dyn.o \
    ncdio_atm.o \
    abortutils.o \
    pmgrid.o \
    co2_cycle.o \
    cam_control_mod.o \
    phys_control.o \
    mpishorthand.o \
    microp_driver.o \
    shr_kind_mod.o \
    chemistry.o \
    cam_logfile.o \
    dyn_comp.o \
    dyn_internal_state.o \
    tracers.o \
    stratiform.o \
    constituents.o \
    mod_comm.o \

startup_initialconds.o: \
    spmd_utils.o \
    phys_buffer.o \
    radae.o \
    ioFileMod.o \
    readinitial.o \
    cam_pio_utils.o \
    pio.o \
    shr_kind_mod.o \
    history_defaults.o \
    dyn_comp.o \
    buffer.o \
    filenames.o \
    inidat.o \
    comsrf.o \

inital.o: \
    dynamics_vars.o \
    phys_grid.o \
    startup_initialconds.o \
    shr_kind_mod.o \
    chem_surfvals.o \
    ref_pres.o \
    dyn_comp.o \
    dyn_internal_state.o \

check_energy.o: \
    time_manager.o \
    physconst.o \
    spmd_utils.o \
    phys_buffer.o \
    abortutils.o \
    cam_history.o \
    physics_types.o \
    shr_kind_mod.o \
    phys_gmean.o \
    cam_logfile.o \
    ppgrid.o \
    constituents.o \

dp_coupling.o: \
    physconst.o \
    phys_buffer.o \
    rgrid.o \
    dynamics_vars.o \
    metdata.o \
    phys_grid.o \
    spmd_dyn.o \
    abortutils.o \
    pmgrid.o \
    check_energy.o \
    geopotential.o \
    phys_control.o \
    physics_types.o \
    shr_kind_mod.o \
    perf_mod.o \
    ctem.o \
    cam_logfile.o \
    shr_const_mod.o \
    dyn_comp.o \
    ppgrid.o \
    constituents.o \

fv_prints.o: \
    parutilitiesmodule.o \
    repro_sum_mod.o \
    dynamics_vars.o \
    phys_grid.o \
    camsrfexch_types.o \
    mpishorthand.o \
    physics_types.o \
    shr_kind_mod.o \
    perf_mod.o \
    phys_gmean.o \
    cam_logfile.o \
    ppgrid.o \
    constituents.o \

stepon.o: \
    spmd_utils.o \
    advect_tend.o \
    phys_buffer.o \
    shr_sys_mod.o \
    dynamics_vars.o \
    pmgrid.o \
    mpishorthand.o \
    hycoef.o \
    ppgrid.o \
    time_manager.o \
    physconst.o \
    commap.o \
    fv_control_mod.o \
    abortutils.o \
    camsrfexch_types.o \
    cam_control_mod.o \
    physics_types.o \
    shr_kind_mod.o \
    dp_coupling.o \
    perf_mod.o \
    cam_logfile.o \
    dyn_comp.o \
    dyn_internal_state.o \
    constituents.o \
    fv_prints.o \

ionosphere.o: \
    phys_buffer.o \
    abortutils.o \
    physics_types.o \
    shr_kind_mod.o \

cloud_diagnostics.o: \
    phys_buffer.o \
    physics_types.o \

cloud_rad_props.o: \
    phys_buffer.o \
    physics_types.o \
    radconstants.o \
    ppgrid.o \

tidal_diag.o: \
    cam_history.o \
    ppgrid.o \
    time_manager.o \
    physics_types.o \
    shr_kind_mod.o \
    shr_const_mod.o \

constituent_burden.o: \
    physconst.o \
    cam_history.o \
    shr_kind_mod.o \
    physics_types.o \
    ppgrid.o \
    constituents.o \

cam_diagnostics.o: \
    time_manager.o \
    physconst.o \
    tidal_diag.o \
    phys_buffer.o \
    infnan.o \
    abortutils.o \
    cam_history.o \
    dycore.o \
    check_energy.o \
    co2_cycle.o \
    constituent_burden.o \
    interpolate_data.o \
    cam_control_mod.o \
    camsrfexch_types.o \
    phys_control.o \
    scamMod.o \
    physics_types.o \
    shr_kind_mod.o \
    chemistry.o \
    buffer.o \
    wv_saturation.o \
    ppgrid.o \
    constituents.o \

flux_avg.o: \
    phys_buffer.o \
    phys_debug.o \
    phys_grid.o \
    camsrfexch_types.o \
    physics_types.o \
    shr_kind_mod.o \
    ppgrid.o \

macrop_driver.o: \
    time_manager.o \
    physconst.o \
    phys_buffer.o \
    convect_shallow.o \
    cldwat.o \
    cam_history.o \
    phys_control.o \
    physics_types.o \
    shr_kind_mod.o \
    cloud_fraction.o \
    perf_mod.o \
    cldwat2m_macro.o \
    cam_logfile.o \
    ppgrid.o \
    constituents.o \

gw_drag.o: \
    spmd_utils.o \
    phys_grid.o \
    abortutils.o \
    cam_history.o \
    dycore.o \
    phys_control.o \
    mpishorthand.o \
    scamMod.o \
    physics_types.o \
    shr_kind_mod.o \
    cam_logfile.o \
    namelist_utils.o \
    ppgrid.o \
    units.o \

zm_conv_intr.o: \
    spmd_utils.o \
    phys_buffer.o \
    phys_grid.o \
    cam_history.o \
    pmgrid.o \
    phys_control.o \
    ppgrid.o \
    time_manager.o \
    physconst.o \
    check_energy.o \
    error_messages.o \
    physics_types.o \
    shr_kind_mod.o \
    perf_mod.o \
    zm_conv.o \
    cam_logfile.o \
    constituents.o \

convect_deep.o: \
    physconst.o \
    spmd_utils.o \
    phys_buffer.o \
    abortutils.o \
    cam_history.o \
    pmgrid.o \
    phys_control.o \
    physics_types.o \
    shr_kind_mod.o \
    cam_logfile.o \
    gw_drag.o \
    ppgrid.o \
    constituents.o \
    zm_conv_intr.o \

rayleigh_friction.o: \
    spmd_utils.o \
    ppgrid.o \
    physics_types.o \
    shr_kind_mod.o \
    cam_logfile.o \

majorsp_diffusion.o: \
    abortutils.o \
    physics_types.o \
    shr_kind_mod.o \
    ppgrid.o \

sslt_rebin.o: \
    phys_buffer.o \
    cam_history.o \
    ppgrid.o \
    physics_types.o \
    shr_kind_mod.o \
    constituents.o \

physpkg.o: \
    spmd_utils.o \
    rad_solar_var.o \
    prescribed_ghg.o \
    phys_buffer.o \
    cam3_ozone_data.o \
    solar_data.o \
    aerosol_intr.o \
    infnan.o \
    convect_shallow.o \
    phys_grid.o \
    ionosphere.o \
    cloud_diagnostics.o \
    cloud_rad_props.o \
    cam_history.o \
    cam_diagnostics.o \
    cldwat.o \
    dycore.o \
    conv_water.o \
    mpishorthand.o \
    phys_control.o \
    chemistry.o \
    flux_avg.o \
    ppgrid.o \
    prescribed_ozone.o \
    aircraft_emit.o \
    polar_avg.o \
    macrop_driver.o \
    time_manager.o \
    physconst.o \
    pio.o \
    prescribed_aero.o \
    tropopause.o \
    aer_rad_props.o \
    aoa_tracers.o \
    metdata.o \
    ncdio_atm.o \
    prescribed_volcaero.o \
    abortutils.o \
    convect_deep.o \
    rayleigh_friction.o \
    check_energy.o \
    co2_cycle.o \
    camsrfexch_types.o \
    cam_control_mod.o \
    startup_initialconds.o \
    scamMod.o \
    microp_driver.o \
    shr_kind_mod.o \
    physics_types.o \
    cloud_fraction.o \
    radiation.o \
    perf_mod.o \
    phys_gmean.o \
    ref_pres.o \
    cam_logfile.o \
    phys_debug_util.o \
    vertical_diffusion.o \
    rad_constituents.o \
    gw_drag.o \
    buffer.o \
    iondrag.o \
    cam3_aero_data.o \
    majorsp_diffusion.o \
    tracers.o \
    comsrf.o \
    sslt_rebin.o \
    constituents.o \
    stratiform.o \
    aerodep_flx.o \
    radheat.o \

cam_comp.o: \
    time_manager.o \
    history_scam.o \
    spmd_utils.o \
    phys_buffer.o \
    infnan.o \
    shr_sys_mod.o \
    metdata.o \
    abortutils.o \
    cam_history.o \
    cam_restart.o \
    dycore.o \
    pmgrid.o \
    startup_initialconds.o \
    cam_control_mod.o \
    camsrfexch_types.o \
    mpishorthand.o \
    scamMod.o \
    physics_types.o \
    shr_kind_mod.o \
    perf_mod.o \
    inital.o \
    history_defaults.o \
    stepon.o \
    cam_logfile.o \
    dyn_comp.o \
    ppgrid.o \
    physpkg.o \
    units.o \
    cam_pio_utils.o \

seq_infodata_mod.o: \
    shr_sys_mod.o \
    shr_orb_mod.o \
    shr_string_mod.o \
    shr_file_mod.o \
    seq_comm_mct.o \
    shr_kind_mod.o \
    seq_io_mod.o \
    shr_mpi_mod.o \

seq_cdata_mod.o: \
    shr_sys_mod.o \
    mct_mod.o \
    seq_comm_mct.o \
    shr_kind_mod.o \
    seq_infodata_mod.o \

runtime_opts.o: \
    spmd_utils.o \
    uwshcu.o \
    prescribed_ghg.o \
    phys_buffer.o \
    repro_sum_mod.o \
    cam3_ozone_data.o \
    solar_data.o \
    phys_grid.o \
    cldwat.o \
    cam_restart.o \
    cam_diagnostics.o \
    cam_history.o \
    dycore.o \
    pmgrid.o \
    mpishorthand.o \
    phys_control.o \
    chemistry.o \
    chem_surfvals.o \
    pspect.o \
    prescribed_ozone.o \
    aircraft_emit.o \
    units.o \
    sat_hist.o \
    physconst.o \
    time_manager.o \
    shr_string_mod.o \
    prescribed_aero.o \
    tropopause.o \
    pkg_cld_sediment.o \
    rgrid.o \
    aoa_tracers.o \
    metdata.o \
    prescribed_volcaero.o \
    abortutils.o \
    rayleigh_friction.o \
    check_energy.o \
    modal_aer_opt.o \
    co2_cycle.o \
    cam_control_mod.o \
    scamMod.o \
    shr_kind_mod.o \
    cloud_fraction.o \
    radiation.o \
    zm_conv.o \
    phys_debug_util.o \
    hk_conv.o \
    cam_logfile.o \
    radiation_data.o \
    rad_constituents.o \
    gw_drag.o \
    namelist_utils.o \
    cospsimulator_intr.o \
    iondrag.o \
    filenames.o \
    cam3_aero_data.o \
    tracers.o \
    constituents.o \
    aerodep_flx.o \
    radheat.o \

cam_cpl_indices.o: \
    seq_drydep_mod.o \
    mct_mod.o \
    seq_flds_mod.o \

seq_timemgr_mod.o: \
    ESMF_Mod.o \
    shr_sys_mod.o \
    shr_string_mod.o \
    shr_file_mod.o \
    seq_comm_mct.o \
    shr_kind_mod.o \
    seq_io_mod.o \
    shr_mpi_mod.o \
    shr_cal_mod.o \

atm_comp_mct.o: \
    physconst.o \
    time_manager.o \
    dyn_grid.o \
    spmd_utils.o \
    pio.o \
    cam_comp.o \
    ESMF_Mod.o \
    dust_intr.o \
    shr_sys_mod.o \
    phys_grid.o \
    shr_file_mod.o \
    seq_drydep_mod.o \
    abortutils.o \
    cam_history.o \
    cam_restart.o \
    pmgrid.o \
    co2_cycle.o \
    camsrfexch_types.o \
    cam_control_mod.o \
    scamMod.o \
    phys_control.o \
    mpishorthand.o \
    shr_kind_mod.o \
    radiation.o \
    perf_mod.o \
    seq_cdata_mod.o \
    ioFileMod.o \
    cam_logfile.o \
    runtime_opts.o \
    shr_const_mod.o \
    filenames.o \
    ppgrid.o \
    cam_cpl_indices.o \
    constituents.o \
    mct_mod.o \
    seq_timemgr_mod.o \
    seq_flds_mod.o \
    seq_infodata_mod.o \
    cam_pio_utils.o \

benergy.o: \
    dynamics_vars.o \
    shr_kind_mod.o \
    cam_logfile.o \
    mod_comm.o \

binary_io.o: \
    spmd_utils.o \
    spmd_dyn.o \
    abortutils.o \
    pmgrid.o \
    mpishorthand.o \
    shr_kind_mod.o \
    cam_logfile.o \

bnddyi.o: \
    abortutils.o \
    shr_kind_mod.o \
    cam_logfile.o \

seq_flds_indices.o: \
    shr_sys_mod.o \
    seq_drydep_mod.o \
    mct_mod.o \
    shr_string_mod.o \
    seq_flds_mod.o \

seq_diag_mct.o: \
    ESMF_Mod.o \
    shr_sys_mod.o \
    seq_timemgr_mod.o \
    mct_mod.o \
    seq_flds_indices.o \
    seq_comm_mct.o \
    shr_kind_mod.o \
    seq_cdata_mod.o \
    shr_const_mod.o \
    shr_mpi_mod.o \
    seq_infodata_mod.o \

seq_rearr_mod.o: \
    shr_sys_mod.o \
    seq_diag_mct.o \
    mct_mod.o \
    seq_comm_mct.o \
    shr_kind_mod.o \
    seq_cdata_mod.o \
    seq_flds_mod.o \

map_ocnocn_mct.o: \
    shr_sys_mod.o \
    seq_comm_mct.o \
    seq_cdata_mod.o \
    seq_rearr_mod.o \
    mct_mod.o \

mrg_x2s_mct.o: \
    seq_flds_indices.o \
    seq_comm_mct.o \
    shr_kind_mod.o \
    seq_cdata_mod.o \
    mct_mod.o \
    seq_flds_mod.o \

ice_comp_mct.o: \
    ESMF_Mod.o \
    seq_cdata_mod.o \
    mct_mod.o \
    seq_infodata_mod.o \

mrg_x2o_mct.o: \
    seq_flds_indices.o \
    seq_comm_mct.o \
    shr_kind_mod.o \
    seq_cdata_mod.o \
    mct_mod.o \
    seq_flds_mod.o \
    seq_infodata_mod.o \

seq_avdata_mod.o: \
    mct_mod.o \
    shr_kind_mod.o \
    seq_cdata_mod.o \
    seq_infodata_mod.o \

seq_hist_mod.o: \
    ESMF_Mod.o \
    shr_sys_mod.o \
    seq_timemgr_mod.o \
    mct_mod.o \
    seq_comm_mct.o \
    shr_kind_mod.o \
    seq_cdata_mod.o \
    seq_avdata_mod.o \
    seq_io_mod.o \
    seq_infodata_mod.o \
    shr_cal_mod.o \

mrg_x2a_mct.o: \
    seq_flds_indices.o \
    seq_comm_mct.o \
    shr_kind_mod.o \
    seq_cdata_mod.o \
    mct_mod.o \
    seq_flds_mod.o \

map_iceocn_mct.o: \
    shr_sys_mod.o \
    seq_comm_mct.o \
    seq_cdata_mod.o \
    mct_mod.o \

seq_map_mod.o: \
    shr_sys_mod.o \
    mct_mod.o \
    seq_comm_mct.o \
    shr_kind_mod.o \
    shr_const_mod.o \

map_atmlnd_mct.o: \
    seq_map_mod.o \
    shr_sys_mod.o \
    seq_flds_indices.o \
    m_die.o \
    seq_comm_mct.o \
    shr_kind_mod.o \
    seq_cdata_mod.o \
    shr_const_mod.o \
    shr_mct_mod.o \
    mct_mod.o \
    seq_infodata_mod.o \

map_atmice_mct.o: \
    seq_map_mod.o \
    shr_sys_mod.o \
    seq_flds_indices.o \
    m_die.o \
    seq_comm_mct.o \
    shr_kind_mod.o \
    seq_cdata_mod.o \
    shr_mct_mod.o \
    mct_mod.o \
    seq_flds_mod.o \
    seq_infodata_mod.o \

map_snoglc_mct.o: \
    shr_sys_mod.o \
    seq_comm_mct.o \
    seq_cdata_mod.o \
    mct_mod.o \

map_atmocn_mct.o: \
    seq_map_mod.o \
    shr_sys_mod.o \
    seq_flds_indices.o \
    m_die.o \
    seq_comm_mct.o \
    shr_kind_mod.o \
    seq_cdata_mod.o \
    shr_const_mod.o \
    shr_mct_mod.o \
    mct_mod.o \
    seq_infodata_mod.o \

seq_domain_mct.o: \
    shr_sys_mod.o \
    map_iceocn_mct.o \
    map_atmlnd_mct.o \
    mct_mod.o \
    map_atmice_mct.o \
    seq_comm_mct.o \
    map_snoglc_mct.o \
    shr_kind_mod.o \
    seq_cdata_mod.o \
    map_atmocn_mct.o \
    shr_mpi_mod.o \
    seq_infodata_mod.o \

seq_rest_mod.o: \
    ESMF_Mod.o \
    shr_sys_mod.o \
    seq_diag_mct.o \
    seq_timemgr_mod.o \
    mct_mod.o \
    shr_file_mod.o \
    seq_comm_mct.o \
    shr_kind_mod.o \
    seq_cdata_mod.o \
    seq_avdata_mod.o \
    seq_io_mod.o \
    shr_mpi_mod.o \
    seq_infodata_mod.o \
    shr_cal_mod.o \

mrg_x2l_mct.o: \
    seq_flds_indices.o \
    seq_comm_mct.o \
    shr_kind_mod.o \
    seq_cdata_mod.o \
    mct_mod.o \
    seq_flds_mod.o \

seq_frac_mct.o: \
    shr_sys_mod.o \
    map_iceocn_mct.o \
    map_atmlnd_mct.o \
    mct_mod.o \
    map_atmice_mct.o \
    seq_comm_mct.o \
    shr_kind_mod.o \
    seq_cdata_mod.o \
    map_atmocn_mct.o \
    shr_const_mod.o \

shr_flux_mod.o: \
    shr_sys_mod.o \
    phys_control.o \
    shr_log_mod.o \
    physconst.o \
    shr_kind_mod.o \

seq_flux_mct.o: \
    shr_sys_mod.o \
    shr_flux_mod.o \
    shr_mct_mod.o \
    mct_mod.o \
    shr_orb_mod.o \
    seq_flds_indices.o \
    seq_comm_mct.o \
    shr_kind_mod.o \
    seq_cdata_mod.o \
    seq_infodata_mod.o \

map_lndlnd_mct.o: \
    shr_sys_mod.o \
    seq_comm_mct.o \
    seq_cdata_mod.o \
    seq_rearr_mod.o \
    mct_mod.o \

map_iceice_mct.o: \
    shr_sys_mod.o \
    seq_comm_mct.o \
    seq_cdata_mod.o \
    seq_rearr_mod.o \
    mct_mod.o \

map_glcglc_mct.o: \
    shr_sys_mod.o \
    seq_comm_mct.o \
    seq_cdata_mod.o \
    seq_rearr_mod.o \
    mct_mod.o \

lnd_comp_mct.o: \
    ESMF_Mod.o \
    seq_cdata_mod.o \
    mct_mod.o \
    seq_infodata_mod.o \

ocn_types.o: \
    shr_kind_mod.o \
    ppgrid.o \

ocn_comp.o: \
    physconst.o \
    phys_grid.o \
    ocn_types.o \
    abortutils.o \
    shr_kind_mod.o \
    ppgrid.o \

ocn_comp_mct.o: \
    physconst.o \
    spmd_utils.o \
    ESMF_Mod.o \
    shr_sys_mod.o \
    phys_grid.o \
    ocn_types.o \
    seq_flds_indices.o \
    shr_kind_mod.o \
    perf_mod.o \
    seq_cdata_mod.o \
    ppgrid.o \
    ocn_comp.o \
    seq_timemgr_mod.o \
    mct_mod.o \
    seq_flds_mod.o \
    seq_infodata_mod.o \

map_rofrof_mct.o: \
    shr_sys_mod.o \
    seq_comm_mct.o \
    seq_cdata_mod.o \
    seq_rearr_mod.o \
    mct_mod.o \

map_atmatm_mct.o: \
    shr_sys_mod.o \
    seq_comm_mct.o \
    seq_cdata_mod.o \
    seq_rearr_mod.o \
    mct_mod.o \

map_rofocn_mct.o: \
    shr_sys_mod.o \
    seq_cdata_mod.o \
    shr_mct_mod.o \
    mct_mod.o \
    seq_infodata_mod.o \

shr_mem_mod.o: \
    shr_log_mod.o \
    shr_kind_mod.o \

map_snosno_mct.o: \
    shr_sys_mod.o \
    seq_comm_mct.o \
    seq_cdata_mod.o \
    seq_rearr_mod.o \
    mct_mod.o \

mrg_x2g_mct.o: \
    seq_flds_indices.o \
    seq_comm_mct.o \
    shr_kind_mod.o \
    seq_cdata_mod.o \
    mct_mod.o \
    seq_flds_mod.o \

mrg_x2i_mct.o: \
    seq_flds_indices.o \
    seq_comm_mct.o \
    shr_kind_mod.o \
    seq_cdata_mod.o \
    mct_mod.o \
    seq_flds_mod.o \
    seq_infodata_mod.o \

glc_comp_mct.o: \
    ESMF_Mod.o \
    seq_cdata_mod.o \
    mct_mod.o \
    seq_infodata_mod.o \

ccsm_comp_mod.o: \
    map_ocnocn_mct.o \
    mrg_x2s_mct.o \
    ice_comp_mct.o \
    shr_orb_mod.o \
    mrg_x2o_mct.o \
    ESMF_Mod.o \
    shr_map_mod.o \
    seq_hist_mod.o \
    mrg_x2a_mct.o \
    atm_comp_mct.o \
    seq_domain_mct.o \
    map_atmice_mct.o \
    seq_rest_mod.o \
    shr_sys_mod.o \
    mrg_x2l_mct.o \
    seq_frac_mct.o \
    seq_diag_mct.o \
    shr_file_mod.o \
    seq_flds_indices.o \
    seq_flux_mct.o \
    map_lndlnd_mct.o \
    map_iceice_mct.o \
    map_iceocn_mct.o \
    map_glcglc_mct.o \
    lnd_comp_mct.o \
    seq_comm_mct.o \
    map_snoglc_mct.o \
    ocn_comp_mct.o \
    shr_kind_mod.o \
    map_rofrof_mct.o \
    map_atmlnd_mct.o \
    map_atmatm_mct.o \
    perf_mod.o \
    seq_cdata_mod.o \
    map_rofocn_mct.o \
    seq_avdata_mod.o \
    map_atmocn_mct.o \
    shr_mem_mod.o \
    shr_const_mod.o \
    seq_io_mod.o \
    shr_mpi_mod.o \
    shr_scam_mod.o \
    map_snosno_mct.o \
    mrg_x2g_mct.o \
    mrg_x2i_mct.o \
    seq_timemgr_mod.o \
    mct_mod.o \
    glc_comp_mct.o \
    seq_infodata_mod.o \
    shr_cal_mod.o \

ccsm_driver.o: \
    ESMF_Mod.o \
    shr_sys_mod.o \
    perf_mod.o \
    ccsm_comp_mod.o \

tp_core.o: \
    shr_kind_mod.o \

sw_core.o: \
    tp_core.o \
    dynamics_vars.o \
    shr_kind_mod.o \
    pft_module.o \

cd_core.o: \
    spmd_utils.o \
    sw_core.o \
    fv_control_mod.o \
    dynamics_vars.o \
    metdata.o \
    abortutils.o \
    mpishorthand.o \
    shr_kind_mod.o \
    pft_module.o \
    cam_logfile.o \
    mod_comm.o \
    FVperf_module.o \

cldsav.o: \
    shr_kind_mod.o \
    ppgrid.o \

comspe.o: \
    pmgrid.o \
    shr_kind_mod.o \
    pspect.o \

cpslec.o: \
    shr_kind_mod.o \
    ppgrid.o \

d2a3dijk.o: \
    parutilitiesmodule.o \
    dynamics_vars.o \
    shr_kind_mod.o \
    mod_comm.o \

d2a3dikj.o: \
    parutilitiesmodule.o \
    repro_sum_mod.o \
    dynamics_vars.o \
    shr_kind_mod.o \
    perf_mod.o \
    cam_logfile.o \
    mod_comm.o \

dadadj.o: \
    physconst.o \
    phys_grid.o \
    abortutils.o \
    cam_control_mod.o \
    shr_kind_mod.o \
    cam_logfile.o \
    ppgrid.o \

diag_dynvar_ic.o: \
    dynamics_vars.o \
    cam_history.o \
    shr_kind_mod.o \
    constituents.o \

mean_module.o: \
    parutilitiesmodule.o \
    commap.o \
    repro_sum_mod.o \
    dynamics_vars.o \
    shr_kind_mod.o \
    perf_mod.o \
    cam_logfile.o \

dryairm.o: \
    dynamics_vars.o \
    cam_control_mod.o \
    shr_kind_mod.o \
    mean_module.o \
    cam_logfile.o \
    constituents.o \

dsd.o: \
    array_lib.o \
    math_lib.o \

mapz_module.o: \
    abortutils.o \
    shr_kind_mod.o \
    cam_logfile.o \
    FVperf_module.o \

epvd.o: \
    parutilitiesmodule.o \
    dynamics_vars.o \
    shr_kind_mod.o \
    mapz_module.o \
    mod_comm.o \

esinti.o: \
    shr_kind_mod.o \
    wv_saturation.o \

fft99.o: \
    shr_kind_mod.o \
    cam_logfile.o \

fill_module.o: \
    shr_kind_mod.o \
    cam_logfile.o \

gauaw_mod.o: \
    abortutils.o \
    shr_kind_mod.o \

geopk.o: \
    parutilitiesmodule.o \
    dynamics_vars.o \
    spmd_dyn.o \
    decompmodule.o \
    shr_kind_mod.o \
    mod_comm.o \

gffgch.o: \
    physconst.o \
    abortutils.o \
    shr_kind_mod.o \
    cam_logfile.o \

hirsbt.o: \
    time_manager.o \
    physconst.o \
    hirsbtpar.o \
    shr_kind_mod.o \
    ppgrid.o \

initcom.o: \
    physconst.o \
    spmd_utils.o \
    commap.o \
    rgrid.o \
    abortutils.o \
    pmgrid.o \
    shr_kind_mod.o \
    cam_logfile.o \
    pspect.o \

initindx.o: \
    physconst.o \
    ghg_data.o \
    spmd_utils.o \
    prescribed_ghg.o \
    prescribed_aero.o \
    phys_buffer.o \
    cam3_ozone_data.o \
    string_utils.o \
    aoa_tracers.o \
    aerosol_intr.o \
    convect_shallow.o \
    ionosphere.o \
    prescribed_volcaero.o \
    convect_deep.o \
    cam_diagnostics.o \
    check_energy.o \
    co2_cycle.o \
    conv_water.o \
    cam_control_mod.o \
    phys_control.o \
    microp_driver.o \
    shr_kind_mod.o \
    radiation.o \
    chemistry.o \
    vertical_diffusion.o \
    gw_drag.o \
    iondrag.o \
    flux_avg.o \
    cam3_aero_data.o \
    tracers.o \
    sslt_rebin.o \
    prescribed_ozone.o \
    stratiform.o \
    constituents.o \
    aircraft_emit.o \
    macrop_driver.o \

intp_util.o: \
    phys_grid.o \
    abortutils.o \
    shr_kind_mod.o \
    cam_logfile.o \
    ppgrid.o \

iop_surf.o: \
    physconst.o \
    camsrfexch_types.o \
    scamMod.o \
    ppgrid.o \

load_hydrometeor_classes.o: \
    radar_simulator_types.o \

m_AccumulatorComms.o: \
    m_AttrVect.o \
    m_GlobalMap.o \
    m_AttrVectComms.o \
    m_die.o \
    m_stdio.o \
    m_GlobalSegMap.o \
    m_Accumulator.o \
    m_mpif90.o \

m_AttrVectReduce.o: \
    m_AttrVect.o \
    m_List.o \
    m_die.o \
    m_stdio.o \
    m_mpif90.o \
    m_realkinds.o \

m_StrTemplate.o: \
    m_die.o \
    m_stdio.o \
    m_chars.o \

m_FileResolv.o: \
    m_StrTemplate.o \
    m_die.o \

m_Merge.o: \
    m_AttrVect.o \
    m_String.o \
    m_List.o \
    m_GeneralGrid.o \
    m_die.o \
    m_stdio.o \
    m_realkinds.o \

m_SpatialIntegralV.o: \
    m_AttrVect.o \
    m_List.o \
    m_die.o \
    m_stdio.o \
    m_AttrVectReduce.o \
    m_mpif90.o \
    m_realkinds.o \

m_SpatialIntegral.o: \
    m_AttrVect.o \
    m_SpatialIntegralV.o \
    m_String.o \
    m_List.o \
    m_GeneralGrid.o \
    m_die.o \
    m_stdio.o \
    m_AttrVectReduce.o \
    m_mpif90.o \
    m_realkinds.o \

m_zeit.o: \
    m_SortingTools.o \
    m_ioutil.o \
    m_die.o \
    m_stdio.o \
    m_mpif90.o \

marsaglia.o: \
    shr_kind_mod.o \

mcshallow.o: \
    error_function.o \
    cam_history.o \
    cam_logfile.o \
    ppgrid.o \

pio_quicksort.o: \
    pio_kinds.o \

mct_rearrange.o: \
    m_AttrVect.o \
    alloc_mod.o \
    pio_support.o \
    m_Rearranger.o \
    m_GlobalSegMap.o \
    pio_quicksort.o \
    pio_kinds.o \
    m_MCTWorld.o \
    pio_types.o \

mo_msis_ubc.o: \
    physconst.o \
    time_manager.o \
    spmd_utils.o \
    phys_grid.o \
    abortutils.o \
    pmgrid.o \
    shr_kind_mod.o \
    ref_pres.o \
    cam_logfile.o \
    ppgrid.o \
    constituents.o \

mo_regrider.o: \
    abortutils.o \
    dycore.o \
    scamMod.o \
    shr_kind_mod.o \
    cam_logfile.o \
    ppgrid.o \

mo_solar_parms.o: \
    time_manager.o \
    pio.o \
    spmd_utils.o \
    time_utils.o \
    abortutils.o \
    error_messages.o \
    shr_kind_mod.o \
    ioFileMod.o \
    cam_logfile.o \
    cam_pio_utils.o \

msise00.o: \
    shr_kind_mod.o \
    cam_logfile.o \

p_d_adjust.o: \
    parutilitiesmodule.o \
    repro_sum_mod.o \
    dynamics_vars.o \
    shr_kind_mod.o \
    perf_mod.o \
    cam_logfile.o \

par_vecsum.o: \
    parutilitiesmodule.o \
    shr_kind_mod.o \

par_xsum.o: \
    parutilitiesmodule.o \
    repro_sum_mod.o \
    dynamics_vars.o \
    shr_kind_mod.o \
    cam_logfile.o \
    FVperf_module.o \

pio_msg_callbacks.o: \
    pio_support.o \
    piolib_mod.o \
    pio.o \
    pio_msg_mod.o \
    pio_kinds.o \

pio_msg_getput_callbacks.o: \
    pio_support.o \
    pio.o \
    pio_msg_mod.o \
    pio_kinds.o \

pio_nf_utils.o: \
    pio_support.o \
    pionfput_mod.o \
    nf_mod.o \
    pio_types.o \
    pionfget_mod.o \
    pio_kinds.o \

pkez.o: \
    shr_kind_mod.o \

puminterfaces.o: \
    parutilitiesmodule.o \
    decompmodule.o \
    shr_kind_mod.o \

qneg3.o: \
    shr_kind_mod.o \
    cam_logfile.o \

qneg4.o: \
    phys_grid.o \
    ppgrid.o \
    physconst.o \
    shr_kind_mod.o \
    cam_logfile.o \
    constituents.o \

radar_simulator.o: \
    mrgrnk.o \
    radar_simulator_types.o \
    array_lib.o \
    math_lib.o \
    optics_lib.o \

redistributemodule.o: \
    parutilitiesmodule.o \
    decompmodule.o \
    shr_kind_mod.o \
    debugutilitiesmodule.o \

sgexx.o: \
    abortutils.o \
    shr_kind_mod.o \
    cam_logfile.o \

shr_infnan_mod.o: \
    shr_kind_mod.o \

shr_msg_mod.o: \
    shr_sys_mod.o \
    shr_log_mod.o \
    shr_file_mod.o \

shr_vmath_mod.o: \
    shr_log_mod.o \
    shr_kind_mod.o \

srchutil.o: \
    shr_kind_mod.o \

srfxfer.o: \
    cam_history.o \
    chem_surfvals.o \
    ppgrid.o \
    physconst.o \
    co2_cycle.o \
    cam_control_mod.o \
    camsrfexch_types.o \
    physics_types.o \
    shr_kind_mod.o \
    comsrf.o \
    constituents.o \

sulchem.o: \
    cam_history.o \
    ppgrid.o \
    physconst.o \
    abortutils.o \
    shr_kind_mod.o \
    perf_mod.o \
    cam_logfile.o \

te_map.o: \
    dynamics_vars.o \
    phys_control.o \
    shr_kind_mod.o \
    mapz_module.o \
    cam_logfile.o \
    mod_comm.o \

tphysac.o: \
    phys_buffer.o \
    aerosol_intr.o \
    ionosphere.o \
    cam_diagnostics.o \
    dycore.o \
    phys_control.o \
    chemistry.o \
    flux_avg.o \
    ppgrid.o \
    time_manager.o \
    physconst.o \
    aoa_tracers.o \
    abortutils.o \
    rayleigh_friction.o \
    check_energy.o \
    cam_control_mod.o \
    camsrfexch_types.o \
    physics_types.o \
    shr_kind_mod.o \
    perf_mod.o \
    cam_logfile.o \
    vertical_diffusion.o \
    gw_drag.o \
    iondrag.o \
    majorsp_diffusion.o \
    tracers.o \
    constituents.o \

tphysbc.o: \
    phys_buffer.o \
    aerosol_intr.o \
    convect_shallow.o \
    cloud_diagnostics.o \
    cam_history.o \
    cam_diagnostics.o \
    dycore.o \
    phys_control.o \
    ppgrid.o \
    macrop_driver.o \
    time_manager.o \
    physconst.o \
    tropopause.o \
    convect_deep.o \
    check_energy.o \
    camsrfexch_types.o \
    microp_driver.o \
    physics_types.o \
    shr_kind_mod.o \
    radiation.o \
    perf_mod.o \
    sslt_rebin.o \
    constituents.o \
    stratiform.o \

tphysidl.o: \
    phys_grid.o \
    cam_history.o \
    ppgrid.o \
    time_manager.o \
    physconst.o \
    abortutils.o \
    check_energy.o \
    physics_types.o \
    shr_kind_mod.o \
    ref_pres.o \
    cam_logfile.o \

trac2d.o: \
    parutilitiesmodule.o \
    tp_core.o \
    dynamics_vars.o \
    FVperf_module.o \
    fill_module.o \
    shr_kind_mod.o \
    mod_comm.o \

tsinti.o: \
    cam_control_mod.o \
    shr_kind_mod.o \

uv3s_update.o: \
    parutilitiesmodule.o \
    dynamics_vars.o \
    cam_history.o \
    shr_kind_mod.o \
    mod_comm.o \

virtem.o: \
    shr_kind_mod.o \

vrtmap.o: \
    srchutil.o \
    abortutils.o \
    shr_kind_mod.o \
    cam_logfile.o \

wrap_mpi.o: \
    mpishorthand.o \
    abortutils.o \
    shr_kind_mod.o \
    perf_mod.o \
    cam_logfile.o \

wrf_error_fatal.o: \
    shr_sys_mod.o \

zeff.o: \
    math_lib.o \
    optics_lib.o \

zenith.o: \
    shr_orb_mod.o \
    cam_control_mod.o \
    shr_kind_mod.o \

netcdf.o: \
    typeSizes.o \

netcdf_test.o: \
    netcdf.o \
    typeSizes.o \

validate-cam.o: \
    netcdf.o \

