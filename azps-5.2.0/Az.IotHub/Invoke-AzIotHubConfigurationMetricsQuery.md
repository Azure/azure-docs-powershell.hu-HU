---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubconfigurationmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
ms.openlocfilehash: 85793ba3097297de646db4695cac36173bb01673
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338670"
---
# <span data-ttu-id="d946e-101">Invoke-AzIotHubConfigurationMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="d946e-101">Invoke-AzIotHubConfigurationMetricsQuery</span></span>

## <span data-ttu-id="d946e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d946e-102">SYNOPSIS</span></span>
<span data-ttu-id="d946e-103">IoT-eszköz konfigurációs metrikus lekérdezésének meghívása.</span><span class="sxs-lookup"><span data-stu-id="d946e-103">Invoke an IoT device configuration metric query.</span></span>

## <span data-ttu-id="d946e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d946e-104">SYNTAX</span></span>

### <span data-ttu-id="d946e-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d946e-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d946e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d946e-106">InputObjectSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d946e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d946e-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d946e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d946e-108">DESCRIPTION</span></span>
<span data-ttu-id="d946e-109">Egy IoT-eszköz konfigurációjában definiált cél egyéni vagy rendszermetrikát értékel ki.</span><span class="sxs-lookup"><span data-stu-id="d946e-109">Evaluate a target custom or system metric defined in an IoT device configuration.</span></span>
<span data-ttu-id="d946e-110">Vannak előre definiált rendszermetrikák, amelyeket az Iot Hub számít ki, és nem szabhatók testre.</span><span class="sxs-lookup"><span data-stu-id="d946e-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="d946e-111">A "Célzott" a célként megadott feltételnek megfelelő eszközpárok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d946e-111">"Targeted" specifies the number of device twins that match the target condition.</span></span>
- <span data-ttu-id="d946e-112">Az "Alkalmazva" érték a konfiguráció által módosított eszközkészletek számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d946e-112">"Applied" specified the number of device twins that have been modified by the configuration.</span></span> 

## <span data-ttu-id="d946e-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d946e-113">EXAMPLES</span></span>

### <span data-ttu-id="d946e-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="d946e-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigurationMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "warningLimit"
```

<span data-ttu-id="d946e-115">Kiértékelheti az egyéni "warningLimit" mutatót.</span><span class="sxs-lookup"><span data-stu-id="d946e-115">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="d946e-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="d946e-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "applied" -MetricType "system"
```

<span data-ttu-id="d946e-117">A rendszer "alkalmazott" mutatószámának kiértékelése.</span><span class="sxs-lookup"><span data-stu-id="d946e-117">Evaluate the system 'applied' metric.</span></span>

## <span data-ttu-id="d946e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d946e-118">PARAMETERS</span></span>

### <span data-ttu-id="d946e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d946e-119">-DefaultProfile</span></span>
<span data-ttu-id="d946e-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d946e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d946e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d946e-121">-InputObject</span></span>
<span data-ttu-id="d946e-122">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="d946e-122">IotHub object</span></span>

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

### <span data-ttu-id="d946e-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d946e-123">-IotHubName</span></span>
<span data-ttu-id="d946e-124">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="d946e-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d946e-125">-MetricName</span><span class="sxs-lookup"><span data-stu-id="d946e-125">-MetricName</span></span>
<span data-ttu-id="d946e-126">Célmérték kiértékelési célmérték.</span><span class="sxs-lookup"><span data-stu-id="d946e-126">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="d946e-127">-MetricType</span><span class="sxs-lookup"><span data-stu-id="d946e-127">-MetricType</span></span>
<span data-ttu-id="d946e-128">Azt jelzi, hogy melyik metrikus gyűjteményt kell használni a metrikák kikereséséhez.</span><span class="sxs-lookup"><span data-stu-id="d946e-128">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="d946e-129">-Name</span><span class="sxs-lookup"><span data-stu-id="d946e-129">-Name</span></span>
<span data-ttu-id="d946e-130">A konfiguráció azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d946e-130">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="d946e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d946e-131">-ResourceGroupName</span></span>
<span data-ttu-id="d946e-132">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d946e-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d946e-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d946e-133">-ResourceId</span></span>
<span data-ttu-id="d946e-134">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="d946e-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d946e-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d946e-135">-Confirm</span></span>
<span data-ttu-id="d946e-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d946e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d946e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d946e-137">-WhatIf</span></span>
<span data-ttu-id="d946e-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d946e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d946e-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d946e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d946e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d946e-140">CommonParameters</span></span>
<span data-ttu-id="d946e-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d946e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d946e-142">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d946e-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d946e-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d946e-143">INPUTS</span></span>

### <span data-ttu-id="d946e-144">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d946e-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d946e-145">System.String</span><span class="sxs-lookup"><span data-stu-id="d946e-145">System.String</span></span>

## <span data-ttu-id="d946e-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d946e-146">OUTPUTS</span></span>

### <span data-ttu-id="d946e-147">Microsoft.Azure.Commands.Management.iotHub.Models.PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="d946e-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="d946e-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d946e-148">NOTES</span></span>

## <span data-ttu-id="d946e-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d946e-149">RELATED LINKS</span></span>
