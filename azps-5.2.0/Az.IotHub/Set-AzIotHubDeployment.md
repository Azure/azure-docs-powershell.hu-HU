---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
ms.openlocfilehash: 947eec246c5dac9543522ade583426246c731d3e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327582"
---
# <span data-ttu-id="cbebb-101">Set-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="cbebb-101">Set-AzIotHubDeployment</span></span>

## <span data-ttu-id="cbebb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbebb-102">SYNOPSIS</span></span>
<span data-ttu-id="cbebb-103">Frissítse az IoT Edge-telepítés elnémítható mezőit.</span><span class="sxs-lookup"><span data-stu-id="cbebb-103">Update the mutable fields of IoT Edge deployment.</span></span>

## <span data-ttu-id="cbebb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cbebb-104">SYNTAX</span></span>

### <span data-ttu-id="cbebb-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cbebb-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbebb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cbebb-106">InputObjectSet</span></span>
```
Set-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbebb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cbebb-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbebb-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cbebb-108">DESCRIPTION</span></span>
<span data-ttu-id="cbebb-109">Frissítse egy IoT Edge-telepítés megadott tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="cbebb-109">Update specified properties of an IoT Edge deployment.</span></span>
<span data-ttu-id="cbebb-110">Megjegyzés: A konfigurációs tartalom nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="cbebb-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="cbebb-111">A frissíthető konfigurációs tulajdonságok a "címkék", a "metrikák", a "prioritás" és a "targetCondition".</span><span class="sxs-lookup"><span data-stu-id="cbebb-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="cbebb-112">További https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  információt itt is láthat.</span><span class="sxs-lookup"><span data-stu-id="cbebb-112">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  for more information.</span></span>

## <span data-ttu-id="cbebb-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cbebb-113">EXAMPLES</span></span>

### <span data-ttu-id="cbebb-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="cbebb-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="cbebb-115">Az IoT Edge-telepítés prioritásának megváltoztatása és a cél feltételének frissítése.</span><span class="sxs-lookup"><span data-stu-id="cbebb-115">Alter the priority of IoT Edge deployment and update its target condition.</span></span>

### <span data-ttu-id="cbebb-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="cbebb-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels -Metric $metrics
```

<span data-ttu-id="cbebb-117">Frissítse az IoT Edge-telepítés metrikait és címkéit.</span><span class="sxs-lookup"><span data-stu-id="cbebb-117">Update the metrics and labels of IoT Edge deployment.</span></span>

## <span data-ttu-id="cbebb-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbebb-118">PARAMETERS</span></span>

### <span data-ttu-id="cbebb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbebb-119">-DefaultProfile</span></span>
<span data-ttu-id="cbebb-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cbebb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbebb-121">-Force</span><span class="sxs-lookup"><span data-stu-id="cbebb-121">-Force</span></span>
<span data-ttu-id="cbebb-122">Lehetővé teszi a telepítési objektum cseréjét akkor is, ha a legutóbbi beolvasás óta frissült.</span><span class="sxs-lookup"><span data-stu-id="cbebb-122">Allows deployment object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="cbebb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbebb-123">-InputObject</span></span>
<span data-ttu-id="cbebb-124">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="cbebb-124">IotHub object</span></span>

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

### <span data-ttu-id="cbebb-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="cbebb-125">-IotHubName</span></span>
<span data-ttu-id="cbebb-126">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="cbebb-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="cbebb-127">-Label</span><span class="sxs-lookup"><span data-stu-id="cbebb-127">-Label</span></span>
<span data-ttu-id="cbebb-128">A céltelepítéshez alkalmazandó címkék térképe.</span><span class="sxs-lookup"><span data-stu-id="cbebb-128">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="cbebb-129">-Metric</span><span class="sxs-lookup"><span data-stu-id="cbebb-129">-Metric</span></span>
<span data-ttu-id="cbebb-130">Az IoT Edge üzembe helyezési metrikák definíciójának lekérdezésgyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="cbebb-130">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="cbebb-131">-Name</span><span class="sxs-lookup"><span data-stu-id="cbebb-131">-Name</span></span>
<span data-ttu-id="cbebb-132">A központi telepítés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cbebb-132">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="cbebb-133">-Priority</span><span class="sxs-lookup"><span data-stu-id="cbebb-133">-Priority</span></span>
<span data-ttu-id="cbebb-134">A telepítés súlyát versenyben álló szabályok (legnagyobb nyeremények) esetén.</span><span class="sxs-lookup"><span data-stu-id="cbebb-134">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="cbebb-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbebb-135">-ResourceGroupName</span></span>
<span data-ttu-id="cbebb-136">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="cbebb-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cbebb-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbebb-137">-ResourceId</span></span>
<span data-ttu-id="cbebb-138">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="cbebb-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="cbebb-139">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="cbebb-139">-TargetCondition</span></span>
<span data-ttu-id="cbebb-140">Cél feltétel, amelyben egy Edge-telepítés érvényes.</span><span class="sxs-lookup"><span data-stu-id="cbebb-140">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="cbebb-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cbebb-141">-Confirm</span></span>
<span data-ttu-id="cbebb-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cbebb-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbebb-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbebb-143">-WhatIf</span></span>
<span data-ttu-id="cbebb-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cbebb-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbebb-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cbebb-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbebb-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbebb-146">CommonParameters</span></span>
<span data-ttu-id="cbebb-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbebb-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbebb-148">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbebb-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbebb-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cbebb-149">INPUTS</span></span>

### <span data-ttu-id="cbebb-150">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="cbebb-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="cbebb-151">System.String</span><span class="sxs-lookup"><span data-stu-id="cbebb-151">System.String</span></span>

## <span data-ttu-id="cbebb-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbebb-152">OUTPUTS</span></span>

### <span data-ttu-id="cbebb-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="cbebb-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="cbebb-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cbebb-154">NOTES</span></span>

## <span data-ttu-id="cbebb-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cbebb-155">RELATED LINKS</span></span>
