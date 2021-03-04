---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: b1495f4b7473225697567ca3e9d87e98107ce001
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928993"
---
# <span data-ttu-id="a1f09-101">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1f09-101">Set-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="a1f09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1f09-102">SYNOPSIS</span></span>
<span data-ttu-id="a1f09-103">Módosítja az integrációs fiók kötegkonfigurációját.</span><span class="sxs-lookup"><span data-stu-id="a1f09-103">Modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="a1f09-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a1f09-104">SYNTAX</span></span>

### <span data-ttu-id="a1f09-105">ByIntegrationAccountAndParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a1f09-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1f09-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="a1f09-106">ByIntegrationAccountAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1f09-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="a1f09-107">ByIntegrationAccountAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1f09-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="a1f09-108">ByInputObjectAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1f09-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="a1f09-109">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1f09-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="a1f09-110">ByInputObjectAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1f09-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="a1f09-111">ByResourceIdAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationDefinition <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1f09-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="a1f09-112">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1f09-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="a1f09-113">ByResourceIdAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1f09-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a1f09-114">DESCRIPTION</span></span>
<span data-ttu-id="a1f09-115">A **Set-AzIntegrationAccountBatchConfiguration** parancsmag módosítja az integrációs fiók kötegkonfigurációját.</span><span class="sxs-lookup"><span data-stu-id="a1f09-115">The **Set-AzIntegrationAccountBatchConfiguration** cmdlet modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="a1f09-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a1f09-116">EXAMPLES</span></span>

### <span data-ttu-id="a1f09-117">1. példa: Köteg-konfiguráció módosítása helyi fájl használatával</span><span class="sxs-lookup"><span data-stu-id="a1f09-117">Example 1: Modify a batch configuration using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="a1f09-118">Módosítsa a "sampleBatchConfig" nevű kötegkonfigurációt az "$batchConfigurationFilePath" fájl elérési útján.</span><span class="sxs-lookup"><span data-stu-id="a1f09-118">Modify a batch configuration named "sampleBatchConfig" using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="a1f09-119">2. példa: Köteg konfigurációjának módosítása JSON-karakterlánc használatával</span><span class="sxs-lookup"><span data-stu-id="a1f09-119">Example 2: Modify a batch configuration using a JSON string</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="a1f09-120">Módosítsa a "sampleBatchConfig" nevű kötegkonfigurációt a "$batchConfigurationContent" karakterláncot tartalmazó JSON karakterlánc használatával.</span><span class="sxs-lookup"><span data-stu-id="a1f09-120">Modify a batch configuration named "sampleBatchConfig" using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="a1f09-121">3. példa: Köteg-konfiguráció módosítása paraméterek használatával</span><span class="sxs-lookup"><span data-stu-id="a1f09-121">Example 3: Modify a batch configuration using parameters</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="a1f09-122">Módosítsa a "sampleBatchConfig" nevű kötegkonfigurációt úgy, hogy manuálisan biztosítja az összes szükséges paramétert.</span><span class="sxs-lookup"><span data-stu-id="a1f09-122">Modify a batch configuration named "sampleBatchConfig" by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="a1f09-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1f09-123">PARAMETERS</span></span>

### <span data-ttu-id="a1f09-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="a1f09-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="a1f09-125">Az integrációs fiók kötegkonfigurációs definíciója.</span><span class="sxs-lookup"><span data-stu-id="a1f09-125">The integration account batch configuration definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndJson, ByInputObjectAndJson, ByResourceIdAndJson
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1f09-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="a1f09-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="a1f09-127">Az integrációs fiók konfigurációs fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="a1f09-127">The integration account batch configuration file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByInputObjectAndFilePath, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1f09-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="a1f09-128">-BatchGroupName</span></span>
<span data-ttu-id="a1f09-129">Az integrációs fiók kötegkonfigurációs csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="a1f09-129">The integration account batch configuration group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1f09-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="a1f09-130">-BatchSize</span></span>
<span data-ttu-id="a1f09-131">Az integrációs fiók kötegkonfigurációs kötegének mérete.</span><span class="sxs-lookup"><span data-stu-id="a1f09-131">The integration account batch configuration batch size.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1f09-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1f09-132">-DefaultProfile</span></span>
<span data-ttu-id="a1f09-133">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1f09-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1f09-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1f09-134">-InputObject</span></span>
<span data-ttu-id="a1f09-135">Egy integrációs fiók kötegkonfigurációja.</span><span class="sxs-lookup"><span data-stu-id="a1f09-135">An integration account batch configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration
Parameter Sets: ByInputObjectAndJson, ByInputObjectAndFilePath, ByInputObjectAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1f09-136">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="a1f09-136">-MessageCount</span></span>
<span data-ttu-id="a1f09-137">Az integrációs fiók köteg konfigurációs üzenetszáma.</span><span class="sxs-lookup"><span data-stu-id="a1f09-137">The integration account batch configuration message count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1f09-138">-Metadata</span><span class="sxs-lookup"><span data-stu-id="a1f09-138">-Metadata</span></span>
<span data-ttu-id="a1f09-139">Az integrációs fiók kötegkonfigurációs metaadatai.</span><span class="sxs-lookup"><span data-stu-id="a1f09-139">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="a1f09-140">-Name</span><span class="sxs-lookup"><span data-stu-id="a1f09-140">-Name</span></span>
<span data-ttu-id="a1f09-141">Az integrációs fiók kötegkonfigurációs neve.</span><span class="sxs-lookup"><span data-stu-id="a1f09-141">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1f09-142">-ParentName</span><span class="sxs-lookup"><span data-stu-id="a1f09-142">-ParentName</span></span>
<span data-ttu-id="a1f09-143">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="a1f09-143">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1f09-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1f09-144">-ResourceGroupName</span></span>
<span data-ttu-id="a1f09-145">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a1f09-145">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1f09-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1f09-146">-ResourceId</span></span>
<span data-ttu-id="a1f09-147">Az integrációs fiók köteg konfigurációs erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a1f09-147">The integration account batch configuration resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdAndJson, ByResourceIdAndFilePath, ByResourceIdAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1f09-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="a1f09-148">-ScheduleFrequency</span></span>
<span data-ttu-id="a1f09-149">Az integrációs fiók kötegkonfigurációs ütemezésének gyakorisága.</span><span class="sxs-lookup"><span data-stu-id="a1f09-149">The integration account batch configuration schedule frequency.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:
Accepted values: Month, Week, Day, Hour, Minute, Second

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1f09-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="a1f09-150">-ScheduleInterval</span></span>
<span data-ttu-id="a1f09-151">Az integrációs fiók kötegkonfigurációs ütemezési intervalluma.</span><span class="sxs-lookup"><span data-stu-id="a1f09-151">The integration account batch configuration schedule interval.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1f09-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="a1f09-152">-ScheduleStartTime</span></span>
<span data-ttu-id="a1f09-153">Az integrációs fiók kötegkonfigurációs ütemezésének kezdési ideje.</span><span class="sxs-lookup"><span data-stu-id="a1f09-153">The integration account batch configuration schedule start time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1f09-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="a1f09-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="a1f09-155">Az integrációs fiók kötegkonfigurációs ütemezési időzónája.</span><span class="sxs-lookup"><span data-stu-id="a1f09-155">The integration account batch configuration schedule time zone.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1f09-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1f09-156">-Confirm</span></span>
<span data-ttu-id="a1f09-157">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a1f09-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1f09-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1f09-158">-WhatIf</span></span>
<span data-ttu-id="a1f09-159">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a1f09-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1f09-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a1f09-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1f09-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1f09-161">CommonParameters</span></span>
<span data-ttu-id="a1f09-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1f09-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1f09-163">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1f09-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1f09-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1f09-164">INPUTS</span></span>

### <span data-ttu-id="a1f09-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1f09-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="a1f09-166">System.String</span><span class="sxs-lookup"><span data-stu-id="a1f09-166">System.String</span></span>

## <span data-ttu-id="a1f09-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1f09-167">OUTPUTS</span></span>

### <span data-ttu-id="a1f09-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1f09-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="a1f09-169">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a1f09-169">NOTES</span></span>

## <span data-ttu-id="a1f09-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1f09-170">RELATED LINKS</span></span>
