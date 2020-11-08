---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
ms.openlocfilehash: 16c3ab31959268aa998d50290180d4d8b3231ccf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011151"
---
# <span data-ttu-id="5df9e-101">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="5df9e-101">Update-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="5df9e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5df9e-102">SYNOPSIS</span></span>
<span data-ttu-id="5df9e-103">A Twin eszközök címkéit és a kívánt tulajdonságait frissíti.</span><span class="sxs-lookup"><span data-stu-id="5df9e-103">Updates tags and desired properties of a device twin.</span></span>

## <span data-ttu-id="5df9e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5df9e-104">SYNTAX</span></span>

### <span data-ttu-id="5df9e-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5df9e-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5df9e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5df9e-106">InputObjectSet</span></span>
```
Update-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5df9e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5df9e-107">ResourceIdSet</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5df9e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5df9e-108">DESCRIPTION</span></span>
<span data-ttu-id="5df9e-109">A Twin eszközök frissítése vagy cseréje</span><span class="sxs-lookup"><span data-stu-id="5df9e-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="5df9e-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twinsTovábbi információt itt talál.</span><span class="sxs-lookup"><span data-stu-id="5df9e-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="5df9e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="5df9e-111">EXAMPLES</span></span>

### <span data-ttu-id="5df9e-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5df9e-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="5df9e-113">A frissített Device Twin objektum értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="5df9e-113">Returns the updated device twin object.</span></span>

### <span data-ttu-id="5df9e-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="5df9e-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="5df9e-115">Az Device Twin objektum értékét frissített kívánt tulajdonságokkal jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="5df9e-115">Returns the device twin object with updated desired properties.</span></span>

### <span data-ttu-id="5df9e-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="5df9e-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Partial
```

<span data-ttu-id="5df9e-117">Az Device Twin objektum értékét számítja ki a frissített címkék tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="5df9e-117">Returns the device twin object with updated tags property.</span></span>

### <span data-ttu-id="5df9e-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="5df9e-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="5df9e-119">A kicserélt eszköz Twin objektumát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="5df9e-119">Returns the replaced device twin object.</span></span>

## <span data-ttu-id="5df9e-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5df9e-120">PARAMETERS</span></span>

### <span data-ttu-id="5df9e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5df9e-121">-DefaultProfile</span></span>
<span data-ttu-id="5df9e-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5df9e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5df9e-123">– Kívánt</span><span class="sxs-lookup"><span data-stu-id="5df9e-123">-Desired</span></span>
<span data-ttu-id="5df9e-124">Adja hozzá vagy frissítse a kívánt tulajdonságot egy különálló eszközön.</span><span class="sxs-lookup"><span data-stu-id="5df9e-124">Add or update the desired property in a device twin.</span></span>

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

### <span data-ttu-id="5df9e-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="5df9e-125">-DeviceId</span></span>
<span data-ttu-id="5df9e-126">Céleszköz-azonosító.</span><span class="sxs-lookup"><span data-stu-id="5df9e-126">Target Device Id.</span></span>

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

### <span data-ttu-id="5df9e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5df9e-127">-InputObject</span></span>
<span data-ttu-id="5df9e-128">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="5df9e-128">IotHub object</span></span>

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

### <span data-ttu-id="5df9e-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="5df9e-129">-IotHubName</span></span>
<span data-ttu-id="5df9e-130">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="5df9e-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5df9e-131">-Részleges</span><span class="sxs-lookup"><span data-stu-id="5df9e-131">-Partial</span></span>
<span data-ttu-id="5df9e-132">Megengedi, hogy csak részlegesen frissítse az eszközök címkéit és a kívánt tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="5df9e-132">Allows to only partially update the tags and desired properties of a device twin.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df9e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5df9e-133">-ResourceGroupName</span></span>
<span data-ttu-id="5df9e-134">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="5df9e-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5df9e-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5df9e-135">-ResourceId</span></span>
<span data-ttu-id="5df9e-136">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="5df9e-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5df9e-137">-Címke</span><span class="sxs-lookup"><span data-stu-id="5df9e-137">-Tag</span></span>
<span data-ttu-id="5df9e-138">Adja hozzá vagy frissítse a címkék tulajdonságot egy különálló eszközön.</span><span class="sxs-lookup"><span data-stu-id="5df9e-138">Add or update the tags property in a device twin.</span></span>

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

### <span data-ttu-id="5df9e-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5df9e-139">-Confirm</span></span>
<span data-ttu-id="5df9e-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5df9e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5df9e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5df9e-141">-WhatIf</span></span>
<span data-ttu-id="5df9e-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5df9e-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5df9e-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5df9e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5df9e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5df9e-144">CommonParameters</span></span>
<span data-ttu-id="5df9e-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5df9e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5df9e-146">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5df9e-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5df9e-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5df9e-147">INPUTS</span></span>

### <span data-ttu-id="5df9e-148">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="5df9e-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5df9e-149">System. String</span><span class="sxs-lookup"><span data-stu-id="5df9e-149">System.String</span></span>

## <span data-ttu-id="5df9e-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5df9e-150">OUTPUTS</span></span>

### <span data-ttu-id="5df9e-151">System. String</span><span class="sxs-lookup"><span data-stu-id="5df9e-151">System.String</span></span>

## <span data-ttu-id="5df9e-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5df9e-152">NOTES</span></span>

## <span data-ttu-id="5df9e-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5df9e-153">RELATED LINKS</span></span>
