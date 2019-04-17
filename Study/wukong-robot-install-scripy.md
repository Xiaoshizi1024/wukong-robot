# 利用一件试安装  

## 背景
 
-  树莓派3B+
-  2Mir 


## 实验 

1.  树莓派换源

`sudo wget http://wukong-install.oss-cn-hangzhou.aliyuncs.com/changeSource.sh && sudo chmod 777 changeSource.sh &&./changeSource.sh
` 
2. 正式启动一件安装 
`sudo wget http://wukong-install.oss-cn-hangzhou.aliyuncs.com/install.sh && sudo chmod 777 install.sh &&./install.sh
` 

安装过后发现莓没有安装第三方的技能库， 也还没有`_snowboydetect.so` 


### 安装细节  


2. 正式启动一件安装 
`sudo wget http://wukong-install.oss-cn-hangzhou.aliyuncs.com/install.sh && sudo chmod 777 install.sh &&./install.sh
```
swig-3.0.10/Examples/test-suite/scilab/scilab_pointer_conversion_functions_runme.sci
swig-3.0.10/Examples/test-suite/scilab/sizet_runme.sci
swig-3.0.10/Examples/test-suite/scilab/return_const_value_runme.sci
swig-3.0.10/Examples/test-suite/scilab/sneaky1_runme.sci
swig-3.0.10/Examples/test-suite/scilab/overload_extend_runme.sci
swig-3.0.10/Examples/test-suite/scilab/simple_array_runme.sci
swig-3.0.10/Examples/test-suite/scilab/newobject2_runme.sci
swig-3.0.10/Examples/test-suite/scilab/arrays_dimensionless_runme.sci
swig-3.0.10/Examples/test-suite/scilab/bools_runme.sci
swig-3.0.10/Examples/test-suite/scilab/inherit_missing_runme.sci
swig-3.0.10/Examples/test-suite/scilab/inout_runme.sci
swig-3.0.10/Examples/test-suite/scilab/constover_runme.sci
swig-3.0.10/Examples/test-suite/scilab/li_typemaps_runme.sci
swig-3.0.10/Examples/test-suite/scilab/primitive_types_runme.sci
swig-3.0.10/Examples/test-suite/scilab/cpp_basic_runme.sci
swig-3.0.10/Examples/test-suite/scilab/abstract_typedef_runme.sci
swig-3.0.10/Examples/test-suite/scilab/varargs_overload_runme.sci
swig-3.0.10/Examples/test-suite/scilab/overload_arrays_runme.sci
swig-3.0.10/Examples/test-suite/scilab/cpp_enum_runme.sci
swig-3.0.10/Examples/test-suite/scilab/anonymous_bitfield_runme.sci
swig-3.0.10/Examples/test-suite/scilab/member_pointer_runme.sci
swig-3.0.10/Examples/test-suite/scilab/li_cpointer_runme.sci
swig-3.0.10/Examples/test-suite/scilab/li_std_deque_runme.sci
swig-3.0.10/Examples/test-suite/scilab/smart_pointer_simple_runme.sci
swig-3.0.10/Examples/test-suite/scilab/inctest_runme.sci
swig-3.0.10/Examples/test-suite/scilab/union_parameter_runme.sci
swig-3.0.10/Examples/test-suite/scilab/abstract_inherit_runme.sci
swig-3.0.10/Examples/test-suite/scilab/char_constant_runme.sci
swig-3.0.10/Examples/test-suite/scilab/overload_extend2_runme.sci
swig-3.0.10/Examples/test-suite/scilab/primitive_ref_runme.sci
swig-3.0.10/Examples/test-suite/scilab/overload_simple_runme.sci
swig-3.0.10/Examples/test-suite/scilab/funcptr_cpp_runme.sci
swig-3.0.10/Examples/test-suite/scilab/integers_runme.sci
swig-3.0.10/Examples/test-suite/scilab/apply_strings_runme.sci
swig-3.0.10/Examples/test-suite/scilab/li_std_pair_runme.sci
swig-3.0.10/Examples/test-suite/scilab/overload_complicated_runme.sci
swig-3.0.10/Examples/test-suite/scilab/template_classes_runme.sci
swig-3.0.10/Examples/test-suite/scilab/nested_structs_runme.sci
swig-3.0.10/Examples/test-suite/scilab/swigtest.quit
swig-3.0.10/Examples/test-suite/scilab/scilab_identifier_name_runme.sci
swig-3.0.10/Examples/test-suite/scilab/ret_by_value_runme.sci
swig-3.0.10/Examples/test-suite/scilab/li_std_except_runme.sci
swig-3.0.10/Examples/test-suite/scilab/array_member_runme.sci
swig-3.0.10/Examples/test-suite/scilab/typedef_struct_cpp_runme.sci
swig-3.0.10/Examples/test-suite/scilab/access_change_runme.sci
swig-3.0.10/Examples/test-suite/scilab/enums_runme.sci
swig-3.0.10/Examples/test-suite/scilab/varargs_runme.sci
swig-3.0.10/Examples/test-suite/scilab/li_std_string_extra_runme.sci
swig-3.0.10/Examples/test-suite/scilab/funcptr_runme.sci
swig-3.0.10/Examples/test-suite/scilab/name_runme.sci
swig-3.0.10/Examples/test-suite/scilab/scilab_li_matrix_runme.sci
swig-3.0.10/Examples/test-suite/python_director.i
swig-3.0.10/Examples/test-suite/exception_partial_info.i
swig-3.0.10/Examples/test-suite/smart_pointer_const_overload.i
swig-3.0.10/Examples/test-suite/member_template.i
swig-3.0.10/Examples/test-suite/samename.i
swig-3.0.10/Examples/test-suite/li_std_pair_using.i
swig-3.0.10/Examples/test-suite/nested_directors.i
swig-3.0.10/Examples/test-suite/overload_arrays.i
swig-3.0.10/Examples/test-suite/director_smartptr.i
swig-3.0.10/Examples/test-suite/li_std_set.i
swig-3.0.10/Examples/test-suite/default_constructor.i
swig-3.0.10/Examples/test-suite/template_explicit.i
swig-3.0.10/Examples/test-suite/arrays_dimensionless.i
swig-3.0.10/Examples/test-suite/naturalvar_more.i
swig-3.0.10/Examples/test-suite/template_typemaps_typedef2.i
swig-3.0.10/Examples/test-suite/exception_order.i
swig-3.0.10/Examples/test-suite/threads_exception.i
swig-3.0.10/Examples/test-suite/using_inherit.i
swig-3.0.10/Examples/test-suite/namespace_union.i
swig-3.0.10/Examples/test-suite/template_using.i
swig-3.0.10/Examples/test-suite/char_constant.i
swig-3.0.10/Examples/test-suite/expressions.i
swig-3.0.10/Examples/test-suite/ruby_minherit_shared_ptr.i
swig-3.0.10/Examples/test-suite/README
swig-3.0.10/Examples/test-suite/conversion_operators.i
swig-3.0.10/Examples/test-suite/arrayref.i
swig-3.0.10/Examples/test-suite/ocaml/
swig-3.0.10/Examples/test-suite/ocaml/minherit_runme.ml
swig-3.0.10/Examples/test-suite/ocaml/throw_exception_runme.ml
swig-3.0.10/Examples/test-suite/ocaml/name_runme.ml
swig-3.0.10/Examples/test-suite/ocaml/Makefile.in
swig-3.0.10/Examples/test-suite/ocaml/unions_runme.ml
swig-3.0.10/Examples/test-suite/ocaml/using_protected_runme.ml
swig-3.0.10/Examples/test-suite/ocaml/sneaky1_runme.ml
swig-3.0.10/Examples/test-suite/ocaml/typename_runme.ml
swig-3.0.10/Examples/test-suite/ocaml/newobject1_runme.ml
swig-3.0.10/Examples/test-suite/ocaml/makedebugtop
swig-3.0.10/Examples/test-suite/ocaml/class_ignore_runme.ml
swig-3.0.10/Examples/test-suite/ocaml/overload_copy_runme.ml
swig-3.0.10/Examples/test-suite/ocaml/README
swig-3.0.10/Examples/test-suite/ocaml/imports_runme.ml
swig-3.0.10/Examples/test-suite/ocaml/typedef_mptr_runme.ml
swig-3.0.10/Examples/test-suite/ocaml/voidtest_runme.ml
swig-3.0.10/Examples/test-suite/ocaml/varargs_runme.ml
swig-3.0.10/Examples/test-suite/friends_template.i
swig-3.0.10/Examples/test-suite/javascript/
swig-3.0.10/Examples/test-suite/javascript/empty_c_runme.js
swig-3.0.10/Examples/test-suite/javascript/preproc_include_runme.js
swig-3.0.10/Examples/test-suite/javascript/cpp_enum_runme.js
swig-3.0.10/Examples/test-suite/javascript/rename_simple_runme.js
swig-3.0.10/Examples/test-suite/javascript/cpp_namespace_runme.js
swig-3.0.10/Examples/test-suite/javascript/arrays_global_runme.js
swig-3.0.10/Examples/test-suite/javascript/constructor_copy_runme.js
swig-3.0.10/Examples/test-suite/javascript/abstract_access_runme.js
swig-3.0.10/Examples/test-suite/javascript/nspace_runme.js
swig-3.0.10/Examples/test-suite/javascript/empty_runme.js
swig-3.0.10/Examples/test-suite/javascript/Makefile.in
swig-3.0.10/Examples/test-suite/javascript/typemap_ns_using_runme.js
swig-3.0.10/Examples/test-suite/javascript/cpp11_strongly_typed_enumerations_runme.js
swig-3.0.10/Examples/test-suite/javascript/typedef_scope_runme.js
swig-3.0.10/Examples/test-suite/javascript/rename2_runme.js
swig-3.0.10/Examples/test-suite/javascript/rename1_runme.js
swig-3.0.10/Examples/test-suite/javascript/cpp_static_runme.js
swig-3.0.10/Examples/test-suite/javascript/typemap_delete_runme.js
swig-3.0.10/Examples/test-suite/javascript/abstract_typedef_runme.js
swig-3.0.10/Examples/test-suite/javascript/null_pointer_runme.js
swig-3.0.10/Examples/test-suite/javascript/infinity_runme.js
swig-3.0.10/Examples/test-suite/javascript/abstract_virtual_runme.js
swig-3.0.10/Examples/test-suite/javascript/struct_value_runme.js
swig-3.0.10/Examples/test-suite/javascript/namespace_virtual_method_runme.js
swig-3.0.10/Examples/test-suite/javascript/class_ignore_runme.js
swig-3.0.10/Examples/test-suite/javascript/complextest_runme.js
swig-3.0.10/Examples/test-suite/javascript/rename4_runme.js
swig-3.0.10/Examples/test-suite/javascript/using1_runme.js
swig-3.0.10/Examples/test-suite/javascript/char_strings_runme.js
swig-3.0.10/Examples/test-suite/javascript/ret_by_value_runme.js
swig-3.0.10/Examples/test-suite/javascript/char_binary_runme.js
swig-3.0.10/Examples/test-suite/javascript/typemap_namespace_runme.js
swig-3.0.10/Examples/test-suite/javascript/disown_runme.js
swig-3.0.10/Examples/test-suite/javascript/overload_copy_runme.js
swig-3.0.10/Examples/test-suite/javascript/class_scope_weird_runme.js
swig-3.0.10/Examples/test-suite/javascript/callback_runme.js
swig-3.0.10/Examples/test-suite/javascript/abstract_inherit_runme.js
swig-3.0.10/Examples/test-suite/javascript/typedef_class_runme.js
swig-3.0.10/Examples/test-suite/javascript/using2_runme.js
swig-3.0.10/Examples/test-suite/javascript/director_alternating_runme.js
swig-3.0.10/Examples/test-suite/javascript/node_template/
swig-3.0.10/Examples/test-suite/javascript/node_template/index.js.in
swig-3.0.10/Examples/test-suite/javascript/node_template/binding.gyp.in
swig-3.0.10/Examples/test-suite/javascript/dynamic_cast_runme.js
swig-3.0.10/Examples/test-suite/javascript/template_static_runme.js
swig-3.0.10/Examples/test-suite/javascript/rename_scope_runme.js
swig-3.0.10/Examples/test-suite/javascript/abstract_typedef2_runme.js
swig-3.0.10/Examples/test-suite/javascript/varargs_runme.js
swig-3.0.10/Examples/test-suite/javascript/enum_template_runme.js
swig-3.0.10/Examples/test-suite/javascript/nspace_extend_runme.js
swig-3.0.10/Examples/test-suite/javascript/array_member_runme.js
swig-3.0.10/Examples/test-suite/javascript/constover_runme.js
swig-3.0.10/Examples/test-suite/javascript/typemap_arrays_runme.js
swig-3.0.10/Examples/test-suite/javascript/string_simple_runme.js
swig-3.0.10/Examples/test-suite/javascript/preproc_runme.js
swig-3.0.10/Examples/test-suite/javascript/rename3_runme.js
swig-3.0.10/Examples/test-suite/javascript/typedef_inherit_runme.js
swig-3.0.10/Examples/test-suite/cpp11_result_of.i
swig-3.0.10/Examples/test-suite/li_std_map.i
swig-3.0.10/Examples/test-suite/smart_pointer_not.i
swig-3.0.10/Examples/test-suite/template_default_arg_overloaded.i
swig-3.0.10/Examples/test-suite/constructor_exception.i
swig-3.0.10/Examples/test-suite/inherit_member.i
swig-3.0.10/Examples/test-suite/template_inherit_abstract.i
swig-3.0.10/Examples/test-suite/li_std_wstring.i
swig-3.0.10/Examples/test-suite/typedef_array_member.i
swig-3.0.10/Examples/test-suite/java_enums.i
swig-3.0.10/Examples/test-suite/director_finalizer.i
swig-3.0.10/Examples/test-suite/global_vars.i
swig-3.0.10/Examples/test-suite/sizet.i
swig-3.0.10/Examples/test-suite/template_typedef_cplx5.i
swig-3.0.10/Examples/test-suite/rename2.i
swig-3.0.10/Examples/test-suite/clientdata_prop.list
swig-3.0.10/Examples/test-suite/template_qualifier.i
swig-3.0.10/Examples/test-suite/overload_rename.i
swig-3.0.10/Examples/test-suite/sneaky1.i
swig-3.0.10/Examples/test-suite/director_exception.i
swig-3.0.10/Examples/test-suite/template_keyword_in_type.i
swig-3.0.10/Examples/test-suite/sym.i
swig-3.0.10/Examples/test-suite/li_std_queue.i
swig-3.0.10/Examples/test-suite/li_std_vector_ptr.i
swig-3.0.10/Examples/test-suite/li_std_functors.i
swig-3.0.10/Examples/test-suite/immutable_values.i
swig-3.0.10/Examples/test-suite/go_subdir_import_a.i
swig-3.0.10/Examples/test-suite/java/
swig-3.0.10/Examples/test-suite/java/using_directive_and_declaration_runme.java
swig-3.0.10/Examples/test-suite/java/aggregate_runme.java
swig-3.0.10/Examples/test-suite/java/director_unroll_runme.java
swig-3.0.10/Examples/test-suite/java/imports_runme.java
swig-3.0.10/Examples/test-suite/java/array_member_runme.java
swig-3.0.10/Examples/test-suite/java/enum_macro_runme.java
swig-3.0.10/Examples/test-suite/java/smart_pointer_const_overload_runme.java
swig-3.0.10/Examples/test-suite/java/multiple_inheritance_interfaces_runme.java
swig-3.0.10/Examples/test-suite/java/template_namespace_forward_declaration_runme.java
swig-3.0.10/Examples/test-suite/java/pointer_reference_runme.java
swig-3.0.10/Examples/test-suite/java/li_std_string_runme.java
swig-3.0.10/Examples/test-suite/java/java_lib_arrays_dimensionless_runme.java
swig-3.0.10/Examples/test-suite/java/director_nspace_runme.java
swig-3.0.10/Examples/test-suite/java/java_prepost_runme.java
swig-3.0.10/Examples/test-suite/java/java_director_runme.java
swig-3.0.10/Examples/test-suite/java/director_primitives_runme.java
swig-3.0.10/Examples/test-suite/java/enum_thorough_typeunsafe_runme.java
swig-3.0.10/Examples/test-suite/java/li_std_except_runme.java
swig-3.0.10/Examples/test-suite/java/java_throws_runme.java
swig-3.0.10/Examples/test-suite/java/cpp11_li_std_array_runme.java
swig-3.0.10/Examples/test-suite/java/rename1_runme.java
swig-3.0.10/Examples/test-suite/java/java_director_assumeoverride_runme.java
swig-3.0.10/Examples/test-suite/java/ignore_parameter_runme.java
swig-3.0.10/Examples/test-suite/java/director_exception_runme.java
swig-3.0.10/Examples/test-suite/java/java_typemaps_proxy_runme.java
swig-3.0.10/Examples/test-suite/java/director_classes_runme.java
swig-3.0.10/Examples/test-suite/java/template_partial_specialization_runme.java
swig-3.0.10/Examples/test-suite/java/inctest_runme.java
swig-3.0.10/Examples/test-suite/java/director_string_runme.java
swig-3.0.10/Examples/test-suite/java/Makefile.in
swig-3.0.10/Examples/test-suite/java/nested_class_runme.java
swig-3.0.10/Examples/test-suite/java/nested_structs_runme.java
swig-3.0.10/Examples/test-suite/java/li_boost_intrusive_ptr_runme.java
swig-3.0.10/Examples/test-suite/java/dynamic_cast_runme.java
swig-3.0.10/Examples/test-suite/java/template_templated_constructors_runme.java
swig-3.0.10/Examples/test-suite/java/director_binary_string_runme.java
swig-3.0.10/Examples/test-suite/java/naturalvar_more_runme.java
swig-3.0.10/Examples/test-suite/java/derived_nested_runme.java
swig-3.0.10/Examples/test-suite/java/extend_special_variables_runme.java
swig-3.0.10/Examples/test-suite/java/java_director_ptrclass_runme.java
swig-3.0.10/Examples/test-suite/java/director_thread_runme.java
swig-3.0.10/Examples/test-suite/java/nested_workaround_runme.java
swig-3.0.10/Examples/test-suite/java/li_typemaps_runme.java
swig-3.0.10/Examples/test-suite/java/director_protected_runme.java
swig-3.0.10/Examples/test-suite/java/template_typedef_typedef_runme.java
swig-3.0.10/Examples/test-suite/java/director_nested_class_runme.java
swig-3.0.10/Examples/test-suite/java/template_default_arg_runme.java
swig-3.0.10/Examples/test-suite/java/template_classes_runme.java
swig-3.0.10/Examples/test-suite/java/rename3_runme.java
swig-3.0.10/Examples/test-suite/java/director_smartptr_runme.java
swig-3.0.10/Examples/test-suite/java/apply_signed_char_runme.java
swig-3.0.10/Examples/test-suite/java/cpp11_strongly_typed_enumerations_runme.java
swig-3.0.10/Examples/test-suite/java/intermediary_classname_runme.java
swig-3.0.10/Examples/test-suite/java/smart_pointer_ignore_runme.java
swig-3.0.10/Examples/test-suite/java/cpp11_result_of_runme.java
swig-3.0.10/Examples/test-suite/java/li_boost_shared_ptr_attribute_runme.java
swig-3.0.10/Examples/test-suite/java/li_std_auto_ptr_runme.java
swig-3.0.10/Examples/test-suite/java/multiple_inheritance_runme.java
swig-3.0.10/Examples/test-suite/java/extern_declaration_runme.java
swig-3.0.10/Examples/test-suite/java/java_director_exception_feature_runme.java
swig-3.0.10/Examples/test-suite/java/java_pragmas_runme.java
swig-3.0.10/Examples/test-suite/java/curiously_recurring_template_pattern_runme.java
swig-3.0.10/Examples/test-suite/java/java_enums_runme.java
swig-3.0.10/Examples/test-suite/java/java_constants_runme.java
swig-3.0.10/Examples/test-suite/java/default_constructor_runme.java
swig-3.0.10/Examples/test-suite/java/using_pointers_runme.java
swig-3.0.10/Examples/test-suite/java/template_template_parameters_runme.java
swig-3.0.10/Examples/test-suite/java/li_std_vector_runme.java
swig-3.0.10/Examples/test-suite/java/rename4_runme.java
swig-3.0.10/Examples/test-suite/java/li_boost_shared_ptr_template_runme.java
swig-3.0.10/Examples/test-suite/java/enum_forward_runme.java
swig-3.0.10/Examples/test-suite/java/director_basic_runme.java
swig-3.0.10/Examples/test-suite/java/member_pointer_runme.java
swig-3.0.10/Examples/test-suite/java/naturalvar_onoff_runme.java
swig-3.0.10/Examples/test-suite/java/director_wombat_runme.java
swig-3.0.10/Examples/test-suite/java/cpp_typedef_runme.java
swig-3.0.10/Examples/test-suite/java/java_jnitypes_runme.java
swig-3.0.10/Examples/test-suite/java/operator_overload_runme.java
swig-3.0.10/Examples/test-suite/java/java_lib_arrays_runme.java
swig-3.0.10/Examples/test-suite/java/typemap_out_optimal_runme.java
swig-3.0.10/Examples/test-suite/java/unions_runme.java
swig-3.0.10/Examples/test-suite/java/enum_thorough_runme.java
swig-3.0.10/Examples/test-suite/java/friends_template_runme.java
swig-3.0.10/Examples/test-suite/java/rename2_runme.java
swig-3.0.10/Examples/test-suite/java/cpp11_strongly_typed_enumerations_simple_runme.java
swig-3.0.10/Examples/test-suite/java/ret_by_value_runme.java
swig-3.0.10/Examples/test-suite/java/typemap_arrays_runme.java
swig-3.0.10/Examples/test-suite/java/li_carrays_runme.java
swig-3.0.10/Examples/test-suite/java/template_default_class_parms_runme.java
swig-3.0.10/Examples/test-suite/java/director_abstract_runme.java
swig-3.0.10/Examples/test-suite/java/apply_strings_runme.java
swig-3.0.10/Examples/test-suite/java/template_nested_typemaps_runme.java
swig-3.0.10/Examples/test-suite/java/global_namespace_runme.java
swig-3.0.10/Examples/test-suite/java/extend_default_runme.java
swig-3.0.10/Examples/test-suite/java/char_strings_runme.java
swig-3.0.10/Examples/test-suite/java/java_lib_various_runme.java
swig-3.0.10/Examples/test-suite/java/profiletest_runme.java
swig-3.0.10/Examples/test-suite/java/nested_extend_c_runme.java
swig-3.0.10/Examples/test-suite/java/long_long_runme.java
swig-3.0.10/Examples/test-suite/java/template_partial_specialization_typedef_runme.java
swig-3.0.10/Examples/test-suite/java/using_directive_and_declaration_forward_runme.java
swig-3.0.10/Examples/test-suite/java/template_default_class_parms_typedef_runme.java
swig-3.0.10/Examples/test-suite/java/director_enum_runme.java
swig-3.0.10/Examples/test-suite/java/director_ref_runme.java
swig-3.0.10/Examples/test-suite/java/extend_constructor_destructor_runme.java
swig-3.0.10/Examples/test-suite/java/default_args_runme.java
swig-3.0.10/Examples/test-suite/java/char_binary_runme.java
swig-3.0.10/Examples/test-suite/java/virtual_poly_runme.java
swig-3.0.10/Examples/test-suite/java/sizet_runme.java
swig-3.0.10/Examples/test-suite/java/enum_thorough_proper_runme.java
swig-3.0.10/Examples/test-suite/java/overload_template_runme.java
swig-3.0.10/Examples/test-suite/java/li_boost_shared_ptr_bits_runme.java
swig-3.0.10/Examples/test-suite/java/multiple_inheritance_abstract_runme.java
swig-3.0.10/Examples/test-suite/java/wallkw_runme.java
swig-3.0.10/Examples/test-suite/java/memberin_extend_runme.java
swig-3.0.10/Examples/test-suite/java/arrays_global_twodim_runme.java
swig-3.0.10/Examples/test-suite/java/minherit2_runme.java
swig-3.0.10/Examples/test-suite/java/nested_template_base_runme.java
swig-3.0.10/Examples/test-suite/java/varargs_runme.java
swig-3.0.10/Examples/test-suite/java/friends_runme.java
swig-3.0.10/Examples/test-suite/java/java_typemaps_typewrapper_runme.java
swig-3.0.10/Examples/test-suite/java/li_boost_shared_ptr_runme.java
swig-3.0.10/Examples/test-suite/java/director_pass_by_value_runme.java
swig-3.0.10/Examples/test-suite/java/inherit_target_language_runme.java
swig-3.0.10/Examples/test-suite/java/template_methods_runme.java
swig-3.0.10/Examples/test-suite/java/special_variable_macros_runme.java
swig-3.0.10/Examples/test-suite/java/multiple_inheritance_shared_ptr_runme.java
swig-3.0.10/Examples/test-suite/java/li_cdata_cpp_runme.java
swig-3.0.10/Examples/test-suite/java/template_typedef_inherit_runme.java
swig-3.0.10/Examples/test-suite/java/constant_directive_runme.java
swig-3.0.10/Examples/test-suite/java/cpp11_constexpr_runme.java
swig-3.0.10/Examples/test-suite/java/primitive_ref_runme.java
swig-3.0.10/Examples/test-suite/java/rename_pcre_enum_runme.java
swig-3.0.10/Examples/test-suite/java/li_std_vector_enum_runme.java
swig-3.0.10/Examples/test-suite/java/nspace_extend_runme.java
swig-3.0.10/Examples/test-suite/java/nspace_runme.java
swig-3.0.10/Examples/test-suite/java/director_default_runme.java
swig-3.0.10/Examples/test-suite/java/rename_pcre_encoder_runme.java
swig-3.0.10/Examples/test-suite/java/README
swig-3.0.10/Examples/test-suite/java/kwargs_feature_runme.java
swig-3.0.10/Examples/test-suite/java/director_frob_runme.java
swig-3.0.10/Examples/test-suite/java/multiple_inheritance_nspace_runme.java
swig-3.0.10/Examples/test-suite/java/template_nested_runme.java
swig-3.0.10/Examples/test-suite/java/template_using_directive_and_declaration_forward_runme.java
swig-3.0.10/Examples/test-suite/java/overload_complicated_runme.java
swig-3.0.10/Examples/test-suite/java/cpp11_type_aliasing_runme.java
swig-3.0.10/Examples/test-suite/java/enum_thorough_simple_runme.java
swig-3.0.10/Examples/test-suite/java/java_pgcpp_runme.java
swig-3.0.10/Examples/test-suite/java/special_variables_runme.java
swig-3.0.10/Examples/test-suite/java/namespace_forward_declaration_runme.java
swig-3.0.10/Examples/test-suite/java/extend_typedef_class_runme.java
swig-3.0.10/Examples/test-suite/java/allprotected_runme.java
swig-3.0.10/Examples/test-suite/java/cpp11_thread_local_runme.java
swig-3.0.10/Examples/test-suite/java/li_carrays_cpp_runme.java
swig-3.0.10/Examples/test-suite/java/rname_runme.java
swig-3.0.10/Examples/test-suite/java/li_cdata_runme.java
swig-3.0.10/Examples/test-suite/java/director_ignore_runme.java
swig-3.0.10/Examples/test-suite/java/typemap_namespace_runme.java
swig-3.0.10/Examples/test-suite/java/cpp11_lambda_functions_runme.java
swig-3.0.10/Examples/test-suite/java/director_classic_runme.java
swig-3.0.10/Examples/test-suite/java/java_director_exception_feature_nspace_runme.java
swig-3.0.10/Examples/test-suite/java/preproc_line_file_runme.java
swig-3.0.10/Examples/test-suite/char_binary.i
swig-3.0.10/Examples/test-suite/li_std_pair_lang_object.i
swig-3.0.10/Examples/test-suite/template_default2.i
swig-3.0.10/Examples/test-suite/preproc_constants_c.i
swig-3.0.10/Examples/test-suite/insert_directive.i
swig-3.0.10/Examples/test-suite/template_default_arg.i
swig-3.0.10/Examples/test-suite/template_using_directive_and_declaration_forward.i
swig-3.0.10/Examples/test-suite/imports.list
swig-3.0.10/Examples/test-suite/exception_classname.i
swig-3.0.10/Examples/test-suite/struct_initialization.i
swig-3.0.10/Examples/test-suite/template_matrix.i
swig-3.0.10/Examples/test-suite/pointer_in_out.i
swig-3.0.10/Examples/test-suite/shared_ptr_wrapper.h
swig-3.0.10/Examples/test-suite/enum_thorough_typeunsafe.i
swig-3.0.10/Examples/test-suite/typemap_directorout.i
swig-3.0.10/Examples/test-suite/multiple_inheritance_abstract.i
swig-3.0.10/Examples/test-suite/apply_signed_char.i
swig-3.0.10/Examples/test-suite/python_abstractbase.i
swig-3.0.10/Examples/test-suite/schemerunme/
swig-3.0.10/Examples/test-suite/schemerunme/imports.scm
swig-3.0.10/Examples/test-suite/schemerunme/li_typemaps_proxy.scm
swig-3.0.10/Examples/test-suite/schemerunme/overload_copy.scm
swig-3.0.10/Examples/test-suite/schemerunme/unions_proxy.scm
swig-3.0.10/Examples/test-suite/schemerunme/char_constant.scm
swig-3.0.10/Examples/test-suite/schemerunme/cpp_enum.scm
swig-3.0.10/Examples/test-suite/schemerunme/overload_subtype.scm
swig-3.0.10/Examples/test-suite/schemerunme/integers.scm
swig-3.0.10/Examples/test-suite/schemerunme/multivalue.scm
swig-3.0.10/Examples/test-suite/schemerunme/import_nomodule.scm
swig-3.0.10/Examples/test-suite/schemerunme/overload_extend_c.scm
swig-3.0.10/Examples/test-suite/schemerunme/contract.scm
swig-3.0.10/Examples/test-suite/schemerunme/global_vars_proxy.scm
swig-3.0.10/Examples/test-suite/schemerunme/global_vars.scm
swig-3.0.10/Examples/test-suite/schemerunme/constover.scm
swig-3.0.10/Examples/test-suite/schemerunme/class_ignore.scm
swig-3.0.10/Examples/test-suite/schemerunme/name.scm
swig-3.0.10/Examples/test-suite/schemerunme/dynamic_cast.scm
swig-3.0.10/Examples/test-suite/schemerunme/overload_complicated.scm
swig-3.0.10/Examples/test-suite/schemerunme/li_std_string.scm
swig-3.0.10/Examples/test-suite/schemerunme/multiple_inheritance_proxy.scm
swig-3.0.10/Examples/test-suite/schemerunme/inherit_missing.scm
swig-3.0.10/Examples/test-suite/schemerunme/overload_simple.scm
swig-3.0.10/Examples/test-suite/schemerunme/list_vector.scm
swig-3.0.10/Examples/test-suite/schemerunme/overload_extend.scm
swig-3.0.10/Examples/test-suite/schemerunme/cpp_namespace.scm
swig-3.0.10/Examples/test-suite/schemerunme/unions.scm
swig-3.0.10/Examples/test-suite/schemerunme/typename.scm
swig-3.0.10/Examples/test-suite/schemerunme/pointer_in_out.scm
swig-3.0.10/Examples/test-suite/schemerunme/reference_global_vars.scm
swig-3.0.10/Examples/test-suite/schemerunme/li_typemaps.scm
swig-3.0.10/Examples/test-suite/schemerunme/typedef_inherit.scm
swig-3.0.10/Examples/test-suite/schemerunme/casts.scm
swig-3.0.10/Examples/test-suite/langobj.i
swig-3.0.10/Examples/test-suite/template_typemaps.i
swig-3.0.10/Examples/test-suite/member_pointer.i
swig-3.0.10/Examples/test-suite/python_nondynamic.i
swig-3.0.10/Examples/test-suite/packageoption.h
swig-3.0.10/Examples/test-suite/template_specialization_defarg.i
swig-3.0.10/Examples/test-suite/smart_pointer_ignore.i
swig-3.0.10/Examples/test-suite/array_typedef_memberin.i
swig-3.0.10/Examples/test-suite/preproc_include_h2.i
swig-3.0.10/Examples/test-suite/smart_pointer_template_defaults_overload.i
swig-3.0.10/Examples/test-suite/implicittest.i
swig-3.0.10/Examples/test-suite/li_cpointer_cpp.i
swig-3.0.10/Examples/test-suite/abstract_typedef.i
swig-3.0.10/Examples/test-suite/overload_complicated.i
swig-3.0.10/Examples/test-suite/funcptr_cpp.i
swig-3.0.10/Examples/test-suite/const_const_2.i
swig-3.0.10/Examples/test-suite/preproc_include_h3.i
swig-3.0.10/Examples/test-suite/template_basic.i
swig-3.0.10/Examples/test-suite/template_tbase_template.i
swig-3.0.10/Examples/test-suite/extend_typedef_class.i
swig-3.0.10/Examples/test-suite/constructor_value.i
swig-3.0.10/Examples/test-suite/features.i
swig-3.0.10/Examples/test-suite/ret_by_value.i
swig-3.0.10/Examples/test-suite/simple_array.i
swig-3.0.10/Examples/test-suite/constant_directive.i
swig-3.0.10/Examples/test-suite/sizeof_pointer.i
swig-3.0.10/Examples/test-suite/smart_pointer_template_const_overload.i
swig-3.0.10/Examples/test-suite/ignore_parameter.i
swig-3.0.10/Examples/test-suite/scilab_enums.i
swig-3.0.10/Examples/test-suite/scilab_pointer_conversion_functions.i
swig-3.0.10/Examples/test-suite/multiple_inheritance_interfaces.i
swig-3.0.10/Examples/test-suite/refcount.h
swig-3.0.10/Examples/test-suite/typemap_delete.i
swig-3.0.10/Examples/test-suite/friends.i
swig-3.0.10/Examples/test-suite/director_unroll.i
swig-3.0.10/Examples/test-suite/director_property.i
swig-3.0.10/Examples/test-suite/operator_pointer_ref.i
swig-3.0.10/Examples/test-suite/typemap_namespace.i
swig-3.0.10/Examples/test-suite/empty_c.i
swig-3.0.10/Examples/test-suite/director_stl.i
swig-3.0.10/Examples/test-suite/cpp11_hash_tables.i
swig-3.0.10/Examples/test-suite/li_cmalloc.i
swig-3.0.10/Examples/test-suite/inout.i
swig-3.0.10/Examples/test-suite/special_variable_macros.i
swig-3.0.10/Examples/test-suite/li_std_deque.i
swig-3.0.10/Examples/test-suite/overload_numeric.i
swig-3.0.10/Examples/test-suite/typemap_global_scope.i
swig-3.0.10/Examples/test-suite/template_typedef_rec.i
swig-3.0.10/Examples/test-suite/using_directive_and_declaration_forward.i
swig-3.0.10/Examples/test-suite/li_std_list.i
swig-3.0.10/Examples/test-suite/li_swigtype_inout.i
swig-3.0.10/Examples/test-suite/cpp11_default_delete.i
swig-3.0.10/Examples/test-suite/rename.h
swig-3.0.10/Examples/test-suite/java_throws.i
swig-3.0.10/Examples/test-suite/li_boost_intrusive_ptr.i
swig-3.0.10/Examples/test-suite/template_typedef_import.i
swig-3.0.10/Examples/test-suite/allowexcept.i
swig-3.0.10/Examples/test-suite/typemap_manyargs.i
swig-3.0.10/Examples/test-suite/java_nspacewithoutpackage.i
swig-3.0.10/Examples/test-suite/template_int_const.i
swig-3.0.10/Examples/test-suite/template_partial_arg.i
swig-3.0.10/Examples/test-suite/typemap_template.i
swig-3.0.10/Examples/test-suite/smart_pointer_const2.i
swig-3.0.10/Examples/test-suite/template_ns2.i
swig-3.0.10/Examples/test-suite/namespace_class.i
swig-3.0.10/Examples/test-suite/director_binary_string.i
swig-3.0.10/Examples/test-suite/function_typedef.i
swig-3.0.10/Examples/test-suite/unicode_strings.i
swig-3.0.10/Examples/test-suite/template_arg_replace.i
swig-3.0.10/Examples/test-suite/cpp11_inheriting_constructors.i
swig-3.0.10/Examples/java/
swig-3.0.10/Examples/java/index.html
swig-3.0.10/Examples/java/pointer/
swig-3.0.10/Examples/java/pointer/index.html
swig-3.0.10/Examples/java/pointer/example.i
swig-3.0.10/Examples/java/pointer/Makefile
swig-3.0.10/Examples/java/pointer/example.c
swig-3.0.10/Examples/java/pointer/runme.java
swig-3.0.10/Examples/java/class/
swig-3.0.10/Examples/java/class/index.html
swig-3.0.10/Examples/java/class/example.i
swig-3.0.10/Examples/java/class/example.cxx
swig-3.0.10/Examples/java/class/example.h
swig-3.0.10/Examples/java/class/Makefile
swig-3.0.10/Examples/java/class/runme.java
swig-3.0.10/Examples/java/class/example.dsp
swig-3.0.10/Examples/java/typemap/
swig-3.0.10/Examples/java/typemap/index.html
swig-3.0.10/Examples/java/typemap/example.i
swig-3.0.10/Examples/java/typemap/Makefile
swig-3.0.10/Examples/java/typemap/runme.java
swig-3.0.10/Examples/java/enum/
swig-3.0.10/Examples/java/enum/index.html
swig-3.0.10/Examples/java/enum/example.i
swig-3.0.10/Examples/java/enum/example.cxx
swig-3.0.10/Examples/java/enum/example.h
swig-3.0.10/Examples/java/enum/Makefile
swig-3.0.10/Examples/java/enum/runme.java
swig-3.0.10/Examples/java/template/
swig-3.0.10/Examples/java/template/index.html
swig-3.0.10/Examples/java/template/example.i
swig-3.0.10/Examples/java/template/example.h
swig-3.0.10/Examples/java/template/Makefile
swig-3.0.10/Examples/java/template/runme.java
swig-3.0.10/Examples/java/nested/
swig-3.0.10/Examples/java/nested/example.i
swig-3.0.10/Examples/java/nested/example.cxx
swig-3.0.10/Examples/java/nested/example.h
swig-3.0.10/Examples/java/nested/Makefile
swig-3.0.10/Examples/java/nested/runme.java
swig-3.0.10/Examples/java/nested/example.dsp
swig-3.0.10/Examples/java/funcptr/
swig-3.0.10/Examples/java/funcptr/index.html
swig-3.0.10/Examples/java/funcptr/example.i
swig-3.0.10/Examples/java/funcptr/example.h
swig-3.0.10/Examples/java/funcptr/Makefile
swig-3.0.10/Examples/java/funcptr/example.c
swig-3.0.10/Examples/java/funcptr/runme.java
swig-3.0.10/Examples/java/native/
swig-3.0.10/Examples/java/native/index.html
swig-3.0.10/Examples/java/native/example.i
swig-3.0.10/Examples/java/native/Makefile
swig-3.0.10/Examples/java/native/runme.java
swig-3.0.10/Examples/java/simple/
swig-3.0.10/Examples/java/simple/index.html
swig-3.0.10/Examples/java/simple/example.i
swig-3.0.10/Examples/java/simple/Makefile
swig-3.0.10/Examples/java/simple/example.c
swig-3.0.10/Examples/java/simple/runme.java
swig-3.0.10/Examples/java/simple/example.dsp
swig-3.0.10/Examples/java/reference/
swig-3.0.10/Examples/java/reference/index.html
swig-3.0.10/Examples/java/reference/example.i
swig-3.0.10/Examples/java/reference/example.cxx
swig-3.0.10/Examples/java/reference/example.h
swig-3.0.10/Examples/java/reference/Makefile
swig-3.0.10/Examples/java/reference/runme.java
swig-3.0.10/Examples/java/check.list
swig-3.0.10/Examples/java/callback/
swig-3.0.10/Examples/java/callback/index.html
swig-3.0.10/Examples/java/callback/example.i
swig-3.0.10/Examples/java/callback/example.cxx
swig-3.0.10/Examples/java/callback/example.h
swig-3.0.10/Examples/java/callback/Makefile
swig-3.0.10/Examples/java/callback/runme.java
swig-3.0.10/Examples/java/extend/
swig-3.0.10/Examples/java/extend/index.html
swig-3.0.10/Examples/java/extend/example.i
swig-3.0.10/Examples/java/extend/example.cxx
swig-3.0.10/Examples/java/extend/example.h
swig-3.0.10/Examples/java/extend/Makefile
swig-3.0.10/Examples/java/extend/runme.java
swig-3.0.10/Examples/java/variables/
swig-3.0.10/Examples/java/variables/index.html
swig-3.0.10/Examples/java/variables/example.i
swig-3.0.10/Examples/java/variables/example.h
swig-3.0.10/Examples/java/variables/Makefile
swig-3.0.10/Examples/java/variables/example.c
swig-3.0.10/Examples/java/variables/runme.java
swig-3.0.10/Examples/java/multimap/
swig-3.0.10/Examples/java/multimap/example.i
swig-3.0.10/Examples/java/multimap/Makefile
swig-3.0.10/Examples/java/multimap/example.c
swig-3.0.10/Examples/java/multimap/runme.java
swig-3.0.10/Examples/java/multimap/example.dsp
swig-3.0.10/Examples/java/constants/
swig-3.0.10/Examples/java/constants/index.html
swig-3.0.10/Examples/java/constants/example.i
swig-3.0.10/Examples/java/constants/Makefile
swig-3.0.10/Examples/java/constants/runme.java
swig-3.0.10/swig.spec.in
swig-3.0.10/appveyor.yml
swig-3.0.10/README
正在读取软件包列表... 完成
正在分析软件包的依赖关系树       
正在读取状态信息... 完成       
libpcre3-dev 已经是最新版 (2:8.39-3)。
libpcre3 已经是最新版 (2:8.39-3)。
有一些软件包无法被安装。如果您用的是 unstable 发行版，这也许是
因为系统无法达到您要求的状态造成的。该版本中可能会有一些您需要的软件
包尚未被创建或是它们已被从新到(Incoming)目录移出。
下列信息可能会对解决问题有所帮助：

下列软件包有未满足的依赖关系：
 libatlas-base-dev : 依赖: libatlas-dev 但是它将不会被安装
E: 无法修正错误，因为您要求某些软件包保持现状，就是它们破坏了软件包间的依赖关系。
checking build system type... armv7l-unknown-linux-gnueabihf
checking host system type... armv7l-unknown-linux-gnueabihf
checking for a BSD-compatible install... /usr/bin/install -c
checking whether build environment is sane... yes
checking for a thread-safe mkdir -p... /bin/mkdir -p
checking for gawk... no
checking for mawk... mawk
checking whether make sets $(MAKE)... yes
checking whether make supports nested variables... yes
checking for gcc... gcc
checking whether the C compiler works... yes
checking for C compiler default output file name... a.out
checking for suffix of executables... 
checking whether we are cross compiling... no
checking for suffix of object files... o
checking whether we are using the GNU C compiler... yes
checking whether gcc accepts -g... yes
checking for gcc option to accept ISO C89... none needed
checking whether gcc understands -c and -o together... yes
checking for style of include used by make... GNU
checking dependency style of gcc... gcc3
checking for g++... g++
checking whether we are using the GNU C++ compiler... yes
checking whether g++ accepts -g... yes
checking dependency style of g++... gcc3
checking maximum warning verbosity option... no
checking how to run the C preprocessor... gcc -E
checking for grep that handles long lines and -e... /bin/grep
checking for egrep... /bin/grep -E
checking for ANSI C header files... yes
checking for popen... yes
checking whether to enable PCRE support... yes
checking whether to use local PCRE... no
checking for a sed that does not truncate output... /bin/sed
checking for pcre-config... /usr/bin/pcre-config
checking whether to enable ccache-swig... yes

Checking packages required for SWIG developers.
Note : None of the following packages are required for users to compile and install SWIG from the distributed tarball

checking for bison... no
checking for byacc... no

Checking for installed target languages and other information in order to compile and run
the examples and test-suite invoked by 'make check'.
Note : None of the following packages are required for users to compile and install SWIG from the distributed tarball

checking for boostlib >= 1.20.0... configure: We could not detect the boost libraries (version 1.20 or higher). If you have a staged boost library (still not installed) please specify $BOOST_ROOT in your environment and do not give a PATH to --with-boost option.  If you are sure you have boost installed, then check your version number looking in <boost/version.hpp>. See http://randspringer.de/boost for more documentation.
configure: ISYSTEM: -isystem 
checking SO... .so
checking LDSHARED... gcc -shared
checking CXXSHARED... gcc -shared
checking TRYLINKINGWITHCXX... CXXSHARED= g++ -shared 
checking CCSHARED... -fpic
checking RPATH... -Xlinker -rpath $(exec_prefix)/lib -Xlinker -rpath .
checking LINKFORSHARED... -Xlinker -export-dynamic
checking PLATCFLAGS... 
checking whether to enable C++11 testing... no
checking for dlopen in -ldl... yes
checking for shl_load in -ldld... no
checking for library containing t_open... no
checking for library containing gethostbyname... none required
checking for library containing socket... none required
checking for swill_init in -lswill... no
checking for main in -lieee... yes
checking for crypt in -lcrypt... yes
checking for pkg-config... pkg-config
checking for Tcl configuration... no
checking for Tcl header files... not found
checking for Tcl library... not found
checking for python... python
checking for python major version number... 2
checking for Python os.name... posix
checking for Python prefix... /usr
checking for Python exec-prefix... /usr
checking for Python version... python2.7
checking for Python lib dir... lib
checking for Python header files... -I/usr/include/python2.7 -I/usr/lib/python2.7/config
checking for Python library directory... Not found
checking for Python library... -lpython2.7
checking for python3... python3
checking for python3-config... python3-config
checking for python3 major version number... 3
checking for Python 3.x os.name... posix
checking for Python 3.x prefix... /usr
checking for Python 3.x exec-prefix... /usr
checking for Python 3.x version... python3.5
checking for Python 3.x lib dir... lib
checking for Python 3.x header files... -I/usr/include/python3.5m -I/usr/include/python3.5m
checking for Python 3.x library directory... Not found
checking for Python 3.x library... -lpython3.5
checking for pep8... no
checking for perl... perl
checking for Perl5 header files... /usr/lib/arm-linux-gnueabihf/perl/5.24/CORE
checking for Perl5 library... perl
checking for Perl5 ccflags... -D_REENTRANT -D_GNU_SOURCE -DDEBIAN -fwrapv -fno-strict-aliasing -pipe -isystem /usr/local/include -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
checking for Perl5 ccdlflags... -Wl,-E
checking for Perl5 cccdlflags... -fPIC
checking for Perl5 ldflags...  -fstack-protector-strong -L/usr/local/lib
checking for Perl5 Test::More module... found
checking for octave... no
checking for scilab... no
checking for java JDK... no (JAVA_HOME is not defined)
checking for java... java
checking for javac... javac
checking for java include file jni.h... not found
checking for nodejs... nodejs
checking for node-gyp... no
checking for JavaScriptCore/JavaScript.h... not found
checking for JavaScriptCore/Webkit library... not found
checking for V8 Javascript v8.h... not found
checking for V8 Javascript library... not found
checking for gcj... no
checking for gcjh... no
checking for android... no
checking for adb... no
checking for ant... ant
checking for ndk-build... no
checking for guile-config... no
checking for mzscheme... no
checking for mzc... no
checking for ruby... no
checking for Ruby header files... could not figure out how to run ruby
checking for php5... no
checking for php... no
checking for PHP header files... could not find -config or obtain PHP version from it
checking for Ocaml DL load generator... checking for ocamldlgen... no
checking for Ocaml package tool... checking for ocamlfind... no
checking for Ocaml compiler... checking for ocamlc... no
checking for Ocaml toplevel creator... checking for ocamlmktop... no
checking for Ocaml Pre-Processor-Pretty-Printer... checking for camlp4... no
checking for pike... no
checking for pike7.8... no
checking for pike7.6... no
checking for pike7.4... no
checking for pike7.2... no
checking for chicken... no
checking for csc... no
checking for csi... no
checking for mono-csc... no
checking for gmcs... no
checking for mcs... no
checking for cscc... no
checking for lua5.4... no
checking for lua5.3... no
checking for lua5.2... no
checking for lua5.1... /usr/bin/lua5.1
checking Lua version... Lua 5.1 or later
checking whether Lua dynamic loading is enabled... yes
checking lua.h usability... no
checking lua.h presence... no
checking for lua.h... no
checking for lua.h in other locations... not found
checking for library containing lua_close... no
checking for alisp... no
configure: Disabling CLISP
checking for R... no
checking for go... no
checking for gccgo... no
checking for dmd... no
checking for ldmd... no
checking for gdmd... no
checking for dmd... no
checking for gdmd... no
checking that generated files are newer than configure... done
configure: creating ./config.status
config.status: creating Makefile
config.status: creating swig.spec
config.status: creating Examples/Makefile
config.status: creating Examples/d/example.mk
config.status: creating Examples/xml/Makefile
config.status: creating Examples/test-suite/errors/Makefile
config.status: creating Examples/test-suite/chicken/Makefile
config.status: creating Examples/test-suite/csharp/Makefile
config.status: creating Examples/test-suite/d/Makefile
config.status: creating Examples/test-suite/guile/Makefile
config.status: creating Examples/test-suite/java/Makefile
config.status: creating Examples/test-suite/javascript/Makefile
config.status: creating Examples/test-suite/mzscheme/Makefile
config.status: creating Examples/test-suite/ocaml/Makefile
config.status: creating Examples/test-suite/octave/Makefile
config.status: creating Examples/test-suite/perl5/Makefile
config.status: creating Examples/test-suite/php/Makefile
config.status: creating Examples/test-suite/pike/Makefile
config.status: creating Examples/test-suite/python/Makefile
config.status: creating Examples/test-suite/ruby/Makefile
config.status: creating Examples/test-suite/scilab/Makefile
config.status: creating Examples/test-suite/tcl/Makefile
config.status: creating Examples/test-suite/lua/Makefile
config.status: creating Examples/test-suite/allegrocl/Makefile
config.status: creating Examples/test-suite/clisp/Makefile
config.status: creating Examples/test-suite/cffi/Makefile
config.status: creating Examples/test-suite/uffi/Makefile
config.status: creating Examples/test-suite/r/Makefile
config.status: creating Examples/test-suite/go/Makefile
config.status: creating Source/Makefile
config.status: creating Tools/javascript/Makefile
config.status: creating preinst-swig
config.status: creating CCache/ccache_swig_config.h
config.status: creating Source/Include/swigconfig.h
config.status: executing depfiles commands
config.status: executing Examples commands
=== configuring in CCache (/home/pi/install_temp/swig-3.0.10/CCache)
configure: running /bin/bash ./configure --disable-option-checking '--prefix=/usr'  '--without-clisp' '--without-maximum-compile-warnings' --cache-file=/dev/null --srcdir=.
configure: Configuring ccache
checking for gcc... gcc
checking whether the C compiler works... yes
checking for C compiler default output file name... a.out
checking for suffix of executables... 
checking whether we are cross compiling... no
checking for suffix of object files... o
checking whether we are using the GNU C compiler... yes
checking whether gcc accepts -g... yes
checking for gcc option to accept ISO C89... none needed
checking how to run the C preprocessor... gcc -E
checking for a BSD-compatible install... /usr/bin/install -c
checking for dirent.h that defines DIR... yes
checking for library containing opendir... none required
checking whether time.h and sys/time.h may both be included... yes
checking for sys/wait.h that is POSIX.1 compatible... yes
checking for grep that handles long lines and -e... /bin/grep
checking for egrep... /bin/grep -E
checking for ANSI C header files... yes
checking for sys/types.h... yes
checking for sys/stat.h... yes
checking for stdlib.h... yes
checking for string.h... yes
checking for memory.h... yes
checking for strings.h... yes
checking for inttypes.h... yes
checking for stdint.h... yes
checking for unistd.h... yes
checking ctype.h usability... yes
checking ctype.h presence... yes
checking for ctype.h... yes
checking for strings.h... (cached) yes
checking for stdlib.h... (cached) yes
checking for string.h... (cached) yes
checking pwd.h usability... yes
checking pwd.h presence... yes
checking for pwd.h... yes
checking sys/time.h usability... yes
checking sys/time.h presence... yes
checking for sys/time.h... yes
checking for realpath... yes
checking for snprintf... yes
checking for vsnprintf... yes
checking for vasprintf... yes
checking for asprintf... yes
checking for mkstemp... yes
checking for gethostname... yes
checking for getpwuid... yes
checking for utimes... yes
checking for compar_fn_t in stdlib.h... yes
checking for C99 vsnprintf... yes
checking zlib.h usability... yes
checking zlib.h presence... yes
checking for zlib.h... yes
checking for gzdopen in -lz... yes
configure: creating ./config.status
config.status: creating Makefile
config.status: creating config.h

The SWIG test-suite and examples are configured for the following languages:
perl5 python 

make[1]: Entering directory '/home/pi/install_temp/swig-3.0.10/Source'
make  all-am
make[2]: Entering directory '/home/pi/install_temp/swig-3.0.10/Source'
depbase=`echo CParse/cscanner.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT CParse/cscanner.o -MD -MP -MF $depbase.Tpo -c -o CParse/cscanner.o CParse/cscanner.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo CParse/parser.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT CParse/parser.o -MD -MP -MF $depbase.Tpo -c -o CParse/parser.o CParse/parser.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo CParse/templ.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT CParse/templ.o -MD -MP -MF $depbase.Tpo -c -o CParse/templ.o CParse/templ.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo CParse/util.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT CParse/util.o -MD -MP -MF $depbase.Tpo -c -o CParse/util.o CParse/util.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo DOH/base.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT DOH/base.o -MD -MP -MF $depbase.Tpo -c -o DOH/base.o DOH/base.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo DOH/file.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT DOH/file.o -MD -MP -MF $depbase.Tpo -c -o DOH/file.o DOH/file.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo DOH/fio.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT DOH/fio.o -MD -MP -MF $depbase.Tpo -c -o DOH/fio.o DOH/fio.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo DOH/hash.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT DOH/hash.o -MD -MP -MF $depbase.Tpo -c -o DOH/hash.o DOH/hash.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo DOH/list.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT DOH/list.o -MD -MP -MF $depbase.Tpo -c -o DOH/list.o DOH/list.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo DOH/memory.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT DOH/memory.o -MD -MP -MF $depbase.Tpo -c -o DOH/memory.o DOH/memory.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo DOH/string.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT DOH/string.o -MD -MP -MF $depbase.Tpo -c -o DOH/string.o DOH/string.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo DOH/void.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
gcc -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT DOH/void.o -MD -MP -MF $depbase.Tpo -c -o DOH/void.o DOH/void.c &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/allegrocl.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/allegrocl.o -MD -MP -MF $depbase.Tpo -c -o Modules/allegrocl.o Modules/allegrocl.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/allocate.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/allocate.o -MD -MP -MF $depbase.Tpo -c -o Modules/allocate.o Modules/allocate.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/browser.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/browser.o -MD -MP -MF $depbase.Tpo -c -o Modules/browser.o Modules/browser.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/cffi.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/cffi.o -MD -MP -MF $depbase.Tpo -c -o Modules/cffi.o Modules/cffi.cxx &&\
mv -f $depbase.Tpo $depbase.Po
depbase=`echo Modules/chicken.o | sed 's|[^/]*$|.deps/&|;s|\.o$||'`;\
g++ -DHAVE_CONFIG_H   -I../Source/Include -I../Source/CParse -I../Source/Include -I../Source/DOH -I../Source/CParse -I../Source/Preprocessor -I../Source/Swig -I../Source/Modules   -g -O2 -MT Modules/chicken.o -MD -MP -MF $depbase.Tpo -c -o Modules/chicken.o Modules/chicken.cxx &&\
mv -f $depbase.Tpo $depbase.Po

```