---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmodulemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
ms.openlocfilehash: e9faa07f4addabcb556819e1d45b63a0dec0f6b3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195970"
---
# <span data-ttu-id="a2364-101">Invoke-AzIotHubModuleMethod</span><span class="sxs-lookup"><span data-stu-id="a2364-101">Invoke-AzIotHubModuleMethod</span></span>

## <span data-ttu-id="a2364-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2364-102">SYNOPSIS</span></span>
<span data-ttu-id="a2364-103">Az Edge modul metódusának meghívása</span><span class="sxs-lookup"><span data-stu-id="a2364-103">Invoke an Edge module method.</span></span>

## <span data-ttu-id="a2364-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2364-104">SYNTAX</span></span>

### <span data-ttu-id="a2364-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a2364-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId] <String> -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>]
 [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2364-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a2364-106">InputObjectSet</span></span>
```
Invoke-AzIotHubModuleMethod [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2364-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a2364-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2364-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2364-108">DESCRIPTION</span></span>
<span data-ttu-id="a2364-109">Az Edge modul metódusának meghívása</span><span class="sxs-lookup"><span data-stu-id="a2364-109">Invoke an Edge module method.</span></span> <span data-ttu-id="a2364-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methodsTovábbi információt itt talál.</span><span class="sxs-lookup"><span data-stu-id="a2364-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="a2364-111">Példák</span><span class="sxs-lookup"><span data-stu-id="a2364-111">EXAMPLES</span></span>

### <span data-ttu-id="a2364-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a2364-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubModuleMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Name "methodName" -Payload "method-input" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="a2364-113">Az Edge modul metódusának meghívása</span><span class="sxs-lookup"><span data-stu-id="a2364-113">Invoke an Edge module method.</span></span>

## <span data-ttu-id="a2364-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2364-114">PARAMETERS</span></span>

### <span data-ttu-id="a2364-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="a2364-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="a2364-116">A kapcsolat sikeres létrejöttének megvárni kívánt másodpercek száma.</span><span class="sxs-lookup"><span data-stu-id="a2364-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="a2364-117">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="a2364-117">Default is 10.</span></span>

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

### <span data-ttu-id="a2364-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2364-118">-DefaultProfile</span></span>
<span data-ttu-id="a2364-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2364-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2364-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="a2364-120">-DeviceId</span></span>
<span data-ttu-id="a2364-121">Céleszköz-azonosító.</span><span class="sxs-lookup"><span data-stu-id="a2364-121">Target Device Id.</span></span>

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

### <span data-ttu-id="a2364-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2364-122">-InputObject</span></span>
<span data-ttu-id="a2364-123">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="a2364-123">IotHub object</span></span>

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

### <span data-ttu-id="a2364-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a2364-124">-IotHubName</span></span>
<span data-ttu-id="a2364-125">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="a2364-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a2364-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="a2364-126">-ModuleId</span></span>
<span data-ttu-id="a2364-127">A céleszköz modul azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a2364-127">Target device's module id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2364-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a2364-128">-Name</span></span>
<span data-ttu-id="a2364-129">Annak a módszernek a neve, amelyre hivatkozni kell az eszköz modulban.</span><span class="sxs-lookup"><span data-stu-id="a2364-129">The name of the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="a2364-130">-Hasznos teher</span><span class="sxs-lookup"><span data-stu-id="a2364-130">-Payload</span></span>
<span data-ttu-id="a2364-131">Annak a módszernek a hasznos tartalma, amellyel az eszköz modult meg lehet hívni.</span><span class="sxs-lookup"><span data-stu-id="a2364-131">The payload for the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="a2364-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2364-132">-ResourceGroupName</span></span>
<span data-ttu-id="a2364-133">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a2364-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a2364-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2364-134">-ResourceId</span></span>
<span data-ttu-id="a2364-135">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="a2364-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a2364-136">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="a2364-136">-ResponseTimeOut</span></span>
<span data-ttu-id="a2364-137">Annak a másodpercnek a száma, ameddig az eredmény a közvetlen módszerrel érkezik.</span><span class="sxs-lookup"><span data-stu-id="a2364-137">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="a2364-138">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="a2364-138">Default is 10.</span></span>

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

### <span data-ttu-id="a2364-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a2364-139">-Confirm</span></span>
<span data-ttu-id="a2364-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a2364-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2364-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2364-141">-WhatIf</span></span>
<span data-ttu-id="a2364-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a2364-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2364-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a2364-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2364-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2364-144">CommonParameters</span></span>
<span data-ttu-id="a2364-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2364-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2364-146">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2364-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2364-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2364-147">INPUTS</span></span>

### <span data-ttu-id="a2364-148">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a2364-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a2364-149">System. String</span><span class="sxs-lookup"><span data-stu-id="a2364-149">System.String</span></span>

## <span data-ttu-id="a2364-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2364-150">OUTPUTS</span></span>

### <span data-ttu-id="a2364-151">Microsoft. Azure. Command. Management. IotHub. models. PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="a2364-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="a2364-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2364-152">NOTES</span></span>

## <span data-ttu-id="a2364-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2364-153">RELATED LINKS</span></span>
