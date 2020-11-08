---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
ms.openlocfilehash: 375e225d4c09368fac82db240988132952a0ada7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187790"
---
# <span data-ttu-id="7eb98-101">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="7eb98-101">Add-AzIotHubDeployment</span></span>

## <span data-ttu-id="7eb98-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7eb98-102">SYNOPSIS</span></span>
<span data-ttu-id="7eb98-103">IoT elhelyezése a TARGET IoT-központban</span><span class="sxs-lookup"><span data-stu-id="7eb98-103">Add an IoT Edge deployment in a target IoT Hub.</span></span>

## <span data-ttu-id="7eb98-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7eb98-104">SYNTAX</span></span>

### <span data-ttu-id="7eb98-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7eb98-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-ModulesContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7eb98-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7eb98-106">InputObjectSet</span></span>
```
Add-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-ModulesContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7eb98-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7eb98-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-ModulesContent <Hashtable>] [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7eb98-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7eb98-108">DESCRIPTION</span></span>
<span data-ttu-id="7eb98-109">Az igény szerinti kiértékeléshez a felhasználó által definiált mérőszámokkal hozhat létre Edge-bevezetést.</span><span class="sxs-lookup"><span data-stu-id="7eb98-109">Edge deployments can be created with user defined metrics for on demand evaluation.</span></span>
<span data-ttu-id="7eb98-110"> https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoringTovábbi információt itt talál.</span><span class="sxs-lookup"><span data-stu-id="7eb98-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="7eb98-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7eb98-111">EXAMPLES</span></span>

### <span data-ttu-id="7eb98-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7eb98-112">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="7eb98-113">Az alapértelmezett metaadatokat tartalmazó Edge-példány létrehozása</span><span class="sxs-lookup"><span data-stu-id="7eb98-113">Create an Edge deployment with default metadata.</span></span>

### <span data-ttu-id="7eb98-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="7eb98-114">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="7eb98-115">A 3-as prioritású, az épület 9 épületében megjelölt eszközön a "teszt" beállítással rendelkező Edge-példány létrehozása.</span><span class="sxs-lookup"><span data-stu-id="7eb98-115">Create an Edge deployment with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="7eb98-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="7eb98-116">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Metric $metrics
```

<span data-ttu-id="7eb98-117">A felhasználói metrikákat tartalmazó él-és kivezetést hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="7eb98-117">Create an Edge deployment with user metrics.</span></span>

### <span data-ttu-id="7eb98-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="7eb98-118">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels
```

<span data-ttu-id="7eb98-119">Éleket hozhat létre címkékkel.</span><span class="sxs-lookup"><span data-stu-id="7eb98-119">Create an Edge deployment with labels.</span></span>

### <span data-ttu-id="7eb98-120">4. példa</span><span class="sxs-lookup"><span data-stu-id="7eb98-120">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -ModulesContent $content
```

<span data-ttu-id="7eb98-121">Tartalommal rendelkező Edge-környezet létrehozása</span><span class="sxs-lookup"><span data-stu-id="7eb98-121">Create an Edge deployment with content.</span></span>

## <span data-ttu-id="7eb98-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7eb98-122">PARAMETERS</span></span>

### <span data-ttu-id="7eb98-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eb98-123">-DefaultProfile</span></span>
<span data-ttu-id="7eb98-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7eb98-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7eb98-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7eb98-125">-InputObject</span></span>
<span data-ttu-id="7eb98-126">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="7eb98-126">IotHub object</span></span>

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

### <span data-ttu-id="7eb98-127">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="7eb98-127">-IotHubName</span></span>
<span data-ttu-id="7eb98-128">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="7eb98-128">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7eb98-129">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="7eb98-129">-Label</span></span>
<span data-ttu-id="7eb98-130">A cél központi telepítéséhez alkalmazható címkék megfeleltetése.</span><span class="sxs-lookup"><span data-stu-id="7eb98-130">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="7eb98-131">-Metrikus</span><span class="sxs-lookup"><span data-stu-id="7eb98-131">-Metric</span></span>
<span data-ttu-id="7eb98-132">Lekérdezések gyűjteménye a IoT Edge telepítő metrikák definíciója szerint.</span><span class="sxs-lookup"><span data-stu-id="7eb98-132">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="7eb98-133">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="7eb98-133">-ModulesContent</span></span>
<span data-ttu-id="7eb98-134">Az IoT-hoz készült modulok központi telepítése</span><span class="sxs-lookup"><span data-stu-id="7eb98-134">Deployment content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="7eb98-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7eb98-135">-Name</span></span>
<span data-ttu-id="7eb98-136">A központi telepítő azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7eb98-136">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="7eb98-137">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="7eb98-137">-Priority</span></span>
<span data-ttu-id="7eb98-138">A bevezetés súlya a versengő szabályok (legmagasabb WINS) esetén.</span><span class="sxs-lookup"><span data-stu-id="7eb98-138">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="7eb98-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eb98-139">-ResourceGroupName</span></span>
<span data-ttu-id="7eb98-140">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7eb98-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7eb98-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7eb98-141">-ResourceId</span></span>
<span data-ttu-id="7eb98-142">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="7eb98-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7eb98-143">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="7eb98-143">-TargetCondition</span></span>
<span data-ttu-id="7eb98-144">Annak a célnak a feltétele, amelyben az Edge-példány érvényes.</span><span class="sxs-lookup"><span data-stu-id="7eb98-144">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="7eb98-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7eb98-145">-Confirm</span></span>
<span data-ttu-id="7eb98-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7eb98-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7eb98-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7eb98-147">-WhatIf</span></span>
<span data-ttu-id="7eb98-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7eb98-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7eb98-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7eb98-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7eb98-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eb98-150">CommonParameters</span></span>
<span data-ttu-id="7eb98-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7eb98-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eb98-152">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eb98-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eb98-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7eb98-153">INPUTS</span></span>

### <span data-ttu-id="7eb98-154">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7eb98-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7eb98-155">System. String</span><span class="sxs-lookup"><span data-stu-id="7eb98-155">System.String</span></span>

## <span data-ttu-id="7eb98-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7eb98-156">OUTPUTS</span></span>

### <span data-ttu-id="7eb98-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="7eb98-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="7eb98-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7eb98-158">NOTES</span></span>

## <span data-ttu-id="7eb98-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7eb98-159">RELATED LINKS</span></span>
