---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: e7b0a5296147408633316ed27f0cba87a65d3a2a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024003"
---
# <span data-ttu-id="e85e6-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="e85e6-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="e85e6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e85e6-102">SYNOPSIS</span></span>
<span data-ttu-id="e85e6-103">Az eszközök tanúsítványigénylési csoportjának frissítése</span><span class="sxs-lookup"><span data-stu-id="e85e6-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="e85e6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e85e6-104">SYNTAX</span></span>

### <span data-ttu-id="e85e6-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e85e6-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e85e6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e85e6-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e85e6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e85e6-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e85e6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e85e6-108">DESCRIPTION</span></span>
<span data-ttu-id="e85e6-109">A tanúsítványigénylési csoport frissítése az Azure IoT hub eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="e85e6-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="e85e6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e85e6-110">EXAMPLES</span></span>

### <span data-ttu-id="e85e6-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e85e6-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="e85e6-112">A tanúsítványigénylési házirendek és hubok frissítése a tanúsítványigénylési csoportok számára.</span><span class="sxs-lookup"><span data-stu-id="e85e6-112">Update allocation policy and hubs for an enrollment group.</span></span>

## <span data-ttu-id="e85e6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e85e6-113">PARAMETERS</span></span>

### <span data-ttu-id="e85e6-114">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="e85e6-114">-AllocationPolicy</span></span>
<span data-ttu-id="e85e6-115">A hub-hoz rendelt eszközhöz tartozó kiosztás típusa.</span><span class="sxs-lookup"><span data-stu-id="e85e6-115">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="e85e6-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e85e6-116">-ApiVersion</span></span>
<span data-ttu-id="e85e6-117">A kiépítési szolgáltatás API-változata az egyéni hozzárendelés-kérésben.</span><span class="sxs-lookup"><span data-stu-id="e85e6-117">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="e85e6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e85e6-118">-DefaultProfile</span></span>
<span data-ttu-id="e85e6-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e85e6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e85e6-120">– Kívánt</span><span class="sxs-lookup"><span data-stu-id="e85e6-120">-Desired</span></span>
<span data-ttu-id="e85e6-121">Kezdeti dupla kívánt tulajdonságok.</span><span class="sxs-lookup"><span data-stu-id="e85e6-121">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="e85e6-122">-DpsName</span><span class="sxs-lookup"><span data-stu-id="e85e6-122">-DpsName</span></span>
<span data-ttu-id="e85e6-123">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="e85e6-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="e85e6-124">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="e85e6-124">-DpsObject</span></span>
<span data-ttu-id="e85e6-125">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="e85e6-125">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="e85e6-126">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="e85e6-126">-EdgeEnabled</span></span>
<span data-ttu-id="e85e6-127">Megjelölés az Edge engedélyezésével</span><span class="sxs-lookup"><span data-stu-id="e85e6-127">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="e85e6-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="e85e6-128">-IotHub</span></span>
<span data-ttu-id="e85e6-129">A cél IoT-hub állomásnevét tároló neve.</span><span class="sxs-lookup"><span data-stu-id="e85e6-129">Host name of target IoT Hub.</span></span>
<span data-ttu-id="e85e6-130">Szóközzel tagolt lista használata több IoT-hub esetében.</span><span class="sxs-lookup"><span data-stu-id="e85e6-130">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="e85e6-131">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="e85e6-131">-IotHubHostName</span></span>
<span data-ttu-id="e85e6-132">A cél IoT-hub állomásneve.</span><span class="sxs-lookup"><span data-stu-id="e85e6-132">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="e85e6-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e85e6-133">-Name</span></span>
<span data-ttu-id="e85e6-134">A beiratkozási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e85e6-134">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="e85e6-135">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="e85e6-135">-ProvisioningStatus</span></span>
<span data-ttu-id="e85e6-136">A beiratkozási bejegyzés engedélyezése és letiltása</span><span class="sxs-lookup"><span data-stu-id="e85e6-136">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="e85e6-137">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="e85e6-137">-ReprovisionPolicy</span></span>
<span data-ttu-id="e85e6-138">Az eszközöknek a különböző IOT-hub-ra való ismételt kiépítéshez való ismételt kiépítésekor kezelendő adatforgalom.</span><span class="sxs-lookup"><span data-stu-id="e85e6-138">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="e85e6-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e85e6-139">-ResourceGroupName</span></span>
<span data-ttu-id="e85e6-140">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e85e6-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e85e6-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e85e6-141">-ResourceId</span></span>
<span data-ttu-id="e85e6-142">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="e85e6-142">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="e85e6-143">-Címke</span><span class="sxs-lookup"><span data-stu-id="e85e6-143">-Tag</span></span>
<span data-ttu-id="e85e6-144">Első Twin-Címkék</span><span class="sxs-lookup"><span data-stu-id="e85e6-144">Initial twin tags.</span></span>

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

### <span data-ttu-id="e85e6-145">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="e85e6-145">-WebhookUrl</span></span>
<span data-ttu-id="e85e6-146">Az egyéni hozzárendelés-kérelmekhez használt webhorog URL-címe.</span><span class="sxs-lookup"><span data-stu-id="e85e6-146">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="e85e6-147">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e85e6-147">-Confirm</span></span>
<span data-ttu-id="e85e6-148">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e85e6-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e85e6-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e85e6-149">-WhatIf</span></span>
<span data-ttu-id="e85e6-150">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e85e6-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e85e6-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e85e6-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e85e6-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e85e6-152">CommonParameters</span></span>
<span data-ttu-id="e85e6-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e85e6-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e85e6-154">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e85e6-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e85e6-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e85e6-155">INPUTS</span></span>

### <span data-ttu-id="e85e6-156">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="e85e6-156">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="e85e6-157">System. String</span><span class="sxs-lookup"><span data-stu-id="e85e6-157">System.String</span></span>

## <span data-ttu-id="e85e6-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e85e6-158">OUTPUTS</span></span>

### <span data-ttu-id="e85e6-159">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="e85e6-159">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="e85e6-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e85e6-160">NOTES</span></span>

## <span data-ttu-id="e85e6-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e85e6-161">RELATED LINKS</span></span>
