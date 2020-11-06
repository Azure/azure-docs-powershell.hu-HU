---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: a6d09b573225efa5f8467e9ca02edb65a87ebe10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495522"
---
# <span data-ttu-id="5a43a-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="5a43a-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="5a43a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5a43a-102">SYNOPSIS</span></span>
<span data-ttu-id="5a43a-103">Az Azure SQL-adatbázisok naplózási beállításainak módosítása</span><span class="sxs-lookup"><span data-stu-id="5a43a-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a43a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5a43a-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a43a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5a43a-105">DESCRIPTION</span></span>
<span data-ttu-id="5a43a-106">A **set-AzureRmSqlDatabaseAuditing** parancsmag egy Azure SQL-adatbázis naplózási beállításait módosítja.</span><span class="sxs-lookup"><span data-stu-id="5a43a-106">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="5a43a-107">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paraméterrel keresse meg az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="5a43a-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="5a43a-108">Adja meg a *StorageAccountName* paramétert a naplók tárolási fiókjának a megadásához, illetve a *StorageKeyType* paramétert a tárolási kulcsok meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="5a43a-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="5a43a-109">A házirend engedélyezéséhez vagy letiltásához használja az *állami* paramétert.</span><span class="sxs-lookup"><span data-stu-id="5a43a-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="5a43a-110">A naplók adatmegőrzését úgy is megadhatja, hogy az *RetentionInDays* paraméter értékét adja meg a naplók időszakának meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="5a43a-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="5a43a-111">A parancsmag sikeres futtatása után az adatbázis naplózása engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="5a43a-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="5a43a-112">Ha a parancsmag sikerrel jár, és a *PassThru* paramétert használja, az adatbázis-azonosítók mellett egy olyan objektumot ad eredményül, amely leírja az aktuális blob-naplózási házirendet.</span><span class="sxs-lookup"><span data-stu-id="5a43a-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="5a43a-113">Az adatbázis-azonosítók közé tartoznak a következők: a **ResourceGroupName** , a **kiszolgálónév** és a **databasename**.</span><span class="sxs-lookup"><span data-stu-id="5a43a-113">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="5a43a-114">Példák</span><span class="sxs-lookup"><span data-stu-id="5a43a-114">EXAMPLES</span></span>

### <span data-ttu-id="5a43a-115">1. példa: az Azure SQL-adatbázisok naplózási házirendjének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="5a43a-115">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="5a43a-116">2. példa: az Azure SQL-adatbázisok blob-naplózási házirendjének letiltása</span><span class="sxs-lookup"><span data-stu-id="5a43a-116">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

## <span data-ttu-id="5a43a-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5a43a-117">PARAMETERS</span></span>

### <span data-ttu-id="5a43a-118">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="5a43a-118">-AuditAction</span></span>
<span data-ttu-id="5a43a-119">A naplózási műveletek halmaza</span><span class="sxs-lookup"><span data-stu-id="5a43a-119">The set of the audit actions</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a43a-120">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="5a43a-120">-AuditActionGroup</span></span>
<span data-ttu-id="5a43a-121">A naplózási műveletek csoportjának készlete</span><span class="sxs-lookup"><span data-stu-id="5a43a-121">The set of the audit action groups</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases: 
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a43a-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5a43a-122">-DatabaseName</span></span>
<span data-ttu-id="5a43a-123">SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="5a43a-123">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a43a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a43a-124">-PassThru</span></span>
<span data-ttu-id="5a43a-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5a43a-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5a43a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a43a-126">-ResourceGroupName</span></span>
<span data-ttu-id="5a43a-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5a43a-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a43a-128">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="5a43a-128">-RetentionInDays</span></span>
<span data-ttu-id="5a43a-129">A naplók adatmegőrzési napjainak száma</span><span class="sxs-lookup"><span data-stu-id="5a43a-129">The number of retention days for the audit logs</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a43a-130">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="5a43a-130">-ServerName</span></span>
<span data-ttu-id="5a43a-131">SQL-adatbázis kiszolgálójának neve</span><span class="sxs-lookup"><span data-stu-id="5a43a-131">SQL Database server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a43a-132">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="5a43a-132">-State</span></span>
<span data-ttu-id="5a43a-133">A naplózási házirend állapota</span><span class="sxs-lookup"><span data-stu-id="5a43a-133">The state of the auditing policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a43a-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5a43a-134">-StorageAccountName</span></span>
<span data-ttu-id="5a43a-135">A tárolási fiók neve</span><span class="sxs-lookup"><span data-stu-id="5a43a-135">The name of the storage account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a43a-136">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="5a43a-136">-StorageKeyType</span></span>
<span data-ttu-id="5a43a-137">A tárolási kulcs típusa</span><span class="sxs-lookup"><span data-stu-id="5a43a-137">The type of the storage key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a43a-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5a43a-138">-Confirm</span></span>
<span data-ttu-id="5a43a-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5a43a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a43a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a43a-140">-WhatIf</span></span>
<span data-ttu-id="5a43a-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5a43a-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a43a-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5a43a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a43a-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a43a-143">-DefaultProfile</span></span>
<span data-ttu-id="5a43a-144">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a43a-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a43a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a43a-145">CommonParameters</span></span>
<span data-ttu-id="5a43a-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5a43a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a43a-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a43a-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a43a-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a43a-148">INPUTS</span></span>

## <span data-ttu-id="5a43a-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a43a-149">OUTPUTS</span></span>

### <span data-ttu-id="5a43a-150">Microsoft. Azure. Command. SQL. Security. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="5a43a-150">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="5a43a-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5a43a-151">NOTES</span></span>

## <span data-ttu-id="5a43a-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a43a-152">RELATED LINKS</span></span>

