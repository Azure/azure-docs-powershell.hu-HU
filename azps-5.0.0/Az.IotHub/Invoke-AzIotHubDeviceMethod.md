---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdevicemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
ms.openlocfilehash: 78247b26d2f8e6618d3999389efa509e3f8854b9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195975"
---
# <span data-ttu-id="c8917-101">Invoke-AzIotHubDeviceMethod</span><span class="sxs-lookup"><span data-stu-id="c8917-101">Invoke-AzIotHubDeviceMethod</span></span>

## <span data-ttu-id="c8917-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c8917-102">SYNOPSIS</span></span>
<span data-ttu-id="c8917-103">Közvetlen módszer meghívása egy eszközön.</span><span class="sxs-lookup"><span data-stu-id="c8917-103">Invoke a direct method on a device.</span></span>

## <span data-ttu-id="c8917-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c8917-104">SYNTAX</span></span>

### <span data-ttu-id="c8917-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c8917-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8917-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c8917-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-InputObject] <PSIotHub> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8917-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c8917-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceId] <String> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8917-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c8917-108">DESCRIPTION</span></span>
<span data-ttu-id="c8917-109">Közvetlen módszer meghívása egy eszközön.</span><span class="sxs-lookup"><span data-stu-id="c8917-109">Invoke a direct method on a device.</span></span> <span data-ttu-id="c8917-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methodsTovábbi információt itt talál.</span><span class="sxs-lookup"><span data-stu-id="c8917-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="c8917-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c8917-111">EXAMPLES</span></span>

### <span data-ttu-id="c8917-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c8917-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeviceMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Name "methodName" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="c8917-113">Eszköz metódusának meghívása</span><span class="sxs-lookup"><span data-stu-id="c8917-113">Invoke a device method.</span></span>

## <span data-ttu-id="c8917-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c8917-114">PARAMETERS</span></span>

### <span data-ttu-id="c8917-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="c8917-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="c8917-116">A kapcsolat sikeres létrejöttének megvárni kívánt másodpercek száma.</span><span class="sxs-lookup"><span data-stu-id="c8917-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="c8917-117">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="c8917-117">Default is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8917-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8917-118">-DefaultProfile</span></span>
<span data-ttu-id="c8917-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c8917-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8917-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="c8917-120">-DeviceId</span></span>
<span data-ttu-id="c8917-121">Céleszköz-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c8917-121">Target Device Id.</span></span>

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

### <span data-ttu-id="c8917-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8917-122">-InputObject</span></span>
<span data-ttu-id="c8917-123">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="c8917-123">IotHub object</span></span>

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

### <span data-ttu-id="c8917-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="c8917-124">-IotHubName</span></span>
<span data-ttu-id="c8917-125">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="c8917-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c8917-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c8917-126">-Name</span></span>
<span data-ttu-id="c8917-127">Annak a módszernek a neve, amelyre hivatkozni szeretne az eszközön.</span><span class="sxs-lookup"><span data-stu-id="c8917-127">The name of the method to invoke on this device.</span></span>

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

### <span data-ttu-id="c8917-128">-Hasznos teher</span><span class="sxs-lookup"><span data-stu-id="c8917-128">-Payload</span></span>
<span data-ttu-id="c8917-129">Az eszközre való hivatkozáshoz használt módszer tartalma.</span><span class="sxs-lookup"><span data-stu-id="c8917-129">The payload for the method to invoke on this device.</span></span>

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

### <span data-ttu-id="c8917-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8917-130">-ResourceGroupName</span></span>
<span data-ttu-id="c8917-131">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c8917-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c8917-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8917-132">-ResourceId</span></span>
<span data-ttu-id="c8917-133">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="c8917-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c8917-134">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="c8917-134">-ResponseTimeOut</span></span>
<span data-ttu-id="c8917-135">Annak a másodpercnek a száma, ameddig az eredmény a közvetlen módszerrel érkezik.</span><span class="sxs-lookup"><span data-stu-id="c8917-135">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="c8917-136">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="c8917-136">Default is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8917-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c8917-137">-Confirm</span></span>
<span data-ttu-id="c8917-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c8917-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8917-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8917-139">-WhatIf</span></span>
<span data-ttu-id="c8917-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c8917-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8917-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c8917-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8917-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8917-142">CommonParameters</span></span>
<span data-ttu-id="c8917-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c8917-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8917-144">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8917-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8917-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8917-145">INPUTS</span></span>

### <span data-ttu-id="c8917-146">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c8917-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c8917-147">System. String</span><span class="sxs-lookup"><span data-stu-id="c8917-147">System.String</span></span>

## <span data-ttu-id="c8917-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8917-148">OUTPUTS</span></span>

### <span data-ttu-id="c8917-149">Microsoft. Azure. Command. Management. IotHub. models. PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="c8917-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="c8917-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c8917-150">NOTES</span></span>

## <span data-ttu-id="c8917-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8917-151">RELATED LINKS</span></span>
