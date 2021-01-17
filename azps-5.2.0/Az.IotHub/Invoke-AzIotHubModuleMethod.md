---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmodulemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
ms.openlocfilehash: e9faa07f4addabcb556819e1d45b63a0dec0f6b3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342882"
---
# <span data-ttu-id="1084f-101">Invoke-AzIotHubModuleMethod</span><span class="sxs-lookup"><span data-stu-id="1084f-101">Invoke-AzIotHubModuleMethod</span></span>

## <span data-ttu-id="1084f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1084f-102">SYNOPSIS</span></span>
<span data-ttu-id="1084f-103">Edge-modul metódus meghívása</span><span class="sxs-lookup"><span data-stu-id="1084f-103">Invoke an Edge module method.</span></span>

## <span data-ttu-id="1084f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1084f-104">SYNTAX</span></span>

### <span data-ttu-id="1084f-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1084f-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId] <String> -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>]
 [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1084f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1084f-106">InputObjectSet</span></span>
```
Invoke-AzIotHubModuleMethod [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1084f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1084f-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1084f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1084f-108">DESCRIPTION</span></span>
<span data-ttu-id="1084f-109">Edge-modul metódus meghívása</span><span class="sxs-lookup"><span data-stu-id="1084f-109">Invoke an Edge module method.</span></span> <span data-ttu-id="1084f-110">További https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods információt itt is láthat.</span><span class="sxs-lookup"><span data-stu-id="1084f-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="1084f-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1084f-111">EXAMPLES</span></span>

### <span data-ttu-id="1084f-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="1084f-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubModuleMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Name "methodName" -Payload "method-input" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="1084f-113">Edge-modul metódus meghívása</span><span class="sxs-lookup"><span data-stu-id="1084f-113">Invoke an Edge module method.</span></span>

## <span data-ttu-id="1084f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1084f-114">PARAMETERS</span></span>

### <span data-ttu-id="1084f-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="1084f-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="1084f-116">A kapcsolat sikeres kapcsolódásáig várakozási másodpercek száma.</span><span class="sxs-lookup"><span data-stu-id="1084f-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="1084f-117">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="1084f-117">Default is 10.</span></span>

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

### <span data-ttu-id="1084f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1084f-118">-DefaultProfile</span></span>
<span data-ttu-id="1084f-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1084f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1084f-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="1084f-120">-DeviceId</span></span>
<span data-ttu-id="1084f-121">Céleszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1084f-121">Target Device Id.</span></span>

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

### <span data-ttu-id="1084f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1084f-122">-InputObject</span></span>
<span data-ttu-id="1084f-123">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="1084f-123">IotHub object</span></span>

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

### <span data-ttu-id="1084f-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="1084f-124">-IotHubName</span></span>
<span data-ttu-id="1084f-125">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="1084f-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1084f-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="1084f-126">-ModuleId</span></span>
<span data-ttu-id="1084f-127">A céleszköz modulazonosítója.</span><span class="sxs-lookup"><span data-stu-id="1084f-127">Target device's module id.</span></span>

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

### <span data-ttu-id="1084f-128">-Name</span><span class="sxs-lookup"><span data-stu-id="1084f-128">-Name</span></span>
<span data-ttu-id="1084f-129">Az eszközmodulon meghívni használt módszer neve.</span><span class="sxs-lookup"><span data-stu-id="1084f-129">The name of the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="1084f-130">-Hasznos terhelés</span><span class="sxs-lookup"><span data-stu-id="1084f-130">-Payload</span></span>
<span data-ttu-id="1084f-131">Az eszközmodulon meghívható metódus hasznos terhelése.</span><span class="sxs-lookup"><span data-stu-id="1084f-131">The payload for the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="1084f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1084f-132">-ResourceGroupName</span></span>
<span data-ttu-id="1084f-133">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="1084f-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1084f-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1084f-134">-ResourceId</span></span>
<span data-ttu-id="1084f-135">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="1084f-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1084f-136">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="1084f-136">-ResponseTimeOut</span></span>
<span data-ttu-id="1084f-137">A közvetlen módszertől kapott eredmény bekért várakozási másodpercek száma.</span><span class="sxs-lookup"><span data-stu-id="1084f-137">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="1084f-138">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="1084f-138">Default is 10.</span></span>

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

### <span data-ttu-id="1084f-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1084f-139">-Confirm</span></span>
<span data-ttu-id="1084f-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1084f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1084f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1084f-141">-WhatIf</span></span>
<span data-ttu-id="1084f-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1084f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1084f-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1084f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1084f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1084f-144">CommonParameters</span></span>
<span data-ttu-id="1084f-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1084f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1084f-146">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1084f-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1084f-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1084f-147">INPUTS</span></span>

### <span data-ttu-id="1084f-148">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1084f-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1084f-149">System.String</span><span class="sxs-lookup"><span data-stu-id="1084f-149">System.String</span></span>

## <span data-ttu-id="1084f-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1084f-150">OUTPUTS</span></span>

### <span data-ttu-id="1084f-151">Microsoft.Azure.Commands.Management.iotHub.Models.PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="1084f-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="1084f-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1084f-152">NOTES</span></span>

## <span data-ttu-id="1084f-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1084f-153">RELATED LINKS</span></span>
