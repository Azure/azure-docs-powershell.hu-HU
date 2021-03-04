---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
ms.openlocfilehash: 0f2e7cd2abc61cde9f060eaabf6634385b6ec258
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942538"
---
# <span data-ttu-id="452d5-101">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="452d5-101">Add-AzIotHubDevice</span></span>

## <span data-ttu-id="452d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="452d5-102">SYNOPSIS</span></span>
<span data-ttu-id="452d5-103">Hozzon létre egy eszközt egy IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="452d5-103">Create a device in an IoT Hub.</span></span>

## <span data-ttu-id="452d5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="452d5-104">SYNTAX</span></span>

### <span data-ttu-id="452d5-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="452d5-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled]
 [-Children <String[]>] [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="452d5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="452d5-106">InputObjectSet</span></span>
```
Add-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="452d5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="452d5-107">ResourceIdSet</span></span>
```
Add-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="452d5-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="452d5-108">DESCRIPTION</span></span>
<span data-ttu-id="452d5-109">Hozzon létre egy másik engedélyezési típust az IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="452d5-109">Create a device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="452d5-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="452d5-110">EXAMPLES</span></span>

### <span data-ttu-id="452d5-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="452d5-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled
```

<span data-ttu-id="452d5-112">Hozzon létre egy edge-kompatibilis IoT-eszközt alapértelmezett hitelesítéssel (megosztott privát kulcs).</span><span class="sxs-lookup"><span data-stu-id="452d5-112">Create an edge enabled IoT device with default authorization (shared private key).</span></span>

### <span data-ttu-id="452d5-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="452d5-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -AuthMethod "x509_ca" -Status Disabled -StatusReason "Some Reason"
```

<span data-ttu-id="452d5-114">Hozzon létre egy IoT-eszközt a legfelső szintű hitelesítésszolgáltatói hitelesítésszolgáltatóval letiltott állapottal és okból kifolyólag.</span><span class="sxs-lookup"><span data-stu-id="452d5-114">Create an IoT device with root CA authorization with disabled status and reason.</span></span>

### <span data-ttu-id="452d5-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="452d5-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled -Children device1,device2
```

<span data-ttu-id="452d5-116">Hozzon létre egy edge-kompatibilis IoT-eszközt, és vegyen fel hozzá gyermekeszközöket.</span><span class="sxs-lookup"><span data-stu-id="452d5-116">Create an edge enabled IoT device and add child devices to it.</span></span>

### <span data-ttu-id="452d5-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="452d5-117">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -ParentDeviceId parentDevice1
```

<span data-ttu-id="452d5-118">Hozzon létre egy IoT-eszközt, és állítsa be a szülőeszközét.</span><span class="sxs-lookup"><span data-stu-id="452d5-118">Create an IoT device and set its parent device.</span></span>

## <span data-ttu-id="452d5-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="452d5-119">PARAMETERS</span></span>

### <span data-ttu-id="452d5-120">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="452d5-120">-AuthMethod</span></span>
<span data-ttu-id="452d5-121">Az engedélyezési típus, amely alapján egy entitást létre kell hozatni.</span><span class="sxs-lookup"><span data-stu-id="452d5-121">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="452d5-122">-Gyermekek</span><span class="sxs-lookup"><span data-stu-id="452d5-122">-Children</span></span>
<span data-ttu-id="452d5-123">A gyermekeszköz-lista (vesszővel elválasztva) hozzáadása csak a nem edge-hez használható eszközöket tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="452d5-123">Add child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="452d5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="452d5-124">-DefaultProfile</span></span>
<span data-ttu-id="452d5-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="452d5-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="452d5-126">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="452d5-126">-DeviceId</span></span>
<span data-ttu-id="452d5-127">Céleszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="452d5-127">Target Device Id.</span></span>

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

### <span data-ttu-id="452d5-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="452d5-128">-EdgeEnabled</span></span>
<span data-ttu-id="452d5-129">Flag indicating edge enablement.</span><span class="sxs-lookup"><span data-stu-id="452d5-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="452d5-130">-Force</span><span class="sxs-lookup"><span data-stu-id="452d5-130">-Force</span></span>
<span data-ttu-id="452d5-131">Felülírja a nem edge-beli eszköz szülőeszközét.</span><span class="sxs-lookup"><span data-stu-id="452d5-131">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="452d5-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="452d5-132">-InputObject</span></span>
<span data-ttu-id="452d5-133">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="452d5-133">IotHub object</span></span>

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

### <span data-ttu-id="452d5-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="452d5-134">-IotHubName</span></span>
<span data-ttu-id="452d5-135">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="452d5-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="452d5-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="452d5-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="452d5-137">Explicit öna aláírt tanúsítvány thumbprint for use for primary key.</span><span class="sxs-lookup"><span data-stu-id="452d5-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="452d5-138">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="452d5-138">-ParentDeviceId</span></span>
<span data-ttu-id="452d5-139">A peremhálózati eszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="452d5-139">Id of edge device.</span></span>

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

### <span data-ttu-id="452d5-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="452d5-140">-ResourceGroupName</span></span>
<span data-ttu-id="452d5-141">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="452d5-141">Name of the Resource Group</span></span>

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

### <span data-ttu-id="452d5-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="452d5-142">-ResourceId</span></span>
<span data-ttu-id="452d5-143">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="452d5-143">IotHub Resource Id</span></span>

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

### <span data-ttu-id="452d5-144">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="452d5-144">-SecondaryThumbprint</span></span>
<span data-ttu-id="452d5-145">Explicit öna aláírt tanúsítvány thumbprint for use for secondary key.</span><span class="sxs-lookup"><span data-stu-id="452d5-145">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="452d5-146">-Állapot</span><span class="sxs-lookup"><span data-stu-id="452d5-146">-Status</span></span>
<span data-ttu-id="452d5-147">Eszközállapot beállítása létrehozáskor.</span><span class="sxs-lookup"><span data-stu-id="452d5-147">Set device status upon creation.</span></span>

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

### <span data-ttu-id="452d5-148">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="452d5-148">-StatusReason</span></span>
<span data-ttu-id="452d5-149">Az eszközállapot leírása.</span><span class="sxs-lookup"><span data-stu-id="452d5-149">Description for device status.</span></span>

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

### <span data-ttu-id="452d5-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="452d5-150">-Confirm</span></span>
<span data-ttu-id="452d5-151">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="452d5-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="452d5-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="452d5-152">-WhatIf</span></span>
<span data-ttu-id="452d5-153">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="452d5-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="452d5-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="452d5-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="452d5-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="452d5-155">CommonParameters</span></span>
<span data-ttu-id="452d5-156">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="452d5-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="452d5-157">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="452d5-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="452d5-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="452d5-158">INPUTS</span></span>

### <span data-ttu-id="452d5-159">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="452d5-159">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="452d5-160">System.String</span><span class="sxs-lookup"><span data-stu-id="452d5-160">System.String</span></span>

## <span data-ttu-id="452d5-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="452d5-161">OUTPUTS</span></span>

### <span data-ttu-id="452d5-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="452d5-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="452d5-163">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="452d5-163">NOTES</span></span>

## <span data-ttu-id="452d5-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="452d5-164">RELATED LINKS</span></span>
