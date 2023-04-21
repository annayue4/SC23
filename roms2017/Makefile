
BIN     = roms2017

FC      = ftn -Ofast #O3 -hfp3
FFLAGS	= 
EXTRA_FFLAGS = -I src -DSPEC -DNDEBUG -DBENCHMARK -DNO_GETTIMEOFDAY -DNestedGrids=1
OMP_FLAGS = -DSPEC_SUPPRESS_OPENMP
LIBS = -static

# rate -DSPEC_SUPPRESS_OPENMP
# speed -DSPEC_OPENMP

SOURCES = \
    bbl.F90 \
    bc_2d.F90 \
    exchange_2d.F90 \
    mod_param.F90 \
    mod_kinds.F90 \
    mod_grid.F90 \
    mod_scalars.F90 \
    mod_bbl.F90 \
    mod_forces.F90 \
    mod_ocean.F90 \
    mod_sediment.F90 \
    mod_parallel.F90 \
    mod_iounits.F90 \
    mod_strings.F90 \
    mod_stepping.F90 \
    mp_exchange.F90 \
    bc_3d.F90 \
    exchange_3d.F90 \
    bc_bry2d.F90 \
    bc_bry3d.F90 \
    bulk_flux.F90 \
    mod_mixing.F90 \
    bvf_mix.F90 \
    conv_2d.F90 \
    conv_3d.F90 \
    conv_bry2d.F90 \
    conv_bry3d.F90 \
    diag.F90 \
    analytical.F90 \
    distribute.F90 \
    mod_ncparam.F90 \
    mod_biology.F90 \
    mod_eclight.F90 \
    mod_boundary.F90 \
    mod_clima.F90 \
    mod_sources.F90 \
    mod_netcdf.F90 \
    strings.F90 \
    forcing.F90 \
    mod_coupling.F90 \
    frc_adjust.F90 \
    get_data.F90 \
    mod_obs.F90 \
    get_idata.F90 \
    mod_tides.F90 \
    nf_fread3d.F90 \
    nf_fread4d.F90 \
    gls_corstep.F90 \
    tkebc_im.F90 \
    gls_prestep.F90 \
    hmixing.F90 \
    ini_fields.F90 \
    set_depth.F90 \
    t3dbc_im.F90 \
    u2dbc_im.F90 \
    u3dbc_im.F90 \
    v2dbc_im.F90 \
    v3dbc_im.F90 \
    zetabc.F90 \
    initial.F90 \
    ini_adjust.F90 \
    mod_fourdvar.F90 \
    state_addition.F90 \
    state_copy.F90 \
    metrics.F90 \
    ocean_coupler.F90 \
    mod_coupler.F90 \
    roms_export.F90 \
    roms_import.F90 \
    omega.F90 \
    rho_eos.F90 \
    mod_eoscoef.F90 \
    set_massflux.F90 \
    stiffness.F90 \
    wpoints.F90 \
    mod_storage.F90 \
    interp_floats.F90 \
    lmd_bkpp.F90 \
    shapiro.F90 \
    lmd_skpp.F90 \
    lmd_swfrac.F90 \
    lmd_vmix.F90 \
    main2d.F90 \
    dotproduct.F90 \
    obc_adjust.F90 \
    oi_update.F90 \
    radiation_stress.F90 \
    mod_diags.F90 \
    set_avg.F90 \
    mod_average.F90 \
    set_tides.F90 \
    set_vbc.F90 \
    step2d.F90 \
    obc_volcons.F90 \
    wetdry.F90 \
    step_floats.F90 \
    mod_floats.F90 \
    vwalk_floats.F90 \
    utility.F90 \
    main3d.F90 \
    biology.F90 \
    my25_corstep.F90 \
    my25_prestep.F90 \
    rhs3d.F90 \
    pre_step3d.F90 \
    prsgrd.F90 \
    t3dmix.F90 \
    uv3dmix.F90 \
    sediment.F90 \
    sed_bed.F90 \
    sed_bedload.F90 \
    sed_fluxes.F90 \
    sed_settling.F90 \
    sed_surface.F90 \
    set_zeta.F90 \
    step3d_t.F90 \
    mpdata_adiff.F90 \
    step3d_uv.F90 \
    wvelocity.F90 \
    output.F90 \
    set_data.F90 \
    set_2dfld.F90 \
    set_3dfld.F90 \
    abort.F90 \
    ocean_control.F90 \
    back_cost.F90 \
    cgradient.F90 \
    nf_fread2d.F90 \
    nf_fread2d_bry.F90 \
    nf_fread3d_bry.F90 \
    state_dotprod.F90 \
    state_initialize.F90 \
    state_scale.F90 \
    cost_grad.F90 \
    normalization.F90 \
    nf_fwrite2d.F90 \
    nf_fwrite3d.F90 \
    white_noise.F90 \
    nrutil.F90 \
    packing.F90 \
    posterior.F90 \
    posterior_var.F90 \
    state_product.F90 \
    propagator.F90 \
    random_ic.F90 \
    sum_grad.F90 \
    zeta_balance.F90 \
    checkadj.F90 \
    checkdefs.F90 \
    checkerror.F90 \
    checkvars.F90 \
    close_io.F90 \
    congrad.F90 \
    def_avg.F90 \
    def_var.F90 \
    def_diags.F90 \
    def_dim.F90 \
    def_error.F90 \
    def_floats.F90 \
    def_gst.F90 \
    def_hessian.F90 \
    def_his.F90 \
    def_impulse.F90 \
    def_info.F90 \
    def_ini.F90 \
    def_lanczos.F90 \
    def_mod.F90 \
    def_norm.F90 \
    def_rst.F90 \
    def_station.F90 \
    def_tides.F90 \
    extract_obs.F90 \
    extract_sta.F90 \
    frc_weak.F90 \
    gasdev.F90 \
    get_2dfld.F90 \
    get_2dfldr.F90 \
    get_3dfld.F90 \
    get_3dfldr.F90 \
    get_bounds.F90 \
    get_cycle.F90 \
    get_date.F90 \
    get_grid.F90 \
    get_gst.F90 \
    get_ngfld.F90 \
    get_ngfldr.F90 \
    get_state.F90 \
    get_varcoords.F90 \
    grid_coords.F90 \
    interpolate.F90 \
    ini_lanczos.F90 \
    inp_par.F90 \
    ran_state.F90 \
    lubksb.F90 \
    ludcmp.F90 \
    mp_routines.F90 \
    nf_fwrite2d_bry.F90 \
    nf_fwrite3d_bry.F90 \
    nf_fwrite4d.F90 \
    obs_cost.F90 \
    obs_depth.F90 \
    obs_initial.F90 \
    obs_read.F90 \
    obs_write.F90 \
    ran1.F90 \
    regrid.F90 \
    rep_matrix.F90 \
    set_2dfldr.F90 \
    set_3dfldr.F90 \
    set_diags.F90 \
    set_ngfld.F90 \
    set_ngfldr.F90 \
    set_scoord.F90 \
    set_weights.F90 \
    stats_modobs.F90 \
    timers.F90 \
    wrt_avg.F90 \
    wrt_diags.F90 \
    wrt_error.F90 \
    wrt_floats.F90 \
    wrt_gst.F90 \
    wrt_hessian.F90 \
    wrt_his.F90 \
    wrt_impulse.F90 \
    wrt_info.F90 \
    wrt_ini.F90 \
    wrt_rst.F90 \
    wrt_station.F90 \
    wrt_tides.F90 \
    mod_arrays.F90 \
    mod_nesting.F90 \
    esmf_roms.F90 \
    master.F90


OBJ     = $(SOURCES:.F90=.o)

VPATH	= src
.SUFFIXES: .F90

ifeq ($(MAKECMDGOALS),roms2017_omp)
BIN       = roms2017_omp
OMP_FLAGS = -DSPEC_OPENMP
endif

$(BIN): x$(BIN) $(BIN).execute.script
	cp $(BIN).execute.script $(BIN)
x$(BIN): $(OBJ)
	$(FC) $(FFLAGS) -o x$(BIN) $(OBJ) $(LDFLAGS) $(LIBS)

.F90.o:
	$(FC) -c $(EXTRA_FFLAGS) $(OMP_FLAGS) $(FFLAGS) $<

clean:
	-rm -f core
	-rm -f $(OBJ) *.mod

clobber: clean
	-rm -f $(BIN) x$(BIN) $(BIN)_omp x$(BIN)_omp varinfo.dat ocean_bench*.in

# dependencies
bc_2d.o: \
    mod_param.o \
    exchange_2d.o \
    mod_grid.o \
    mod_scalars.o \

exchange_2d.o: \
    mod_param.o \

mod_param.o: \
    mod_kinds.o \

mod_grid.o: \
    mod_kinds.o \
    mod_param.o \

mod_scalars.o: \
    mod_param.o \

mod_forces.o: \
    mod_kinds.o \
    mod_param.o \

mod_ocean.o: \
    mod_kinds.o \
    mod_param.o \

mod_parallel.o: \
    mod_param.o \
    mod_strings.o \
    mod_iounits.o \
    mod_scalars.o \

mod_iounits.o: \
    mod_param.o \

mod_stepping.o: \
    mod_param.o \

bc_3d.o: \
    mod_param.o \
    exchange_3d.o \
    mod_grid.o \
    mod_scalars.o \

exchange_3d.o: \
    mod_param.o \

bc_bry2d.o: \
    mod_param.o \
    mod_scalars.o \

bc_bry3d.o: \
    mod_param.o \
    mod_scalars.o \

bulk_flux.o: \
    mod_param.o \
    mod_forces.o \
    mod_grid.o \
    mod_mixing.o \
    mod_ocean.o \
    mod_stepping.o \
    mod_scalars.o \
    exchange_2d.o \
    mod_kinds.o \

mod_mixing.o: \
    mod_kinds.o \
    mod_param.o \
    mod_scalars.o \

diag.o: \
    mod_param.o \
    mod_grid.o \
    mod_ocean.o \
    mod_stepping.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_scalars.o \

analytical.o: \
    mod_param.o \
    mod_forces.o \
    mod_ncparam.o \
    mod_scalars.o \
    exchange_2d.o \
    mod_grid.o \
    mod_parallel.o \
    mod_ocean.o \
    mod_stepping.o \

mod_ncparam.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_scalars.o \

mod_netcdf.o: \
    mod_kinds.o \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_scalars.o \
    mod_ncparam.o \

mod_coupling.o: \
    mod_kinds.o \
    mod_param.o \

get_data.o: \
    mod_param.o \
    mod_boundary.o \
    mod_forces.o \
    mod_grid.o \
    mod_iounits.o \
    mod_ncparam.o \
    mod_scalars.o \
    mod_stepping.o \

nf_fread3d.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_ncparam.o \
    mod_netcdf.o \
    mod_scalars.o \

nf_fread4d.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_ncparam.o \
    mod_netcdf.o \
    mod_scalars.o \

ini_fields.o: \
    mod_param.o \
    mod_grid.o \
    mod_coupling.o \
    mod_ocean.o \
    mod_stepping.o \
    mod_scalars.o \
    exchange_2d.o \
    exchange_3d.o \
    set_depth.o \
    t3dbc_im.o \
    u3dbc_im.o \
    v3dbc_im.o \
    u2dbc_im.o \
    v2dbc_im.o \
    zetabc.o \

set_depth.o: \
    mod_param.o \
    mod_coupling.o \
    mod_grid.o \
    mod_ocean.o \
    mod_stepping.o \
    mod_scalars.o \
    exchange_2d.o \
    exchange_3d.o \

t3dbc_im.o: \
    mod_param.o \
    mod_ocean.o \
    mod_stepping.o \
    mod_boundary.o \
    mod_grid.o \
    mod_scalars.o \

u2dbc_im.o: \
    mod_param.o \
    mod_ocean.o \
    mod_stepping.o \
    mod_boundary.o \
    mod_forces.o \
    mod_grid.o \
    mod_scalars.o \

u3dbc_im.o: \
    mod_param.o \
    mod_ocean.o \
    mod_stepping.o \
    mod_boundary.o \
    mod_grid.o \
    mod_scalars.o \

v2dbc_im.o: \
    mod_param.o \
    mod_ocean.o \
    mod_stepping.o \
    mod_boundary.o \
    mod_forces.o \
    mod_grid.o \
    mod_scalars.o \

v3dbc_im.o: \
    mod_param.o \
    mod_ocean.o \
    mod_stepping.o \
    mod_boundary.o \
    mod_grid.o \
    mod_scalars.o \

zetabc.o: \
    mod_param.o \
    mod_ocean.o \
    mod_stepping.o \
    mod_boundary.o \
    mod_grid.o \
    mod_scalars.o \

initial.o: \
    mod_param.o \
    mod_parallel.o \
    mod_grid.o \
    mod_iounits.o \
    mod_ncparam.o \
    mod_ocean.o \
    mod_scalars.o \
    mod_stepping.o \
    analytical.o \
    metrics.o \
    set_depth.o \
    omega.o \
    rho_eos.o \
    set_massflux.o \
    stiffness.o \

state_addition.o: \
    mod_param.o \

state_copy.o: \
    mod_param.o \

metrics.o: \
    mod_param.o \
    mod_grid.o \
    mod_ocean.o \
    mod_stepping.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_ncparam.o \
    mod_scalars.o \
    exchange_2d.o \
    set_depth.o \

omega.o: \
    mod_param.o \
    mod_grid.o \
    mod_ocean.o \
    mod_scalars.o \
    bc_3d.o \

rho_eos.o: \
    mod_param.o \
    mod_coupling.o \
    mod_grid.o \
    mod_mixing.o \
    mod_ocean.o \
    mod_stepping.o \
    mod_eoscoef.o \
    mod_scalars.o \
    exchange_2d.o \
    exchange_3d.o \

mod_eoscoef.o: \
    mod_kinds.o \

set_massflux.o: \
    mod_param.o \
    mod_grid.o \
    mod_ocean.o \
    mod_stepping.o \
    mod_scalars.o \
    exchange_3d.o \

stiffness.o: \
    mod_param.o \
    mod_grid.o \
    mod_ocean.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_scalars.o \

shapiro.o: \
    mod_param.o \

lmd_skpp.o: \
    mod_param.o \
    mod_forces.o \
    mod_grid.o \
    mod_mixing.o \
    mod_ocean.o \
    mod_stepping.o \
    mod_scalars.o \
    bc_2d.o \

lmd_swfrac.o: \
    mod_param.o \
    mod_mixing.o \
    mod_scalars.o \

lmd_vmix.o: \
    mod_param.o \
    mod_grid.o \
    mod_mixing.o \
    mod_ocean.o \
    mod_stepping.o \
    lmd_skpp.o \
    mod_scalars.o \
    bc_3d.o \

set_vbc.o: \
    mod_param.o \
    mod_grid.o \
    mod_forces.o \
    mod_ocean.o \
    mod_stepping.o \
    mod_scalars.o \
    bc_2d.o \

step2d.o: \
    mod_param.o \
    mod_coupling.o \
    mod_forces.o \
    mod_grid.o \
    mod_mixing.o \
    mod_ocean.o \
    mod_stepping.o \
    mod_scalars.o \
    exchange_2d.o \
    u2dbc_im.o \
    v2dbc_im.o \
    zetabc.o \

utility.o: \
    mod_kinds.o \

main3d.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_scalars.o \
    mod_stepping.o \
    bulk_flux.o \
    diag.o \
    ini_fields.o \
    lmd_vmix.o \
    omega.o \
    rho_eos.o \
    rhs3d.o \
    set_depth.o \
    set_massflux.o \
    set_vbc.o \
    set_zeta.o \
    step2d.o \
    step3d_t.o \
    step3d_uv.o \
    wvelocity.o \

rhs3d.o: \
    mod_param.o \
    mod_coupling.o \
    mod_forces.o \
    mod_grid.o \
    mod_ocean.o \
    mod_stepping.o \
    pre_step3d.o \
    prsgrd.o \
    t3dmix.o \
    uv3dmix.o \
    mod_scalars.o \

pre_step3d.o: \
    mod_param.o \
    mod_forces.o \
    mod_grid.o \
    mod_mixing.o \
    mod_ocean.o \
    mod_stepping.o \
    mod_scalars.o \
    exchange_3d.o \
    t3dbc_im.o \

prsgrd.o: \
    mod_param.o \
    mod_grid.o \
    mod_ocean.o \
    mod_stepping.o \
    mod_scalars.o \

t3dmix.o: \
    mod_param.o \
    mod_grid.o \
    mod_mixing.o \
    mod_ocean.o \
    mod_stepping.o \
    mod_scalars.o \

uv3dmix.o: \
    mod_param.o \
    mod_coupling.o \
    mod_grid.o \
    mod_mixing.o \
    mod_ocean.o \
    mod_stepping.o \
    mod_scalars.o \

set_zeta.o: \
    mod_param.o \
    mod_coupling.o \
    mod_ocean.o \
    mod_scalars.o \
    exchange_2d.o \

step3d_t.o: \
    mod_param.o \
    mod_grid.o \
    mod_mixing.o \
    mod_ocean.o \
    mod_stepping.o \
    mod_ncparam.o \
    mod_scalars.o \
    exchange_3d.o \
    t3dbc_im.o \

step3d_uv.o: \
    mod_param.o \
    mod_coupling.o \
    mod_forces.o \
    mod_grid.o \
    mod_mixing.o \
    mod_ocean.o \
    mod_stepping.o \
    mod_scalars.o \
    exchange_2d.o \
    exchange_3d.o \
    u3dbc_im.o \
    v3dbc_im.o \

wvelocity.o: \
    mod_param.o \
    mod_coupling.o \
    mod_grid.o \
    mod_ocean.o \
    mod_stepping.o \
    mod_scalars.o \
    bc_3d.o \
    exchange_2d.o \

output.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_ncparam.o \
    mod_netcdf.o \
    mod_scalars.o \

set_data.o: \
    mod_param.o \
    mod_boundary.o \
    mod_forces.o \
    mod_grid.o \
    mod_mixing.o \
    mod_ncparam.o \
    mod_ocean.o \
    mod_stepping.o \
    mod_scalars.o \
    analytical.o \
    exchange_2d.o \
    set_2dfld.o \
    set_3dfld.o \

set_2dfld.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_ncparam.o \
    mod_scalars.o \
    exchange_2d.o \

set_3dfld.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_ncparam.o \
    mod_scalars.o \
    exchange_3d.o \

abort.o: \
    ocean_control.o \

ocean_control.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_scalars.o \
    mod_ncparam.o \

nf_fread2d.o: \
    mod_param.o \
    mod_parallel.o \
    mod_grid.o \
    mod_iounits.o \
    mod_ncparam.o \
    mod_netcdf.o \
    mod_scalars.o \

nf_fread2d_bry.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_ncparam.o \
    mod_netcdf.o \
    mod_scalars.o \

nf_fread3d_bry.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_ncparam.o \
    mod_netcdf.o \
    mod_scalars.o \

state_dotprod.o: \
    mod_param.o \
    mod_parallel.o \
    mod_ncparam.o \

state_initialize.o: \
    mod_param.o \

state_scale.o: \
    mod_param.o \

nf_fwrite2d.o: \
    mod_param.o \
    mod_parallel.o \
    mod_ncparam.o \
    mod_netcdf.o \
    mod_scalars.o \

nf_fwrite3d.o: \
    mod_param.o \
    mod_parallel.o \
    mod_ncparam.o \
    mod_netcdf.o \
    mod_scalars.o \

white_noise.o: \
    mod_kinds.o \
    mod_param.o \
    mod_parallel.o \
    mod_scalars.o \
    nrutil.o \

nrutil.o: \
    mod_kinds.o \

state_product.o: \
    mod_param.o \
    mod_parallel.o \
    mod_ncparam.o \

checkadj.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_scalars.o \
    mod_strings.o \
    strings.o \

checkdefs.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_scalars.o \
    mod_strings.o \

checkerror.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_scalars.o \

checkvars.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_ncparam.o \
    mod_netcdf.o \
    mod_scalars.o \

close_io.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_ncparam.o \
    mod_netcdf.o \
    mod_scalars.o \

def_var.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_ncparam.o \
    mod_netcdf.o \
    mod_scalars.o \

def_dim.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_netcdf.o \
    mod_scalars.o \

def_his.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_ncparam.o \
    mod_netcdf.o \
    mod_scalars.o \
    def_var.o \

def_info.o: \
    mod_param.o \
    mod_parallel.o \
    mod_grid.o \
    mod_iounits.o \
    mod_ncparam.o \
    mod_netcdf.o \
    mod_scalars.o \
    mod_strings.o \
    def_var.o \

def_rst.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_ncparam.o \
    mod_netcdf.o \
    mod_scalars.o \
    def_var.o \

extract_sta.o: \
    mod_param.o \
    mod_parallel.o \
    mod_grid.o \
    mod_ncparam.o \
    mod_scalars.o \

gasdev.o: \
    mod_kinds.o \
    nrutil.o \

get_2dfld.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_ncparam.o \
    mod_netcdf.o \
    mod_scalars.o \
    nf_fread2d.o \
    nf_fread3d.o \

get_3dfld.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_ncparam.o \
    mod_netcdf.o \
    mod_scalars.o \
    nf_fread3d.o \

get_bounds.o: \
    mod_param.o \
    mod_parallel.o \
    mod_ncparam.o \

get_cycle.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_netcdf.o \
    mod_scalars.o \

get_date.o: \
    mod_kinds.o \

get_ngfld.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_ncparam.o \
    mod_netcdf.o \
    mod_scalars.o \

get_state.o: \
    mod_param.o \
    mod_parallel.o \
    mod_grid.o \
    mod_iounits.o \
    mod_mixing.o \
    mod_ncparam.o \
    mod_netcdf.o \
    mod_ocean.o \
    mod_scalars.o \
    mod_stepping.o \
    mod_strings.o \
    nf_fread2d.o \
    nf_fread3d.o \
    nf_fread4d.o \
    strings.o \

get_varcoords.o: \
    mod_param.o \
    mod_parallel.o \
    mod_grid.o \
    mod_iounits.o \
    mod_netcdf.o \
    mod_scalars.o \

interpolate.o: \
    mod_kinds.o \
    mod_param.o \
    mod_scalars.o \

inp_par.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_ncparam.o \
    mod_scalars.o \
    ran_state.o \
    mod_netcdf.o \
    mod_strings.o \
    mod_kinds.o \

ran_state.o: \
    mod_kinds.o \
    nrutil.o \

lubksb.o: \
    mod_kinds.o \

ludcmp.o: \
    mod_kinds.o \

mp_routines.o: \
    mod_kinds.o \

nf_fwrite2d_bry.o: \
    mod_param.o \
    mod_parallel.o \
    mod_ncparam.o \
    mod_netcdf.o \
    mod_scalars.o \

nf_fwrite3d_bry.o: \
    mod_param.o \
    mod_parallel.o \
    mod_ncparam.o \
    mod_netcdf.o \
    mod_scalars.o \

nf_fwrite4d.o: \
    mod_param.o \
    mod_parallel.o \
    mod_ncparam.o \
    mod_netcdf.o \
    mod_scalars.o \

ran1.o: \
    mod_kinds.o \
    ran_state.o \

regrid.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_ncparam.o \
    mod_scalars.o \
    interpolate.o \

set_ngfld.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_ncparam.o \
    mod_scalars.o \

set_scoord.o: \
    mod_param.o \
    mod_parallel.o \
    mod_grid.o \
    mod_iounits.o \
    mod_scalars.o \

set_weights.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_scalars.o \

timers.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_strings.o \

wrt_his.o: \
    mod_param.o \
    mod_parallel.o \
    mod_coupling.o \
    mod_forces.o \
    mod_grid.o \
    mod_iounits.o \
    mod_mixing.o \
    mod_ncparam.o \
    mod_netcdf.o \
    mod_ocean.o \
    mod_scalars.o \
    mod_stepping.o \
    nf_fwrite2d.o \
    nf_fwrite3d.o \
    omega.o \

wrt_info.o: \
    mod_param.o \
    mod_parallel.o \
    mod_grid.o \
    mod_iounits.o \
    mod_ncparam.o \
    mod_netcdf.o \
    mod_scalars.o \
    nf_fwrite2d.o \
    strings.o \

wrt_rst.o: \
    mod_param.o \
    mod_parallel.o \
    mod_grid.o \
    mod_iounits.o \
    mod_mixing.o \
    mod_ncparam.o \
    mod_netcdf.o \
    mod_ocean.o \
    mod_scalars.o \
    mod_stepping.o \
    nf_fwrite2d.o \
    nf_fwrite3d.o \

mod_arrays.o: \
    mod_param.o \
    mod_parallel.o \
    mod_coupling.o \
    mod_forces.o \
    mod_grid.o \
    mod_mixing.o \
    mod_ocean.o \

master.o: \
    mod_param.o \
    mod_parallel.o \
    mod_iounits.o \
    mod_scalars.o \
    ocean_control.o \

