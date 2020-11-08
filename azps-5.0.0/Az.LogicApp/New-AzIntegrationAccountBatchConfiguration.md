---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: c31768cff6af5f36212dbf32b08b016fa47c8a63
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195858"
---
# <span data-ttu-id="2c390-101">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c390-101">New-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="2c390-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2c390-102">SYNOPSIS</span></span>
<span data-ttu-id="2c390-103">Létrehozza az integrációs fiók kötegének konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="2c390-103">Creates an integration account batch configuration.</span></span>

## <span data-ttu-id="2c390-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2c390-104">SYNTAX</span></span>

### <span data-ttu-id="2c390-105">ByIntegrationAccountAndParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2c390-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c390-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="2c390-106">ByIntegrationAccountAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c390-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="2c390-107">ByIntegrationAccountAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c390-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="2c390-108">ByInputObjectAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c390-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="2c390-109">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c390-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="2c390-110">ByInputObjectAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c390-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="2c390-111">ByResourceIdAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c390-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="2c390-112">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c390-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="2c390-113">ByResourceIdAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c390-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="2c390-114">DESCRIPTION</span></span>
<span data-ttu-id="2c390-115">A **Get-AzIntegrationAccountBatchConfiguration** parancsmag új köteg-konfigurációt hoz létre egy integrációs fiókban.</span><span class="sxs-lookup"><span data-stu-id="2c390-115">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet creates a new batch configuration in an integration account.</span></span>

## <span data-ttu-id="2c390-116">Példák</span><span class="sxs-lookup"><span data-stu-id="2c390-116">EXAMPLES</span></span>

### <span data-ttu-id="2c390-117">1. példa: új köteg-konfiguráció létrehozása helyi fájl használatával</span><span class="sxs-lookup"><span data-stu-id="2c390-117">Example 1: Create new batch configuration using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="2c390-118">Új köteg-konfiguráció létrehozása a "$batchConfigurationFilePath" fájl elérési útján található fájl elérési útján található helyi fájl használatával.</span><span class="sxs-lookup"><span data-stu-id="2c390-118">Creates a new batch configuration using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="2c390-119">2. példa: új köteg-konfiguráció létrehozása JSON-karakterlánc használatával</span><span class="sxs-lookup"><span data-stu-id="2c390-119">Example 2: Create new batch configuration using a JSON string</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="2c390-120">Új köteg-konfiguráció létrehozása a "$batchConfigurationContent" JSON-karakterlánc használatával.</span><span class="sxs-lookup"><span data-stu-id="2c390-120">Creates a new batch configuration using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="2c390-121">3. példa: új köteg-konfiguráció létrehozása paraméterek használatával</span><span class="sxs-lookup"><span data-stu-id="2c390-121">Example 3: Create new batch configuration using parameters</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="2c390-122">Új köteg-konfiguráció létrehozása manuálisan, az összes szükséges paramétert megadva.</span><span class="sxs-lookup"><span data-stu-id="2c390-122">Creates a new batch configuration by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="2c390-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2c390-123">PARAMETERS</span></span>

### <span data-ttu-id="2c390-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="2c390-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="2c390-125">Az integrációs fiók kötegének konfigurációs definíciója.</span><span class="sxs-lookup"><span data-stu-id="2c390-125">The integration account batch configuration definition.</span></span>

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

### <span data-ttu-id="2c390-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="2c390-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="2c390-127">Az integrációs fiók kötegfájl-konfigurációs fájljának elérési útja.</span><span class="sxs-lookup"><span data-stu-id="2c390-127">The integration account batch configuration file path.</span></span>

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

### <span data-ttu-id="2c390-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="2c390-128">-BatchGroupName</span></span>
<span data-ttu-id="2c390-129">Az integrációs fiók kötegének konfigurációs csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="2c390-129">The integration account batch configuration group name.</span></span>

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

### <span data-ttu-id="2c390-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="2c390-130">-BatchSize</span></span>
<span data-ttu-id="2c390-131">Az integrációs fiók kötegének konfigurációját tartalmazó köteg mérete.</span><span class="sxs-lookup"><span data-stu-id="2c390-131">The integration account batch configuration batch size.</span></span>

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

### <span data-ttu-id="2c390-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c390-132">-DefaultProfile</span></span>
<span data-ttu-id="2c390-133">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2c390-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c390-134">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="2c390-134">-MessageCount</span></span>
<span data-ttu-id="2c390-135">Az integrációs fiók kötegelt beállítási üzeneteinek száma.</span><span class="sxs-lookup"><span data-stu-id="2c390-135">The integration account batch configuration message count.</span></span>

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

### <span data-ttu-id="2c390-136">-Metadata</span><span class="sxs-lookup"><span data-stu-id="2c390-136">-Metadata</span></span>
<span data-ttu-id="2c390-137">Az integrációs fiók kötegelt konfigurációs metaadata.</span><span class="sxs-lookup"><span data-stu-id="2c390-137">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="2c390-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2c390-138">-Name</span></span>
<span data-ttu-id="2c390-139">Az integrációs fiók kötegének neve.</span><span class="sxs-lookup"><span data-stu-id="2c390-139">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="2c390-140">-ParentName</span><span class="sxs-lookup"><span data-stu-id="2c390-140">-ParentName</span></span>
<span data-ttu-id="2c390-141">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="2c390-141">The integration account name.</span></span>

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

### <span data-ttu-id="2c390-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2c390-142">-ParentObject</span></span>
<span data-ttu-id="2c390-143">Az integrációs fiók objektuma.</span><span class="sxs-lookup"><span data-stu-id="2c390-143">An integration account object.</span></span>

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

### <span data-ttu-id="2c390-144">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2c390-144">-ParentResourceId</span></span>
<span data-ttu-id="2c390-145">Az integrációs fiók kötegének konfigurációs erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2c390-145">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="2c390-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c390-146">-ResourceGroupName</span></span>
<span data-ttu-id="2c390-147">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="2c390-147">The resource group name.</span></span>

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

### <span data-ttu-id="2c390-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="2c390-148">-ScheduleFrequency</span></span>
<span data-ttu-id="2c390-149">Az integrációs fiók kötegelt konfigurációja ütemtervének gyakorisága.</span><span class="sxs-lookup"><span data-stu-id="2c390-149">The integration account batch configuration schedule frequency.</span></span>

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

### <span data-ttu-id="2c390-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="2c390-150">-ScheduleInterval</span></span>
<span data-ttu-id="2c390-151">Az integrációs fiók kötegének ütemezési intervalluma.</span><span class="sxs-lookup"><span data-stu-id="2c390-151">The integration account batch configuration schedule interval.</span></span>

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

### <span data-ttu-id="2c390-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="2c390-152">-ScheduleStartTime</span></span>
<span data-ttu-id="2c390-153">Az integrációs fiók kötegelt beállítási ütemezése kezdési időpontja.</span><span class="sxs-lookup"><span data-stu-id="2c390-153">The integration account batch configuration schedule start time.</span></span>

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

### <span data-ttu-id="2c390-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="2c390-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="2c390-155">Az integrációs fiók kötegének konfigurációs ütemezése időzóna.</span><span class="sxs-lookup"><span data-stu-id="2c390-155">The integration account batch configuration schedule time zone.</span></span>

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

### <span data-ttu-id="2c390-156">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2c390-156">-Confirm</span></span>
<span data-ttu-id="2c390-157">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2c390-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c390-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c390-158">-WhatIf</span></span>
<span data-ttu-id="2c390-159">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2c390-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c390-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2c390-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c390-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c390-161">CommonParameters</span></span>
<span data-ttu-id="2c390-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2c390-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c390-163">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c390-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c390-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c390-164">INPUTS</span></span>

### <span data-ttu-id="2c390-165">Microsoft. Azure. Management. Logic. models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="2c390-165">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="2c390-166">System. String</span><span class="sxs-lookup"><span data-stu-id="2c390-166">System.String</span></span>

## <span data-ttu-id="2c390-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c390-167">OUTPUTS</span></span>

### <span data-ttu-id="2c390-168">Microsoft. Azure. Command. LogicApp. models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c390-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="2c390-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2c390-169">NOTES</span></span>

## <span data-ttu-id="2c390-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c390-170">RELATED LINKS</span></span>
