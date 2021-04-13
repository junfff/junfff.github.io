---
title: Unity3d::Rotation
date: 2021-04-13 14:21:22 +/-TTTT
categories: [Unity3d]
tags: [Rust]
---

# Flavors:
{
        private const float rotateSpeed = 16f;//旋转速度

        private void RotateRotation(Transform transform, float angle)
        {
            Quaternion result = Quaternion.Euler(0, 90 - angle, 0);
            transform.rotation = Quaternion.RotateTowards(transform.rotation, result, rotateSpeed * Time.deltaTime * 100);
        }

        private void RotateCharacter(Transform transform, Vector3 _direction)
        {
            _direction.y = 0;
            Vector3 targetForward = Vector3.RotateTowards(transform.forward, _direction.normalized, rotateSpeed * Time.deltaTime, .1f);
            Quaternion _newRotation = Quaternion.LookRotation(targetForward);
            transform.rotation = _newRotation;
        }
}
