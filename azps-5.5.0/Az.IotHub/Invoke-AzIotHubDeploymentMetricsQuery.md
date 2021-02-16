---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdeploymentmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
ms.openlocfilehash: 570caa5d788fae000834a7f3a79230849daf372f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167347"
---
# <span data-ttu-id="29367-101">Invoke-AzIotHubDeploymentMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="29367-101">Invoke-AzIotHubDeploymentMetricsQuery</span></span>

## <span data-ttu-id="29367-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29367-102">SYNOPSIS</span></span>
<span data-ttu-id="29367-103">Az IoT Edge üzembe helyezési metrikus lekérdezésének meghívása.</span><span class="sxs-lookup"><span data-stu-id="29367-103">Invoke an IoT Edge deployment metric query.</span></span>

## <span data-ttu-id="29367-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="29367-104">SYNTAX</span></span>

### <span data-ttu-id="29367-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="29367-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29367-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="29367-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29367-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="29367-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29367-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="29367-108">DESCRIPTION</span></span>
<span data-ttu-id="29367-109">Egy IoT Edge-telepítésben definiált cél egyéni vagy rendszermetrikát értékel ki.</span><span class="sxs-lookup"><span data-stu-id="29367-109">Evaluate a target custom or system metric defined in an IoT Edge deployment.</span></span>
<span data-ttu-id="29367-110">Vannak előre definiált rendszermetrikák, amelyeket az Iot Hub számít ki, és nem szabhatók testre.</span><span class="sxs-lookup"><span data-stu-id="29367-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="29367-111">A "Célzott" szó azokat az IoT Edge-eszközöket jeleníti meg, amelyek megfelelnek a központi telepítés célcsoport-építési feltételének.</span><span class="sxs-lookup"><span data-stu-id="29367-111">"Targeted" shows the IoT Edge devices that match the deployment targeting condition.</span></span>
- <span data-ttu-id="29367-112">Az "Alkalmazva" érték azokat a célzott IoT Edge-eszközöket jeleníti meg, amelyekre nem egy magasabb prioritású másik telepítés van megcélva.</span><span class="sxs-lookup"><span data-stu-id="29367-112">"Applied" shows the targeted IoT Edge devices that are not targeted by another deployment of higher priority.</span></span>
- <span data-ttu-id="29367-113">A "Sikeres jelentés" az IoT Edge-eszközökhöz azt jelzi, hogy a modulok telepítése sikeresen megtörtént.</span><span class="sxs-lookup"><span data-stu-id="29367-113">"Reporting Success" shows the IoT Edge devices that have reported that the modules have been deployed successfully.</span></span>
- <span data-ttu-id="29367-114">A "Hiba bejelentése" az IoT Edge eszközeit jeleníti meg, amelyek arról számoltak be, hogy egy vagy több modul telepítése nem sikerült.</span><span class="sxs-lookup"><span data-stu-id="29367-114">"Reporting Failure" shows the IoT Edge devices that have reported that one or more modules haven't been deployed successfully.</span></span> 
  <span data-ttu-id="29367-115">A hiba további vizsgálatához csatlakozzon távolról az adott eszközökhöz, és tekintse meg a naplófájlokat.</span><span class="sxs-lookup"><span data-stu-id="29367-115">To further investigate the error, connect remotely to those devices and view the log files.</span></span>

## <span data-ttu-id="29367-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="29367-116">EXAMPLES</span></span>

### <span data-ttu-id="29367-117">1. példa</span><span class="sxs-lookup"><span data-stu-id="29367-117">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeploymentMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "warningLimit"
```

<span data-ttu-id="29367-118">Kiértékelheti az egyéni "warningLimit" mutatót.</span><span class="sxs-lookup"><span data-stu-id="29367-118">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="29367-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="29367-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeployMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "Reporting Success" -MetricType "system"
```

<span data-ttu-id="29367-120">A rendszer "Sikeres jelentés" mutatószámának kiértékelése.</span><span class="sxs-lookup"><span data-stu-id="29367-120">Evaluate the system 'Reporting Success' metric.</span></span>

## <span data-ttu-id="29367-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29367-121">PARAMETERS</span></span>

### <span data-ttu-id="29367-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29367-122">-DefaultProfile</span></span>
<span data-ttu-id="29367-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="29367-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29367-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29367-124">-InputObject</span></span>
<span data-ttu-id="29367-125">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="29367-125">IotHub object</span></span>

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

### <span data-ttu-id="29367-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="29367-126">-IotHubName</span></span>
<span data-ttu-id="29367-127">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="29367-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="29367-128">-MetricName</span><span class="sxs-lookup"><span data-stu-id="29367-128">-MetricName</span></span>
<span data-ttu-id="29367-129">Célmérték kiértékelési célmérték.</span><span class="sxs-lookup"><span data-stu-id="29367-129">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="29367-130">-MetricType</span><span class="sxs-lookup"><span data-stu-id="29367-130">-MetricType</span></span>
<span data-ttu-id="29367-131">Azt jelzi, hogy melyik metrikus gyűjteményt kell használni a metrikák kikereséséhez.</span><span class="sxs-lookup"><span data-stu-id="29367-131">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="29367-132">-Name</span><span class="sxs-lookup"><span data-stu-id="29367-132">-Name</span></span>
<span data-ttu-id="29367-133">A központi telepítés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="29367-133">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="29367-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29367-134">-ResourceGroupName</span></span>
<span data-ttu-id="29367-135">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="29367-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="29367-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29367-136">-ResourceId</span></span>
<span data-ttu-id="29367-137">IotHub erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="29367-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="29367-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29367-138">-Confirm</span></span>
<span data-ttu-id="29367-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="29367-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29367-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29367-140">-WhatIf</span></span>
<span data-ttu-id="29367-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="29367-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29367-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="29367-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29367-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29367-143">CommonParameters</span></span>
<span data-ttu-id="29367-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29367-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29367-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29367-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29367-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="29367-146">INPUTS</span></span>

### <span data-ttu-id="29367-147">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="29367-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="29367-148">System.String</span><span class="sxs-lookup"><span data-stu-id="29367-148">System.String</span></span>

## <span data-ttu-id="29367-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29367-149">OUTPUTS</span></span>

### <span data-ttu-id="29367-150">Microsoft.Azure.Commands.Management.iotHub.Models.PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="29367-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="29367-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="29367-151">NOTES</span></span>

## <span data-ttu-id="29367-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29367-152">RELATED LINKS</span></span>
