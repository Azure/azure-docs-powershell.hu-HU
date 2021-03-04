---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 2267f9420e545fd693b734aaf8f90e89cce000a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940721"
---
# <span data-ttu-id="199cf-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="199cf-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="199cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="199cf-102">SYNOPSIS</span></span>
<span data-ttu-id="199cf-103">Speciális veszélyforrás-védelmi beállításokat ad meg egy SQL-készletben.</span><span class="sxs-lookup"><span data-stu-id="199cf-103">Sets a advanced threat protection settings on a SQL pool.</span></span>

## <span data-ttu-id="199cf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="199cf-104">SYNTAX</span></span>

### <span data-ttu-id="199cf-105">UpdateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="199cf-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>]
 [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="199cf-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="199cf-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="199cf-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="199cf-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="199cf-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="199cf-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="199cf-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="199cf-109">DESCRIPTION</span></span>
<span data-ttu-id="199cf-110">Az **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** parancsmag speciális veszélyforrás-védelmi beállításokat ad meg egy Azure Synapse Analytics SQL-készletben.</span><span class="sxs-lookup"><span data-stu-id="199cf-110">The **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="199cf-111">Ahhoz, hogy egy SQL-készletben lehetővé tegye a komplex veszélyforrások elleni védelmet, engedélyeznie kell a naplózási beállításokat az SQL-készleten.</span><span class="sxs-lookup"><span data-stu-id="199cf-111">In order to enable advanced threat protection on a SQL pool an auditing settings must be enabled on that SQL pool.</span></span>

## <span data-ttu-id="199cf-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="199cf-112">EXAMPLES</span></span>

### <span data-ttu-id="199cf-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="199cf-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="199cf-114">Ez a parancs a ContosoSqlPool nevű SQL-készlet komplex veszélyforrás-védelmi beállításait állítja be a ContosoWorkspace nevű munkaterület alatt.</span><span class="sxs-lookup"><span data-stu-id="199cf-114">This command sets the advanced threat protection settings for a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="199cf-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="199cf-115">PARAMETERS</span></span>

### <span data-ttu-id="199cf-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="199cf-116">-AsJob</span></span>
<span data-ttu-id="199cf-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="199cf-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="199cf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="199cf-118">-DefaultProfile</span></span>
<span data-ttu-id="199cf-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="199cf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="199cf-120">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="199cf-120">-EmailAdmin</span></span>
<span data-ttu-id="199cf-121">Azt határozza meg, hogy e-mail-rendszergazdáknak kell-e e-maileket küldeni.</span><span class="sxs-lookup"><span data-stu-id="199cf-121">Defines whether to email administrators.</span></span>

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

### <span data-ttu-id="199cf-122">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="199cf-122">-ExcludedDetectionType</span></span>
<span data-ttu-id="199cf-123">Kizárni a kimutatástípusokat.</span><span class="sxs-lookup"><span data-stu-id="199cf-123">Detection types to exclude.</span></span>

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

### <span data-ttu-id="199cf-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="199cf-124">-InputObject</span></span>
<span data-ttu-id="199cf-125">SQL-készlet bemeneti objektuma, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="199cf-125">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="199cf-126">-Name</span><span class="sxs-lookup"><span data-stu-id="199cf-126">-Name</span></span>
<span data-ttu-id="199cf-127">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="199cf-127">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="199cf-128">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="199cf-128">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="199cf-129">Pontosvesszővel elválasztott e-mail-címlista, amelybe az értesítéseket küldeni lehet.</span><span class="sxs-lookup"><span data-stu-id="199cf-129">A semicolon separated list of email addresses to send the alerts to.</span></span>

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

### <span data-ttu-id="199cf-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="199cf-130">-ResourceGroupName</span></span>
<span data-ttu-id="199cf-131">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="199cf-131">Resource group name.</span></span>

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

### <span data-ttu-id="199cf-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="199cf-132">-ResourceId</span></span>
<span data-ttu-id="199cf-133">A Synapse SQL-készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="199cf-133">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="199cf-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="199cf-134">-RetentionInDays</span></span>
<span data-ttu-id="199cf-135">A naplók adatmegőrzési napjainak száma.</span><span class="sxs-lookup"><span data-stu-id="199cf-135">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="199cf-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="199cf-136">-StorageAccountName</span></span>
<span data-ttu-id="199cf-137">A tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="199cf-137">The name of the storage account.</span></span>

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

### <span data-ttu-id="199cf-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="199cf-138">-WorkspaceName</span></span>
<span data-ttu-id="199cf-139">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="199cf-139">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="199cf-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="199cf-140">-WorkspaceObject</span></span>
<span data-ttu-id="199cf-141">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="199cf-141">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="199cf-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="199cf-142">-Confirm</span></span>
<span data-ttu-id="199cf-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="199cf-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="199cf-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="199cf-144">-WhatIf</span></span>
<span data-ttu-id="199cf-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="199cf-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="199cf-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="199cf-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="199cf-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="199cf-147">CommonParameters</span></span>
<span data-ttu-id="199cf-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="199cf-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="199cf-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="199cf-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="199cf-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="199cf-150">INPUTS</span></span>

### <span data-ttu-id="199cf-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="199cf-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="199cf-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="199cf-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="199cf-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="199cf-153">OUTPUTS</span></span>

### <span data-ttu-id="199cf-154">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="199cf-154">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span></span>

## <span data-ttu-id="199cf-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="199cf-155">NOTES</span></span>

## <span data-ttu-id="199cf-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="199cf-156">RELATED LINKS</span></span>
