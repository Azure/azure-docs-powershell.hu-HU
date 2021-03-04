---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubdevicemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
ms.openlocfilehash: 4c3782496041be7328ede29fad5ab3818791a0be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924089"
---
# <span data-ttu-id="8c6fd-101">Invoke-AzIotHubDeviceMethod</span><span class="sxs-lookup"><span data-stu-id="8c6fd-101">Invoke-AzIotHubDeviceMethod</span></span>

## <span data-ttu-id="8c6fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c6fd-102">SYNOPSIS</span></span>
<span data-ttu-id="8c6fd-103">Közvetlen metódus meghívása egy eszközön.</span><span class="sxs-lookup"><span data-stu-id="8c6fd-103">Invoke a direct method on a device.</span></span>

## <span data-ttu-id="8c6fd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8c6fd-104">SYNTAX</span></span>

### <span data-ttu-id="8c6fd-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8c6fd-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c6fd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8c6fd-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-InputObject] <PSIotHub> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c6fd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8c6fd-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceId] <String> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c6fd-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8c6fd-108">DESCRIPTION</span></span>
<span data-ttu-id="8c6fd-109">Közvetlen metódus meghívása egy eszközön.</span><span class="sxs-lookup"><span data-stu-id="8c6fd-109">Invoke a direct method on a device.</span></span> <span data-ttu-id="8c6fd-110">További https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods információt itt is láthat.</span><span class="sxs-lookup"><span data-stu-id="8c6fd-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="8c6fd-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8c6fd-111">EXAMPLES</span></span>

### <span data-ttu-id="8c6fd-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="8c6fd-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeviceMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Name "methodName" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="8c6fd-113">Eszközmódszer meghívása.</span><span class="sxs-lookup"><span data-stu-id="8c6fd-113">Invoke a device method.</span></span>

## <span data-ttu-id="8c6fd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c6fd-114">PARAMETERS</span></span>

### <span data-ttu-id="8c6fd-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="8c6fd-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="8c6fd-116">A kapcsolat sikeres kapcsolódásáig várakozási másodpercek száma.</span><span class="sxs-lookup"><span data-stu-id="8c6fd-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="8c6fd-117">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="8c6fd-117">Default is 10.</span></span>

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

### <span data-ttu-id="8c6fd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c6fd-118">-DefaultProfile</span></span>
<span data-ttu-id="8c6fd-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8c6fd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c6fd-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="8c6fd-120">-DeviceId</span></span>
<span data-ttu-id="8c6fd-121">Céleszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8c6fd-121">Target Device Id.</span></span>

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

### <span data-ttu-id="8c6fd-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c6fd-122">-InputObject</span></span>
<span data-ttu-id="8c6fd-123">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="8c6fd-123">IotHub object</span></span>

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

### <span data-ttu-id="8c6fd-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="8c6fd-124">-IotHubName</span></span>
<span data-ttu-id="8c6fd-125">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="8c6fd-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8c6fd-126">-Name</span><span class="sxs-lookup"><span data-stu-id="8c6fd-126">-Name</span></span>
<span data-ttu-id="8c6fd-127">Az eszközön meghívni használt módszer neve.</span><span class="sxs-lookup"><span data-stu-id="8c6fd-127">The name of the method to invoke on this device.</span></span>

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

### <span data-ttu-id="8c6fd-128">-Hasznos terhelés</span><span class="sxs-lookup"><span data-stu-id="8c6fd-128">-Payload</span></span>
<span data-ttu-id="8c6fd-129">Az eszközön meghívható módszer hasznos terhelése.</span><span class="sxs-lookup"><span data-stu-id="8c6fd-129">The payload for the method to invoke on this device.</span></span>

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

### <span data-ttu-id="8c6fd-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c6fd-130">-ResourceGroupName</span></span>
<span data-ttu-id="8c6fd-131">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="8c6fd-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8c6fd-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c6fd-132">-ResourceId</span></span>
<span data-ttu-id="8c6fd-133">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="8c6fd-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8c6fd-134">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="8c6fd-134">-ResponseTimeOut</span></span>
<span data-ttu-id="8c6fd-135">A közvetlen módszertől kapott eredmény bekért várakozási másodpercek száma.</span><span class="sxs-lookup"><span data-stu-id="8c6fd-135">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="8c6fd-136">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="8c6fd-136">Default is 10.</span></span>

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

### <span data-ttu-id="8c6fd-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c6fd-137">-Confirm</span></span>
<span data-ttu-id="8c6fd-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8c6fd-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c6fd-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c6fd-139">-WhatIf</span></span>
<span data-ttu-id="8c6fd-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8c6fd-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c6fd-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8c6fd-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c6fd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c6fd-142">CommonParameters</span></span>
<span data-ttu-id="8c6fd-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c6fd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c6fd-144">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c6fd-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c6fd-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c6fd-145">INPUTS</span></span>

### <span data-ttu-id="8c6fd-146">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8c6fd-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8c6fd-147">System.String</span><span class="sxs-lookup"><span data-stu-id="8c6fd-147">System.String</span></span>

## <span data-ttu-id="8c6fd-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c6fd-148">OUTPUTS</span></span>

### <span data-ttu-id="8c6fd-149">Microsoft.Azure.Commands.Management.iotHub.Models.PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="8c6fd-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="8c6fd-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8c6fd-150">NOTES</span></span>

## <span data-ttu-id="8c6fd-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c6fd-151">RELATED LINKS</span></span>
