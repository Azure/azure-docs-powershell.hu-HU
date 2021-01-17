---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
ms.openlocfilehash: 40fa5d382972c53de94187c9731748be5b1bfe2a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386579"
---
# <span data-ttu-id="622f6-101">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="622f6-101">Set-AzIotHubConfiguration</span></span>

## <span data-ttu-id="622f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="622f6-102">SYNOPSIS</span></span>
<span data-ttu-id="622f6-103">Frissítse a konfigurációs regisztráció elnémítható mezőit.</span><span class="sxs-lookup"><span data-stu-id="622f6-103">Update the mutable fields of the configuration registration.</span></span>

## <span data-ttu-id="622f6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="622f6-104">SYNTAX</span></span>

### <span data-ttu-id="622f6-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="622f6-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name] <String>
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="622f6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="622f6-106">InputObjectSet</span></span>
```
Set-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="622f6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="622f6-107">ResourceIdSet</span></span>
```
Set-AzIotHubConfiguration [-ResourceId] <String> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="622f6-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="622f6-108">DESCRIPTION</span></span>
<span data-ttu-id="622f6-109">Frissítse az IoT automatikus eszközkezelési konfigurációjának megadott tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="622f6-109">Update specified properties of an IoT automatic device management configuration.</span></span>
<span data-ttu-id="622f6-110">Megjegyzés: A konfigurációs tartalom nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="622f6-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="622f6-111">A frissíthető konfigurációs tulajdonságok a "címkék", a "metrikák", a "prioritás" és a "targetCondition".</span><span class="sxs-lookup"><span data-stu-id="622f6-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="622f6-112">További https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management információt itt is láthat.</span><span class="sxs-lookup"><span data-stu-id="622f6-112">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="622f6-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="622f6-113">EXAMPLES</span></span>

### <span data-ttu-id="622f6-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="622f6-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="622f6-115">Az eszközkonfiguráció prioritásának megváltoztatása és a cél feltételének frissítése</span><span class="sxs-lookup"><span data-stu-id="622f6-115">Alter the priority of a device configuration and update its target condition</span></span>

### <span data-ttu-id="622f6-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="622f6-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels -Metric $metrics
```

<span data-ttu-id="622f6-117">Eszközkonfiguráció metrikák és címkék frissítése</span><span class="sxs-lookup"><span data-stu-id="622f6-117">Update the metrics and labels of a device configuration</span></span>

## <span data-ttu-id="622f6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="622f6-118">PARAMETERS</span></span>

### <span data-ttu-id="622f6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="622f6-119">-DefaultProfile</span></span>
<span data-ttu-id="622f6-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="622f6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="622f6-121">-Force</span><span class="sxs-lookup"><span data-stu-id="622f6-121">-Force</span></span>
<span data-ttu-id="622f6-122">Lehetővé teszi a konfigurációs objektum cseréjét akkor is, ha a legutóbbi beolvasás óta frissült.</span><span class="sxs-lookup"><span data-stu-id="622f6-122">Allows configuration object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="622f6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="622f6-123">-InputObject</span></span>
<span data-ttu-id="622f6-124">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="622f6-124">IotHub object</span></span>

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

### <span data-ttu-id="622f6-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="622f6-125">-IotHubName</span></span>
<span data-ttu-id="622f6-126">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="622f6-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="622f6-127">-Label</span><span class="sxs-lookup"><span data-stu-id="622f6-127">-Label</span></span>
<span data-ttu-id="622f6-128">A célkonfigurációhoz alkalmazandó címkék térképe.</span><span class="sxs-lookup"><span data-stu-id="622f6-128">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="622f6-129">-Metric</span><span class="sxs-lookup"><span data-stu-id="622f6-129">-Metric</span></span>
<span data-ttu-id="622f6-130">A konfigurációs metrikák definíciójának lekérdezésgyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="622f6-130">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="622f6-131">-Name</span><span class="sxs-lookup"><span data-stu-id="622f6-131">-Name</span></span>
<span data-ttu-id="622f6-132">A konfiguráció azonosítója.</span><span class="sxs-lookup"><span data-stu-id="622f6-132">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="622f6-133">-Priority</span><span class="sxs-lookup"><span data-stu-id="622f6-133">-Priority</span></span>
<span data-ttu-id="622f6-134">Az eszköz konfigurációjának súlya versenyben álló szabályok (legnagyobb nyeremények) esetén.</span><span class="sxs-lookup"><span data-stu-id="622f6-134">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="622f6-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="622f6-135">-ResourceGroupName</span></span>
<span data-ttu-id="622f6-136">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="622f6-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="622f6-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="622f6-137">-ResourceId</span></span>
<span data-ttu-id="622f6-138">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="622f6-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="622f6-139">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="622f6-139">-TargetCondition</span></span>
<span data-ttu-id="622f6-140">Cél feltétel, amelyre egy eszközkonfiguráció érvényes.</span><span class="sxs-lookup"><span data-stu-id="622f6-140">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="622f6-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="622f6-141">-Confirm</span></span>
<span data-ttu-id="622f6-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="622f6-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="622f6-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="622f6-143">-WhatIf</span></span>
<span data-ttu-id="622f6-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="622f6-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="622f6-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="622f6-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="622f6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="622f6-146">CommonParameters</span></span>
<span data-ttu-id="622f6-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="622f6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="622f6-148">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="622f6-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="622f6-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="622f6-149">INPUTS</span></span>

### <span data-ttu-id="622f6-150">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="622f6-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="622f6-151">System.String</span><span class="sxs-lookup"><span data-stu-id="622f6-151">System.String</span></span>

## <span data-ttu-id="622f6-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="622f6-152">OUTPUTS</span></span>

### <span data-ttu-id="622f6-153">Microsoft.Azure.Commands.Management.iotHub.Models.PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="622f6-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="622f6-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="622f6-154">NOTES</span></span>

## <span data-ttu-id="622f6-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="622f6-155">RELATED LINKS</span></span>
