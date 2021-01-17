---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
ms.openlocfilehash: 947eec246c5dac9543522ade583426246c731d3e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386566"
---
# <span data-ttu-id="d9395-101">Set-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="d9395-101">Set-AzIotHubDeployment</span></span>

## <span data-ttu-id="d9395-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9395-102">SYNOPSIS</span></span>
<span data-ttu-id="d9395-103">Frissítse az IoT Edge-telepítés elnémítható mezőit.</span><span class="sxs-lookup"><span data-stu-id="d9395-103">Update the mutable fields of IoT Edge deployment.</span></span>

## <span data-ttu-id="d9395-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d9395-104">SYNTAX</span></span>

### <span data-ttu-id="d9395-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d9395-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9395-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d9395-106">InputObjectSet</span></span>
```
Set-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9395-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d9395-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9395-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d9395-108">DESCRIPTION</span></span>
<span data-ttu-id="d9395-109">Frissítse egy IoT Edge-telepítés megadott tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="d9395-109">Update specified properties of an IoT Edge deployment.</span></span>
<span data-ttu-id="d9395-110">Megjegyzés: A konfigurációs tartalom nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="d9395-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="d9395-111">A frissíthető konfigurációs tulajdonságok a "címkék", a "metrikák", a "prioritás" és a "targetCondition".</span><span class="sxs-lookup"><span data-stu-id="d9395-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="d9395-112">További https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  információt itt is láthat.</span><span class="sxs-lookup"><span data-stu-id="d9395-112">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  for more information.</span></span>

## <span data-ttu-id="d9395-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d9395-113">EXAMPLES</span></span>

### <span data-ttu-id="d9395-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="d9395-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="d9395-115">Az IoT Edge-telepítés prioritásának megváltoztatása és a cél feltételének frissítése.</span><span class="sxs-lookup"><span data-stu-id="d9395-115">Alter the priority of IoT Edge deployment and update its target condition.</span></span>

### <span data-ttu-id="d9395-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="d9395-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels -Metric $metrics
```

<span data-ttu-id="d9395-117">Frissítse az IoT Edge-telepítés metrikait és címkéit.</span><span class="sxs-lookup"><span data-stu-id="d9395-117">Update the metrics and labels of IoT Edge deployment.</span></span>

## <span data-ttu-id="d9395-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9395-118">PARAMETERS</span></span>

### <span data-ttu-id="d9395-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9395-119">-DefaultProfile</span></span>
<span data-ttu-id="d9395-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d9395-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9395-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d9395-121">-Force</span></span>
<span data-ttu-id="d9395-122">Lehetővé teszi a telepítési objektum cseréjét akkor is, ha a legutóbbi beolvasás óta frissült.</span><span class="sxs-lookup"><span data-stu-id="d9395-122">Allows deployment object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="d9395-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9395-123">-InputObject</span></span>
<span data-ttu-id="d9395-124">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="d9395-124">IotHub object</span></span>

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

### <span data-ttu-id="d9395-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d9395-125">-IotHubName</span></span>
<span data-ttu-id="d9395-126">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="d9395-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d9395-127">-Label</span><span class="sxs-lookup"><span data-stu-id="d9395-127">-Label</span></span>
<span data-ttu-id="d9395-128">A céltelepítéshez alkalmazandó címkék térképe.</span><span class="sxs-lookup"><span data-stu-id="d9395-128">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="d9395-129">-Metric</span><span class="sxs-lookup"><span data-stu-id="d9395-129">-Metric</span></span>
<span data-ttu-id="d9395-130">Az IoT Edge üzembe helyezési metrikák definíciójának lekérdezésgyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="d9395-130">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="d9395-131">-Name</span><span class="sxs-lookup"><span data-stu-id="d9395-131">-Name</span></span>
<span data-ttu-id="d9395-132">A központi telepítés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d9395-132">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="d9395-133">-Priority</span><span class="sxs-lookup"><span data-stu-id="d9395-133">-Priority</span></span>
<span data-ttu-id="d9395-134">A telepítés súlyát versenyben álló szabályok (legnagyobb nyeremények) esetén.</span><span class="sxs-lookup"><span data-stu-id="d9395-134">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="d9395-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9395-135">-ResourceGroupName</span></span>
<span data-ttu-id="d9395-136">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d9395-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d9395-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9395-137">-ResourceId</span></span>
<span data-ttu-id="d9395-138">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="d9395-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d9395-139">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="d9395-139">-TargetCondition</span></span>
<span data-ttu-id="d9395-140">Cél feltétel, amelyben egy Edge-telepítés érvényes.</span><span class="sxs-lookup"><span data-stu-id="d9395-140">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="d9395-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9395-141">-Confirm</span></span>
<span data-ttu-id="d9395-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d9395-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9395-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9395-143">-WhatIf</span></span>
<span data-ttu-id="d9395-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d9395-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9395-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d9395-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9395-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9395-146">CommonParameters</span></span>
<span data-ttu-id="d9395-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9395-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9395-148">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9395-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9395-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d9395-149">INPUTS</span></span>

### <span data-ttu-id="d9395-150">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d9395-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d9395-151">System.String</span><span class="sxs-lookup"><span data-stu-id="d9395-151">System.String</span></span>

## <span data-ttu-id="d9395-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9395-152">OUTPUTS</span></span>

### <span data-ttu-id="d9395-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="d9395-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="d9395-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d9395-154">NOTES</span></span>

## <span data-ttu-id="d9395-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d9395-155">RELATED LINKS</span></span>
