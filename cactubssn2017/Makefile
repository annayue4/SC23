BIN     = cactubssn2017
CC      = cc -Ofast 
CXX     = CC -Ofast
FC      = ftn -Ofast
CFLAGS	=
FFLAGS	=
CXXFLAGS = 

# Intel CFLAGS needs -std=c99

EXTRA_FLAGS = -I./src/include -DSPEC -DSPEC_CPU -DNDEBUG
EXTRA_CFLAGS = $(EXTRA_FLAGS) -DCCODE
EXTRA_FFLAGS = $(EXTRA_FLAGS) -DFCODE
EXTRA_CXXFLAGS = $(EXTRA_CFLAGS) -DCCTK_DISABLE_RESTRICT=1
OMP_FLAGS = -DSPEC_SUPPRESS_OPENMP

# rate -DSPEC_SUPPRESS_OPENMP
# speed -DSPEC_OPENMP

LIBS = -lm

SOURCES = \
    src/gnu/getopt.c \
    src/gnu/getopt1.c \
    src/gnu/regex.c \
    src/ADMBase/InitSymBound.c \
    src/ADMBase/Initialisation.c \
    src/ADMBase/ParamCheck.c \
    src/ADMBase/Static.c \
    src/ADMBase/cctk_Bindings/cctk_ThornBindings.c \
    src/ADMCoupling/cctk_Bindings/cctk_ThornBindings.c \
    src/ADMMacros/SetLocalSpatialOrder.c \
    src/ADMMacros/cctk_Bindings/cctk_ThornBindings.c \
    src/Boundary/Boundary.c \
    src/Boundary/Check.c \
    src/Boundary/CopyBoundary.c \
    src/Boundary/FlatBoundary.c \
    src/Boundary/NoneBoundary.c \
    src/Boundary/RadiationBoundary.c \
    src/Boundary/Register.c \
    src/Boundary/RobinBoundary.c \
    src/Boundary/ScalarBoundary.c \
    src/Boundary/StaticBoundary.c \
    src/Boundary/cctk_Bindings/cctk_ThornBindings.c \
    src/Cactus/IO/FortranBindingsIO.c \
    src/Cactus/IO/IOMethods.c \
    src/Cactus/IO/OverloadIO.c \
    src/Cactus/cctk_Bindings/cctk_ThornBindings.c \
    src/Cactus/comm/CactusDefaultComm.c \
    src/Cactus/comm/CactusSync.c \
    src/Cactus/comm/Interp.c \
    src/Cactus/comm/OverloadComm.c \
    src/Cactus/comm/Reduction.c \
    src/Cactus/main/ActiveThorns.c \
    src/Cactus/main/Banner.c \
    src/Cactus/main/CactusDefaultEvolve.c \
    src/Cactus/main/CactusDefaultInitialise.c \
    src/Cactus/main/CactusDefaultMainLoopIndex.c \
    src/Cactus/main/CactusDefaultShutdown.c \
    src/Cactus/main/CallStartupFunctions.c \
    src/Cactus/main/CommandLine.c \
    src/Cactus/main/Complex.c \
    src/Cactus/main/ConfigData.c \
    src/Cactus/main/Coord.c \
    src/Cactus/main/DebugDefines.c \
    src/Cactus/main/DefaultTimers.c \
    src/Cactus/main/Dummies.c \
    src/Cactus/main/FortranWrappers.c \
    src/Cactus/main/GHExtensions.c \
    src/Cactus/main/Groups.c \
    src/Cactus/main/GroupsOnGH.c \
    src/Cactus/main/InitialiseCactus.c \
    src/Cactus/main/InitialiseDataStructures.c \
    src/Cactus/main/MainUtils.c \
    src/Cactus/main/Names.c \
    src/Cactus/main/OverloadMain.c \
    src/Cactus/main/Parameters.c \
    src/Cactus/main/ProcessCommandLine.c \
    src/Cactus/main/ProcessEnvironment.c \
    src/Cactus/main/ProcessParameterDatabase.c \
    src/Cactus/main/ScheduleInterface.c \
    src/Cactus/main/SetParams.c \
    src/Cactus/main/SetupCache.c \
    src/Cactus/main/ShutdownCactus.c \
    src/Cactus/main/Subsystems.c \
    src/Cactus/main/Termination.c \
    src/Cactus/main/Traverse.c \
    src/Cactus/main/WarnLevel.c \
    src/Cactus/main/flesh.cc \
    src/Cactus/piraha/AutoGrammar.cc \
    src/Cactus/piraha/Boundary.cc \
    src/Cactus/piraha/Bracket.cc \
    src/Cactus/piraha/Call.cc \
    src/Cactus/piraha/Dot.cc \
    src/Cactus/piraha/End.cc \
    src/Cactus/piraha/Grammar.cc \
    src/Cactus/piraha/Group.cc \
    src/Cactus/piraha/ILiteral.cc \
    src/Cactus/piraha/Literal.cc \
    src/Cactus/piraha/Lookup.cc \
    src/Cactus/piraha/Matcher.cc \
    src/Cactus/piraha/Multi.cc \
    src/Cactus/piraha/NegLookAhead.cc \
    src/Cactus/piraha/Or.cc \
    src/Cactus/piraha/ReParse.cc \
    src/Cactus/piraha/Seq.cc \
    src/Cactus/piraha/Start.cc \
    src/Cactus/piraha/smart_ptr.cc \
    src/Cactus/schedule/ScheduleCreater.c \
    src/Cactus/schedule/ScheduleSorter.c \
    src/Cactus/schedule/ScheduleTraverse.c \
    src/Cactus/util/Cache.c \
    src/Cactus/util/CactusTimers.c \
    src/Cactus/util/Expression.c \
    src/Cactus/util/File.c \
    src/Cactus/util/Hash.c \
    src/Cactus/util/Malloc.c \
    src/Cactus/util/Math.c \
    src/Cactus/util/Misc.c \
    src/Cactus/util/Network.c \
    src/Cactus/util/ParseFile.c \
    src/Cactus/util/RegisterKeyedFunction.c \
    src/Cactus/util/SKBinTree.c \
    src/Cactus/util/StoreHandledData.c \
    src/Cactus/util/StoreKeyedData.c \
    src/Cactus/util/StoreNamedData.c \
    src/Cactus/util/String.c \
    src/Cactus/util/StringList.c \
    src/Cactus/util/Table.c \
    src/Cactus/util/Time.c \
    src/Cactus/util/snprintf.c \
    src/CactusBindings/Functions/ADMBase_Functions.c \
    src/CactusBindings/Functions/AliasedFunctions.c \
    src/CactusBindings/Functions/Boundary_Functions.c \
    src/CactusBindings/Functions/CartGrid3D_Functions.c \
    src/CactusBindings/Functions/CoordBase_Functions.c \
    src/CactusBindings/Functions/GaugeWave_Functions.c \
    src/CactusBindings/Functions/GenericFD_Functions.c \
    src/CactusBindings/Functions/IOASCII_Functions.c \
    src/CactusBindings/Functions/IOBasic_Functions.c \
    src/CactusBindings/Functions/IOUtil_Functions.c \
    src/CactusBindings/Functions/IsFunctionAliased.c \
    src/CactusBindings/Functions/ML_BSSN_Functions.c \
    src/CactusBindings/Functions/ML_BSSN_Helper_Functions.c \
    src/CactusBindings/Functions/MoL_Functions.c \
    src/CactusBindings/Functions/PUGHInterp_Functions.c \
    src/CactusBindings/Functions/PUGHSlab_Functions.c \
    src/CactusBindings/Functions/RegisterThornFunctions.c \
    src/CactusBindings/Functions/StaticConformal_Functions.c \
    src/CactusBindings/Functions/SymBase_Functions.c \
    src/CactusBindings/Implementations/ImplementationBindings.c \
    src/CactusBindings/Parameters/ADMBase_Parameters.c \
    src/CactusBindings/Parameters/ADMCoupling_Parameters.c \
    src/CactusBindings/Parameters/ADMMacros_Parameters.c \
    src/CactusBindings/Parameters/BindingsParameters.c \
    src/CactusBindings/Parameters/Boundary_Parameters.c \
    src/CactusBindings/Parameters/Cactus_Parameters.c \
    src/CactusBindings/Parameters/CartGrid3D_Parameters.c \
    src/CactusBindings/Parameters/CoordBase_Parameters.c \
    src/CactusBindings/Parameters/CoordGauge_Parameters.c \
    src/CactusBindings/Parameters/Fortran_Parameters.c \
    src/CactusBindings/Parameters/GaugeWave_Parameters.c \
    src/CactusBindings/Parameters/GenericFD_Parameters.c \
    src/CactusBindings/Parameters/Global.c \
    src/CactusBindings/Parameters/IOASCII_Parameters.c \
    src/CactusBindings/Parameters/IOBasic_Parameters.c \
    src/CactusBindings/Parameters/IOUtil_Parameters.c \
    src/CactusBindings/Parameters/LocalReduce_Parameters.c \
    src/CactusBindings/Parameters/ML_BSSN_Helper_Parameters.c \
    src/CactusBindings/Parameters/ML_BSSN_Parameters.c \
    src/CactusBindings/Parameters/MoL_Parameters.c \
    src/CactusBindings/Parameters/PUGHInterp_Parameters.c \
    src/CactusBindings/Parameters/PUGHReduce_Parameters.c \
    src/CactusBindings/Parameters/PUGHSlab_Parameters.c \
    src/CactusBindings/Parameters/PUGH_Parameters.c \
    src/CactusBindings/Parameters/StaticConformal_Parameters.c \
    src/CactusBindings/Parameters/SymBase_Parameters.c \
    src/CactusBindings/Parameters/Time_Parameters.c \
    src/CactusBindings/Parameters/TmunuBase_Parameters.c \
    src/CactusBindings/Schedule/BindingsParameterRecovery.c \
    src/CactusBindings/Schedule/BindingsSchedule.c \
    src/CactusBindings/Schedule/ScheduleADMBase.c \
    src/CactusBindings/Schedule/ScheduleADMCoupling.c \
    src/CactusBindings/Schedule/ScheduleADMMacros.c \
    src/CactusBindings/Schedule/ScheduleBoundary.c \
    src/CactusBindings/Schedule/ScheduleCactus.c \
    src/CactusBindings/Schedule/ScheduleCartGrid3D.c \
    src/CactusBindings/Schedule/ScheduleCoordBase.c \
    src/CactusBindings/Schedule/ScheduleCoordGauge.c \
    src/CactusBindings/Schedule/ScheduleFortran.c \
    src/CactusBindings/Schedule/ScheduleGaugeWave.c \
    src/CactusBindings/Schedule/ScheduleGenericFD.c \
    src/CactusBindings/Schedule/ScheduleIOASCII.c \
    src/CactusBindings/Schedule/ScheduleIOBasic.c \
    src/CactusBindings/Schedule/ScheduleIOUtil.c \
    src/CactusBindings/Schedule/ScheduleLocalReduce.c \
    src/CactusBindings/Schedule/ScheduleML_BSSN.c \
    src/CactusBindings/Schedule/ScheduleML_BSSN_Helper.c \
    src/CactusBindings/Schedule/ScheduleMoL.c \
    src/CactusBindings/Schedule/SchedulePUGH.c \
    src/CactusBindings/Schedule/SchedulePUGHInterp.c \
    src/CactusBindings/Schedule/SchedulePUGHReduce.c \
    src/CactusBindings/Schedule/SchedulePUGHSlab.c \
    src/CactusBindings/Schedule/ScheduleStaticConformal.c \
    src/CactusBindings/Schedule/ScheduleSymBase.c \
    src/CactusBindings/Schedule/ScheduleTime.c \
    src/CactusBindings/Schedule/ScheduleTmunuBase.c \
    src/CactusBindings/Variables/ADMBase.c \
    src/CactusBindings/Variables/ADMCoupling.c \
    src/CactusBindings/Variables/ADMMacros.c \
    src/CactusBindings/Variables/BindingsVariables.c \
    src/CactusBindings/Variables/Boundary.c \
    src/CactusBindings/Variables/Cactus.c \
    src/CactusBindings/Variables/CartGrid3D.c \
    src/CactusBindings/Variables/CoordBase.c \
    src/CactusBindings/Variables/CoordGauge.c \
    src/CactusBindings/Variables/Fortran.c \
    src/CactusBindings/Variables/GaugeWave.c \
    src/CactusBindings/Variables/GenericFD.c \
    src/CactusBindings/Variables/IOASCII.c \
    src/CactusBindings/Variables/IOBasic.c \
    src/CactusBindings/Variables/IOUtil.c \
    src/CactusBindings/Variables/LocalReduce.c \
    src/CactusBindings/Variables/ML_BSSN.c \
    src/CactusBindings/Variables/ML_BSSN_Helper.c \
    src/CactusBindings/Variables/MoL.c \
    src/CactusBindings/Variables/PUGH.c \
    src/CactusBindings/Variables/PUGHInterp.c \
    src/CactusBindings/Variables/PUGHReduce.c \
    src/CactusBindings/Variables/PUGHSlab.c \
    src/CactusBindings/Variables/StaticConformal.c \
    src/CactusBindings/Variables/SymBase.c \
    src/CactusBindings/Variables/Time.c \
    src/CactusBindings/Variables/TmunuBase.c \
    src/CartGrid3D/CartGrid3D.c \
    src/CartGrid3D/DecodeSymParameters.c \
    src/CartGrid3D/GetSymmetry.c \
    src/CartGrid3D/ParamCheck.c \
    src/CartGrid3D/RegisterSymmetries.c \
    src/CartGrid3D/SetSymmetry.c \
    src/CartGrid3D/Startup.c \
    src/CartGrid3D/Symmetry.c \
    src/CartGrid3D/cctk_Bindings/cctk_ThornBindings.c \
    src/CoordBase/CoordBase.c \
    src/CoordBase/Domain.c \
    src/CoordBase/GHExtension.c \
    src/CoordBase/cctk_Bindings/cctk_ThornBindings.c \
    src/CoordGauge/Slicing.c \
    src/CoordGauge/cctk_Bindings/cctk_ThornBindings.c \
    src/Fortran/cctk.f90 \
    src/Fortran/cctk_ActiveThorns.f90 \
    src/Fortran/cctk_Banner.f90 \
    src/Fortran/cctk_Bindings/cctk_ThornBindings.c \
    src/Fortran/cctk_Cache.f90 \
    src/Fortran/cctk_Comm.f90 \
    src/Fortran/cctk_CommandLine.f90 \
    src/Fortran/cctk_Complex.f90 \
    src/Fortran/cctk_Constants.f90 \
    src/Fortran/cctk_Coord.f90 \
    src/Fortran/cctk_DebugDefines.f90 \
    src/Fortran/cctk_Faces.f90 \
    src/Fortran/cctk_File.f90 \
    src/Fortran/cctk_Flesh.f90 \
    src/Fortran/cctk_FortranString1.f90 \
    src/Fortran/cctk_FortranWrappers.f90 \
    src/Fortran/cctk_GHExtensions.f90 \
    src/Fortran/cctk_GNU.f90 \
    src/Fortran/cctk_Groups.f90 \
    src/Fortran/cctk_GroupsOnGH.f90 \
    src/Fortran/cctk_IO.f90 \
    src/Fortran/cctk_IOMethods.f90 \
    src/Fortran/cctk_Interp.f90 \
    src/Fortran/cctk_Main.f90 \
    src/Fortran/cctk_Malloc1.f90 \
    src/Fortran/cctk_Math.f90 \
    src/Fortran/cctk_MemAlloc.f90 \
    src/Fortran/cctk_Misc.f90 \
    src/Fortran/cctk_ParamCheck.f90 \
    src/Fortran/cctk_Parameter.f90 \
    src/Fortran/cctk_Reduction.f90 \
    src/Fortran/cctk_Schedule.f90 \
    src/Fortran/cctk_Sync.f90 \
    src/Fortran/cctk_Termination.f90 \
    src/Fortran/cctk_Timers.f90 \
    src/Fortran/cctk_Types.f90 \
    src/Fortran/cctk_Version.f90 \
    src/Fortran/cctk_WarnLevel.f90 \
    src/Fortran/paramcheck.f90 \
    src/Fortran/util_Table.f90 \
    src/GaugeWave/Boundaries.cc \
    src/GaugeWave/GaugeWave_always.cc \
    src/GaugeWave/GaugeWave_initial.cc \
    src/GaugeWave/ParamCheck.cc \
    src/GaugeWave/RegisterMoL.cc \
    src/GaugeWave/RegisterSymmetries.cc \
    src/GaugeWave/Startup.cc \
    src/GaugeWave/cctk_Bindings/cctk_ThornBindings.c \
    src/GenericFD/GenericFD.c \
    src/GenericFD/cctk_Bindings/cctk_ThornBindings.c \
    src/IOASCII/ChooseOutput.c \
    src/IOASCII/Output1D.c \
    src/IOASCII/Output2D.c \
    src/IOASCII/Output3D.c \
    src/IOASCII/Startup.c \
    src/IOASCII/Write1D.c \
    src/IOASCII/Write2D.c \
    src/IOASCII/Write3D.c \
    src/IOASCII/cctk_Bindings/cctk_ThornBindings.c \
    src/IOBasic/OutputInfo.c \
    src/IOBasic/OutputScalar.c \
    src/IOBasic/Startup.c \
    src/IOBasic/WriteInfo.c \
    src/IOBasic/WriteScalar.c \
    src/IOBasic/cctk_Bindings/cctk_ThornBindings.c \
    src/IOUtil/AdvertisedFiles.c \
    src/IOUtil/CheckpointRecovery.c \
    src/IOUtil/Startup.c \
    src/IOUtil/Utils.c \
    src/IOUtil/cctk_Bindings/cctk_ThornBindings.c \
    src/LocalReduce/AvgFunctions.c \
    src/LocalReduce/CountFunctions.c \
    src/LocalReduce/MaxFunctions.c \
    src/LocalReduce/MinFunctions.c \
    src/LocalReduce/Norm1Functions.c \
    src/LocalReduce/Norm2Functions.c \
    src/LocalReduce/Norm3Functions.c \
    src/LocalReduce/Norm4Functions.c \
    src/LocalReduce/NormInfFunctions.c \
    src/LocalReduce/Reduction.c \
    src/LocalReduce/ReductionAvg.c \
    src/LocalReduce/ReductionCount.c \
    src/LocalReduce/ReductionMax.c \
    src/LocalReduce/ReductionMin.c \
    src/LocalReduce/ReductionNorm1.c \
    src/LocalReduce/ReductionNorm2.c \
    src/LocalReduce/ReductionNorm3.c \
    src/LocalReduce/ReductionNorm4.c \
    src/LocalReduce/ReductionNormInf.c \
    src/LocalReduce/ReductionSum.c \
    src/LocalReduce/Startup.c \
    src/LocalReduce/SumFunctions.c \
    src/LocalReduce/cctk_Bindings/cctk_ThornBindings.c \
    src/ML_BSSN/Boundaries.cc \
    src/ML_BSSN/ML_BSSN_Advect.cc \
    src/ML_BSSN/ML_BSSN_Dissipation.cc \
    src/ML_BSSN/ML_BSSN_InitGamma.cc \
    src/ML_BSSN/ML_BSSN_InitRHS.cc \
    src/ML_BSSN/ML_BSSN_Minkowski.cc \
    src/ML_BSSN/ML_BSSN_RHS.cc \
    src/ML_BSSN/ML_BSSN_RHSStaticBoundary.cc \
    src/ML_BSSN/ML_BSSN_boundary.cc \
    src/ML_BSSN/ML_BSSN_constraints.cc \
    src/ML_BSSN/ML_BSSN_convertFromADMBase.cc \
    src/ML_BSSN/ML_BSSN_convertFromADMBaseGamma.cc \
    src/ML_BSSN/ML_BSSN_convertToADMBase.cc \
    src/ML_BSSN/ML_BSSN_convertToADMBaseDtLapseShift.cc \
    src/ML_BSSN/ML_BSSN_convertToADMBaseDtLapseShiftBoundary.cc \
    src/ML_BSSN/ML_BSSN_convertToADMBaseFakeDtLapseShift.cc \
    src/ML_BSSN/ML_BSSN_enforce.cc \
    src/ML_BSSN/RegisterMoL.cc \
    src/ML_BSSN/RegisterSymmetries.cc \
    src/ML_BSSN/Startup.cc \
    src/ML_BSSN/cctk_Bindings/cctk_ThornBindings.c \
    src/ML_BSSN_Helper/ExtrapolateGammas.c \
    src/ML_BSSN_Helper/NewRad.c \
    src/ML_BSSN_Helper/RegisterConstrained.c \
    src/ML_BSSN_Helper/RegisterSlicing.c \
    src/ML_BSSN_Helper/SelectBCsADMBase.c \
    src/ML_BSSN_Helper/SetGroupTags.c \
    src/ML_BSSN_Helper/cctk_Bindings/cctk_ThornBindings.c \
    src/MoL/AB.c \
    src/MoL/ChangeType.c \
    src/MoL/Counter.c \
    src/MoL/Euler.c \
    src/MoL/GenericRK.c \
    src/MoL/ICN.c \
    src/MoL/IndexArrays.c \
    src/MoL/InitialCopy.c \
    src/MoL/Operators.c \
    src/MoL/ParamCheck.c \
    src/MoL/RHSNaNCheck.c \
    src/MoL/RK2-MR-2_1.c \
    src/MoL/RK2.c \
    src/MoL/RK3.c \
    src/MoL/RK4-MR-2_1.c \
    src/MoL/RK4-RK2.c \
    src/MoL/RK4.c \
    src/MoL/RK45.c \
    src/MoL/RK65.c \
    src/MoL/RK87.c \
    src/MoL/RKCoefficients.c \
    src/MoL/Registration.c \
    src/MoL/SandR.c \
    src/MoL/SetTime.c \
    src/MoL/Startup.c \
    src/MoL/StepSize.c \
    src/MoL/cctk_Bindings/cctk_ThornBindings.c \
    src/PUGH/Comm.c \
    src/PUGH/Evolve.c \
    src/PUGH/FinishReceiveGA.c \
    src/PUGH/GHExtension.c \
    src/PUGH/LoadAware.c \
    src/PUGH/Overloadables.c \
    src/PUGH/P2LMappings.c \
    src/PUGH/PostReceiveGA.c \
    src/PUGH/PostSendGA.c \
    src/PUGH/PughUtils.c \
    src/PUGH/Registration.c \
    src/PUGH/SetupGroup.c \
    src/PUGH/SetupPGH.c \
    src/PUGH/SetupPGV.c \
    src/PUGH/Startup.c \
    src/PUGH/Storage.c \
    src/PUGH/Topology.c \
    src/PUGH/Vectors.cc \
    src/PUGH/cctk_Bindings/cctk_ThornBindings.c \
    src/PUGHInterp/InterpGridArrays.c \
    src/PUGHInterp/Startup.c \
    src/PUGHInterp/cctk_Bindings/cctk_ThornBindings.c \
    src/PUGHReduce/ReduceArraysGlobally.c \
    src/PUGHReduce/ReduceGA.c \
    src/PUGHReduce/Reduction.c \
    src/PUGHReduce/ReductionAvg.c \
    src/PUGHReduce/ReductionCount.c \
    src/PUGHReduce/ReductionMax.c \
    src/PUGHReduce/ReductionMin.c \
    src/PUGHReduce/ReductionNorm1.c \
    src/PUGHReduce/ReductionNorm2.c \
    src/PUGHReduce/ReductionNorm3.c \
    src/PUGHReduce/ReductionNorm4.c \
    src/PUGHReduce/ReductionNormInf.c \
    src/PUGHReduce/ReductionSum.c \
    src/PUGHReduce/Startup.c \
    src/PUGHReduce/cctk_Bindings/cctk_ThornBindings.c \
    src/PUGHSlab/DatatypeConversion.c \
    src/PUGHSlab/GetHyperslab.c \
    src/PUGHSlab/Mapping.c \
    src/PUGHSlab/cctk_Bindings/cctk_ThornBindings.c \
    src/StaticConformal/ConfPhys.c \
    src/StaticConformal/Initialise.c \
    src/StaticConformal/cctk_Bindings/cctk_ThornBindings.c \
    src/SymBase/Check.c \
    src/SymBase/Faces.c \
    src/SymBase/Handles.c \
    src/SymBase/Interpolation.c \
    src/SymBase/Startup.c \
    src/SymBase/Statistics.c \
    src/SymBase/Table.c \
    src/SymBase/cctk_Bindings/cctk_ThornBindings.c \
    src/Time/Courant.c \
    src/Time/Given.c \
    src/Time/Initialise.c \
    src/Time/Simple.c \
    src/Time/cctk_Bindings/cctk_ThornBindings.c \
    src/TmunuBase/CopyTmunu.f90 \
    src/TmunuBase/SetStressEnergyState.f90 \
    src/TmunuBase/SetTmunu.f90 \
    src/TmunuBase/ZeroTmunu.f90 \
    src/TmunuBase/cctk_Bindings/cctk_ThornBindings.c \
    src/datestamp.c

# With the above dupliate source names in different directories,
# one can not just dump all .o's into one file, so keep .o in
# the source directory and add "src" to the above paths.
 
TMPOBJ  = $(SOURCES:.c=.o)
TMPOBJ2 = $(TMPOBJ:.cc=.o)
OBJ     = $(TMPOBJ2:.f90=.o)
.SUFFIXES: .f90

ifeq ($(MAKECMDGOALS),cactubssn2017_omp)
BIN       = cactubssn2017_omp
OMP_FLAGS = -DSPEC_OPENMP
endif


$(BIN):	x$(BIN) $(BIN).execute.script
	cp $(BIN).execute.script $(BIN)
x$(BIN): $(OBJ)
	$(CXX) $(CXXFLAGS) -o x$(BIN) $(OBJ) $(LDFLAGS) $(LIBS)

.c.o:
	$(CC) -c -o $@ $(EXTRA_CFLAGS) $(OMP_FLAGS) $(CFLAGS) $<

.cc.o:
	$(CXX) -c -o $@ $(EXTRA_CXXFLAGS) $(OMP_FLAGS) $(CXXFLAGS) $<

.f90.o:
	$(FC) -c -o $@ $(EXTRA_FFLAGS) $(OMP_FLAGS) $(FFLAGS) $<

clean:
	-rm -f core
	-rm -f $(OBJ) *.mod src/Fortran/*.mod

clobber: clean
	-rm -f $(BIN) x$(BIN) $(BIN)_omp x$(BIN)_omp gxx.xl gxy.xl spec_*.par

# Dependencies
src/Fortran/cctk.o:  \
    src/Fortran/util_Table.o \
    src/Fortran/cctk_WarnLevel.o \
    src/Fortran/cctk_Version.o \
    src/Fortran/cctk_Types.o \
    src/Fortran/cctk_Timers.o \
    src/Fortran/cctk_Termination.o \
    src/Fortran/cctk_Sync.o \
    src/Fortran/cctk_Schedule.o \
    src/Fortran/cctk_Reduction.o \
    src/Fortran/cctk_Parameter.o \
    src/Fortran/cctk_ParamCheck.o \
    src/Fortran/cctk_Misc.o \
    src/Fortran/cctk_MemAlloc.o \
    src/Fortran/cctk_Math.o \
    src/Fortran/cctk_Malloc1.o \
    src/Fortran/cctk_Main.o \
    src/Fortran/cctk_Interp.o \
    src/Fortran/cctk_IOMethods.o \
    src/Fortran/cctk_IO.o \
    src/Fortran/cctk_GroupsOnGH.o \
    src/Fortran/cctk_Groups.o \
    src/Fortran/cctk_GNU.o \
    src/Fortran/cctk_GHExtensions.o \
    src/Fortran/cctk_FortranWrappers.o \
    src/Fortran/cctk_FortranString1.o \
    src/Fortran/cctk_Flesh.o \
    src/Fortran/cctk_File.o \
    src/Fortran/cctk_Faces.o \
    src/Fortran/cctk_DebugDefines.o \
    src/Fortran/cctk_Coord.o \
    src/Fortran/cctk_Constants.o \
    src/Fortran/cctk_Complex.o \
    src/Fortran/cctk_CommandLine.o \
    src/Fortran/cctk_Comm.o \
    src/Fortran/cctk_Cache.o \
    src/Fortran/cctk_Banner.o \
    src/Fortran/cctk_ActiveThorns.o

