set(ImGuizmoFiles
    ${CMAKE_CURRENT_LIST_DIR}/GraphEditor.h
    ${CMAKE_CURRENT_LIST_DIR}/ImCurveEdit.h
    ${CMAKE_CURRENT_LIST_DIR}/ImGradient.h
    ${CMAKE_CURRENT_LIST_DIR}/ImGuizmo.h
    ${CMAKE_CURRENT_LIST_DIR}/ImSequencer.h
    ${CMAKE_CURRENT_LIST_DIR}/ImZoomSlider.h
    ${CMAKE_CURRENT_LIST_DIR}/GraphEditor.cpp
    ${CMAKE_CURRENT_LIST_DIR}/ImCurveEdit.cpp
    ${CMAKE_CURRENT_LIST_DIR}/ImGradient.cpp
    ${CMAKE_CURRENT_LIST_DIR}/ImGuizmo.cpp
    ${CMAKE_CURRENT_LIST_DIR}/ImSequencer.cpp)

add_library(ImGuizmo STATIC ${ImGuizmoFiles})

target_include_directories(ImGuizmo PUBLIC ${CMAKE_CURRENT_LIST_DIR})

# User must link imgui static library, see https://github.com/YUZHIGUIYI/imgui.git, the docking branch
target_link_libraries(ImGuizmo PUBLIC ImGuiDocking)