---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 4fb27d1d822d72de9564e9acc900122016940c6d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334698"
---
# <span data-ttu-id="35583-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="35583-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="35583-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35583-102">SYNOPSIS</span></span>
<span data-ttu-id="35583-103">Frissíti a komplex veszélyforrások elleni védelem speciális beállításait egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="35583-103">Updates an advanced threat protection settings on a workspace.</span></span>

## <span data-ttu-id="35583-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="35583-104">SYNTAX</span></span>

### <span data-ttu-id="35583-105">UpdateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="35583-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35583-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35583-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35583-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="35583-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-NotificationRecipientsEmail <String>]
 [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="35583-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="35583-108">DESCRIPTION</span></span>
<span data-ttu-id="35583-109">**AzSynapseSqlAdvancedThreatProtectionSetting** parancsmagja egy Azure Synapse Analytics Workspace komplex veszélyforrás-védelmi beállításait frissíti.</span><span class="sxs-lookup"><span data-stu-id="35583-109">The **Update-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet updates an advanced threat protection settings on an Azure Synapse Analytics Workspace.</span></span> <span data-ttu-id="35583-110">Ahhoz, hogy a komplex veszélyforrások elleni védelem speciálisan elérhető legyen egy munkaterületen, engedélyezni kell a naplózási beállításokat az ott található munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="35583-110">In order to enable advanced threat protection on a workspace an auditing settings must be enabled on that workspace.</span></span>

## <span data-ttu-id="35583-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="35583-111">EXAMPLES</span></span>

### <span data-ttu-id="35583-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="35583-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -NotificationRecipientsEmail "admin01@contoso.com;secadmin@contoso.com" -EmailAdmin $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="35583-113">Ez a parancs frissíti a ContosoWorkspace nevű munkaterület komplex veszélyforrás-védelmi beállításait.</span><span class="sxs-lookup"><span data-stu-id="35583-113">This command updates the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="35583-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35583-114">PARAMETERS</span></span>

### <span data-ttu-id="35583-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35583-115">-AsJob</span></span>
<span data-ttu-id="35583-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="35583-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35583-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35583-117">-DefaultProfile</span></span>
<span data-ttu-id="35583-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="35583-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35583-119">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="35583-119">-EmailAdmin</span></span>
<span data-ttu-id="35583-120">Azt határozza meg, hogy e-mail-rendszergazdáknak kell-e e-maileket küldeni.</span><span class="sxs-lookup"><span data-stu-id="35583-120">Defines whether to email administrators.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: EmailAdmins

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35583-121">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="35583-121">-ExcludedDetectionType</span></span>
<span data-ttu-id="35583-122">Kizárni a kimutatástípusokat.</span><span class="sxs-lookup"><span data-stu-id="35583-122">Detection types to exclude.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35583-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35583-123">-InputObject</span></span>
<span data-ttu-id="35583-124">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="35583-124">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35583-125">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="35583-125">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="35583-126">Pontosvesszővel elválasztott e-mail-címlista, amelybe az értesítéseket küldeni lehet.</span><span class="sxs-lookup"><span data-stu-id="35583-126">A semicolon separated list of email addresses to send the alerts to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NotificationRecipientsEmails

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35583-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35583-127">-ResourceGroupName</span></span>
<span data-ttu-id="35583-128">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="35583-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35583-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35583-129">-ResourceId</span></span>
<span data-ttu-id="35583-130">A Synapse-munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="35583-130">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35583-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="35583-131">-RetentionInDays</span></span>
<span data-ttu-id="35583-132">A naplók adatmegőrzési napjainak száma.</span><span class="sxs-lookup"><span data-stu-id="35583-132">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35583-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="35583-133">-StorageAccountName</span></span>
<span data-ttu-id="35583-134">A tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="35583-134">The name of the storage account.</span></span>

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

### <span data-ttu-id="35583-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="35583-135">-WorkspaceName</span></span>
<span data-ttu-id="35583-136">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="35583-136">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35583-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35583-137">-Confirm</span></span>
<span data-ttu-id="35583-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="35583-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35583-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35583-139">-WhatIf</span></span>
<span data-ttu-id="35583-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="35583-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35583-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="35583-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35583-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35583-142">CommonParameters</span></span>
<span data-ttu-id="35583-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35583-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35583-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35583-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35583-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35583-145">INPUTS</span></span>

### <span data-ttu-id="35583-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="35583-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="35583-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35583-147">OUTPUTS</span></span>

### <span data-ttu-id="35583-148">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="35583-148">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="35583-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="35583-149">NOTES</span></span>

## <span data-ttu-id="35583-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35583-150">RELATED LINKS</span></span>
