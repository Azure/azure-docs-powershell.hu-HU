---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
ms.openlocfilehash: 0779403a23a36c972a0d5597d40231b5cc026b37
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195959"
---
# <span data-ttu-id="e1f50-101">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="e1f50-101">Set-AzIotHubDevice</span></span>

## <span data-ttu-id="e1f50-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1f50-102">SYNOPSIS</span></span>
<span data-ttu-id="e1f50-103">IoT-hub eszköz frissítése</span><span class="sxs-lookup"><span data-stu-id="e1f50-103">Update an IoT Hub device.</span></span>

## <span data-ttu-id="e1f50-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1f50-104">SYNTAX</span></span>

### <span data-ttu-id="e1f50-105">ResourceSetForStatus (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e1f50-105">ResourceSetForStatus (Default)</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1f50-106">InputObjectSetForAuth</span><span class="sxs-lookup"><span data-stu-id="e1f50-106">InputObjectSetForAuth</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1f50-107">InputObjectSetForStatus</span><span class="sxs-lookup"><span data-stu-id="e1f50-107">InputObjectSetForStatus</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1f50-108">InputObjectSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="e1f50-108">InputObjectSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1f50-109">ResourceSetForAuth</span><span class="sxs-lookup"><span data-stu-id="e1f50-109">ResourceSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1f50-110">ResourceSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="e1f50-110">ResourceSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-EdgeEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1f50-111">ResourceIdSetForAuth</span><span class="sxs-lookup"><span data-stu-id="e1f50-111">ResourceIdSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1f50-112">ResourceIdSetForStatus</span><span class="sxs-lookup"><span data-stu-id="e1f50-112">ResourceIdSetForStatus</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1f50-113">ResourceIdSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="e1f50-113">ResourceIdSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1f50-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1f50-114">DESCRIPTION</span></span>
<span data-ttu-id="e1f50-115">IoT-hub eszköz frissítése</span><span class="sxs-lookup"><span data-stu-id="e1f50-115">Update an IoT Hub device.</span></span>

## <span data-ttu-id="e1f50-116">Példák</span><span class="sxs-lookup"><span data-stu-id="e1f50-116">EXAMPLES</span></span>

### <span data-ttu-id="e1f50-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e1f50-117">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -EdgeEnabled
```

<span data-ttu-id="e1f50-118">Az Edge képességeinek bekapcsolása az eszközön.</span><span class="sxs-lookup"><span data-stu-id="e1f50-118">Turn on edge capabilities for device.</span></span>

### <span data-ttu-id="e1f50-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="e1f50-119">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Status Disabled
```

<span data-ttu-id="e1f50-120">Letilthatja az eszköz állapotát.</span><span class="sxs-lookup"><span data-stu-id="e1f50-120">Disable device status.</span></span>

### <span data-ttu-id="e1f50-121">3. példa</span><span class="sxs-lookup"><span data-stu-id="e1f50-121">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "x509_ca"
```

<span data-ttu-id="e1f50-122">IOT-hub eszköz engedélyezési típusának frissítése</span><span class="sxs-lookup"><span data-stu-id="e1f50-122">Update authorization type of an Iot Hub device.</span></span>

## <span data-ttu-id="e1f50-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1f50-123">PARAMETERS</span></span>

### <span data-ttu-id="e1f50-124">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="e1f50-124">-AuthMethod</span></span>
<span data-ttu-id="e1f50-125">Az engedély típusa: egy entitást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e1f50-125">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f50-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1f50-126">-DefaultProfile</span></span>
<span data-ttu-id="e1f50-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1f50-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1f50-128">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="e1f50-128">-DeviceId</span></span>
<span data-ttu-id="e1f50-129">Céleszköz-azonosító.</span><span class="sxs-lookup"><span data-stu-id="e1f50-129">Target Device Id.</span></span>

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

### <span data-ttu-id="e1f50-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="e1f50-130">-EdgeEnabled</span></span>
<span data-ttu-id="e1f50-131">Megjelölés az Edge engedélyezésével</span><span class="sxs-lookup"><span data-stu-id="e1f50-131">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: InputObjectSetForEdgeEnabled, ResourceSetForEdgeEnabled, ResourceIdSetForEdgeEnabled
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f50-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1f50-132">-InputObject</span></span>
<span data-ttu-id="e1f50-133">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="e1f50-133">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSetForAuth, InputObjectSetForStatus, InputObjectSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f50-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e1f50-134">-IotHubName</span></span>
<span data-ttu-id="e1f50-135">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="e1f50-135">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, ResourceSetForAuth, ResourceSetForEdgeEnabled
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f50-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="e1f50-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="e1f50-137">Explicit önaláírt tanúsítvány-ujjlenyomat az elsődleges kulcshoz való használathoz.</span><span class="sxs-lookup"><span data-stu-id="e1f50-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f50-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1f50-138">-ResourceGroupName</span></span>
<span data-ttu-id="e1f50-139">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e1f50-139">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, ResourceSetForAuth, ResourceSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f50-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1f50-140">-ResourceId</span></span>
<span data-ttu-id="e1f50-141">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="e1f50-141">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSetForAuth, ResourceIdSetForStatus, ResourceIdSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f50-142">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="e1f50-142">-SecondaryThumbprint</span></span>
<span data-ttu-id="e1f50-143">Explicit önaláírt tanúsítvány-ujjlenyomat a másodlagos kulcshoz való használathoz.</span><span class="sxs-lookup"><span data-stu-id="e1f50-143">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f50-144">-Állapot</span><span class="sxs-lookup"><span data-stu-id="e1f50-144">-Status</span></span>
<span data-ttu-id="e1f50-145">Állítsa be az eszköz állapotát a létrehozás során.</span><span class="sxs-lookup"><span data-stu-id="e1f50-145">Set device status upon creation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceStatus
Parameter Sets: ResourceSetForStatus, InputObjectSetForStatus, ResourceIdSetForStatus
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f50-146">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="e1f50-146">-StatusReason</span></span>
<span data-ttu-id="e1f50-147">Az eszköz állapotának leírása.</span><span class="sxs-lookup"><span data-stu-id="e1f50-147">Description for device status.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, InputObjectSetForStatus, ResourceIdSetForStatus
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f50-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e1f50-148">-Confirm</span></span>
<span data-ttu-id="e1f50-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e1f50-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1f50-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1f50-150">-WhatIf</span></span>
<span data-ttu-id="e1f50-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e1f50-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1f50-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e1f50-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1f50-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1f50-153">CommonParameters</span></span>
<span data-ttu-id="e1f50-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e1f50-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1f50-155">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1f50-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1f50-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1f50-156">INPUTS</span></span>

### <span data-ttu-id="e1f50-157">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e1f50-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e1f50-158">System. String</span><span class="sxs-lookup"><span data-stu-id="e1f50-158">System.String</span></span>

## <span data-ttu-id="e1f50-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1f50-159">OUTPUTS</span></span>

### <span data-ttu-id="e1f50-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDEvice</span><span class="sxs-lookup"><span data-stu-id="e1f50-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="e1f50-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1f50-161">NOTES</span></span>

## <span data-ttu-id="e1f50-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1f50-162">RELATED LINKS</span></span>
