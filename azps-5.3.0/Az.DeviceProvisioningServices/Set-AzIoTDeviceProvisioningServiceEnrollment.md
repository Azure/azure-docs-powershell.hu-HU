---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: 47c5c5119e41f3feeaccda66871d902e631c9ac2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376933"
---
# <span data-ttu-id="78652-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="78652-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="78652-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78652-102">SYNOPSIS</span></span>
<span data-ttu-id="78652-103">Eszközregisztrációs rekord frissítése.</span><span class="sxs-lookup"><span data-stu-id="78652-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="78652-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="78652-104">SYNTAX</span></span>

### <span data-ttu-id="78652-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="78652-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78652-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="78652-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78652-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="78652-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78652-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="78652-108">DESCRIPTION</span></span>
<span data-ttu-id="78652-109">Frissítsen egy eszköz regisztrálását egy Azure IoT Hub eszközszolgáltató szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="78652-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="78652-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="78652-110">EXAMPLES</span></span>

### <span data-ttu-id="78652-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="78652-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="78652-112">Egy regisztrációs rekordhoz frissítse a foglalási házirendet és a központokat.</span><span class="sxs-lookup"><span data-stu-id="78652-112">Update allocation policy and hubs for an enrollment record.</span></span>

### <span data-ttu-id="78652-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="78652-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="78652-114">Frissítse a regisztráció kezdeti állapotát.</span><span class="sxs-lookup"><span data-stu-id="78652-114">Update an enrollment's initial twin state.</span></span>

## <span data-ttu-id="78652-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78652-115">PARAMETERS</span></span>

### <span data-ttu-id="78652-116">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="78652-116">-AllocationPolicy</span></span>
<span data-ttu-id="78652-117">A Központhoz rendelt eszköz kiosztásának típusa.</span><span class="sxs-lookup"><span data-stu-id="78652-117">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="78652-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="78652-118">-ApiVersion</span></span>
<span data-ttu-id="78652-119">A kiépítési szolgáltatás API-verziója az egyéni hozzárendelési kérésben.</span><span class="sxs-lookup"><span data-stu-id="78652-119">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="78652-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78652-120">-DefaultProfile</span></span>
<span data-ttu-id="78652-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="78652-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78652-122">-Kívánt</span><span class="sxs-lookup"><span data-stu-id="78652-122">-Desired</span></span>
<span data-ttu-id="78652-123">A kezdeti kíván tulajdonságok.</span><span class="sxs-lookup"><span data-stu-id="78652-123">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="78652-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="78652-124">-DeviceId</span></span>
<span data-ttu-id="78652-125">IoT-központ eszközazonosítója.</span><span class="sxs-lookup"><span data-stu-id="78652-125">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="78652-126">-DpsName</span><span class="sxs-lookup"><span data-stu-id="78652-126">-DpsName</span></span>
<span data-ttu-id="78652-127">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="78652-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="78652-128">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="78652-128">-DpsObject</span></span>
<span data-ttu-id="78652-129">IoT-eszköz kiépítési szolgáltatásobjektuma</span><span class="sxs-lookup"><span data-stu-id="78652-129">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="78652-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="78652-130">-EdgeEnabled</span></span>
<span data-ttu-id="78652-131">Flag indicating edge enablement.</span><span class="sxs-lookup"><span data-stu-id="78652-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="78652-132">-IotHub</span><span class="sxs-lookup"><span data-stu-id="78652-132">-IotHub</span></span>
<span data-ttu-id="78652-133">A cél IoT-központ állomásneve.</span><span class="sxs-lookup"><span data-stu-id="78652-133">Host name of target IoT Hub.</span></span>
<span data-ttu-id="78652-134">Több IoT-központhoz használjon térközt választó listát.</span><span class="sxs-lookup"><span data-stu-id="78652-134">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="78652-135">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="78652-135">-IotHubHostName</span></span>
<span data-ttu-id="78652-136">A cél IoT-központ állomásneve.</span><span class="sxs-lookup"><span data-stu-id="78652-136">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="78652-137">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="78652-137">-ProvisioningStatus</span></span>
<span data-ttu-id="78652-138">A regisztrációs bejegyzés engedélyezése vagy letiltása.</span><span class="sxs-lookup"><span data-stu-id="78652-138">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="78652-139">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="78652-139">-RegistrationId</span></span>
<span data-ttu-id="78652-140">Egyéni regisztrációs regisztrációs azonosító.</span><span class="sxs-lookup"><span data-stu-id="78652-140">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="78652-141">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="78652-141">-ReprovisionPolicy</span></span>
<span data-ttu-id="78652-142">A másik Iot-központba való újraépítéssel kezelni szükséges eszközadatok.</span><span class="sxs-lookup"><span data-stu-id="78652-142">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="78652-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78652-143">-ResourceGroupName</span></span>
<span data-ttu-id="78652-144">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="78652-144">Name of the Resource Group</span></span>

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

### <span data-ttu-id="78652-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78652-145">-ResourceId</span></span>
<span data-ttu-id="78652-146">IoT-eszköz kiépítési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="78652-146">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="78652-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="78652-147">-Tag</span></span>
<span data-ttu-id="78652-148">Kezdeti címkecímkék.</span><span class="sxs-lookup"><span data-stu-id="78652-148">Initial twin tags.</span></span>

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

### <span data-ttu-id="78652-149">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="78652-149">-WebhookUrl</span></span>
<span data-ttu-id="78652-150">Az egyéni hozzárendelési kérések webhook URL-címe.</span><span class="sxs-lookup"><span data-stu-id="78652-150">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="78652-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78652-151">-Confirm</span></span>
<span data-ttu-id="78652-152">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="78652-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78652-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78652-153">-WhatIf</span></span>
<span data-ttu-id="78652-154">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="78652-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78652-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="78652-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78652-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78652-156">CommonParameters</span></span>
<span data-ttu-id="78652-157">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78652-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78652-158">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78652-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78652-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78652-159">INPUTS</span></span>

### <span data-ttu-id="78652-160">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="78652-160">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="78652-161">System.String</span><span class="sxs-lookup"><span data-stu-id="78652-161">System.String</span></span>

## <span data-ttu-id="78652-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78652-162">OUTPUTS</span></span>

### <span data-ttu-id="78652-163">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="78652-163">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="78652-164">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="78652-164">NOTES</span></span>

## <span data-ttu-id="78652-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78652-165">RELATED LINKS</span></span>
