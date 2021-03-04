---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: 15d553800aa51bdf4752902dadd8d5b15fcdf2f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939233"
---
# <span data-ttu-id="05aa3-101">Set-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="05aa3-101">Set-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="05aa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05aa3-102">SYNOPSIS</span></span>
<span data-ttu-id="05aa3-103">Egy Azure Synapse Analytics Workspace naplózási beállításait módosítja.</span><span class="sxs-lookup"><span data-stu-id="05aa3-103">Changes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="05aa3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="05aa3-104">SYNTAX</span></span>

### <span data-ttu-id="05aa3-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="05aa3-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05aa3-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05aa3-106">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-AuditActionGroup <AuditActionGroup[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05aa3-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="05aa3-107">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05aa3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="05aa3-108">DESCRIPTION</span></span>
<span data-ttu-id="05aa3-109">A **Set-AzSynapseSqlAuditSetting** parancsmag módosítja az Azure Synapse Analytics Workspace naplózási beállításait.</span><span class="sxs-lookup"><span data-stu-id="05aa3-109">The **Set-AzSynapseSqlAuditSetting** cmdlet changes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>
<span data-ttu-id="05aa3-110">Ha a blobtár a naplók célhelye, a *StorageAccountResourceId* paramétert megadva határozza meg a naplók tárfiókját és a *StorageKeyType* paramétert a tárkulcsok meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="05aa3-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="05aa3-111">A naplók megőrzési időszakának meghatározásához a *RetentionInDays* paraméter értékét megadva is megadhatja a naplók időszakát.</span><span class="sxs-lookup"><span data-stu-id="05aa3-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="05aa3-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="05aa3-112">EXAMPLES</span></span>

### <span data-ttu-id="05aa3-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="05aa3-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

<span data-ttu-id="05aa3-114">Engedélyezze a ContosoWorkspace nevű Azure Synapse Analytics Workspace blobtárhely-naplózási házirendját.</span><span class="sxs-lookup"><span data-stu-id="05aa3-114">Enable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="05aa3-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="05aa3-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Disabled
```

<span data-ttu-id="05aa3-116">Tiltsa le a ContosoWorkspace nevű Azure Synapse Analytics Workspace blobtárhely-naplózási házirendját.</span><span class="sxs-lookup"><span data-stu-id="05aa3-116">Disable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="05aa3-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="05aa3-117">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

<span data-ttu-id="05aa3-118">Engedélyezze a ContosoWorkspace nevű Azure Synapse Analytics Workspace blobtárhely-naplózási házirendját T-SQL predikátum használatával végzett speciális szűréssel.</span><span class="sxs-lookup"><span data-stu-id="05aa3-118">Enable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace with advanced filtering using a T-SQL predicate.</span></span>

### <span data-ttu-id="05aa3-119">4. példa</span><span class="sxs-lookup"><span data-stu-id="05aa3-119">Example 4</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -PredicateExpression ""
```

<span data-ttu-id="05aa3-120">Távolítsa el a speciális szűrési beállítást egy ContosoWorkspace nevű Azure Synapse Analytics Workspace naplózási házirendje alapján.</span><span class="sxs-lookup"><span data-stu-id="05aa3-120">Remove the advanced filtering setting from the auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="05aa3-121">5. példa</span><span class="sxs-lookup"><span data-stu-id="05aa3-121">Example 5</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Set-AzSynapseSqlAuditSetting -BlobStorageTargetState Disabled
```

<span data-ttu-id="05aa3-122">Tiltsa le a ContosoWorkspace nevű Azure Synapse Analytics Workspace blobtárhely-naplózási házirendját a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="05aa3-122">Disable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="05aa3-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05aa3-123">PARAMETERS</span></span>

### <span data-ttu-id="05aa3-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05aa3-124">-AsJob</span></span>
<span data-ttu-id="05aa3-125">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="05aa3-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05aa3-126">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="05aa3-126">-AuditActionGroup</span></span>
<span data-ttu-id="05aa3-127">A javasolt műveletcsoportok a következő kombinációk – ez naplóz minden lekérdezést és tárolt eljárást az adatbázison, valamint a sikeres és sikertelen bejelentkezéseket:</span><span class="sxs-lookup"><span data-stu-id="05aa3-127">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>



<span data-ttu-id="05aa3-128">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="05aa3-128">"BATCH_COMPLETED_GROUP",</span></span>

<span data-ttu-id="05aa3-129">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="05aa3-129">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>

<span data-ttu-id="05aa3-130">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="05aa3-130">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>

<span data-ttu-id="05aa3-131">Ez a fenti kombináció az alapértelmezés szerint konfigurált halmaz is.</span><span class="sxs-lookup"><span data-stu-id="05aa3-131">This above combination is also the set that is configured by default.</span></span>
<span data-ttu-id="05aa3-132">Ezek a csoportok az adatbázison végrehajtott összes SQL-utasításra és tárolt eljárásra vonatkoznak, és nem használhatók más csoportokkal együtt, mert ez ismétlődő naplókat eredményez.</span><span class="sxs-lookup"><span data-stu-id="05aa3-132">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>

<span data-ttu-id="05aa3-133">További információ: https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="05aa3-133">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="05aa3-134">-BlobstorageTargetState</span><span class="sxs-lookup"><span data-stu-id="05aa3-134">-BlobStorageTargetState</span></span>
<span data-ttu-id="05aa3-135">Azt jelzi, hogy a blobtároló a naplórekordok célhelyét jelenti-e.</span><span class="sxs-lookup"><span data-stu-id="05aa3-135">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="05aa3-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05aa3-136">-DefaultProfile</span></span>
<span data-ttu-id="05aa3-137">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="05aa3-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05aa3-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05aa3-138">-InputObject</span></span>
<span data-ttu-id="05aa3-139">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="05aa3-139">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="05aa3-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05aa3-140">-PassThru</span></span>
<span data-ttu-id="05aa3-141">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="05aa3-141">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="05aa3-142">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="05aa3-142">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="05aa3-143">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="05aa3-143">-PredicateExpression</span></span>
<span data-ttu-id="05aa3-144">A naplók szűréséhez használt T-SQL predikátum (WHERE záradék).</span><span class="sxs-lookup"><span data-stu-id="05aa3-144">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="05aa3-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05aa3-145">-ResourceGroupName</span></span>
<span data-ttu-id="05aa3-146">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="05aa3-146">Resource group name.</span></span>

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

### <span data-ttu-id="05aa3-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05aa3-147">-ResourceId</span></span>
<span data-ttu-id="05aa3-148">A Synapse-munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="05aa3-148">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="05aa3-149">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="05aa3-149">-RetentionInDays</span></span>
<span data-ttu-id="05aa3-150">A naplók adatmegőrzési napjainak száma.</span><span class="sxs-lookup"><span data-stu-id="05aa3-150">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="05aa3-151">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="05aa3-151">-StorageAccountResourceId</span></span>
<span data-ttu-id="05aa3-152">A tárfiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="05aa3-152">The storage account resource id</span></span>

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

### <span data-ttu-id="05aa3-153">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="05aa3-153">-StorageKeyType</span></span>
<span data-ttu-id="05aa3-154">Meghatározza, hogy melyik tárelérési kulcsot kell használnia.</span><span class="sxs-lookup"><span data-stu-id="05aa3-154">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="05aa3-155">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="05aa3-155">-WorkspaceName</span></span>
<span data-ttu-id="05aa3-156">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="05aa3-156">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="05aa3-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05aa3-157">-Confirm</span></span>
<span data-ttu-id="05aa3-158">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="05aa3-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05aa3-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05aa3-159">-WhatIf</span></span>
<span data-ttu-id="05aa3-160">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="05aa3-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05aa3-161">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="05aa3-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05aa3-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05aa3-162">CommonParameters</span></span>
<span data-ttu-id="05aa3-163">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05aa3-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05aa3-164">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05aa3-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05aa3-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="05aa3-165">INPUTS</span></span>

### <span data-ttu-id="05aa3-166">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="05aa3-166">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="05aa3-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05aa3-167">OUTPUTS</span></span>

### <span data-ttu-id="05aa3-168">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="05aa3-168">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="05aa3-169">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="05aa3-169">NOTES</span></span>

## <span data-ttu-id="05aa3-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05aa3-170">RELATED LINKS</span></span>
