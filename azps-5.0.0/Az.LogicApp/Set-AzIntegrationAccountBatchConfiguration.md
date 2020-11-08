---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 443f93d6e9099986c9412730ba24eae3655a2b48
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195838"
---
# <span data-ttu-id="c855b-101">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c855b-101">Set-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="c855b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c855b-102">SYNOPSIS</span></span>
<span data-ttu-id="c855b-103">Módosítja az integrációs fiók kötegének konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="c855b-103">Modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="c855b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c855b-104">SYNTAX</span></span>

### <span data-ttu-id="c855b-105">ByIntegrationAccountAndParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c855b-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c855b-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="c855b-106">ByIntegrationAccountAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c855b-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="c855b-107">ByIntegrationAccountAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c855b-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="c855b-108">ByInputObjectAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c855b-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="c855b-109">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c855b-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="c855b-110">ByInputObjectAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c855b-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="c855b-111">ByResourceIdAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationDefinition <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c855b-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="c855b-112">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c855b-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="c855b-113">ByResourceIdAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c855b-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="c855b-114">DESCRIPTION</span></span>
<span data-ttu-id="c855b-115">A **set-AzIntegrationAccountBatchConfiguration** parancsmag módosította az integrációs fiók kötegének konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="c855b-115">The **Set-AzIntegrationAccountBatchConfiguration** cmdlet modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="c855b-116">Példák</span><span class="sxs-lookup"><span data-stu-id="c855b-116">EXAMPLES</span></span>

### <span data-ttu-id="c855b-117">Példa 1: kötegfájl-konfiguráció módosítása helyi fájl használatával</span><span class="sxs-lookup"><span data-stu-id="c855b-117">Example 1: Modify a batch configuration using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="c855b-118">Módosítsa a "sampleBatchConfig" nevű köteg-konfigurációt a "$batchConfigurationFilePath" fájl elérési útján található fájl elérési útján található helyi fájl segítségével.</span><span class="sxs-lookup"><span data-stu-id="c855b-118">Modify a batch configuration named "sampleBatchConfig" using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="c855b-119">2. példa: a kötegek konfigurációjának módosítása JSON-karakterlánc használatával</span><span class="sxs-lookup"><span data-stu-id="c855b-119">Example 2: Modify a batch configuration using a JSON string</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="c855b-120">Módosítsa a "sampleBatchConfig" nevű köteg-konfigurációt a "$batchConfigurationContent" nevű JSON-karakterlánc használatával.</span><span class="sxs-lookup"><span data-stu-id="c855b-120">Modify a batch configuration named "sampleBatchConfig" using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="c855b-121">3. példa: a kötegek konfigurációjának módosítása paraméterek használatával</span><span class="sxs-lookup"><span data-stu-id="c855b-121">Example 3: Modify a batch configuration using parameters</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="c855b-122">Módosítsa a "sampleBatchConfig" nevű köteg-konfigurációt a szükséges paraméterek mindegyikének manuális megadásával.</span><span class="sxs-lookup"><span data-stu-id="c855b-122">Modify a batch configuration named "sampleBatchConfig" by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="c855b-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c855b-123">PARAMETERS</span></span>

### <span data-ttu-id="c855b-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="c855b-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="c855b-125">Az integrációs fiók kötegének konfigurációs definíciója.</span><span class="sxs-lookup"><span data-stu-id="c855b-125">The integration account batch configuration definition.</span></span>

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

### <span data-ttu-id="c855b-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="c855b-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="c855b-127">Az integrációs fiók kötegfájl-konfigurációs fájljának elérési útja.</span><span class="sxs-lookup"><span data-stu-id="c855b-127">The integration account batch configuration file path.</span></span>

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

### <span data-ttu-id="c855b-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="c855b-128">-BatchGroupName</span></span>
<span data-ttu-id="c855b-129">Az integrációs fiók kötegének konfigurációs csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="c855b-129">The integration account batch configuration group name.</span></span>

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

### <span data-ttu-id="c855b-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="c855b-130">-BatchSize</span></span>
<span data-ttu-id="c855b-131">Az integrációs fiók kötegének konfigurációját tartalmazó köteg mérete.</span><span class="sxs-lookup"><span data-stu-id="c855b-131">The integration account batch configuration batch size.</span></span>

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

### <span data-ttu-id="c855b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c855b-132">-DefaultProfile</span></span>
<span data-ttu-id="c855b-133">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c855b-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c855b-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c855b-134">-InputObject</span></span>
<span data-ttu-id="c855b-135">Az integrációs fiók kötegének konfigurációja.</span><span class="sxs-lookup"><span data-stu-id="c855b-135">An integration account batch configuration.</span></span>

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

### <span data-ttu-id="c855b-136">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="c855b-136">-MessageCount</span></span>
<span data-ttu-id="c855b-137">Az integrációs fiók kötegelt beállítási üzeneteinek száma.</span><span class="sxs-lookup"><span data-stu-id="c855b-137">The integration account batch configuration message count.</span></span>

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

### <span data-ttu-id="c855b-138">-Metadata</span><span class="sxs-lookup"><span data-stu-id="c855b-138">-Metadata</span></span>
<span data-ttu-id="c855b-139">Az integrációs fiók kötegelt konfigurációs metaadata.</span><span class="sxs-lookup"><span data-stu-id="c855b-139">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="c855b-140">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c855b-140">-Name</span></span>
<span data-ttu-id="c855b-141">Az integrációs fiók kötegének neve.</span><span class="sxs-lookup"><span data-stu-id="c855b-141">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="c855b-142">-ParentName</span><span class="sxs-lookup"><span data-stu-id="c855b-142">-ParentName</span></span>
<span data-ttu-id="c855b-143">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="c855b-143">The integration account name.</span></span>

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

### <span data-ttu-id="c855b-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c855b-144">-ResourceGroupName</span></span>
<span data-ttu-id="c855b-145">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c855b-145">The resource group name.</span></span>

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

### <span data-ttu-id="c855b-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c855b-146">-ResourceId</span></span>
<span data-ttu-id="c855b-147">Az integrációs fiók kötegének konfigurációs erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c855b-147">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="c855b-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="c855b-148">-ScheduleFrequency</span></span>
<span data-ttu-id="c855b-149">Az integrációs fiók kötegelt konfigurációja ütemtervének gyakorisága.</span><span class="sxs-lookup"><span data-stu-id="c855b-149">The integration account batch configuration schedule frequency.</span></span>

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

### <span data-ttu-id="c855b-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="c855b-150">-ScheduleInterval</span></span>
<span data-ttu-id="c855b-151">Az integrációs fiók kötegének ütemezési intervalluma.</span><span class="sxs-lookup"><span data-stu-id="c855b-151">The integration account batch configuration schedule interval.</span></span>

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

### <span data-ttu-id="c855b-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="c855b-152">-ScheduleStartTime</span></span>
<span data-ttu-id="c855b-153">Az integrációs fiók kötegelt beállítási ütemezése kezdési időpontja.</span><span class="sxs-lookup"><span data-stu-id="c855b-153">The integration account batch configuration schedule start time.</span></span>

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

### <span data-ttu-id="c855b-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="c855b-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="c855b-155">Az integrációs fiók kötegének konfigurációs ütemezése időzóna.</span><span class="sxs-lookup"><span data-stu-id="c855b-155">The integration account batch configuration schedule time zone.</span></span>

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

### <span data-ttu-id="c855b-156">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c855b-156">-Confirm</span></span>
<span data-ttu-id="c855b-157">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c855b-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c855b-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c855b-158">-WhatIf</span></span>
<span data-ttu-id="c855b-159">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c855b-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c855b-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c855b-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c855b-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c855b-161">CommonParameters</span></span>
<span data-ttu-id="c855b-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c855b-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c855b-163">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c855b-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c855b-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c855b-164">INPUTS</span></span>

### <span data-ttu-id="c855b-165">Microsoft. Azure. Command. LogicApp. models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c855b-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="c855b-166">System. String</span><span class="sxs-lookup"><span data-stu-id="c855b-166">System.String</span></span>

## <span data-ttu-id="c855b-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c855b-167">OUTPUTS</span></span>

### <span data-ttu-id="c855b-168">Microsoft. Azure. Command. LogicApp. models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c855b-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="c855b-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c855b-169">NOTES</span></span>

## <span data-ttu-id="c855b-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c855b-170">RELATED LINKS</span></span>