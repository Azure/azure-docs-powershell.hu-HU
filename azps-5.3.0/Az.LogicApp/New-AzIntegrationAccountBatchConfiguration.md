---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: c31768cff6af5f36212dbf32b08b016fa47c8a63
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476886"
---
# <span data-ttu-id="44714-101">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="44714-101">New-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="44714-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44714-102">SYNOPSIS</span></span>
<span data-ttu-id="44714-103">Egy integrációs fiók kötegkonfigurációját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="44714-103">Creates an integration account batch configuration.</span></span>

## <span data-ttu-id="44714-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="44714-104">SYNTAX</span></span>

### <span data-ttu-id="44714-105">ByIntegrationAccountAndParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="44714-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44714-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="44714-106">ByIntegrationAccountAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44714-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="44714-107">ByIntegrationAccountAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44714-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="44714-108">ByInputObjectAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44714-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="44714-109">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44714-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="44714-110">ByInputObjectAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44714-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="44714-111">ByResourceIdAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44714-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="44714-112">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44714-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="44714-113">ByResourceIdAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44714-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="44714-114">DESCRIPTION</span></span>
<span data-ttu-id="44714-115">A **Get-AzIntegrationAccountBatchConfiguration** parancsmag létrehoz egy új kötegkonfigurációt egy integrációs fiókban.</span><span class="sxs-lookup"><span data-stu-id="44714-115">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet creates a new batch configuration in an integration account.</span></span>

## <span data-ttu-id="44714-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="44714-116">EXAMPLES</span></span>

### <span data-ttu-id="44714-117">1. példa: Új kötegkonfiguráció létrehozása helyi fájl használatával</span><span class="sxs-lookup"><span data-stu-id="44714-117">Example 1: Create new batch configuration using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="44714-118">Létrehoz egy új kötegkonfigurációt az "$batchConfigurationFilePath" fájl elérési útjában található helyi fájl használatával.</span><span class="sxs-lookup"><span data-stu-id="44714-118">Creates a new batch configuration using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="44714-119">2. példa: Új kötegkonfiguráció létrehozása JSON-karakterlánc használatával</span><span class="sxs-lookup"><span data-stu-id="44714-119">Example 2: Create new batch configuration using a JSON string</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="44714-120">Létrehoz egy új kötegkonfigurációt a "$batchConfigurationContent" JSON karakterlánc használatával.</span><span class="sxs-lookup"><span data-stu-id="44714-120">Creates a new batch configuration using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="44714-121">3. példa: Új kötegkonfiguráció létrehozása paraméterek használatával</span><span class="sxs-lookup"><span data-stu-id="44714-121">Example 3: Create new batch configuration using parameters</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="44714-122">Új kötegkonfigurációt hoz létre az összes szükséges paraméter manuális meg biztosításával.</span><span class="sxs-lookup"><span data-stu-id="44714-122">Creates a new batch configuration by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="44714-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44714-123">PARAMETERS</span></span>

### <span data-ttu-id="44714-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="44714-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="44714-125">Az integrációs fiók kötegkonfigurációs definíciója.</span><span class="sxs-lookup"><span data-stu-id="44714-125">The integration account batch configuration definition.</span></span>

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

### <span data-ttu-id="44714-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="44714-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="44714-127">Az integrációs fiók konfigurációs fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="44714-127">The integration account batch configuration file path.</span></span>

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

### <span data-ttu-id="44714-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="44714-128">-BatchGroupName</span></span>
<span data-ttu-id="44714-129">Az integrációs fiók kötegkonfigurációs csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="44714-129">The integration account batch configuration group name.</span></span>

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

### <span data-ttu-id="44714-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="44714-130">-BatchSize</span></span>
<span data-ttu-id="44714-131">Az integrációs fiók kötegkonfigurációs kötegének mérete.</span><span class="sxs-lookup"><span data-stu-id="44714-131">The integration account batch configuration batch size.</span></span>

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

### <span data-ttu-id="44714-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44714-132">-DefaultProfile</span></span>
<span data-ttu-id="44714-133">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44714-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44714-134">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="44714-134">-MessageCount</span></span>
<span data-ttu-id="44714-135">Az integrációs fiók köteg konfigurációs üzenetszáma.</span><span class="sxs-lookup"><span data-stu-id="44714-135">The integration account batch configuration message count.</span></span>

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

### <span data-ttu-id="44714-136">-Metadata</span><span class="sxs-lookup"><span data-stu-id="44714-136">-Metadata</span></span>
<span data-ttu-id="44714-137">Az integrációs fiók kötegkonfigurációs metaadatai.</span><span class="sxs-lookup"><span data-stu-id="44714-137">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="44714-138">-Name</span><span class="sxs-lookup"><span data-stu-id="44714-138">-Name</span></span>
<span data-ttu-id="44714-139">Az integrációs fiók kötegkonfigurációs neve.</span><span class="sxs-lookup"><span data-stu-id="44714-139">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44714-140">-ParentName</span><span class="sxs-lookup"><span data-stu-id="44714-140">-ParentName</span></span>
<span data-ttu-id="44714-141">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="44714-141">The integration account name.</span></span>

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

### <span data-ttu-id="44714-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="44714-142">-ParentObject</span></span>
<span data-ttu-id="44714-143">Egy integrációs fiókobjektum.</span><span class="sxs-lookup"><span data-stu-id="44714-143">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObjectAndJson, ByInputObjectAndFilePath, ByInputObjectAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44714-144">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="44714-144">-ParentResourceId</span></span>
<span data-ttu-id="44714-145">Az integrációs fiók köteg konfigurációs erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="44714-145">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="44714-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44714-146">-ResourceGroupName</span></span>
<span data-ttu-id="44714-147">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="44714-147">The resource group name.</span></span>

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

### <span data-ttu-id="44714-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="44714-148">-ScheduleFrequency</span></span>
<span data-ttu-id="44714-149">Az integrációs fiók kötegkonfigurációs ütemezésének gyakorisága.</span><span class="sxs-lookup"><span data-stu-id="44714-149">The integration account batch configuration schedule frequency.</span></span>

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

### <span data-ttu-id="44714-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="44714-150">-ScheduleInterval</span></span>
<span data-ttu-id="44714-151">Az integrációs fiók kötegkonfigurációs ütemezési intervalluma.</span><span class="sxs-lookup"><span data-stu-id="44714-151">The integration account batch configuration schedule interval.</span></span>

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

### <span data-ttu-id="44714-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="44714-152">-ScheduleStartTime</span></span>
<span data-ttu-id="44714-153">Az integrációs fiók kötegkonfigurációs ütemezésének kezdési ideje.</span><span class="sxs-lookup"><span data-stu-id="44714-153">The integration account batch configuration schedule start time.</span></span>

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

### <span data-ttu-id="44714-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="44714-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="44714-155">Az integrációs fiók kötegkonfigurációs ütemezési időzónája.</span><span class="sxs-lookup"><span data-stu-id="44714-155">The integration account batch configuration schedule time zone.</span></span>

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

### <span data-ttu-id="44714-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44714-156">-Confirm</span></span>
<span data-ttu-id="44714-157">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="44714-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44714-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44714-158">-WhatIf</span></span>
<span data-ttu-id="44714-159">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="44714-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44714-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="44714-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44714-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44714-161">CommonParameters</span></span>
<span data-ttu-id="44714-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44714-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44714-163">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44714-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44714-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44714-164">INPUTS</span></span>

### <span data-ttu-id="44714-165">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="44714-165">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="44714-166">System.String</span><span class="sxs-lookup"><span data-stu-id="44714-166">System.String</span></span>

## <span data-ttu-id="44714-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44714-167">OUTPUTS</span></span>

### <span data-ttu-id="44714-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="44714-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="44714-169">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="44714-169">NOTES</span></span>

## <span data-ttu-id="44714-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44714-170">RELATED LINKS</span></span>
