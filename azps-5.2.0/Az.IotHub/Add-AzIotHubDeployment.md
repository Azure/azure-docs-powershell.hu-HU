---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
ms.openlocfilehash: 0e3065cb2ee668f6b0ef5b20ac25ee51d922edc7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342365"
---
# <span data-ttu-id="a9704-101">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="a9704-101">Add-AzIotHubDeployment</span></span>

## <span data-ttu-id="a9704-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9704-102">SYNOPSIS</span></span>
<span data-ttu-id="a9704-103">IoT Edge-telepítés hozzáadása egy cél IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="a9704-103">Add an IoT Edge deployment in a target IoT Hub.</span></span>

## <span data-ttu-id="a9704-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a9704-104">SYNTAX</span></span>

### <span data-ttu-id="a9704-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a9704-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-ModulesContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9704-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a9704-106">InputObjectSet</span></span>
```
Add-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-ModulesContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9704-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a9704-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-ModulesContent <Hashtable>] [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9704-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a9704-108">DESCRIPTION</span></span>
<span data-ttu-id="a9704-109">A peremhálózati telepítéseket a felhasználó által definiált metrikák segítségével lehet létrehozni az igény szerinti értékeléshez.</span><span class="sxs-lookup"><span data-stu-id="a9704-109">Edge deployments can be created with user defined metrics for on demand evaluation.</span></span>
<span data-ttu-id="a9704-110">További https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring információt itt is láthat.</span><span class="sxs-lookup"><span data-stu-id="a9704-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="a9704-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a9704-111">EXAMPLES</span></span>

### <span data-ttu-id="a9704-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="a9704-112">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="a9704-113">Hozzon létre egy edge-telepítést alapértelmezett metaadatokkal.</span><span class="sxs-lookup"><span data-stu-id="a9704-113">Create an Edge deployment with default metadata.</span></span>

### <span data-ttu-id="a9704-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="a9704-114">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="a9704-115">Hozzon létre egy 3-as prioritású Edge-telepítést, amely akkor vonatkozik feltételre, ha egy eszköz meg van címkézve a 9-es épületben, és a környezet "teszt".</span><span class="sxs-lookup"><span data-stu-id="a9704-115">Create an Edge deployment with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="a9704-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="a9704-116">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Metric $metrics
```

<span data-ttu-id="a9704-117">Hozzon létre egy Edge-telepítést felhasználói metrikák segítségével.</span><span class="sxs-lookup"><span data-stu-id="a9704-117">Create an Edge deployment with user metrics.</span></span>

### <span data-ttu-id="a9704-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="a9704-118">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels
```

<span data-ttu-id="a9704-119">Hozzon létre egy Edge-telepítést címkékkel.</span><span class="sxs-lookup"><span data-stu-id="a9704-119">Create an Edge deployment with labels.</span></span>

### <span data-ttu-id="a9704-120">4. példa</span><span class="sxs-lookup"><span data-stu-id="a9704-120">Example 4</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -ModulesContent $content -TargetCondition "from devices.modules where tags.environment='test'"
```

<span data-ttu-id="a9704-121">Hozzon létre egy Edge-telepítést tartalommal.</span><span class="sxs-lookup"><span data-stu-id="a9704-121">Create an Edge deployment with content.</span></span>

## <span data-ttu-id="a9704-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9704-122">PARAMETERS</span></span>

### <span data-ttu-id="a9704-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9704-123">-DefaultProfile</span></span>
<span data-ttu-id="a9704-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9704-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9704-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9704-125">-InputObject</span></span>
<span data-ttu-id="a9704-126">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="a9704-126">IotHub object</span></span>

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

### <span data-ttu-id="a9704-127">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a9704-127">-IotHubName</span></span>
<span data-ttu-id="a9704-128">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="a9704-128">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a9704-129">-Label</span><span class="sxs-lookup"><span data-stu-id="a9704-129">-Label</span></span>
<span data-ttu-id="a9704-130">A céltelepítéshez alkalmazandó címkék térképe.</span><span class="sxs-lookup"><span data-stu-id="a9704-130">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="a9704-131">-Metric</span><span class="sxs-lookup"><span data-stu-id="a9704-131">-Metric</span></span>
<span data-ttu-id="a9704-132">Az IoT Edge üzembe helyezési metrikák definíciójának lekérdezésgyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="a9704-132">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="a9704-133">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="a9704-133">-ModulesContent</span></span>
<span data-ttu-id="a9704-134">Az IoT Edge-eszközökhöz használható modulok telepítési tartalma.</span><span class="sxs-lookup"><span data-stu-id="a9704-134">Deployment content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="a9704-135">-Name</span><span class="sxs-lookup"><span data-stu-id="a9704-135">-Name</span></span>
<span data-ttu-id="a9704-136">A központi telepítés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a9704-136">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="a9704-137">-Priority</span><span class="sxs-lookup"><span data-stu-id="a9704-137">-Priority</span></span>
<span data-ttu-id="a9704-138">A telepítés súlyát versenyben álló szabályok (legnagyobb nyeremények) esetén.</span><span class="sxs-lookup"><span data-stu-id="a9704-138">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="a9704-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9704-139">-ResourceGroupName</span></span>
<span data-ttu-id="a9704-140">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a9704-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a9704-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9704-141">-ResourceId</span></span>
<span data-ttu-id="a9704-142">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="a9704-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a9704-143">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="a9704-143">-TargetCondition</span></span>
<span data-ttu-id="a9704-144">Cél feltétel, amelyben egy Edge-telepítés érvényes.</span><span class="sxs-lookup"><span data-stu-id="a9704-144">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="a9704-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9704-145">-Confirm</span></span>
<span data-ttu-id="a9704-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a9704-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9704-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9704-147">-WhatIf</span></span>
<span data-ttu-id="a9704-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a9704-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9704-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a9704-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9704-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9704-150">CommonParameters</span></span>
<span data-ttu-id="a9704-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9704-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9704-152">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9704-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9704-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a9704-153">INPUTS</span></span>

### <span data-ttu-id="a9704-154">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a9704-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a9704-155">System.String</span><span class="sxs-lookup"><span data-stu-id="a9704-155">System.String</span></span>

## <span data-ttu-id="a9704-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9704-156">OUTPUTS</span></span>

### <span data-ttu-id="a9704-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="a9704-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="a9704-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a9704-158">NOTES</span></span>

## <span data-ttu-id="a9704-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9704-159">RELATED LINKS</span></span>
