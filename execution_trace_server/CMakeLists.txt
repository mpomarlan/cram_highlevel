cmake_minimum_required(VERSION 2.8.3)
project(execution_trace_server)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  cram_reasoning
  cram_plan_knowledge
  cram_execution_trace
  cram_plan_library
  cram_roslisp_common
  cram_utilities
  cram_json_prolog
)

add_service_files(
  FILES
  ListExecutionTraces.srv
  SelectExecutionTrace.srv
)

generate_messages()

catkin_package(
  CATKIN_DEPENDS
  message_runtime
  cram_reasoning
  cram_execution_trace
  cram_plan_library
  cram_roslisp_common
  cram_utilities
  cram_json_prolog
)