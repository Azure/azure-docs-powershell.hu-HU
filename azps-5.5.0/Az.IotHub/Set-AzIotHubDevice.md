---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
ms.openlocfilehash: 0779403a23a36c972a0d5597d40231b5cc026b37
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167283"
---
# <span data-ttu-id="9fdac-101">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="9fdac-101">Set-AzIotHubDevice</span></span>

## <span data-ttu-id="9fdac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fdac-102">SYNOPSIS</span></span>
<span data-ttu-id="9fdac-103">Frissítsen egy IoT-központot.</span><span class="sxs-lookup"><span data-stu-id="9fdac-103">Update an IoT Hub device.</span></span>

## <span data-ttu-id="9fdac-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9fdac-104">SYNTAX</span></span>

### <span data-ttu-id="9fdac-105">ResourceSetForStatus (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9fdac-105">ResourceSetForStatus (Default)</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fdac-106">InputObjectSetForAuth</span><span class="sxs-lookup"><span data-stu-id="9fdac-106">InputObjectSetForAuth</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fdac-107">InputObjectSetForStatus</span><span class="sxs-lookup"><span data-stu-id="9fdac-107">InputObjectSetForStatus</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fdac-108">InputObjectSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="9fdac-108">InputObjectSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fdac-109">ResourceSetForAuth</span><span class="sxs-lookup"><span data-stu-id="9fdac-109">ResourceSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9fdac-110">ResourceSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="9fdac-110">ResourceSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-EdgeEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fdac-111">ResourceIdSetForAuth</span><span class="sxs-lookup"><span data-stu-id="9fdac-111">ResourceIdSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fdac-112">ResourceIdSetForStatus</span><span class="sxs-lookup"><span data-stu-id="9fdac-112">ResourceIdSetForStatus</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fdac-113">ResourceIdSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="9fdac-113">ResourceIdSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fdac-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9fdac-114">DESCRIPTION</span></span>
<span data-ttu-id="9fdac-115">Frissítsen egy IoT-központot.</span><span class="sxs-lookup"><span data-stu-id="9fdac-115">Update an IoT Hub device.</span></span>

## <span data-ttu-id="9fdac-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9fdac-116">EXAMPLES</span></span>

### <span data-ttu-id="9fdac-117">1. példa</span><span class="sxs-lookup"><span data-stu-id="9fdac-117">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -EdgeEnabled
```

<span data-ttu-id="9fdac-118">Kapcsolja be az edge funkciókat az eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="9fdac-118">Turn on edge capabilities for device.</span></span>

### <span data-ttu-id="9fdac-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="9fdac-119">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Status Disabled
```

<span data-ttu-id="9fdac-120">Tiltsa le az eszköz állapotát.</span><span class="sxs-lookup"><span data-stu-id="9fdac-120">Disable device status.</span></span>

### <span data-ttu-id="9fdac-121">3. példa</span><span class="sxs-lookup"><span data-stu-id="9fdac-121">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "x509_ca"
```

<span data-ttu-id="9fdac-122">Frissítse egy Iot Hub-eszköz engedélyezési típusát.</span><span class="sxs-lookup"><span data-stu-id="9fdac-122">Update authorization type of an Iot Hub device.</span></span>

## <span data-ttu-id="9fdac-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9fdac-123">PARAMETERS</span></span>

### <span data-ttu-id="9fdac-124">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="9fdac-124">-AuthMethod</span></span>
<span data-ttu-id="9fdac-125">Az engedélyezési típus, amely alapján egy entitást létre kell hozatni.</span><span class="sxs-lookup"><span data-stu-id="9fdac-125">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="9fdac-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fdac-126">-DefaultProfile</span></span>
<span data-ttu-id="9fdac-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9fdac-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fdac-128">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="9fdac-128">-DeviceId</span></span>
<span data-ttu-id="9fdac-129">Céleszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9fdac-129">Target Device Id.</span></span>

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

### <span data-ttu-id="9fdac-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="9fdac-130">-EdgeEnabled</span></span>
<span data-ttu-id="9fdac-131">Flag indicating edge enablement.</span><span class="sxs-lookup"><span data-stu-id="9fdac-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="9fdac-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fdac-132">-InputObject</span></span>
<span data-ttu-id="9fdac-133">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="9fdac-133">IotHub object</span></span>

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

### <span data-ttu-id="9fdac-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="9fdac-134">-IotHubName</span></span>
<span data-ttu-id="9fdac-135">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="9fdac-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9fdac-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="9fdac-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="9fdac-137">Az elsődleges kulcshoz használható explicit öna aláírt tanúsítvány thumbprint.</span><span class="sxs-lookup"><span data-stu-id="9fdac-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="9fdac-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fdac-138">-ResourceGroupName</span></span>
<span data-ttu-id="9fdac-139">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="9fdac-139">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9fdac-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fdac-140">-ResourceId</span></span>
<span data-ttu-id="9fdac-141">IotHub erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="9fdac-141">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9fdac-142">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="9fdac-142">-SecondaryThumbprint</span></span>
<span data-ttu-id="9fdac-143">Explicit öna aláírt tanúsítvány thumbprint for use for secondary key.</span><span class="sxs-lookup"><span data-stu-id="9fdac-143">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="9fdac-144">-Állapot</span><span class="sxs-lookup"><span data-stu-id="9fdac-144">-Status</span></span>
<span data-ttu-id="9fdac-145">Eszközállapot beállítása létrehozáskor.</span><span class="sxs-lookup"><span data-stu-id="9fdac-145">Set device status upon creation.</span></span>

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

### <span data-ttu-id="9fdac-146">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="9fdac-146">-StatusReason</span></span>
<span data-ttu-id="9fdac-147">Az eszközállapot leírása.</span><span class="sxs-lookup"><span data-stu-id="9fdac-147">Description for device status.</span></span>

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

### <span data-ttu-id="9fdac-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9fdac-148">-Confirm</span></span>
<span data-ttu-id="9fdac-149">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9fdac-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fdac-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fdac-150">-WhatIf</span></span>
<span data-ttu-id="9fdac-151">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9fdac-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fdac-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9fdac-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fdac-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fdac-153">CommonParameters</span></span>
<span data-ttu-id="9fdac-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fdac-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fdac-155">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fdac-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fdac-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9fdac-156">INPUTS</span></span>

### <span data-ttu-id="9fdac-157">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9fdac-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9fdac-158">System.String</span><span class="sxs-lookup"><span data-stu-id="9fdac-158">System.String</span></span>

## <span data-ttu-id="9fdac-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fdac-159">OUTPUTS</span></span>

### <span data-ttu-id="9fdac-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="9fdac-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="9fdac-161">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9fdac-161">NOTES</span></span>

## <span data-ttu-id="9fdac-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9fdac-162">RELATED LINKS</span></span>
