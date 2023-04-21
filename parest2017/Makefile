
BIN     = parest2017

CXX     = CC -fast
CXXFLAGS       = 
EXTRA_CXXFLAGS = -I src -I src/include -DSPEC -DSPEC_CPU -DNDEBUG
#LDFLAGS = -lm -lsci
LIBS = -lm -static 

SOURCES  = \
    src/source/base/auto_derivative_function.cc \
    src/source/base/boost_threads.cc \
    src/source/base/conditional_ostream.cc \
    src/source/base/config.cc \
    src/source/base/convergence_table.cc \
    src/source/base/data_out_base.cc \
    src/source/base/exceptions.cc \
    src/source/base/flow_function.cc \
    src/source/base/function.cc \
    src/source/base/function_derivative.cc \
    src/source/base/function_lib.cc \
    src/source/base/function_lib_cutoff.cc \
    src/source/base/function_parser.cc \
    src/source/base/function_time.cc \
    src/source/base/geometry_info.cc \
    src/source/base/job_identifier.cc \
    src/source/base/log.cc \
    src/source/base/memory_consumption.cc \
    src/source/base/multithread_info.cc \
    src/source/base/parameter_handler.cc \
    src/source/base/parsed_function.cc \
    src/source/base/path_search.cc \
    src/source/base/polynomial.cc \
    src/source/base/polynomial_space.cc \
    src/source/base/polynomials_abf.cc \
    src/source/base/polynomials_bdm.cc \
    src/source/base/polynomials_p.cc \
    src/source/base/polynomials_raviart_thomas.cc \
    src/source/base/quadrature.cc \
    src/source/base/quadrature_lib.cc \
    src/source/base/quadrature_selector.cc \
    src/source/base/subscriptor.cc \
    src/source/base/symmetric_tensor.cc \
    src/source/base/table_handler.cc \
    src/source/base/tensor.cc \
    src/source/base/tensor_function.cc \
    src/source/base/tensor_product_polynomials.cc \
    src/source/base/thread_management.cc \
    src/source/base/timer.cc \
    src/source/base/utilities.cc \
    src/source/dofs/dof_accessor.cc \
    src/source/dofs/dof_faces.cc \
    src/source/dofs/dof_handler.cc \
    src/source/dofs/dof_levels.all_dimensions.cc \
    src/source/dofs/dof_objects.all_dimensions.cc \
    src/source/dofs/dof_objects.cc \
    src/source/dofs/dof_renumbering.cc \
    src/source/dofs/dof_tools.cc \
    src/source/fe/fe.cc \
    src/source/fe/fe_abf.cc \
    src/source/fe/fe_data.cc \
    src/source/fe/fe_dgp.cc \
    src/source/fe/fe_dgp_monomial.cc \
    src/source/fe/fe_dgp_nonparametric.cc \
    src/source/fe/fe_dgq.cc \
    src/source/fe/fe_nedelec.cc \
    src/source/fe/fe_nedelec_1d.cc \
    src/source/fe/fe_nedelec_2d.cc \
    src/source/fe/fe_nedelec_3d.cc \
    src/source/fe/fe_poly.cc \
    src/source/fe/fe_poly_tensor.cc \
    src/source/fe/fe_q.cc \
    src/source/fe/fe_q_hierarchical.cc \
    src/source/fe/fe_raviart_thomas.cc \
    src/source/fe/fe_raviart_thomas_nodal.cc \
    src/source/fe/fe_system.cc \
    src/source/fe/fe_tools.all_dimensions.cc \
    src/source/fe/fe_tools.cc \
    src/source/fe/fe_values.cc \
    src/source/fe/mapping.cc \
    src/source/fe/mapping_c1.cc \
    src/source/fe/mapping_cartesian.cc \
    src/source/fe/mapping_q.cc \
    src/source/fe/mapping_q1.cc \
    src/source/fe/mapping_q1_eulerian.cc \
    src/source/fe/mapping_q_eulerian.cc \
    src/source/grid/grid_generator.cc \
    src/source/grid/grid_in.cc \
    src/source/grid/grid_out.all_dimensions.cc \
    src/source/grid/grid_out.cc \
    src/source/grid/grid_refinement.cc \
    src/source/grid/grid_reordering.cc \
    src/source/grid/grid_tools.cc \
    src/source/grid/intergrid_map.cc \
    src/source/grid/persistent_tria.cc \
    src/source/grid/tria.all_dimensions.cc \
    src/source/grid/tria.cc \
    src/source/grid/tria_accessor.cc \
    src/source/grid/tria_boundary.cc \
    src/source/grid/tria_boundary_lib.cc \
    src/source/grid/tria_faces.cc \
    src/source/grid/tria_levels.cc \
    src/source/grid/tria_objects.all_dimensions.cc \
    src/source/grid/tria_objects.cc \
    src/source/hp/dof_faces.cc \
    src/source/hp/dof_handler.cc \
    src/source/hp/dof_levels.all_dimensions.cc \
    src/source/hp/dof_levels.cc \
    src/source/hp/dof_objects.all_dimensions.cc \
    src/source/hp/fe_collection.cc \
    src/source/hp/fe_values.cc \
    src/source/hp/mapping_collection.cc \
    src/source/lac/block_matrix_array.cc \
    src/source/lac/block_sparse_matrix.cc \
    src/source/lac/block_sparse_matrix_ez.cc \
    src/source/lac/block_sparsity_pattern.cc \
    src/source/lac/block_vector.cc \
    src/source/lac/chunk_sparse_matrix.cc \
    src/source/lac/chunk_sparsity_pattern.cc \
    src/source/lac/compressed_set_sparsity_pattern.cc \
    src/source/lac/compressed_simple_sparsity_pattern.cc \
    src/source/lac/compressed_sparsity_pattern.cc \
    src/source/lac/constraint_matrix.cc \
    src/source/lac/full_matrix.cc \
    src/source/lac/lapack_full_matrix.cc \
    src/source/lac/matrix_lib.cc \
    src/source/lac/matrix_out.cc \
    src/source/lac/petsc_block_sparse_matrix.cc \
    src/source/lac/petsc_full_matrix.cc \
    src/source/lac/petsc_matrix_base.cc \
    src/source/lac/petsc_parallel_block_sparse_matrix.cc \
    src/source/lac/petsc_parallel_block_vector.cc \
    src/source/lac/petsc_parallel_sparse_matrix.cc \
    src/source/lac/petsc_parallel_vector.cc \
    src/source/lac/petsc_precondition.cc \
    src/source/lac/petsc_solver.cc \
    src/source/lac/petsc_sparse_matrix.cc \
    src/source/lac/petsc_vector.cc \
    src/source/lac/petsc_vector_base.cc \
    src/source/lac/precondition_block.cc \
    src/source/lac/precondition_block_ez.cc \
    src/source/lac/solver.cc \
    src/source/lac/solver_control.cc \
    src/source/lac/sparse_decomposition.cc \
    src/source/lac/sparse_direct.cc \
    src/source/lac/sparse_ilu.cc \
    src/source/lac/sparse_matrix.cc \
    src/source/lac/sparse_matrix_ez.cc \
    src/source/lac/sparse_mic.cc \
    src/source/lac/sparse_vanka.cc \
    src/source/lac/sparsity_pattern.cc \
    src/source/lac/sparsity_tools.cc \
    src/source/lac/swappable_vector.cc \
    src/source/lac/tridiagonal_matrix.cc \
    src/source/lac/trilinos_block_sparse_matrix.cc \
    src/source/lac/trilinos_block_vector.cc \
    src/source/lac/trilinos_precondition.cc \
    src/source/lac/trilinos_precondition_block.cc \
    src/source/lac/trilinos_solver.cc \
    src/source/lac/trilinos_solver_block.cc \
    src/source/lac/trilinos_sparse_matrix.cc \
    src/source/lac/trilinos_sparsity_pattern.cc \
    src/source/lac/trilinos_vector.cc \
    src/source/lac/trilinos_vector_base.cc \
    src/source/lac/vector.cc \
    src/source/lac/vector_memory.cc \
    src/source/lac/vector_view.cc \
    src/source/libparest/global_parameters.cc \
    src/source/libparest/graphical_display.cc \
    src/source/libparest/grid_transfer.cc \
    src/source/libparest/message_log.cc \
    src/source/libparest/statistics.cc \
    src/source/libparest/top_level.cc \
    src/source/libparest/utilities.cc \
    src/source/me-tomography/boundary_sources_phantom.cc \
    src/source/me-tomography/boundary_sources_planarz8.cc \
    src/source/me-tomography/coefficient.cc \
    src/source/me-tomography/evaluations.cc \
    src/source/me-tomography/experiment_description.cc \
    src/source/me-tomography/factories.cc \
    src/source/me-tomography/forward.cc \
    src/source/me-tomography/forward_solver_evaluators.cc \
    src/source/me-tomography/forward_solver_parameters.cc \
    src/source/me-tomography/geometry.cc \
    src/source/me-tomography/me_parameters.cc \
    src/source/me-tomography/me_slave.cc \
    src/source/me-tomography/me_tomography.cc \
    src/source/me-tomography/measurement_weights.cc \
    src/source/me-tomography/measurements.cc \
    src/source/me-tomography/problem_description.cc \
    src/source/me-tomography/solver.cc \
    src/source/me-tomography/state_discretization.cc \
    src/source/me-tomography/synthetic_data.cc \
    src/source/me-tomography/targets.cc \
    src/source/multigrid/mg_base.cc \
    src/source/multigrid/mg_dof_accessor.cc \
    src/source/multigrid/mg_dof_handler.cc \
    src/source/multigrid/mg_dof_tools.cc \
    src/source/multigrid/mg_smoother.cc \
    src/source/multigrid/mg_tools.all_dimensions.cc \
    src/source/multigrid/mg_transfer_block.cc \
    src/source/multigrid/mg_transfer_component.cc \
    src/source/multigrid/mg_transfer_prebuilt.cc \
    src/source/multigrid/multigrid.all_dimensions.cc \
    src/source/numerics/data_out.cc \
    src/source/numerics/data_out_faces.cc \
    src/source/numerics/data_out_rotation.cc \
    src/source/numerics/data_out_stack.cc \
    src/source/numerics/data_postprocessor.cc \
    src/source/numerics/derivative_approximation.cc \
    src/source/numerics/error_estimator.cc \
    src/source/numerics/fe_field_function.cc \
    src/source/numerics/histogram.cc \
    src/source/numerics/matrices.all_dimensions.cc \
    src/source/numerics/matrices.cc \
    src/source/numerics/solution_transfer.cc \
    src/source/numerics/time_dependent.cc \
    src/source/numerics/vectors.all_dimensions.cc \
    src/source/numerics/vectors.cc \
    src/source/libparest/master/master.cc \
    src/source/libparest/master/newton_method.cc \
    src/source/libparest/master/step_length_control.cc \
    src/source/libparest/parallel/control.cc \
    src/source/libparest/parallel/message_log.cc \
    src/source/libparest/parallel/multiple_experiments.cc \
    src/source/libparest/parallel/tools.cc \
    src/source/libparest/parameter/base.cc \
    src/source/libparest/parameter/bounds.cc \
    src/source/libparest/parameter/factory.cc \
    src/source/libparest/parameter/field.cc \
    src/source/libparest/parameter/field_discretization.cc \
    src/source/libparest/parameter/regularization.cc \
    src/source/libparest/slave/factory.cc \
    src/source/libparest/slave/slave.cc \
    src/source/libparest/slave/stationary/boundary_values.cc \
    src/source/libparest/slave/stationary/evaluations.cc \
    src/source/libparest/slave/stationary/global_matrix.cc \
    src/source/libparest/slave/stationary/grid_refinement.cc \
    src/source/libparest/slave/stationary/measurements.cc \
    src/source/libparest/slave/stationary/problem_description.cc \
    src/source/libparest/slave/stationary/slave.cc \
    src/source/libparest/slave/stationary/state_discretization.cc \
    src/source/libparest/slave/stationary/synthetic_data.cc

OBJ     = $(SOURCES:.cc=.o)

#VPATH	= src/source
.SUFFIXES: .cc

$(BIN):	x$(BIN) $(BIN).execute.script
	cp $(BIN).execute.script $(BIN)
x$(BIN): $(OBJ)
	$(CXX) $(CXXFLAGS) -o x$(BIN) $(OBJ) $(LDFLAGS) $(LIBS)

.cc.o:
	$(CXX) -c -o $@ $(EXTRA_CXXFLAGS) $(CXXFLAGS) $<

clean:
	-rm -f core
	-rm -f $(OBJ)

clobber: clean
	-rm -f $(BIN) x$(BIN)
	-rm -f me.prm log statistics *.vtk
