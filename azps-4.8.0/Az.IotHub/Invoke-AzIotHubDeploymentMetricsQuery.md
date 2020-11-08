---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdeploymentmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
ms.openlocfilehash: 570caa5d788fae000834a7f3a79230849daf372f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184919"
---
# <span data-ttu-id="994e5-101">Invoke-AzIotHubDeploymentMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="994e5-101">Invoke-AzIotHubDeploymentMetricsQuery</span></span>

## <span data-ttu-id="994e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="994e5-102">SYNOPSIS</span></span>
<span data-ttu-id="994e5-103">Hívja fel a IoT Edge telepítő metrikus lekérdezését.</span><span class="sxs-lookup"><span data-stu-id="994e5-103">Invoke an IoT Edge deployment metric query.</span></span>

## <span data-ttu-id="994e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="994e5-104">SYNTAX</span></span>

### <span data-ttu-id="994e5-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="994e5-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="994e5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="994e5-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="994e5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="994e5-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="994e5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="994e5-108">DESCRIPTION</span></span>
<span data-ttu-id="994e5-109">Kiértékelheti a cél egyéni vagy rendszermetrikáját egy IoT-alapú példányban.</span><span class="sxs-lookup"><span data-stu-id="994e5-109">Evaluate a target custom or system metric defined in an IoT Edge deployment.</span></span>
<span data-ttu-id="994e5-110">A IOT hub által számított előre definiált rendszermetrikák nem szabhatók testre.</span><span class="sxs-lookup"><span data-stu-id="994e5-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="994e5-111">A "célzott" a IoT Edge eszközeit jeleníti meg, amelyek megfelelnek a bevezetési célzási feltételnek.</span><span class="sxs-lookup"><span data-stu-id="994e5-111">"Targeted" shows the IoT Edge devices that match the deployment targeting condition.</span></span>
- <span data-ttu-id="994e5-112">Az "alkalmazott" kifejezés azokat a célzott IoT jeleníti meg, amelyeket a magasabb prioritású példányok nem céloznak meg.</span><span class="sxs-lookup"><span data-stu-id="994e5-112">"Applied" shows the targeted IoT Edge devices that are not targeted by another deployment of higher priority.</span></span>
- <span data-ttu-id="994e5-113">A "jelentéskészítés sikere" a IoT Edge-eszközöket jeleníti meg, amelyek arról számoltak be, hogy sikeresen telepítették a modulokat.</span><span class="sxs-lookup"><span data-stu-id="994e5-113">"Reporting Success" shows the IoT Edge devices that have reported that the modules have been deployed successfully.</span></span>
- <span data-ttu-id="994e5-114">A "jelentéskészítési hiba" a IoT Edge-eszközöket jeleníti meg, amelyek arról számoltak be, hogy egy vagy több modult nem sikerült telepíteni.</span><span class="sxs-lookup"><span data-stu-id="994e5-114">"Reporting Failure" shows the IoT Edge devices that have reported that one or more modules haven't been deployed successfully.</span></span> 
  <span data-ttu-id="994e5-115">A hiba további kivizsgálásához csatlakozzon távolról a fenti eszközökhöz, és tekintse meg a naplófájlokat.</span><span class="sxs-lookup"><span data-stu-id="994e5-115">To further investigate the error, connect remotely to those devices and view the log files.</span></span>

## <span data-ttu-id="994e5-116">Példák</span><span class="sxs-lookup"><span data-stu-id="994e5-116">EXAMPLES</span></span>

### <span data-ttu-id="994e5-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="994e5-117">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeploymentMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "warningLimit"
```

<span data-ttu-id="994e5-118">Az egyéni definiált "warningLimit" metrikájának kiértékelése</span><span class="sxs-lookup"><span data-stu-id="994e5-118">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="994e5-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="994e5-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeployMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "Reporting Success" -MetricType "system"
```

<span data-ttu-id="994e5-120">Értékelje a rendszer "jelentéskészítési siker" mérőszámát.</span><span class="sxs-lookup"><span data-stu-id="994e5-120">Evaluate the system 'Reporting Success' metric.</span></span>

## <span data-ttu-id="994e5-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="994e5-121">PARAMETERS</span></span>

### <span data-ttu-id="994e5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="994e5-122">-DefaultProfile</span></span>
<span data-ttu-id="994e5-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="994e5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="994e5-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="994e5-124">-InputObject</span></span>
<span data-ttu-id="994e5-125">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="994e5-125">IotHub object</span></span>

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

### <span data-ttu-id="994e5-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="994e5-126">-IotHubName</span></span>
<span data-ttu-id="994e5-127">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="994e5-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="994e5-128">-MetricName</span><span class="sxs-lookup"><span data-stu-id="994e5-128">-MetricName</span></span>
<span data-ttu-id="994e5-129">Cél mérőszáma az értékeléshez.</span><span class="sxs-lookup"><span data-stu-id="994e5-129">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="994e5-130">-MetricType</span><span class="sxs-lookup"><span data-stu-id="994e5-130">-MetricType</span></span>
<span data-ttu-id="994e5-131">Azt jelzi, hogy melyik metrika-gyűjteményt kell használni a metrika kereséséhez.</span><span class="sxs-lookup"><span data-stu-id="994e5-131">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="994e5-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="994e5-132">-Name</span></span>
<span data-ttu-id="994e5-133">A központi telepítő azonosítója.</span><span class="sxs-lookup"><span data-stu-id="994e5-133">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="994e5-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="994e5-134">-ResourceGroupName</span></span>
<span data-ttu-id="994e5-135">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="994e5-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="994e5-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="994e5-136">-ResourceId</span></span>
<span data-ttu-id="994e5-137">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="994e5-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="994e5-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="994e5-138">-Confirm</span></span>
<span data-ttu-id="994e5-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="994e5-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="994e5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="994e5-140">-WhatIf</span></span>
<span data-ttu-id="994e5-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="994e5-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="994e5-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="994e5-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="994e5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="994e5-143">CommonParameters</span></span>
<span data-ttu-id="994e5-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="994e5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="994e5-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="994e5-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="994e5-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="994e5-146">INPUTS</span></span>

### <span data-ttu-id="994e5-147">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="994e5-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="994e5-148">System. String</span><span class="sxs-lookup"><span data-stu-id="994e5-148">System.String</span></span>

## <span data-ttu-id="994e5-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="994e5-149">OUTPUTS</span></span>

### <span data-ttu-id="994e5-150">Microsoft. Azure. Command. Management. IotHub. models. PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="994e5-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="994e5-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="994e5-151">NOTES</span></span>

## <span data-ttu-id="994e5-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="994e5-152">RELATED LINKS</span></span>