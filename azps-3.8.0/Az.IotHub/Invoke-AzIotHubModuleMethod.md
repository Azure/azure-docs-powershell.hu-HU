---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmodulemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
ms.openlocfilehash: 818e973d4d7be9fb03e23a23d7264745920f843f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013819"
---
# <span data-ttu-id="2e559-101">Invoke-AzIotHubModuleMethod</span><span class="sxs-lookup"><span data-stu-id="2e559-101">Invoke-AzIotHubModuleMethod</span></span>

## <span data-ttu-id="2e559-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e559-102">SYNOPSIS</span></span>
<span data-ttu-id="2e559-103">Az Edge modul metódusának meghívása</span><span class="sxs-lookup"><span data-stu-id="2e559-103">Invoke an Edge module method.</span></span>

## <span data-ttu-id="2e559-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e559-104">SYNTAX</span></span>

### <span data-ttu-id="2e559-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2e559-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId] <String> -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>]
 [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e559-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2e559-106">InputObjectSet</span></span>
```
Invoke-AzIotHubModuleMethod [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e559-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2e559-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e559-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e559-108">DESCRIPTION</span></span>
<span data-ttu-id="2e559-109">Az Edge modul metódusának meghívása</span><span class="sxs-lookup"><span data-stu-id="2e559-109">Invoke an Edge module method.</span></span> <span data-ttu-id="2e559-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methodsTovábbi információt itt talál.</span><span class="sxs-lookup"><span data-stu-id="2e559-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="2e559-111">Példák</span><span class="sxs-lookup"><span data-stu-id="2e559-111">EXAMPLES</span></span>

### <span data-ttu-id="2e559-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2e559-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubModuleMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Name "methodName" -Payload "method-input" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="2e559-113">Az Edge modul metódusának meghívása</span><span class="sxs-lookup"><span data-stu-id="2e559-113">Invoke an Edge module method.</span></span>

## <span data-ttu-id="2e559-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e559-114">PARAMETERS</span></span>

### <span data-ttu-id="2e559-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="2e559-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="2e559-116">A kapcsolat sikeres létrejöttének megvárni kívánt másodpercek száma.</span><span class="sxs-lookup"><span data-stu-id="2e559-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="2e559-117">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="2e559-117">Default is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e559-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e559-118">-DefaultProfile</span></span>
<span data-ttu-id="2e559-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e559-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e559-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="2e559-120">-DeviceId</span></span>
<span data-ttu-id="2e559-121">Céleszköz-azonosító.</span><span class="sxs-lookup"><span data-stu-id="2e559-121">Target Device Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e559-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e559-122">-InputObject</span></span>
<span data-ttu-id="2e559-123">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="2e559-123">IotHub object</span></span>

```yaml
Type: PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e559-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="2e559-124">-IotHubName</span></span>
<span data-ttu-id="2e559-125">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="2e559-125">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e559-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="2e559-126">-ModuleId</span></span>
<span data-ttu-id="2e559-127">A céleszköz modul azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2e559-127">Target device's module id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e559-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2e559-128">-Name</span></span>
<span data-ttu-id="2e559-129">Annak a módszernek a neve, amelyre hivatkozni kell az eszköz modulban.</span><span class="sxs-lookup"><span data-stu-id="2e559-129">The name of the method to invoke on this device module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e559-130">-Hasznos teher</span><span class="sxs-lookup"><span data-stu-id="2e559-130">-Payload</span></span>
<span data-ttu-id="2e559-131">Annak a módszernek a hasznos tartalma, amellyel az eszköz modult meg lehet hívni.</span><span class="sxs-lookup"><span data-stu-id="2e559-131">The payload for the method to invoke on this device module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e559-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e559-132">-ResourceGroupName</span></span>
<span data-ttu-id="2e559-133">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="2e559-133">Name of the Resource Group</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e559-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e559-134">-ResourceId</span></span>
<span data-ttu-id="2e559-135">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="2e559-135">IotHub Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e559-136">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="2e559-136">-ResponseTimeOut</span></span>
<span data-ttu-id="2e559-137">Annak a másodpercnek a száma, ameddig az eredmény a közvetlen módszerrel érkezik.</span><span class="sxs-lookup"><span data-stu-id="2e559-137">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="2e559-138">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="2e559-138">Default is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e559-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2e559-139">-Confirm</span></span>
<span data-ttu-id="2e559-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2e559-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e559-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e559-141">-WhatIf</span></span>
<span data-ttu-id="2e559-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2e559-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e559-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2e559-143">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e559-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e559-144">CommonParameters</span></span>
<span data-ttu-id="2e559-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e559-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2e559-146">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e559-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e559-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e559-147">INPUTS</span></span>

### <span data-ttu-id="2e559-148">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="2e559-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2e559-149">System. String</span><span class="sxs-lookup"><span data-stu-id="2e559-149">System.String</span></span>

## <span data-ttu-id="2e559-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e559-150">OUTPUTS</span></span>

### <span data-ttu-id="2e559-151">Microsoft. Azure. Command. Management. IotHub. models. PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="2e559-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="2e559-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e559-152">NOTES</span></span>

## <span data-ttu-id="2e559-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e559-153">RELATED LINKS</span></span>
