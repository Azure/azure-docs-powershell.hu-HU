---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
ms.openlocfilehash: 451f809687ea768800f0e9e33ef4c5af9c425150
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330270"
---
# <span data-ttu-id="11995-101">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="11995-101">Update-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="11995-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11995-102">SYNOPSIS</span></span>
<span data-ttu-id="11995-103">Frissíti egy eszköz címkéit és tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="11995-103">Updates tags and desired properties of a device twin.</span></span>

## <span data-ttu-id="11995-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="11995-104">SYNTAX</span></span>

### <span data-ttu-id="11995-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="11995-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11995-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="11995-106">InputObjectSet</span></span>
```
Update-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11995-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="11995-107">ResourceIdSet</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11995-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="11995-108">DESCRIPTION</span></span>
<span data-ttu-id="11995-109">Frissíti vagy lecseréli az eszköz eszközét.</span><span class="sxs-lookup"><span data-stu-id="11995-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="11995-110">További https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins információt itt is láthat.</span><span class="sxs-lookup"><span data-stu-id="11995-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="11995-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="11995-111">EXAMPLES</span></span>

### <span data-ttu-id="11995-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="11995-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="11995-113">Az eszköz frissített objektumát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="11995-113">Returns the updated device twin object.</span></span>

### <span data-ttu-id="11995-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="11995-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="11995-115">A módosított tulajdonsággal frissített eszközobjektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="11995-115">Returns the device twin object with updated desired properties.</span></span>

### <span data-ttu-id="11995-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="11995-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Partial
```

<span data-ttu-id="11995-117">A frissített címketulajdonságú eszközobjektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="11995-117">Returns the device twin object with updated tags property.</span></span>

### <span data-ttu-id="11995-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="11995-118">Example 4</span></span>
```powershell
PS C:\> $updatedTag = @{}
PS C:\> $updatedTag.add("key0","value0")
PS C:\> $updatedDesired =@{}
PS C:\> $updatedDesired.add("desiredkey","desiredvalue")
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="11995-119">A lecserélt eszköz objektumát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="11995-119">Returns the replaced device twin object.</span></span>

## <span data-ttu-id="11995-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11995-120">PARAMETERS</span></span>

### <span data-ttu-id="11995-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11995-121">-DefaultProfile</span></span>
<span data-ttu-id="11995-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11995-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11995-123">-Kívánt</span><span class="sxs-lookup"><span data-stu-id="11995-123">-Desired</span></span>
<span data-ttu-id="11995-124">Adja hozzá vagy frissítse a kívánt tulajdonságot egy eszköz eszközében.</span><span class="sxs-lookup"><span data-stu-id="11995-124">Add or update the desired property in a device twin.</span></span>

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

### <span data-ttu-id="11995-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="11995-125">-DeviceId</span></span>
<span data-ttu-id="11995-126">Céleszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="11995-126">Target Device Id.</span></span>

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

### <span data-ttu-id="11995-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11995-127">-InputObject</span></span>
<span data-ttu-id="11995-128">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="11995-128">IotHub object</span></span>

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

### <span data-ttu-id="11995-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="11995-129">-IotHubName</span></span>
<span data-ttu-id="11995-130">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="11995-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="11995-131">-Részleges</span><span class="sxs-lookup"><span data-stu-id="11995-131">-Partial</span></span>
<span data-ttu-id="11995-132">Lehetővé teszi, hogy csak részben frissítse egy eszköz címkéit és tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="11995-132">Allows to only partially update the tags and desired properties of a device twin.</span></span>

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

### <span data-ttu-id="11995-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11995-133">-ResourceGroupName</span></span>
<span data-ttu-id="11995-134">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="11995-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="11995-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11995-135">-ResourceId</span></span>
<span data-ttu-id="11995-136">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="11995-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="11995-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="11995-137">-Tag</span></span>
<span data-ttu-id="11995-138">Adja hozzá vagy frissítse a címketulajdonságokat egy eszköz eszközén.</span><span class="sxs-lookup"><span data-stu-id="11995-138">Add or update the tags property in a device twin.</span></span>

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

### <span data-ttu-id="11995-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11995-139">-Confirm</span></span>
<span data-ttu-id="11995-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="11995-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11995-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11995-141">-WhatIf</span></span>
<span data-ttu-id="11995-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="11995-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11995-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="11995-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11995-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11995-144">CommonParameters</span></span>
<span data-ttu-id="11995-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11995-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11995-146">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11995-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11995-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11995-147">INPUTS</span></span>

### <span data-ttu-id="11995-148">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="11995-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="11995-149">System.String</span><span class="sxs-lookup"><span data-stu-id="11995-149">System.String</span></span>

## <span data-ttu-id="11995-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11995-150">OUTPUTS</span></span>

### <span data-ttu-id="11995-151">System.String</span><span class="sxs-lookup"><span data-stu-id="11995-151">System.String</span></span>

## <span data-ttu-id="11995-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="11995-152">NOTES</span></span>

## <span data-ttu-id="11995-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11995-153">RELATED LINKS</span></span>
