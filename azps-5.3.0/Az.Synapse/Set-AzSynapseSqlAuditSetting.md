---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: ae09bb11b56bd6c5fa0add402ace850fe560b293
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383205"
---
# <span data-ttu-id="cf907-101">Set-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="cf907-101">Set-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="cf907-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf907-102">SYNOPSIS</span></span>
<span data-ttu-id="cf907-103">Egy Azure Synapse Analytics Workspace naplózási beállításait módosítja.</span><span class="sxs-lookup"><span data-stu-id="cf907-103">Changes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="cf907-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cf907-104">SYNTAX</span></span>

### <span data-ttu-id="cf907-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cf907-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf907-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf907-106">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-AuditActionGroup <AuditActionGroup[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf907-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf907-107">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf907-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cf907-108">DESCRIPTION</span></span>
<span data-ttu-id="cf907-109">A **Set-AzSynapseSqlAuditSetting** parancsmag módosítja az Azure Synapse Analytics Workspace naplózási beállításait.</span><span class="sxs-lookup"><span data-stu-id="cf907-109">The **Set-AzSynapseSqlAuditSetting** cmdlet changes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>
<span data-ttu-id="cf907-110">Ha a blobtár a naplók célhelye, a *StorageAccountResourceId* paramétert megadva határozza meg a naplók tárfiókját és a *StorageKeyType* paramétert a tárkulcsok meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="cf907-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="cf907-111">A naplók megőrzési időszakának meghatározásához a *RetentionInDays* paraméter értékét is meg kell határoznia a naplók időszakának meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="cf907-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="cf907-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cf907-112">EXAMPLES</span></span>

### <span data-ttu-id="cf907-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="cf907-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

<span data-ttu-id="cf907-114">Engedélyezze a ContosoWorkspace nevű Azure Synapse Analytics Workspace blobtárhely-naplózási házirendját.</span><span class="sxs-lookup"><span data-stu-id="cf907-114">Enable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="cf907-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="cf907-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Disabled
```

<span data-ttu-id="cf907-116">Tiltsa le a ContosoWorkspace nevű Azure Synapse Analytics Workspace blobtárhely-naplózási házirendját.</span><span class="sxs-lookup"><span data-stu-id="cf907-116">Disable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="cf907-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="cf907-117">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

<span data-ttu-id="cf907-118">Engedélyezze a ContosoWorkspace nevű Azure Synapse Analytics Workspace blobtárhely-naplózási házirendját T-SQL predikátum használatával végzett speciális szűréssel.</span><span class="sxs-lookup"><span data-stu-id="cf907-118">Enable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace with advanced filtering using a T-SQL predicate.</span></span>

### <span data-ttu-id="cf907-119">4. példa</span><span class="sxs-lookup"><span data-stu-id="cf907-119">Example 4</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -PredicateExpression ""
```

<span data-ttu-id="cf907-120">Távolítsa el a speciális szűrési beállítást egy ContosoWorkspace nevű Azure Synapse Analytics Workspace naplózási házirendje alapján.</span><span class="sxs-lookup"><span data-stu-id="cf907-120">Remove the advanced filtering setting from the auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="cf907-121">5. példa</span><span class="sxs-lookup"><span data-stu-id="cf907-121">Example 5</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Set-AzSynapseSqlAuditSetting -BlobStorageTargetState Disabled
```

<span data-ttu-id="cf907-122">Tiltsa le a ContosoWorkspace nevű Azure Synapse Analytics Workspace blobtárhely-naplózási házirendját a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="cf907-122">Disable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="cf907-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf907-123">PARAMETERS</span></span>

### <span data-ttu-id="cf907-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf907-124">-AsJob</span></span>
<span data-ttu-id="cf907-125">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="cf907-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cf907-126">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="cf907-126">-AuditActionGroup</span></span>
<span data-ttu-id="cf907-127">A javasolt műveletcsoportok a következő kombinációk – ez naplóz minden lekérdezést és tárolt eljárást az adatbázison, valamint a sikeres és sikertelen bejelentkezéseket:</span><span class="sxs-lookup"><span data-stu-id="cf907-127">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>



<span data-ttu-id="cf907-128">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="cf907-128">"BATCH_COMPLETED_GROUP",</span></span>

<span data-ttu-id="cf907-129">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="cf907-129">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>

<span data-ttu-id="cf907-130">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="cf907-130">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>

<span data-ttu-id="cf907-131">Ez a fenti kombináció az alapértelmezés szerint konfigurált halmaz is.</span><span class="sxs-lookup"><span data-stu-id="cf907-131">This above combination is also the set that is configured by default.</span></span>
<span data-ttu-id="cf907-132">Ezek a csoportok az adatbázison végrehajtott összes SQL-utasításra és tárolt eljárásra vonatkoznak, és nem használhatók más csoportokkal együtt, mert ez ismétlődő naplókat eredményez.</span><span class="sxs-lookup"><span data-stu-id="cf907-132">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>

<span data-ttu-id="cf907-133">További információ: https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="cf907-133">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.AuditActionGroup[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf907-134">-BlobstorageTargetState</span><span class="sxs-lookup"><span data-stu-id="cf907-134">-BlobStorageTargetState</span></span>
<span data-ttu-id="cf907-135">Azt jelzi, hogy a blobtároló a naplórekordok célhelyét jelenti-e.</span><span class="sxs-lookup"><span data-stu-id="cf907-135">Indicates whether blob storage is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf907-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf907-136">-DefaultProfile</span></span>
<span data-ttu-id="cf907-137">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf907-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf907-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf907-138">-InputObject</span></span>
<span data-ttu-id="cf907-139">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="cf907-139">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf907-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf907-140">-PassThru</span></span>
<span data-ttu-id="cf907-141">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="cf907-141">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="cf907-142">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="cf907-142">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="cf907-143">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="cf907-143">-PredicateExpression</span></span>
<span data-ttu-id="cf907-144">A naplók szűréséhez használt T-SQL predikátum (WHERE záradék).</span><span class="sxs-lookup"><span data-stu-id="cf907-144">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="cf907-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf907-145">-ResourceGroupName</span></span>
<span data-ttu-id="cf907-146">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cf907-146">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf907-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf907-147">-ResourceId</span></span>
<span data-ttu-id="cf907-148">A Synapse-munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cf907-148">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf907-149">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="cf907-149">-RetentionInDays</span></span>
<span data-ttu-id="cf907-150">A naplók adatmegőrzési napjainak száma.</span><span class="sxs-lookup"><span data-stu-id="cf907-150">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="cf907-151">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="cf907-151">-StorageAccountResourceId</span></span>
<span data-ttu-id="cf907-152">A tárfiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="cf907-152">The storage account resource id</span></span>

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

### <span data-ttu-id="cf907-153">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="cf907-153">-StorageKeyType</span></span>
<span data-ttu-id="cf907-154">Meghatározza, hogy melyik tárelérési kulcsot kell használnia.</span><span class="sxs-lookup"><span data-stu-id="cf907-154">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf907-155">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cf907-155">-WorkspaceName</span></span>
<span data-ttu-id="cf907-156">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="cf907-156">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf907-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf907-157">-Confirm</span></span>
<span data-ttu-id="cf907-158">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cf907-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf907-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf907-159">-WhatIf</span></span>
<span data-ttu-id="cf907-160">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cf907-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf907-161">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cf907-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf907-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf907-162">CommonParameters</span></span>
<span data-ttu-id="cf907-163">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf907-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf907-164">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf907-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf907-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cf907-165">INPUTS</span></span>

### <span data-ttu-id="cf907-166">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cf907-166">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="cf907-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf907-167">OUTPUTS</span></span>

### <span data-ttu-id="cf907-168">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="cf907-168">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="cf907-169">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cf907-169">NOTES</span></span>

## <span data-ttu-id="cf907-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf907-170">RELATED LINKS</span></span>
