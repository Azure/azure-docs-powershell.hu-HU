---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubconfigurationmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
ms.openlocfilehash: 85793ba3097297de646db4695cac36173bb01673
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181960"
---
# <span data-ttu-id="14793-101">Invoke-AzIotHubConfigurationMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="14793-101">Invoke-AzIotHubConfigurationMetricsQuery</span></span>

## <span data-ttu-id="14793-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="14793-102">SYNOPSIS</span></span>
<span data-ttu-id="14793-103">Hivatkozhat egy IoT-eszköz konfigurációs metrikájának lekérdezésére.</span><span class="sxs-lookup"><span data-stu-id="14793-103">Invoke an IoT device configuration metric query.</span></span>

## <span data-ttu-id="14793-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="14793-104">SYNTAX</span></span>

### <span data-ttu-id="14793-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="14793-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14793-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="14793-106">InputObjectSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14793-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="14793-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14793-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="14793-108">DESCRIPTION</span></span>
<span data-ttu-id="14793-109">A IoT-eszközök konfigurációjában definiált célzott egyéni vagy rendszermetrikus adatok kiértékelése.</span><span class="sxs-lookup"><span data-stu-id="14793-109">Evaluate a target custom or system metric defined in an IoT device configuration.</span></span>
<span data-ttu-id="14793-110">A IOT hub által számított előre definiált rendszermetrikák nem szabhatók testre.</span><span class="sxs-lookup"><span data-stu-id="14793-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="14793-111">A "célzott" kifejezés azt adja meg, hogy hány az ikreknek megfelelő eszköz a cél feltételéhez.</span><span class="sxs-lookup"><span data-stu-id="14793-111">"Targeted" specifies the number of device twins that match the target condition.</span></span>
- <span data-ttu-id="14793-112">"Alkalmazott": a konfiguráció által módosított, az ikrek által módosított eszköz számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="14793-112">"Applied" specified the number of device twins that have been modified by the configuration.</span></span> 

## <span data-ttu-id="14793-113">Példák</span><span class="sxs-lookup"><span data-stu-id="14793-113">EXAMPLES</span></span>

### <span data-ttu-id="14793-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="14793-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigurationMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "warningLimit"
```

<span data-ttu-id="14793-115">Az egyéni definiált "warningLimit" metrikájának kiértékelése</span><span class="sxs-lookup"><span data-stu-id="14793-115">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="14793-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="14793-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "applied" -MetricType "system"
```

<span data-ttu-id="14793-117">Értékelje ki a rendszer "alkalmazott" metrikáját.</span><span class="sxs-lookup"><span data-stu-id="14793-117">Evaluate the system 'applied' metric.</span></span>

## <span data-ttu-id="14793-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="14793-118">PARAMETERS</span></span>

### <span data-ttu-id="14793-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14793-119">-DefaultProfile</span></span>
<span data-ttu-id="14793-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="14793-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14793-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14793-121">-InputObject</span></span>
<span data-ttu-id="14793-122">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="14793-122">IotHub object</span></span>

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

### <span data-ttu-id="14793-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="14793-123">-IotHubName</span></span>
<span data-ttu-id="14793-124">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="14793-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="14793-125">-MetricName</span><span class="sxs-lookup"><span data-stu-id="14793-125">-MetricName</span></span>
<span data-ttu-id="14793-126">Cél mérőszáma az értékeléshez.</span><span class="sxs-lookup"><span data-stu-id="14793-126">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="14793-127">-MetricType</span><span class="sxs-lookup"><span data-stu-id="14793-127">-MetricType</span></span>
<span data-ttu-id="14793-128">Azt jelzi, hogy melyik metrika-gyűjteményt kell használni a metrika kereséséhez.</span><span class="sxs-lookup"><span data-stu-id="14793-128">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="14793-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="14793-129">-Name</span></span>
<span data-ttu-id="14793-130">A konfiguráció azonosítója.</span><span class="sxs-lookup"><span data-stu-id="14793-130">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="14793-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14793-131">-ResourceGroupName</span></span>
<span data-ttu-id="14793-132">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="14793-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="14793-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14793-133">-ResourceId</span></span>
<span data-ttu-id="14793-134">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="14793-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="14793-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="14793-135">-Confirm</span></span>
<span data-ttu-id="14793-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="14793-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14793-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14793-137">-WhatIf</span></span>
<span data-ttu-id="14793-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="14793-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14793-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="14793-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14793-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14793-140">CommonParameters</span></span>
<span data-ttu-id="14793-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="14793-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14793-142">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14793-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14793-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="14793-143">INPUTS</span></span>

### <span data-ttu-id="14793-144">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="14793-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="14793-145">System. String</span><span class="sxs-lookup"><span data-stu-id="14793-145">System.String</span></span>

## <span data-ttu-id="14793-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14793-146">OUTPUTS</span></span>

### <span data-ttu-id="14793-147">Microsoft. Azure. Command. Management. IotHub. models. PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="14793-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="14793-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="14793-148">NOTES</span></span>

## <span data-ttu-id="14793-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14793-149">RELATED LINKS</span></span>
