---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdevicemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
ms.openlocfilehash: 78247b26d2f8e6618d3999389efa509e3f8854b9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322149"
---
# <span data-ttu-id="8312a-101">Invoke-AzIotHubDeviceMethod</span><span class="sxs-lookup"><span data-stu-id="8312a-101">Invoke-AzIotHubDeviceMethod</span></span>

## <span data-ttu-id="8312a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8312a-102">SYNOPSIS</span></span>
<span data-ttu-id="8312a-103">Közvetlen metódus meghívása egy eszközön.</span><span class="sxs-lookup"><span data-stu-id="8312a-103">Invoke a direct method on a device.</span></span>

## <span data-ttu-id="8312a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8312a-104">SYNTAX</span></span>

### <span data-ttu-id="8312a-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8312a-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8312a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8312a-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-InputObject] <PSIotHub> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8312a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8312a-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceId] <String> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8312a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8312a-108">DESCRIPTION</span></span>
<span data-ttu-id="8312a-109">Közvetlen metódus meghívása egy eszközön.</span><span class="sxs-lookup"><span data-stu-id="8312a-109">Invoke a direct method on a device.</span></span> <span data-ttu-id="8312a-110">További https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods információt itt is láthat.</span><span class="sxs-lookup"><span data-stu-id="8312a-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="8312a-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8312a-111">EXAMPLES</span></span>

### <span data-ttu-id="8312a-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="8312a-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeviceMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Name "methodName" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="8312a-113">Eszközmódszer meghívása.</span><span class="sxs-lookup"><span data-stu-id="8312a-113">Invoke a device method.</span></span>

## <span data-ttu-id="8312a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8312a-114">PARAMETERS</span></span>

### <span data-ttu-id="8312a-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="8312a-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="8312a-116">A kapcsolat sikeres kapcsolódásáig várakozási másodpercek száma.</span><span class="sxs-lookup"><span data-stu-id="8312a-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="8312a-117">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="8312a-117">Default is 10.</span></span>

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

### <span data-ttu-id="8312a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8312a-118">-DefaultProfile</span></span>
<span data-ttu-id="8312a-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8312a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8312a-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="8312a-120">-DeviceId</span></span>
<span data-ttu-id="8312a-121">Céleszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8312a-121">Target Device Id.</span></span>

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

### <span data-ttu-id="8312a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8312a-122">-InputObject</span></span>
<span data-ttu-id="8312a-123">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="8312a-123">IotHub object</span></span>

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

### <span data-ttu-id="8312a-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="8312a-124">-IotHubName</span></span>
<span data-ttu-id="8312a-125">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="8312a-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8312a-126">-Name</span><span class="sxs-lookup"><span data-stu-id="8312a-126">-Name</span></span>
<span data-ttu-id="8312a-127">Az eszközön meghívni használt módszer neve.</span><span class="sxs-lookup"><span data-stu-id="8312a-127">The name of the method to invoke on this device.</span></span>

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

### <span data-ttu-id="8312a-128">-Hasznos terhelés</span><span class="sxs-lookup"><span data-stu-id="8312a-128">-Payload</span></span>
<span data-ttu-id="8312a-129">Az eszközön meghívható módszer hasznos terhelése.</span><span class="sxs-lookup"><span data-stu-id="8312a-129">The payload for the method to invoke on this device.</span></span>

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

### <span data-ttu-id="8312a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8312a-130">-ResourceGroupName</span></span>
<span data-ttu-id="8312a-131">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="8312a-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8312a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8312a-132">-ResourceId</span></span>
<span data-ttu-id="8312a-133">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="8312a-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8312a-134">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="8312a-134">-ResponseTimeOut</span></span>
<span data-ttu-id="8312a-135">A közvetlen módszer eredményének bekérte várakozási másodpercek száma.</span><span class="sxs-lookup"><span data-stu-id="8312a-135">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="8312a-136">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="8312a-136">Default is 10.</span></span>

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

### <span data-ttu-id="8312a-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8312a-137">-Confirm</span></span>
<span data-ttu-id="8312a-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8312a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8312a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8312a-139">-WhatIf</span></span>
<span data-ttu-id="8312a-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8312a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8312a-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8312a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8312a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8312a-142">CommonParameters</span></span>
<span data-ttu-id="8312a-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8312a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8312a-144">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8312a-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8312a-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8312a-145">INPUTS</span></span>

### <span data-ttu-id="8312a-146">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8312a-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8312a-147">System.String</span><span class="sxs-lookup"><span data-stu-id="8312a-147">System.String</span></span>

## <span data-ttu-id="8312a-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8312a-148">OUTPUTS</span></span>

### <span data-ttu-id="8312a-149">Microsoft.Azure.Commands.Management.iotHub.Models.PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="8312a-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="8312a-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8312a-150">NOTES</span></span>

## <span data-ttu-id="8312a-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8312a-151">RELATED LINKS</span></span>
