---
swagger: "2.0"
x-collection-name: AWS Auto Scaling
x-complete: 0
info:
  title: AWS Auto Scaling API Create Auto Scaling Group
  version: 1.0.0
  description: Creates an Auto Scaling group with the specified name and attributes.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=AttachInstances:
    get:
      summary: Attach Instances
      description: Attaches one or more EC2 instances to the specified Auto Scaling
        group.
      operationId: attachInstances
      x-api-path-slug: actionattachinstances-get
      parameters:
      - in: query
        name: AutoScalingGroupName
        description: The name of the group
        type: string
      - in: query
        name: InstanceIds.member.N
        description: One or more instance IDs
        type: string
      responses:
        200:
          description: OK
      tags:
      - Server Instance
  /?Action=AttachLoadBalancers:
    get:
      summary: Attach Load Balancers
      description: Attaches one or more Classic load balancers to the specified Auto
        Scaling group.
      operationId: attachLoadBalancers
      x-api-path-slug: actionattachloadbalancers-get
      parameters:
      - in: query
        name: AutoScalingGroupName
        description: The name of the group
        type: string
      - in: query
        name: LoadBalancerNames.member.N
        description: One or more load balancer names
        type: string
      responses:
        200:
          description: OK
      tags:
      - Load Balancers
  /?Action=AttachLoadBalancerTargetGroups:
    get:
      summary: Attach Load Balancer Target Groups
      description: Attaches one or more target groups to the specified Auto Scaling
        group.
      operationId: attachLoadBalancerTargetGroups
      x-api-path-slug: actionattachloadbalancertargetgroups-get
      parameters:
      - in: query
        name: AutoScalingGroupName
        description: The name of the Auto Scaling group
        type: string
      - in: query
        name: TargetGroupARNs.member.N
        description: The Amazon Resource Names (ARN) of the target groups
        type: string
      responses:
        200:
          description: OK
      tags:
      - Load Balancers
  /?Action=CompleteLifecycleAction:
    get:
      summary: Complete Lifecycle Action
      description: Completes the lifecycle action for the specified token or instance
        with the specified result.
      operationId: completeLifecycleAction
      x-api-path-slug: actioncompletelifecycleaction-get
      parameters:
      - in: query
        name: AutoScalingGroupName
        description: The name of the group for the lifecycle hook
        type: string
      - in: query
        name: InstanceId
        description: The ID of the instance
        type: string
      - in: query
        name: LifecycleActionResult
        description: The action for the group to take
        type: string
      - in: query
        name: LifecycleActionToken
        description: A universally unique identifier (UUID) that identifies a specific
          lifecycle action associated with an instance
        type: string
      - in: query
        name: LifecycleHookName
        description: The name of the lifecycle hook
        type: string
      responses:
        200:
          description: OK
      tags:
      - Life Cycle
  /?Action=CreateAutoScalingGroup:
    get:
      summary: Create Auto Scaling Group
      description: Creates an Auto Scaling group with the specified name and attributes.
      operationId: createAutoScalingGroup
      x-api-path-slug: actioncreateautoscalinggroup-get
      parameters:
      - in: query
        name: AutoScalingGroupName
        description: The name of the group
        type: string
      - in: query
        name: AvailabilityZones.member.N
        description: One or more Availability Zones for the group
        type: string
      - in: query
        name: DefaultCooldown
        description: The amount of time, in seconds, after a scaling activity completes
          before another scaling activity can start
        type: string
      - in: query
        name: DesiredCapacity
        description: The number of EC2 instances that should be running in the group
        type: string
      - in: query
        name: HealthCheckGracePeriod
        description: The amount of time, in seconds, that Auto Scaling waits before
          checking the health status of an EC2 instance that has come into service
        type: string
      - in: query
        name: HealthCheckType
        description: The service to use for the health checks
        type: string
      - in: query
        name: InstanceId
        description: The ID of the instance used to create a launch configuration
          for the group
        type: string
      - in: query
        name: LaunchConfigurationName
        description: The name of the launch configuration
        type: string
      - in: query
        name: LoadBalancerNames.member.N
        description: One or more Classic load balancers
        type: string
      - in: query
        name: MaxSize
        description: The maximum size of the group
        type: string
      - in: query
        name: MinSize
        description: The minimum size of the group
        type: string
      - in: query
        name: NewInstancesProtectedFromScaleIn
        description: Indicates whether newly launched instances are protected from
          termination by Auto Scaling when scaling in
        type: string
      - in: query
        name: PlacementGroup
        description: The name of the placement group into which youll launch your
          instances, if any
        type: string
      - in: query
        name: Tags.member.N
        description: One or more tags
        type: string
      - in: query
        name: TargetGroupARNs.member.N
        description: The Amazon Resource Names (ARN) of the target groups
        type: string
      - in: query
        name: TerminationPolicies.member.N
        description: One or more termination policies used to select the instance
          to terminate
        type: string
      - in: query
        name: VPCZoneIdentifier
        description: A comma-separated list of subnet identifiers for your virtual
          private cloud (VPC)
        type: string
      responses:
        200:
          description: OK
      tags:
      - Auto Scaling Groups
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---