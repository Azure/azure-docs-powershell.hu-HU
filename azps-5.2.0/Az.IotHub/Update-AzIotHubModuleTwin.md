---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
ms.openlocfilehash: fb2b984453f87422d7a5b9ec5d5178ca6b6c55d5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361715"
---
# <span data-ttu-id="a6180-101">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="a6180-101">Update-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="a6180-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6180-102">SYNOPSIS</span></span>
<span data-ttu-id="a6180-103">Frissíti egy IoT-eszközmodul modul címkéit és tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="a6180-103">Updates tags and desired properties of an IoT device module twin.</span></span>

## <span data-ttu-id="a6180-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a6180-104">SYNTAX</span></span>

### <span data-ttu-id="a6180-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a6180-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6180-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a6180-106">InputObjectSet</span></span>
```
Update-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a6180-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a6180-107">ResourceIdSet</span></span>
```
Update-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a6180-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a6180-108">DESCRIPTION</span></span>
<span data-ttu-id="a6180-109">Frissíti vagy lecseréli az eszköz eszközét.</span><span class="sxs-lookup"><span data-stu-id="a6180-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="a6180-110">További https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins információt itt is láthat.</span><span class="sxs-lookup"><span data-stu-id="a6180-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="a6180-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a6180-111">EXAMPLES</span></span>

### <span data-ttu-id="a6180-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="a6180-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="a6180-113">Az eszközmodul frissített objektumát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="a6180-113">Returns the updated device module twin object.</span></span>

### <span data-ttu-id="a6180-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="a6180-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="a6180-115">Az eszközmodul modul objektumát adja eredményül, mely frissített tulajdonságokat ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="a6180-115">Returns the device module twin object with updated desired properties.</span></span>

### <span data-ttu-id="a6180-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="a6180-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Partial
```

<span data-ttu-id="a6180-117">Frissített címketulajdonságú eszközmodul-objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="a6180-117">Returns the device module twin object with updated tags property.</span></span>

### <span data-ttu-id="a6180-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="a6180-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="a6180-119">A lecserélt eszközmodul modul objektumát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="a6180-119">Returns the replaced device module twin object.</span></span>

## <span data-ttu-id="a6180-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6180-120">PARAMETERS</span></span>

### <span data-ttu-id="a6180-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6180-121">-DefaultProfile</span></span>
<span data-ttu-id="a6180-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a6180-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6180-123">-Kívánt</span><span class="sxs-lookup"><span data-stu-id="a6180-123">-Desired</span></span>
<span data-ttu-id="a6180-124">Adja hozzá vagy frissítse a kívánt tulajdonságot egy modulban.</span><span class="sxs-lookup"><span data-stu-id="a6180-124">Add or update the desired property in a module twin.</span></span>

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

### <span data-ttu-id="a6180-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="a6180-125">-DeviceId</span></span>
<span data-ttu-id="a6180-126">Céleszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a6180-126">Target Device Id.</span></span>

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

### <span data-ttu-id="a6180-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6180-127">-InputObject</span></span>
<span data-ttu-id="a6180-128">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="a6180-128">IotHub object</span></span>

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

### <span data-ttu-id="a6180-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a6180-129">-IotHubName</span></span>
<span data-ttu-id="a6180-130">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="a6180-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a6180-131">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="a6180-131">-ModuleId</span></span>
<span data-ttu-id="a6180-132">Célmodul-azonosító.</span><span class="sxs-lookup"><span data-stu-id="a6180-132">Target Module Id.</span></span>

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

### <span data-ttu-id="a6180-133">-Részleges</span><span class="sxs-lookup"><span data-stu-id="a6180-133">-Partial</span></span>
<span data-ttu-id="a6180-134">Lehetővé teszi, hogy csak részben frissítse egy modul címkéit és tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="a6180-134">Allows to only partially update the tags and desired properties of a module twin.</span></span>

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

### <span data-ttu-id="a6180-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6180-135">-ResourceGroupName</span></span>
<span data-ttu-id="a6180-136">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a6180-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a6180-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6180-137">-ResourceId</span></span>
<span data-ttu-id="a6180-138">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="a6180-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a6180-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="a6180-139">-Tag</span></span>
<span data-ttu-id="a6180-140">Adja hozzá vagy frissítse a címketulajdonságokat egy modulban.</span><span class="sxs-lookup"><span data-stu-id="a6180-140">Add or update the tags property in a module twin.</span></span>

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

### <span data-ttu-id="a6180-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6180-141">-Confirm</span></span>
<span data-ttu-id="a6180-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a6180-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6180-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6180-143">-WhatIf</span></span>
<span data-ttu-id="a6180-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a6180-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6180-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a6180-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6180-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6180-146">CommonParameters</span></span>
<span data-ttu-id="a6180-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6180-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6180-148">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6180-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6180-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6180-149">INPUTS</span></span>

### <span data-ttu-id="a6180-150">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a6180-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a6180-151">System.String</span><span class="sxs-lookup"><span data-stu-id="a6180-151">System.String</span></span>

## <span data-ttu-id="a6180-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6180-152">OUTPUTS</span></span>

### <span data-ttu-id="a6180-153">Microsoft.Azure.Commands.Management.iotHub.Models.PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="a6180-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="a6180-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a6180-154">NOTES</span></span>

## <span data-ttu-id="a6180-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a6180-155">RELATED LINKS</span></span>
