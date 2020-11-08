---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: f8a81df2081420f8d218e094ff43f22e8dd9cc5c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185492"
---
# <span data-ttu-id="df0b5-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="df0b5-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="df0b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df0b5-102">SYNOPSIS</span></span>
<span data-ttu-id="df0b5-103">Eszköz-beiktatási rekord frissítése</span><span class="sxs-lookup"><span data-stu-id="df0b5-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="df0b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df0b5-104">SYNTAX</span></span>

### <span data-ttu-id="df0b5-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="df0b5-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df0b5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="df0b5-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df0b5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="df0b5-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df0b5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="df0b5-108">DESCRIPTION</span></span>
<span data-ttu-id="df0b5-109">Eszköz-igénylés frissítése az Azure IoT hub eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="df0b5-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="df0b5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="df0b5-110">EXAMPLES</span></span>

### <span data-ttu-id="df0b5-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="df0b5-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="df0b5-112">Adatelosztási házirend és hubok frissítése a tanúsítványigénylési rekordokhoz.</span><span class="sxs-lookup"><span data-stu-id="df0b5-112">Update allocation policy and hubs for an enrollment record.</span></span>

## <span data-ttu-id="df0b5-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df0b5-113">PARAMETERS</span></span>

### <span data-ttu-id="df0b5-114">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="df0b5-114">-AllocationPolicy</span></span>
<span data-ttu-id="df0b5-115">A hub-hoz rendelt eszközhöz tartozó kiosztás típusa.</span><span class="sxs-lookup"><span data-stu-id="df0b5-115">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="df0b5-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="df0b5-116">-ApiVersion</span></span>
<span data-ttu-id="df0b5-117">A kiépítési szolgáltatás API-változata az egyéni hozzárendelés-kérésben.</span><span class="sxs-lookup"><span data-stu-id="df0b5-117">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="df0b5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df0b5-118">-DefaultProfile</span></span>
<span data-ttu-id="df0b5-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df0b5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df0b5-120">– Kívánt</span><span class="sxs-lookup"><span data-stu-id="df0b5-120">-Desired</span></span>
<span data-ttu-id="df0b5-121">Kezdeti dupla kívánt tulajdonságok.</span><span class="sxs-lookup"><span data-stu-id="df0b5-121">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="df0b5-122">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="df0b5-122">-DeviceId</span></span>
<span data-ttu-id="df0b5-123">IoT hub-eszköz azonosítója</span><span class="sxs-lookup"><span data-stu-id="df0b5-123">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="df0b5-124">-DpsName</span><span class="sxs-lookup"><span data-stu-id="df0b5-124">-DpsName</span></span>
<span data-ttu-id="df0b5-125">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="df0b5-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="df0b5-126">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="df0b5-126">-DpsObject</span></span>
<span data-ttu-id="df0b5-127">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="df0b5-127">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="df0b5-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="df0b5-128">-EdgeEnabled</span></span>
<span data-ttu-id="df0b5-129">Megjelölés az Edge engedélyezésével</span><span class="sxs-lookup"><span data-stu-id="df0b5-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="df0b5-130">-IotHub</span><span class="sxs-lookup"><span data-stu-id="df0b5-130">-IotHub</span></span>
<span data-ttu-id="df0b5-131">A cél IoT-hub állomásnevét tároló neve.</span><span class="sxs-lookup"><span data-stu-id="df0b5-131">Host name of target IoT Hub.</span></span>
<span data-ttu-id="df0b5-132">Szóközzel tagolt lista használata több IoT-hub esetében.</span><span class="sxs-lookup"><span data-stu-id="df0b5-132">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="df0b5-133">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="df0b5-133">-IotHubHostName</span></span>
<span data-ttu-id="df0b5-134">A cél IoT-hub állomásneve.</span><span class="sxs-lookup"><span data-stu-id="df0b5-134">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="df0b5-135">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="df0b5-135">-ProvisioningStatus</span></span>
<span data-ttu-id="df0b5-136">A beiratkozási bejegyzés engedélyezése és letiltása</span><span class="sxs-lookup"><span data-stu-id="df0b5-136">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="df0b5-137">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="df0b5-137">-RegistrationId</span></span>
<span data-ttu-id="df0b5-138">Egyéni beiratkozási regisztrációs azonosító</span><span class="sxs-lookup"><span data-stu-id="df0b5-138">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="df0b5-139">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="df0b5-139">-ReprovisionPolicy</span></span>
<span data-ttu-id="df0b5-140">Az eszközöknek a különböző IOT-hub-ra való ismételt kiépítéshez való ismételt kiépítésekor kezelendő adatforgalom.</span><span class="sxs-lookup"><span data-stu-id="df0b5-140">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="df0b5-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df0b5-141">-ResourceGroupName</span></span>
<span data-ttu-id="df0b5-142">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="df0b5-142">Name of the Resource Group</span></span>

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

### <span data-ttu-id="df0b5-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df0b5-143">-ResourceId</span></span>
<span data-ttu-id="df0b5-144">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="df0b5-144">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="df0b5-145">-Címke</span><span class="sxs-lookup"><span data-stu-id="df0b5-145">-Tag</span></span>
<span data-ttu-id="df0b5-146">Első Twin-Címkék</span><span class="sxs-lookup"><span data-stu-id="df0b5-146">Initial twin tags.</span></span>

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

### <span data-ttu-id="df0b5-147">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="df0b5-147">-WebhookUrl</span></span>
<span data-ttu-id="df0b5-148">Az egyéni hozzárendelés-kérelmekhez használt webhorog URL-címe.</span><span class="sxs-lookup"><span data-stu-id="df0b5-148">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="df0b5-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="df0b5-149">-Confirm</span></span>
<span data-ttu-id="df0b5-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="df0b5-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df0b5-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df0b5-151">-WhatIf</span></span>
<span data-ttu-id="df0b5-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="df0b5-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df0b5-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="df0b5-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df0b5-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df0b5-154">CommonParameters</span></span>
<span data-ttu-id="df0b5-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df0b5-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df0b5-156">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df0b5-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df0b5-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df0b5-157">INPUTS</span></span>

### <span data-ttu-id="df0b5-158">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="df0b5-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="df0b5-159">System. String</span><span class="sxs-lookup"><span data-stu-id="df0b5-159">System.String</span></span>

## <span data-ttu-id="df0b5-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df0b5-160">OUTPUTS</span></span>

### <span data-ttu-id="df0b5-161">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="df0b5-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="df0b5-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df0b5-162">NOTES</span></span>

## <span data-ttu-id="df0b5-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df0b5-163">RELATED LINKS</span></span>
