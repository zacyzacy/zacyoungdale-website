---
title: "3rd Person Movement"
date: 2021-05-29T18:42:17-04:00
draft: false
---

Learned some fun radian maths for perfect camera relative 3rd person movement in Unity.

```
float targetAngle = Mathf.Atan2(direction.x, direction.z) * Mathf.Rad2Deg + cam.eulerAngles.y;
float angle = Mathf.SmoothDampAngle(transform.eulerAngles.y, targetAngle, ref turnVelocity, turnSmoothTime);
transform.rotation = Quaternion.Euler(0f, angle, 0f);
Vector3 moveDir = Quaternion.Euler(0f, targetAngle, 0f) * Vector3.forward;
controller.Move(moveDir.normalized * speed * Time.deltaTime);
```
