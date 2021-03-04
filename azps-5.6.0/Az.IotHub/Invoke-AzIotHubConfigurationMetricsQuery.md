---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubconfigurationmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
ms.openlocfilehash: 07772e7d0cbec3a2cd8241de3afa0100e1c253cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924113"
---
# <span data-ttu-id="51c67-101">Invoke-AzIotHubConfigurationMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="51c67-101">Invoke-AzIotHubConfigurationMetricsQuery</span></span>

## <span data-ttu-id="51c67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51c67-102">SYNOPSIS</span></span>
<span data-ttu-id="51c67-103">IoT-eszköz konfigurációs metrikus lekérdezésének meghívása.</span><span class="sxs-lookup"><span data-stu-id="51c67-103">Invoke an IoT device configuration metric query.</span></span>

## <span data-ttu-id="51c67-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="51c67-104">SYNTAX</span></span>

### <span data-ttu-id="51c67-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="51c67-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51c67-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="51c67-106">InputObjectSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51c67-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="51c67-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="51c67-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="51c67-108">DESCRIPTION</span></span>
<span data-ttu-id="51c67-109">Egy IoT-eszköz konfigurációjában definiált cél egyéni vagy rendszermetrikát értékel ki.</span><span class="sxs-lookup"><span data-stu-id="51c67-109">Evaluate a target custom or system metric defined in an IoT device configuration.</span></span>
<span data-ttu-id="51c67-110">Vannak előre definiált rendszermetrikák, amelyeket az Iot Hub számít ki, és nem szabhatók testre.</span><span class="sxs-lookup"><span data-stu-id="51c67-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="51c67-111">A "Célzott" a célként megadott feltételnek megfelelő eszközpárok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="51c67-111">"Targeted" specifies the number of device twins that match the target condition.</span></span>
- <span data-ttu-id="51c67-112">Az "Alkalmazva" érték a konfiguráció által módosított eszközkészletek számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="51c67-112">"Applied" specified the number of device twins that have been modified by the configuration.</span></span> 

## <span data-ttu-id="51c67-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="51c67-113">EXAMPLES</span></span>

### <span data-ttu-id="51c67-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="51c67-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigurationMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "warningLimit"
```

<span data-ttu-id="51c67-115">Kiértékelheti az egyéni "warningLimit" mutatót.</span><span class="sxs-lookup"><span data-stu-id="51c67-115">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="51c67-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="51c67-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "applied" -MetricType "system"
```

<span data-ttu-id="51c67-117">A rendszer "alkalmazott" mutatószámának kiértékelése.</span><span class="sxs-lookup"><span data-stu-id="51c67-117">Evaluate the system 'applied' metric.</span></span>

## <span data-ttu-id="51c67-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51c67-118">PARAMETERS</span></span>

### <span data-ttu-id="51c67-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51c67-119">-DefaultProfile</span></span>
<span data-ttu-id="51c67-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="51c67-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51c67-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51c67-121">-InputObject</span></span>
<span data-ttu-id="51c67-122">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="51c67-122">IotHub object</span></span>

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

### <span data-ttu-id="51c67-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="51c67-123">-IotHubName</span></span>
<span data-ttu-id="51c67-124">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="51c67-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="51c67-125">-MetricName</span><span class="sxs-lookup"><span data-stu-id="51c67-125">-MetricName</span></span>
<span data-ttu-id="51c67-126">Célmérték kiértékelési célmérték.</span><span class="sxs-lookup"><span data-stu-id="51c67-126">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="51c67-127">-MetricType</span><span class="sxs-lookup"><span data-stu-id="51c67-127">-MetricType</span></span>
<span data-ttu-id="51c67-128">Azt jelzi, hogy melyik metrikus gyűjteményt kell használni a metrikák kikereséséhez.</span><span class="sxs-lookup"><span data-stu-id="51c67-128">Indicates which metric collection should be used to lookup a metric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricType
Parameter Sets: (All)
Aliases:
Accepted values: Custom, System

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51c67-129">-Name</span><span class="sxs-lookup"><span data-stu-id="51c67-129">-Name</span></span>
<span data-ttu-id="51c67-130">A konfiguráció azonosítója.</span><span class="sxs-lookup"><span data-stu-id="51c67-130">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="51c67-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51c67-131">-ResourceGroupName</span></span>
<span data-ttu-id="51c67-132">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="51c67-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="51c67-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51c67-133">-ResourceId</span></span>
<span data-ttu-id="51c67-134">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="51c67-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="51c67-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51c67-135">-Confirm</span></span>
<span data-ttu-id="51c67-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="51c67-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51c67-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51c67-137">-WhatIf</span></span>
<span data-ttu-id="51c67-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="51c67-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51c67-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="51c67-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51c67-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51c67-140">CommonParameters</span></span>
<span data-ttu-id="51c67-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51c67-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51c67-142">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51c67-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51c67-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="51c67-143">INPUTS</span></span>

### <span data-ttu-id="51c67-144">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="51c67-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="51c67-145">System.String</span><span class="sxs-lookup"><span data-stu-id="51c67-145">System.String</span></span>

## <span data-ttu-id="51c67-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51c67-146">OUTPUTS</span></span>

### <span data-ttu-id="51c67-147">Microsoft.Azure.Commands.Management.iotHub.Models.PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="51c67-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="51c67-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="51c67-148">NOTES</span></span>

## <span data-ttu-id="51c67-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51c67-149">RELATED LINKS</span></span>
