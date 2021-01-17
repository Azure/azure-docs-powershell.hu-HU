---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 3982279b8698a84f23bc83aeccd25083d98363f4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467778"
---
# <span data-ttu-id="17567-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="17567-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="17567-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17567-102">SYNOPSIS</span></span>
<span data-ttu-id="17567-103">Eszközregisztrációs csoport frissítése.</span><span class="sxs-lookup"><span data-stu-id="17567-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="17567-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="17567-104">SYNTAX</span></span>

### <span data-ttu-id="17567-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="17567-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17567-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="17567-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17567-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="17567-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17567-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="17567-108">DESCRIPTION</span></span>
<span data-ttu-id="17567-109">Frissítsen egy regisztrációs csoportot egy Azure IoT-központ eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="17567-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="17567-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="17567-110">EXAMPLES</span></span>

### <span data-ttu-id="17567-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="17567-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="17567-112">Frissítse egy regisztrációs csoport kiosztási házirendját és központját.</span><span class="sxs-lookup"><span data-stu-id="17567-112">Update allocation policy and hubs for an enrollment group.</span></span>

### <span data-ttu-id="17567-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="17567-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="17567-114">Frissítse egy regisztrációs csoport kezdeti állapotát.</span><span class="sxs-lookup"><span data-stu-id="17567-114">Update an enrollment group's initial twin state.</span></span>

## <span data-ttu-id="17567-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17567-115">PARAMETERS</span></span>

### <span data-ttu-id="17567-116">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="17567-116">-AllocationPolicy</span></span>
<span data-ttu-id="17567-117">A Központhoz rendelt eszköz kiosztásának típusa.</span><span class="sxs-lookup"><span data-stu-id="17567-117">Type of allocation for device assigned to the Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSAllocationPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Hashed, GeoLatency, Static, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17567-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="17567-118">-ApiVersion</span></span>
<span data-ttu-id="17567-119">A kiépítési szolgáltatás API-verziója az egyéni hozzárendelési kérésben.</span><span class="sxs-lookup"><span data-stu-id="17567-119">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="17567-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17567-120">-DefaultProfile</span></span>
<span data-ttu-id="17567-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="17567-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17567-122">-Kívánt</span><span class="sxs-lookup"><span data-stu-id="17567-122">-Desired</span></span>
<span data-ttu-id="17567-123">A kezdeti kíván tulajdonságok.</span><span class="sxs-lookup"><span data-stu-id="17567-123">Initial twin desired properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17567-124">-DpsName</span><span class="sxs-lookup"><span data-stu-id="17567-124">-DpsName</span></span>
<span data-ttu-id="17567-125">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="17567-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="17567-126">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="17567-126">-DpsObject</span></span>
<span data-ttu-id="17567-127">IoT-eszköz kiépítési szolgáltatásobjektuma</span><span class="sxs-lookup"><span data-stu-id="17567-127">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17567-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="17567-128">-EdgeEnabled</span></span>
<span data-ttu-id="17567-129">Flag indicating edge enablement.</span><span class="sxs-lookup"><span data-stu-id="17567-129">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17567-130">-IotHub</span><span class="sxs-lookup"><span data-stu-id="17567-130">-IotHub</span></span>
<span data-ttu-id="17567-131">A cél IoT-központ állomásneve.</span><span class="sxs-lookup"><span data-stu-id="17567-131">Host name of target IoT Hub.</span></span>
<span data-ttu-id="17567-132">Több IoT-központhoz használjon térközt választó listát.</span><span class="sxs-lookup"><span data-stu-id="17567-132">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="17567-133">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="17567-133">-IotHubHostName</span></span>
<span data-ttu-id="17567-134">A cél IoT-központ állomásneve.</span><span class="sxs-lookup"><span data-stu-id="17567-134">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="17567-135">-Name</span><span class="sxs-lookup"><span data-stu-id="17567-135">-Name</span></span>
<span data-ttu-id="17567-136">A regisztrációs csoport neve.</span><span class="sxs-lookup"><span data-stu-id="17567-136">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="17567-137">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="17567-137">-ProvisioningStatus</span></span>
<span data-ttu-id="17567-138">A regisztrációs bejegyzés engedélyezése vagy letiltása.</span><span class="sxs-lookup"><span data-stu-id="17567-138">Enable or disable enrollment entry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17567-139">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="17567-139">-ReprovisionPolicy</span></span>
<span data-ttu-id="17567-140">A másik Iot-központba való újraépítéssel kezelni szükséges eszközadatok.</span><span class="sxs-lookup"><span data-stu-id="17567-140">Device data to be handled on re-provision to different Iot Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSReprovisionType
Parameter Sets: (All)
Aliases:
Accepted values: reprovisionandmigratedata, reprovisionandresetdata, never

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17567-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17567-141">-ResourceGroupName</span></span>
<span data-ttu-id="17567-142">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="17567-142">Name of the Resource Group</span></span>

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

### <span data-ttu-id="17567-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17567-143">-ResourceId</span></span>
<span data-ttu-id="17567-144">IoT-eszköz kiépítési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="17567-144">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="17567-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="17567-145">-Tag</span></span>
<span data-ttu-id="17567-146">Kezdeti címkecímkék.</span><span class="sxs-lookup"><span data-stu-id="17567-146">Initial twin tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17567-147">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="17567-147">-WebhookUrl</span></span>
<span data-ttu-id="17567-148">Az egyéni hozzárendelési kérések webhook URL-címe.</span><span class="sxs-lookup"><span data-stu-id="17567-148">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="17567-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17567-149">-Confirm</span></span>
<span data-ttu-id="17567-150">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="17567-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17567-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17567-151">-WhatIf</span></span>
<span data-ttu-id="17567-152">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="17567-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17567-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="17567-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17567-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17567-154">CommonParameters</span></span>
<span data-ttu-id="17567-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17567-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17567-156">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17567-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17567-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17567-157">INPUTS</span></span>

### <span data-ttu-id="17567-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="17567-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="17567-159">System.String</span><span class="sxs-lookup"><span data-stu-id="17567-159">System.String</span></span>

## <span data-ttu-id="17567-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17567-160">OUTPUTS</span></span>

### <span data-ttu-id="17567-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="17567-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="17567-162">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="17567-162">NOTES</span></span>

## <span data-ttu-id="17567-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17567-163">RELATED LINKS</span></span>
