---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 2a81030cdf985ae338692e59d86da30cee50694f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495229"
---
# <span data-ttu-id="87445-101">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="87445-101">Set-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="87445-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="87445-102">SYNOPSIS</span></span>
<span data-ttu-id="87445-103">Az Azure SQL Server-kiszolgálók naplózási beállításainak módosítása</span><span class="sxs-lookup"><span data-stu-id="87445-103">Changes the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87445-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="87445-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87445-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="87445-105">DESCRIPTION</span></span>
<span data-ttu-id="87445-106">A **set-AzureRmSqlServerAuditing** parancsmag az Azure SQL Server-kiszolgálók naplózási beállításait módosítja.</span><span class="sxs-lookup"><span data-stu-id="87445-106">The **Set-AzureRmSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="87445-107">A parancsmag használatához a *ResourceGroupName* és a *kiszolgálónév* paraméterrel keresse meg a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="87445-107">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="87445-108">Adja meg a *StorageAccountName* paramétert a naplók tárolási fiókjának a megadásához, illetve a *StorageKeyType* paramétert a tárolási kulcsok meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="87445-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="87445-109">A házirend engedélyezéséhez vagy letiltásához használja az *állami* paramétert.</span><span class="sxs-lookup"><span data-stu-id="87445-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="87445-110">A naplók adatmegőrzését úgy is megadhatja, hogy az *RetentionInDays* paraméter értékét adja meg a naplók időszakának meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="87445-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="87445-111">A parancsmag sikeres futtatását követően a megadott Azure SQL-kiszolgálón megadott Azure SQL-adatbázisok naplózása engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="87445-111">After the cmdlet runs successfully, auditing of the Azure SQL databases that are defined in the specified Azure SQL server is enabled.</span></span>
<span data-ttu-id="87445-112">Ha a parancsmag sikerrel jár, és a *PassThru* paramétert használja, a kiszolgálói azonosítók mellett egy olyan objektumot ad eredményül, amely leírja az aktuális blob-naplózási házirendet.</span><span class="sxs-lookup"><span data-stu-id="87445-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the server identifiers.</span></span>
<span data-ttu-id="87445-113">A kiszolgálói azonosítók tartalmazzák, de nem korlátozódnak a **ResourceGroupName** és a **kiszolgáló_neve** -ra.</span><span class="sxs-lookup"><span data-stu-id="87445-113">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="87445-114">Példák</span><span class="sxs-lookup"><span data-stu-id="87445-114">EXAMPLES</span></span>

### <span data-ttu-id="87445-115">1. példa: az Azure SQL Server-kiszolgálók naplózási házirendjének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="87445-115">Example 1: Enable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="87445-116">2. példa: az Azure SQL Server-kiszolgálók naplózási házirendjének letiltása</span><span class="sxs-lookup"><span data-stu-id="87445-116">Example 2: Disable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

## <span data-ttu-id="87445-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="87445-117">PARAMETERS</span></span>

### <span data-ttu-id="87445-118">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="87445-118">-AuditActionGroup</span></span>
<span data-ttu-id="87445-119">A használni kívánt műveleti csoportok a következő kombinációk: Ez a művelet naplózza az adatbázissal végzett összes lekérdezést és tárolt eljárást, valamint a sikeres és sikertelen bejelentkezéseket:</span><span class="sxs-lookup"><span data-stu-id="87445-119">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="87445-120">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="87445-120">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="87445-121">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="87445-121">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="87445-122">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="87445-122">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  

<span data-ttu-id="87445-123">Ez a fenti kombináció egyben az alapértelmezés szerint konfigurált halmaz.</span><span class="sxs-lookup"><span data-stu-id="87445-123">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="87445-124">Ezek a csoportok az adatbázissal szemben végrehajtott összes SQL-utasítást és tárolt eljárást lefoglalják, és nem használhatók együtt más csoportokkal, mert ez a művelet duplikálja a naplókat.</span><span class="sxs-lookup"><span data-stu-id="87445-124">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="87445-125">További információ: https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="87445-125">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, AUDIT_CHANGE_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87445-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87445-126">-DefaultProfile</span></span>
<span data-ttu-id="87445-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="87445-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87445-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87445-128">-PassThru</span></span>
<span data-ttu-id="87445-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="87445-129">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87445-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87445-130">-ResourceGroupName</span></span>
<span data-ttu-id="87445-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="87445-131">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87445-132">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="87445-132">-RetentionInDays</span></span>
<span data-ttu-id="87445-133">A naplók retenciós napjainak száma.</span><span class="sxs-lookup"><span data-stu-id="87445-133">The number of retention days for the audit logs.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87445-134">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="87445-134">-ServerName</span></span>
<span data-ttu-id="87445-135">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="87445-135">SQL server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87445-136">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="87445-136">-State</span></span>
<span data-ttu-id="87445-137">A házirend állapota.</span><span class="sxs-lookup"><span data-stu-id="87445-137">The state of the policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87445-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="87445-138">-StorageAccountName</span></span>
<span data-ttu-id="87445-139">A tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="87445-139">The name of the storage account.</span></span> <span data-ttu-id="87445-140">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="87445-140">Wildcard characters are not permitted.</span></span>  
<span data-ttu-id="87445-141">Ehhez a paraméterhez nincs szükség.</span><span class="sxs-lookup"><span data-stu-id="87445-141">This parameter is not required.</span></span>  
<span data-ttu-id="87445-142">Ha nem adja meg ezt a paramétert, a parancsmag a korábban a naplózási házirend részeként megadott tárolási fiókot használja.</span><span class="sxs-lookup"><span data-stu-id="87445-142">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>  
<span data-ttu-id="87445-143">Ha most először adja meg a naplózási házirendet, és nem adja meg ezt a paramétert, a parancsmag nem működik.</span><span class="sxs-lookup"><span data-stu-id="87445-143">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87445-144">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="87445-144">-StorageKeyType</span></span>
<span data-ttu-id="87445-145">Itt adhatja meg, hogy a tárterület-hozzáférési kulcsok közül melyik használható.</span><span class="sxs-lookup"><span data-stu-id="87445-145">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87445-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="87445-146">-Confirm</span></span>
<span data-ttu-id="87445-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="87445-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87445-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87445-148">-WhatIf</span></span>
<span data-ttu-id="87445-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="87445-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87445-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="87445-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87445-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87445-151">CommonParameters</span></span>
<span data-ttu-id="87445-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="87445-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87445-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87445-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87445-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="87445-154">INPUTS</span></span>

### <span data-ttu-id="87445-155">Nincs</span><span class="sxs-lookup"><span data-stu-id="87445-155">None</span></span>
<span data-ttu-id="87445-156">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="87445-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="87445-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87445-157">OUTPUTS</span></span>

### <span data-ttu-id="87445-158">Microsoft. Azure. Command. SQL. Security. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="87445-158">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="87445-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="87445-159">NOTES</span></span>

## <span data-ttu-id="87445-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87445-160">RELATED LINKS</span></span>
