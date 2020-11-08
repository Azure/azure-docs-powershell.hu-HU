---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
ms.openlocfilehash: 1fac3ef0db0022bcb837392bf1c0b64e63c40401
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195961"
---
# <span data-ttu-id="b242e-101">Set-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="b242e-101">Set-AzIotHubDeployment</span></span>

## <span data-ttu-id="b242e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b242e-102">SYNOPSIS</span></span>
<span data-ttu-id="b242e-103">Frissítheti a IoT Edge-telepítések változékony mezőit.</span><span class="sxs-lookup"><span data-stu-id="b242e-103">Update the mutable fields of IoT Edge deployment.</span></span>

## <span data-ttu-id="b242e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b242e-104">SYNTAX</span></span>

### <span data-ttu-id="b242e-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b242e-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b242e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b242e-106">InputObjectSet</span></span>
```
Set-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b242e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b242e-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b242e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b242e-108">DESCRIPTION</span></span>
<span data-ttu-id="b242e-109">A IoT Edge-telepítések megadott tulajdonságainak frissítése</span><span class="sxs-lookup"><span data-stu-id="b242e-109">Update specified properties of an IoT Edge deployment.</span></span>
<span data-ttu-id="b242e-110">Megjegyzés: a konfigurációs tartalmak nem állandók.</span><span class="sxs-lookup"><span data-stu-id="b242e-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="b242e-111">A frissíthető konfigurációs tulajdonságok "címkék", "metrikák", "prioritás" és "targetCondition".</span><span class="sxs-lookup"><span data-stu-id="b242e-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="b242e-112"> https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoringTovábbi információt itt talál.</span><span class="sxs-lookup"><span data-stu-id="b242e-112">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  for more information.</span></span>

## <span data-ttu-id="b242e-113">Példák</span><span class="sxs-lookup"><span data-stu-id="b242e-113">EXAMPLES</span></span>

### <span data-ttu-id="b242e-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b242e-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="b242e-115">Módosítsa a IoT Edge központi verziójának prioritását, és frissítse a cél állapotát.</span><span class="sxs-lookup"><span data-stu-id="b242e-115">Alter the priority of IoT Edge deployment and update its target condition.</span></span>

## <span data-ttu-id="b242e-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b242e-116">PARAMETERS</span></span>

### <span data-ttu-id="b242e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b242e-117">-DefaultProfile</span></span>
<span data-ttu-id="b242e-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b242e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b242e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b242e-119">-Force</span></span>
<span data-ttu-id="b242e-120">Lehetővé teszi a telepítő objektum cseréjét akkor is, ha az utoljára a legutóbbi időpontra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="b242e-120">Allows deployment object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="b242e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b242e-121">-InputObject</span></span>
<span data-ttu-id="b242e-122">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="b242e-122">IotHub object</span></span>

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

### <span data-ttu-id="b242e-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b242e-123">-IotHubName</span></span>
<span data-ttu-id="b242e-124">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="b242e-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b242e-125">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="b242e-125">-Label</span></span>
<span data-ttu-id="b242e-126">A cél központi telepítéséhez alkalmazható címkék megfeleltetése.</span><span class="sxs-lookup"><span data-stu-id="b242e-126">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="b242e-127">-Metrikus</span><span class="sxs-lookup"><span data-stu-id="b242e-127">-Metric</span></span>
<span data-ttu-id="b242e-128">Lekérdezések gyűjteménye a IoT Edge telepítő metrikák definíciója szerint.</span><span class="sxs-lookup"><span data-stu-id="b242e-128">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="b242e-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b242e-129">-Name</span></span>
<span data-ttu-id="b242e-130">A központi telepítő azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b242e-130">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="b242e-131">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="b242e-131">-Priority</span></span>
<span data-ttu-id="b242e-132">A bevezetés súlya a versengő szabályok (legmagasabb WINS) esetén.</span><span class="sxs-lookup"><span data-stu-id="b242e-132">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="b242e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b242e-133">-ResourceGroupName</span></span>
<span data-ttu-id="b242e-134">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="b242e-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b242e-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b242e-135">-ResourceId</span></span>
<span data-ttu-id="b242e-136">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="b242e-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b242e-137">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="b242e-137">-TargetCondition</span></span>
<span data-ttu-id="b242e-138">Annak a célnak a feltétele, amelyben az Edge-példány érvényes.</span><span class="sxs-lookup"><span data-stu-id="b242e-138">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="b242e-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b242e-139">-Confirm</span></span>
<span data-ttu-id="b242e-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b242e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b242e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b242e-141">-WhatIf</span></span>
<span data-ttu-id="b242e-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b242e-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b242e-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b242e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b242e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b242e-144">CommonParameters</span></span>
<span data-ttu-id="b242e-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b242e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b242e-146">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b242e-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b242e-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b242e-147">INPUTS</span></span>

### <span data-ttu-id="b242e-148">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b242e-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b242e-149">System. String</span><span class="sxs-lookup"><span data-stu-id="b242e-149">System.String</span></span>

## <span data-ttu-id="b242e-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b242e-150">OUTPUTS</span></span>

### <span data-ttu-id="b242e-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="b242e-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="b242e-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b242e-152">NOTES</span></span>

## <span data-ttu-id="b242e-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b242e-153">RELATED LINKS</span></span>
