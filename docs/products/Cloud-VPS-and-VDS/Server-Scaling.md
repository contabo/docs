
# Upgrade your VPS / VDS
+ Use your [Customer Dashboard](https://my.contabo.com/vps) to initiate an **upgrade** any-time. With the upgrade, your server will have more performance in no time! We recommend using our 'Live Migration'!
+ VDS upgrade is also possible! To upgrade your _VDS_, please contact our customer support team via email at support@contabo.com.


# Downgrade of a VPS / VDS


Sometimes the VPS or a VDS you subscribe to gives you too much performance. The situation can happen when your use case shifts in a different direction, or you may have decided to reduce performance for cost optimization.


![VPS Upgrade](https://user-images.githubusercontent.com/97171326/165225853-8b23b0aa-44e7-4ffc-8471-0d8777f577a3.png)

A **downgrade** can be a great solution! However, a downgrade (which we understand as any _change_ → to a server model with a lower storage capacity) can currently only be done by ordering a new smaller plan of the required smaller size on our website:

> -> To order a smaller VPS plan [CLICK HERE](https://contabo.com/?show=vps)

After you place the order, our team will continue with the standard provisioning process of this new smaller plan. Once that is finished you can move files from your VPS to the new one and cancel your old VPS. Cancellation can be done in the standard way, at the earliest possible time through your [customer control panel](https://my.contabo.com/vps#). This action generally completes the migration process. If you are looking for a backup solution to store your data, you can try our [Simple Backup with rclone](https://docs.contabo.com/docs/products/Object-Storage/HowTo/simple-backup).

The new downgraded VPS will have a completely new IP address, unfortunately the old one will be replaced.

### Example of the Possibilities:
+ VPS S SSD (400GB) → VPS S NVMe (100GB) ❌ ( We consider this request a downgrade because we would like to move from a 400 GB VPS to a 100 GB VPS.  )
+ VPS S NVMe → VPS M SSD ✅
+ VPS S NVMe → VPS XL NVMe ✅
