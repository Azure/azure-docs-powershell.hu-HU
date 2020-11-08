---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
ms.openlocfilehash: e13cd1ba814bc5bea66a6a3d06506b9822dd38bd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014341"
---
# <span data-ttu-id="a9059-101">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a9059-101">Add-AzIotHubDevice</span></span>

## <span data-ttu-id="a9059-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a9059-102">SYNOPSIS</span></span>
<span data-ttu-id="a9059-103">Hozzon létre egy eszközt egy IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="a9059-103">Create a device in an IoT Hub.</span></span>

## <span data-ttu-id="a9059-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a9059-104">SYNTAX</span></span>

### <span data-ttu-id="a9059-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a9059-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled]
 [-Children <String[]>] [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9059-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a9059-106">InputObjectSet</span></span>
```
Add-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9059-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a9059-107">ResourceIdSet</span></span>
```
Add-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9059-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a9059-108">DESCRIPTION</span></span>
<span data-ttu-id="a9059-109">Hozzon létre egy másik engedélyezési típust tartalmazó eszközt egy IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="a9059-109">Create a device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="a9059-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a9059-110">EXAMPLES</span></span>

### <span data-ttu-id="a9059-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a9059-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled
```

<span data-ttu-id="a9059-112">Hozzon létre egy él engedélyezve IoT-eszközt alapértelmezett engedéllyel (megosztott titkos kulccsal).</span><span class="sxs-lookup"><span data-stu-id="a9059-112">Create an edge enabled IoT device with default authorization (shared private key).</span></span>

### <span data-ttu-id="a9059-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="a9059-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -AuthMethod "x509_ca" -Status Disabled -StatusReason "Some Reason"
```

<span data-ttu-id="a9059-114">IoT-eszköz létrehozása a legfelső szintű HITELESÍTÉSSZOLGÁLTATÓ engedélyezésével, letiltott állapottal és okkal</span><span class="sxs-lookup"><span data-stu-id="a9059-114">Create an IoT device with root CA authorization with disabled status and reason.</span></span>

### <span data-ttu-id="a9059-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="a9059-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled -Children device1,device2
```

<span data-ttu-id="a9059-116">Hozzon létre egy él engedélyezve IoT eszközt, és adjon hozzá alárendelt eszközöket.</span><span class="sxs-lookup"><span data-stu-id="a9059-116">Create an edge enabled IoT device and add child devices to it.</span></span>

### <span data-ttu-id="a9059-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="a9059-117">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -ParentDeviceId parentDevice1
```

<span data-ttu-id="a9059-118">Hozzon létre egy IoT-eszközt, és állítsa be a fölérendelt eszközt.</span><span class="sxs-lookup"><span data-stu-id="a9059-118">Create an IoT device and set its parent device.</span></span>

## <span data-ttu-id="a9059-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a9059-119">PARAMETERS</span></span>

### <span data-ttu-id="a9059-120">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="a9059-120">-AuthMethod</span></span>
<span data-ttu-id="a9059-121">Az engedély típusa: egy entitást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a9059-121">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: (All)
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9059-122">-Children (gyermekek)</span><span class="sxs-lookup"><span data-stu-id="a9059-122">-Children</span></span>
<span data-ttu-id="a9059-123">Az Add Child (vesszővel elválasztott) eszközök listájában csak nem él eszközök találhatók.</span><span class="sxs-lookup"><span data-stu-id="a9059-123">Add child device list (comma separated) includes only non-edge devices.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9059-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9059-124">-DefaultProfile</span></span>
<span data-ttu-id="a9059-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9059-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9059-126">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="a9059-126">-DeviceId</span></span>
<span data-ttu-id="a9059-127">Céleszköz-azonosító.</span><span class="sxs-lookup"><span data-stu-id="a9059-127">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9059-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="a9059-128">-EdgeEnabled</span></span>
<span data-ttu-id="a9059-129">Megjelölés az Edge engedélyezésével</span><span class="sxs-lookup"><span data-stu-id="a9059-129">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9059-130">-Force</span><span class="sxs-lookup"><span data-stu-id="a9059-130">-Force</span></span>
<span data-ttu-id="a9059-131">Felülírja a nem él eszköz fölérendelt eszközét.</span><span class="sxs-lookup"><span data-stu-id="a9059-131">Overwrites the non-edge device's parent device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9059-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9059-132">-InputObject</span></span>
<span data-ttu-id="a9059-133">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="a9059-133">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9059-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a9059-134">-IotHubName</span></span>
<span data-ttu-id="a9059-135">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="a9059-135">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9059-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="a9059-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="a9059-137">Explicit önaláírt tanúsítvány-ujjlenyomat az elsődleges kulcshoz való használathoz.</span><span class="sxs-lookup"><span data-stu-id="a9059-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9059-138">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="a9059-138">-ParentDeviceId</span></span>
<span data-ttu-id="a9059-139">Az Edge-eszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a9059-139">Id of edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9059-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9059-140">-ResourceGroupName</span></span>
<span data-ttu-id="a9059-141">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a9059-141">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9059-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9059-142">-ResourceId</span></span>
<span data-ttu-id="a9059-143">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="a9059-143">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9059-144">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="a9059-144">-SecondaryThumbprint</span></span>
<span data-ttu-id="a9059-145">Explicit önaláírt tanúsítvány-ujjlenyomat a másodlagos kulcshoz való használathoz.</span><span class="sxs-lookup"><span data-stu-id="a9059-145">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9059-146">-Állapot</span><span class="sxs-lookup"><span data-stu-id="a9059-146">-Status</span></span>
<span data-ttu-id="a9059-147">Állítsa be az eszköz állapotát a létrehozás során.</span><span class="sxs-lookup"><span data-stu-id="a9059-147">Set device status upon creation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9059-148">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="a9059-148">-StatusReason</span></span>
<span data-ttu-id="a9059-149">Az eszköz állapotának leírása.</span><span class="sxs-lookup"><span data-stu-id="a9059-149">Description for device status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9059-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a9059-150">-Confirm</span></span>
<span data-ttu-id="a9059-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a9059-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9059-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9059-152">-WhatIf</span></span>
<span data-ttu-id="a9059-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a9059-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9059-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a9059-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9059-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9059-155">CommonParameters</span></span>
<span data-ttu-id="a9059-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a9059-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9059-157">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9059-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9059-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9059-158">INPUTS</span></span>

### <span data-ttu-id="a9059-159">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a9059-159">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a9059-160">System. String</span><span class="sxs-lookup"><span data-stu-id="a9059-160">System.String</span></span>

## <span data-ttu-id="a9059-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9059-161">OUTPUTS</span></span>

### <span data-ttu-id="a9059-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDEvice</span><span class="sxs-lookup"><span data-stu-id="a9059-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="a9059-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a9059-163">NOTES</span></span>

## <span data-ttu-id="a9059-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9059-164">RELATED LINKS</span></span>
