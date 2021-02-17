---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmodulemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
ms.openlocfilehash: e9faa07f4addabcb556819e1d45b63a0dec0f6b3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147803"
---
# <span data-ttu-id="6e060-101">Invoke-AzIotHubModuleMethod</span><span class="sxs-lookup"><span data-stu-id="6e060-101">Invoke-AzIotHubModuleMethod</span></span>

## <span data-ttu-id="6e060-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e060-102">SYNOPSIS</span></span>
<span data-ttu-id="6e060-103">Edge-modul metódus meghívása</span><span class="sxs-lookup"><span data-stu-id="6e060-103">Invoke an Edge module method.</span></span>

## <span data-ttu-id="6e060-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6e060-104">SYNTAX</span></span>

### <span data-ttu-id="6e060-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6e060-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId] <String> -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>]
 [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e060-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6e060-106">InputObjectSet</span></span>
```
Invoke-AzIotHubModuleMethod [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e060-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6e060-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e060-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6e060-108">DESCRIPTION</span></span>
<span data-ttu-id="6e060-109">Edge-modul metódus meghívása</span><span class="sxs-lookup"><span data-stu-id="6e060-109">Invoke an Edge module method.</span></span> <span data-ttu-id="6e060-110">További https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods információt itt is láthat.</span><span class="sxs-lookup"><span data-stu-id="6e060-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="6e060-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6e060-111">EXAMPLES</span></span>

### <span data-ttu-id="6e060-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="6e060-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubModuleMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Name "methodName" -Payload "method-input" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="6e060-113">Edge-modul metódus meghívása</span><span class="sxs-lookup"><span data-stu-id="6e060-113">Invoke an Edge module method.</span></span>

## <span data-ttu-id="6e060-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e060-114">PARAMETERS</span></span>

### <span data-ttu-id="6e060-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="6e060-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="6e060-116">A kapcsolat sikeres kapcsolódásáig várakozási másodpercek száma.</span><span class="sxs-lookup"><span data-stu-id="6e060-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="6e060-117">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="6e060-117">Default is 10.</span></span>

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

### <span data-ttu-id="6e060-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e060-118">-DefaultProfile</span></span>
<span data-ttu-id="6e060-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6e060-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e060-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="6e060-120">-DeviceId</span></span>
<span data-ttu-id="6e060-121">Céleszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6e060-121">Target Device Id.</span></span>

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

### <span data-ttu-id="6e060-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e060-122">-InputObject</span></span>
<span data-ttu-id="6e060-123">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="6e060-123">IotHub object</span></span>

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

### <span data-ttu-id="6e060-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="6e060-124">-IotHubName</span></span>
<span data-ttu-id="6e060-125">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="6e060-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6e060-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="6e060-126">-ModuleId</span></span>
<span data-ttu-id="6e060-127">A céleszköz modulazonosítója.</span><span class="sxs-lookup"><span data-stu-id="6e060-127">Target device's module id.</span></span>

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

### <span data-ttu-id="6e060-128">-Name</span><span class="sxs-lookup"><span data-stu-id="6e060-128">-Name</span></span>
<span data-ttu-id="6e060-129">Az eszközmodulon meghívni használt módszer neve.</span><span class="sxs-lookup"><span data-stu-id="6e060-129">The name of the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="6e060-130">-Hasznos terhelés</span><span class="sxs-lookup"><span data-stu-id="6e060-130">-Payload</span></span>
<span data-ttu-id="6e060-131">Az eszközmodulon meghívni használt módszer hasznos terhelése.</span><span class="sxs-lookup"><span data-stu-id="6e060-131">The payload for the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="6e060-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e060-132">-ResourceGroupName</span></span>
<span data-ttu-id="6e060-133">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="6e060-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6e060-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e060-134">-ResourceId</span></span>
<span data-ttu-id="6e060-135">IotHub erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="6e060-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6e060-136">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="6e060-136">-ResponseTimeOut</span></span>
<span data-ttu-id="6e060-137">A közvetlen módszertől kapott eredmény bekért várakozási másodpercek száma.</span><span class="sxs-lookup"><span data-stu-id="6e060-137">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="6e060-138">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="6e060-138">Default is 10.</span></span>

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

### <span data-ttu-id="6e060-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e060-139">-Confirm</span></span>
<span data-ttu-id="6e060-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6e060-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e060-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e060-141">-WhatIf</span></span>
<span data-ttu-id="6e060-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6e060-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e060-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6e060-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e060-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e060-144">CommonParameters</span></span>
<span data-ttu-id="6e060-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e060-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e060-146">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e060-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e060-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e060-147">INPUTS</span></span>

### <span data-ttu-id="6e060-148">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6e060-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6e060-149">System.String</span><span class="sxs-lookup"><span data-stu-id="6e060-149">System.String</span></span>

## <span data-ttu-id="6e060-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e060-150">OUTPUTS</span></span>

### <span data-ttu-id="6e060-151">Microsoft.Azure.Commands.Management.iotHub.Models.PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="6e060-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="6e060-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6e060-152">NOTES</span></span>

## <span data-ttu-id="6e060-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e060-153">RELATED LINKS</span></span>
