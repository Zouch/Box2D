cmake_minimum_required(VERSION 3.4 FATAL_ERROR)
project(Box2D)

option(BUILD_SHARED_LIBS "" ON)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_WINDOWS_EXPORT_ALL_SYMBOLS ON)

add_library(box2d
    Box2D/Box2D/Dynamics/Contacts/b2EdgeAndCircleContact.cpp
    Box2D/Box2D/Dynamics/Contacts/b2PolygonAndCircleContact.cpp
    Box2D/Box2D/Dynamics/Contacts/b2CircleContact.cpp
    Box2D/Box2D/Dynamics/Contacts/b2ContactSolver.cpp
    Box2D/Box2D/Dynamics/Contacts/b2PolygonContact.cpp
    Box2D/Box2D/Dynamics/Contacts/b2ChainAndPolygonContact.cpp
    Box2D/Box2D/Dynamics/Contacts/b2ChainAndCircleContact.cpp
    Box2D/Box2D/Dynamics/Contacts/b2EdgeAndPolygonContact.cpp
    Box2D/Box2D/Dynamics/Contacts/b2Contact.cpp
    Box2D/Box2D/Dynamics/b2Island.cpp
    Box2D/Box2D/Dynamics/b2World.cpp
    Box2D/Box2D/Dynamics/Joints/b2GearJoint.cpp
    Box2D/Box2D/Dynamics/Joints/b2Joint.cpp
    Box2D/Box2D/Dynamics/Joints/b2PrismaticJoint.cpp
    Box2D/Box2D/Dynamics/Joints/b2MotorJoint.cpp
    Box2D/Box2D/Dynamics/Joints/b2PulleyJoint.cpp
    Box2D/Box2D/Dynamics/Joints/b2DistanceJoint.cpp
    Box2D/Box2D/Dynamics/Joints/b2WeldJoint.cpp
    Box2D/Box2D/Dynamics/Joints/b2RevoluteJoint.cpp
    Box2D/Box2D/Dynamics/Joints/b2RopeJoint.cpp
    Box2D/Box2D/Dynamics/Joints/b2FrictionJoint.cpp
    Box2D/Box2D/Dynamics/Joints/b2MouseJoint.cpp
    Box2D/Box2D/Dynamics/Joints/b2WheelJoint.cpp
    Box2D/Box2D/Dynamics/b2ContactManager.cpp
    Box2D/Box2D/Dynamics/b2Body.cpp
    Box2D/Box2D/Dynamics/b2WorldCallbacks.cpp
    Box2D/Box2D/Dynamics/b2Fixture.cpp
    Box2D/Box2D/Collision/b2CollideEdge.cpp
    Box2D/Box2D/Collision/b2Collision.cpp
    Box2D/Box2D/Collision/b2CollidePolygon.cpp
    Box2D/Box2D/Collision/b2Distance.cpp
    Box2D/Box2D/Collision/b2BroadPhase.cpp
    Box2D/Box2D/Collision/b2CollideCircle.cpp
    Box2D/Box2D/Collision/b2TimeOfImpact.cpp
    Box2D/Box2D/Collision/Shapes/b2CircleShape.cpp
    Box2D/Box2D/Collision/Shapes/b2ChainShape.cpp
    Box2D/Box2D/Collision/Shapes/b2EdgeShape.cpp
    Box2D/Box2D/Collision/Shapes/b2PolygonShape.cpp
    Box2D/Box2D/Collision/b2DynamicTree.cpp
    Box2D/Box2D/Common/b2Draw.cpp
    Box2D/Box2D/Common/b2StackAllocator.cpp
    Box2D/Box2D/Common/b2Settings.cpp
    Box2D/Box2D/Common/b2Math.cpp
    Box2D/Box2D/Common/b2Timer.cpp
    Box2D/Box2D/Common/b2BlockAllocator.cpp
    Box2D/Box2D/Rope/b2Rope.cpp
)

target_include_directories(box2d PUBLIC "$<BUILD_INTERFACE:${BOX2D_SOURCE_DIR}/Box2D>")
target_include_directories(box2d PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/Box2D)
