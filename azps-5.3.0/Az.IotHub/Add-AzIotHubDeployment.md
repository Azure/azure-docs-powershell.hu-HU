---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
ms.openlocfilehash: 0e3065cb2ee668f6b0ef5b20ac25ee51d922edc7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480182"
---
# <span data-ttu-id="9b3f6-101">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="9b3f6-101">Add-AzIotHubDeployment</span></span>

## <span data-ttu-id="9b3f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b3f6-102">SYNOPSIS</span></span>
<span data-ttu-id="9b3f6-103">IoT Edge-telepítés hozzáadása egy cél IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-103">Add an IoT Edge deployment in a target IoT Hub.</span></span>

## <span data-ttu-id="9b3f6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9b3f6-104">SYNTAX</span></span>

### <span data-ttu-id="9b3f6-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9b3f6-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-ModulesContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b3f6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9b3f6-106">InputObjectSet</span></span>
```
Add-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-ModulesContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b3f6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9b3f6-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-ModulesContent <Hashtable>] [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b3f6-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9b3f6-108">DESCRIPTION</span></span>
<span data-ttu-id="9b3f6-109">A peremhálózati telepítéseket a felhasználó által definiált metrikák segítségével lehet létrehozni az igény szerinti értékeléshez.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-109">Edge deployments can be created with user defined metrics for on demand evaluation.</span></span>
<span data-ttu-id="9b3f6-110">További https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring információt itt is láthat.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="9b3f6-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9b3f6-111">EXAMPLES</span></span>

### <span data-ttu-id="9b3f6-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="9b3f6-112">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="9b3f6-113">Hozzon létre egy edge-telepítést alapértelmezett metaadatokkal.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-113">Create an Edge deployment with default metadata.</span></span>

### <span data-ttu-id="9b3f6-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="9b3f6-114">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="9b3f6-115">Hozzon létre egy 3-as prioritású Edge-telepítést, amely akkor vonatkozik feltételre, ha egy eszközt címkéznek a 9-es épületben, és a környezet "teszt".</span><span class="sxs-lookup"><span data-stu-id="9b3f6-115">Create an Edge deployment with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="9b3f6-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="9b3f6-116">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Metric $metrics
```

<span data-ttu-id="9b3f6-117">Hozzon létre egy Edge-telepítést felhasználói metrikák segítségével.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-117">Create an Edge deployment with user metrics.</span></span>

### <span data-ttu-id="9b3f6-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="9b3f6-118">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels
```

<span data-ttu-id="9b3f6-119">Hozzon létre egy Edge-telepítést címkékkel.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-119">Create an Edge deployment with labels.</span></span>

### <span data-ttu-id="9b3f6-120">4. példa</span><span class="sxs-lookup"><span data-stu-id="9b3f6-120">Example 4</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -ModulesContent $content -TargetCondition "from devices.modules where tags.environment='test'"
```

<span data-ttu-id="9b3f6-121">Hozzon létre egy Edge-telepítést tartalommal.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-121">Create an Edge deployment with content.</span></span>

## <span data-ttu-id="9b3f6-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b3f6-122">PARAMETERS</span></span>

### <span data-ttu-id="9b3f6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b3f6-123">-DefaultProfile</span></span>
<span data-ttu-id="9b3f6-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b3f6-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b3f6-125">-InputObject</span></span>
<span data-ttu-id="9b3f6-126">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="9b3f6-126">IotHub object</span></span>

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

### <span data-ttu-id="9b3f6-127">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="9b3f6-127">-IotHubName</span></span>
<span data-ttu-id="9b3f6-128">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="9b3f6-128">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9b3f6-129">-Label</span><span class="sxs-lookup"><span data-stu-id="9b3f6-129">-Label</span></span>
<span data-ttu-id="9b3f6-130">A céltelepítéshez alkalmazandó címkék térképe.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-130">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="9b3f6-131">-Metric</span><span class="sxs-lookup"><span data-stu-id="9b3f6-131">-Metric</span></span>
<span data-ttu-id="9b3f6-132">Az IoT Edge üzembe helyezési metrikák definíciójának lekérdezésgyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-132">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="9b3f6-133">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="9b3f6-133">-ModulesContent</span></span>
<span data-ttu-id="9b3f6-134">Az IoT Edge-eszközökhöz használható modulok telepítési tartalma.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-134">Deployment content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="9b3f6-135">-Name</span><span class="sxs-lookup"><span data-stu-id="9b3f6-135">-Name</span></span>
<span data-ttu-id="9b3f6-136">A központi telepítés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-136">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="9b3f6-137">-Priority</span><span class="sxs-lookup"><span data-stu-id="9b3f6-137">-Priority</span></span>
<span data-ttu-id="9b3f6-138">A telepítés súlyát versenyben álló szabályok (legnagyobb nyeremények) esetén.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-138">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="9b3f6-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b3f6-139">-ResourceGroupName</span></span>
<span data-ttu-id="9b3f6-140">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="9b3f6-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9b3f6-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b3f6-141">-ResourceId</span></span>
<span data-ttu-id="9b3f6-142">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="9b3f6-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9b3f6-143">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="9b3f6-143">-TargetCondition</span></span>
<span data-ttu-id="9b3f6-144">Cél feltétel, amelyben egy Edge-telepítés érvényes.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-144">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="9b3f6-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b3f6-145">-Confirm</span></span>
<span data-ttu-id="9b3f6-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b3f6-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b3f6-147">-WhatIf</span></span>
<span data-ttu-id="9b3f6-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b3f6-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b3f6-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b3f6-150">CommonParameters</span></span>
<span data-ttu-id="9b3f6-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b3f6-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b3f6-152">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b3f6-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b3f6-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b3f6-153">INPUTS</span></span>

### <span data-ttu-id="9b3f6-154">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9b3f6-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9b3f6-155">System.String</span><span class="sxs-lookup"><span data-stu-id="9b3f6-155">System.String</span></span>

## <span data-ttu-id="9b3f6-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b3f6-156">OUTPUTS</span></span>

### <span data-ttu-id="9b3f6-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="9b3f6-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="9b3f6-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9b3f6-158">NOTES</span></span>

## <span data-ttu-id="9b3f6-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b3f6-159">RELATED LINKS</span></span>
