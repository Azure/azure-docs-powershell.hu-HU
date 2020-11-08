---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
ms.openlocfilehash: 0779403a23a36c972a0d5597d40231b5cc026b37
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025699"
---
# <span data-ttu-id="eddba-101">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="eddba-101">Set-AzIotHubDevice</span></span>

## <span data-ttu-id="eddba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eddba-102">SYNOPSIS</span></span>
<span data-ttu-id="eddba-103">IoT-hub eszköz frissítése</span><span class="sxs-lookup"><span data-stu-id="eddba-103">Update an IoT Hub device.</span></span>

## <span data-ttu-id="eddba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eddba-104">SYNTAX</span></span>

### <span data-ttu-id="eddba-105">ResourceSetForStatus (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eddba-105">ResourceSetForStatus (Default)</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eddba-106">InputObjectSetForAuth</span><span class="sxs-lookup"><span data-stu-id="eddba-106">InputObjectSetForAuth</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eddba-107">InputObjectSetForStatus</span><span class="sxs-lookup"><span data-stu-id="eddba-107">InputObjectSetForStatus</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eddba-108">InputObjectSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="eddba-108">InputObjectSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eddba-109">ResourceSetForAuth</span><span class="sxs-lookup"><span data-stu-id="eddba-109">ResourceSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eddba-110">ResourceSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="eddba-110">ResourceSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-EdgeEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eddba-111">ResourceIdSetForAuth</span><span class="sxs-lookup"><span data-stu-id="eddba-111">ResourceIdSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eddba-112">ResourceIdSetForStatus</span><span class="sxs-lookup"><span data-stu-id="eddba-112">ResourceIdSetForStatus</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eddba-113">ResourceIdSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="eddba-113">ResourceIdSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eddba-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="eddba-114">DESCRIPTION</span></span>
<span data-ttu-id="eddba-115">IoT-hub eszköz frissítése</span><span class="sxs-lookup"><span data-stu-id="eddba-115">Update an IoT Hub device.</span></span>

## <span data-ttu-id="eddba-116">Példák</span><span class="sxs-lookup"><span data-stu-id="eddba-116">EXAMPLES</span></span>

### <span data-ttu-id="eddba-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="eddba-117">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -EdgeEnabled
```

<span data-ttu-id="eddba-118">Az Edge képességeinek bekapcsolása az eszközön.</span><span class="sxs-lookup"><span data-stu-id="eddba-118">Turn on edge capabilities for device.</span></span>

### <span data-ttu-id="eddba-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="eddba-119">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Status Disabled
```

<span data-ttu-id="eddba-120">Letilthatja az eszköz állapotát.</span><span class="sxs-lookup"><span data-stu-id="eddba-120">Disable device status.</span></span>

### <span data-ttu-id="eddba-121">3. példa</span><span class="sxs-lookup"><span data-stu-id="eddba-121">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "x509_ca"
```

<span data-ttu-id="eddba-122">IOT-hub eszköz engedélyezési típusának frissítése</span><span class="sxs-lookup"><span data-stu-id="eddba-122">Update authorization type of an Iot Hub device.</span></span>

## <span data-ttu-id="eddba-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eddba-123">PARAMETERS</span></span>

### <span data-ttu-id="eddba-124">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="eddba-124">-AuthMethod</span></span>
<span data-ttu-id="eddba-125">Az engedély típusa: egy entitást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="eddba-125">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="eddba-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eddba-126">-DefaultProfile</span></span>
<span data-ttu-id="eddba-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eddba-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eddba-128">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="eddba-128">-DeviceId</span></span>
<span data-ttu-id="eddba-129">Céleszköz-azonosító.</span><span class="sxs-lookup"><span data-stu-id="eddba-129">Target Device Id.</span></span>

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

### <span data-ttu-id="eddba-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="eddba-130">-EdgeEnabled</span></span>
<span data-ttu-id="eddba-131">Megjelölés az Edge engedélyezésével</span><span class="sxs-lookup"><span data-stu-id="eddba-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="eddba-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eddba-132">-InputObject</span></span>
<span data-ttu-id="eddba-133">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="eddba-133">IotHub object</span></span>

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

### <span data-ttu-id="eddba-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="eddba-134">-IotHubName</span></span>
<span data-ttu-id="eddba-135">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="eddba-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="eddba-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="eddba-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="eddba-137">Explicit önaláírt tanúsítvány-ujjlenyomat az elsődleges kulcshoz való használathoz.</span><span class="sxs-lookup"><span data-stu-id="eddba-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="eddba-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eddba-138">-ResourceGroupName</span></span>
<span data-ttu-id="eddba-139">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="eddba-139">Name of the Resource Group</span></span>

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

### <span data-ttu-id="eddba-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eddba-140">-ResourceId</span></span>
<span data-ttu-id="eddba-141">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="eddba-141">IotHub Resource Id</span></span>

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

### <span data-ttu-id="eddba-142">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="eddba-142">-SecondaryThumbprint</span></span>
<span data-ttu-id="eddba-143">Explicit önaláírt tanúsítvány-ujjlenyomat a másodlagos kulcshoz való használathoz.</span><span class="sxs-lookup"><span data-stu-id="eddba-143">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="eddba-144">-Állapot</span><span class="sxs-lookup"><span data-stu-id="eddba-144">-Status</span></span>
<span data-ttu-id="eddba-145">Állítsa be az eszköz állapotát a létrehozás során.</span><span class="sxs-lookup"><span data-stu-id="eddba-145">Set device status upon creation.</span></span>

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

### <span data-ttu-id="eddba-146">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="eddba-146">-StatusReason</span></span>
<span data-ttu-id="eddba-147">Az eszköz állapotának leírása.</span><span class="sxs-lookup"><span data-stu-id="eddba-147">Description for device status.</span></span>

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

### <span data-ttu-id="eddba-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eddba-148">-Confirm</span></span>
<span data-ttu-id="eddba-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eddba-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eddba-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eddba-150">-WhatIf</span></span>
<span data-ttu-id="eddba-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eddba-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eddba-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eddba-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eddba-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eddba-153">CommonParameters</span></span>
<span data-ttu-id="eddba-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eddba-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eddba-155">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eddba-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eddba-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eddba-156">INPUTS</span></span>

### <span data-ttu-id="eddba-157">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="eddba-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="eddba-158">System. String</span><span class="sxs-lookup"><span data-stu-id="eddba-158">System.String</span></span>

## <span data-ttu-id="eddba-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eddba-159">OUTPUTS</span></span>

### <span data-ttu-id="eddba-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDEvice</span><span class="sxs-lookup"><span data-stu-id="eddba-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="eddba-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eddba-161">NOTES</span></span>

## <span data-ttu-id="eddba-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eddba-162">RELATED LINKS</span></span>
