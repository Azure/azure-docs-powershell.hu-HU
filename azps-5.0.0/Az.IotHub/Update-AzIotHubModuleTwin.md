---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
ms.openlocfilehash: fb2b984453f87422d7a5b9ec5d5178ca6b6c55d5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296894"
---
# <span data-ttu-id="20ccb-101">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="20ccb-101">Update-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="20ccb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="20ccb-102">SYNOPSIS</span></span>
<span data-ttu-id="20ccb-103">A IoT-eszközök moduljainak címkéi és a kívánt tulajdonságai frissítik.</span><span class="sxs-lookup"><span data-stu-id="20ccb-103">Updates tags and desired properties of an IoT device module twin.</span></span>

## <span data-ttu-id="20ccb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="20ccb-104">SYNTAX</span></span>

### <span data-ttu-id="20ccb-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="20ccb-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20ccb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="20ccb-106">InputObjectSet</span></span>
```
Update-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20ccb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="20ccb-107">ResourceIdSet</span></span>
```
Update-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20ccb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="20ccb-108">DESCRIPTION</span></span>
<span data-ttu-id="20ccb-109">A Twin eszközök frissítése vagy cseréje</span><span class="sxs-lookup"><span data-stu-id="20ccb-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="20ccb-110"> https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twinsTovábbi információt itt talál.</span><span class="sxs-lookup"><span data-stu-id="20ccb-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="20ccb-111">Példák</span><span class="sxs-lookup"><span data-stu-id="20ccb-111">EXAMPLES</span></span>

### <span data-ttu-id="20ccb-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="20ccb-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="20ccb-113">A frissített Device Module Twin objektum értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="20ccb-113">Returns the updated device module twin object.</span></span>

### <span data-ttu-id="20ccb-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="20ccb-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="20ccb-115">Az Device Module Twin objektum értékét számítja ki a frissített kívánt tulajdonságokkal.</span><span class="sxs-lookup"><span data-stu-id="20ccb-115">Returns the device module twin object with updated desired properties.</span></span>

### <span data-ttu-id="20ccb-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="20ccb-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Partial
```

<span data-ttu-id="20ccb-117">Az Device Module Twin objektum értékét számítja ki a frissített címkék tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="20ccb-117">Returns the device module twin object with updated tags property.</span></span>

### <span data-ttu-id="20ccb-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="20ccb-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="20ccb-119">A kicserélt Device Module Twin objektum értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="20ccb-119">Returns the replaced device module twin object.</span></span>

## <span data-ttu-id="20ccb-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="20ccb-120">PARAMETERS</span></span>

### <span data-ttu-id="20ccb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20ccb-121">-DefaultProfile</span></span>
<span data-ttu-id="20ccb-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20ccb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20ccb-123">– Kívánt</span><span class="sxs-lookup"><span data-stu-id="20ccb-123">-Desired</span></span>
<span data-ttu-id="20ccb-124">Adja hozzá vagy frissítse a kívánt tulajdonságot egy külön modulban.</span><span class="sxs-lookup"><span data-stu-id="20ccb-124">Add or update the desired property in a module twin.</span></span>

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

### <span data-ttu-id="20ccb-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="20ccb-125">-DeviceId</span></span>
<span data-ttu-id="20ccb-126">Céleszköz-azonosító.</span><span class="sxs-lookup"><span data-stu-id="20ccb-126">Target Device Id.</span></span>

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

### <span data-ttu-id="20ccb-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20ccb-127">-InputObject</span></span>
<span data-ttu-id="20ccb-128">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="20ccb-128">IotHub object</span></span>

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

### <span data-ttu-id="20ccb-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="20ccb-129">-IotHubName</span></span>
<span data-ttu-id="20ccb-130">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="20ccb-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="20ccb-131">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="20ccb-131">-ModuleId</span></span>
<span data-ttu-id="20ccb-132">A cél modul azonosítója</span><span class="sxs-lookup"><span data-stu-id="20ccb-132">Target Module Id.</span></span>

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

### <span data-ttu-id="20ccb-133">-Részleges</span><span class="sxs-lookup"><span data-stu-id="20ccb-133">-Partial</span></span>
<span data-ttu-id="20ccb-134">Megengedi, hogy csak részlegesen frissítse a két modul címkéit és a kívánt tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="20ccb-134">Allows to only partially update the tags and desired properties of a module twin.</span></span>

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

### <span data-ttu-id="20ccb-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20ccb-135">-ResourceGroupName</span></span>
<span data-ttu-id="20ccb-136">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="20ccb-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="20ccb-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20ccb-137">-ResourceId</span></span>
<span data-ttu-id="20ccb-138">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="20ccb-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="20ccb-139">-Címke</span><span class="sxs-lookup"><span data-stu-id="20ccb-139">-Tag</span></span>
<span data-ttu-id="20ccb-140">Adja hozzá vagy frissítse a címkék tulajdonságot egy külön modulban.</span><span class="sxs-lookup"><span data-stu-id="20ccb-140">Add or update the tags property in a module twin.</span></span>

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

### <span data-ttu-id="20ccb-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="20ccb-141">-Confirm</span></span>
<span data-ttu-id="20ccb-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="20ccb-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20ccb-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20ccb-143">-WhatIf</span></span>
<span data-ttu-id="20ccb-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="20ccb-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20ccb-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="20ccb-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20ccb-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20ccb-146">CommonParameters</span></span>
<span data-ttu-id="20ccb-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="20ccb-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20ccb-148">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20ccb-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20ccb-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="20ccb-149">INPUTS</span></span>

### <span data-ttu-id="20ccb-150">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="20ccb-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="20ccb-151">System. String</span><span class="sxs-lookup"><span data-stu-id="20ccb-151">System.String</span></span>

## <span data-ttu-id="20ccb-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20ccb-152">OUTPUTS</span></span>

### <span data-ttu-id="20ccb-153">Microsoft. Azure. Command. Management. IotHub. models. PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="20ccb-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="20ccb-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="20ccb-154">NOTES</span></span>

## <span data-ttu-id="20ccb-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20ccb-155">RELATED LINKS</span></span>
