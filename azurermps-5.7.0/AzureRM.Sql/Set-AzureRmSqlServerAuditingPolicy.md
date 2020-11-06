---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4FCC7D8B-A46E-4E5B-8BE2-F62B3D3E715D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: ee54928b1f32c726bc2847eace77e6ccbe48c4d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495228"
---
# <span data-ttu-id="29b90-101">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="29b90-101">Set-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="29b90-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29b90-102">SYNOPSIS</span></span>
<span data-ttu-id="29b90-103">Módosítja egy SQL-adatbázis kiszolgálójának naplózási házirendjét.</span><span class="sxs-lookup"><span data-stu-id="29b90-103">Changes the auditing policy of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29b90-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29b90-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditingPolicy [-AuditType <AuditType>] [-AuditActionGroup <AuditActionGroups[]>]
 [-PassThru] [-EventType <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-TableIdentifier <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29b90-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="29b90-105">DESCRIPTION</span></span>
<span data-ttu-id="29b90-106">A **set-AzureRmSqlServerAuditingPolicy** parancsmag egy Azure SQL-adatbázis kiszolgálójának naplózási házirendjét módosítja.</span><span class="sxs-lookup"><span data-stu-id="29b90-106">The **Set-AzureRmSqlServerAuditingPolicy** cmdlet changes the auditing policy of an Azure SQL Database server.</span></span>
<span data-ttu-id="29b90-107">Adja meg a *ResourceGroupName* és a *kiszolgálónév* paramétert a kiszolgáló meghatározásához, a *StorageAccountName* paraméterrel megadhatja a naplók tárolási fiókját, és a *StorageKeyType* paraméterrel meghatározhatja a használható tárterület-kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="29b90-107">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server, the *StorageAccountName* parameter to specify the storage account for the audit logs, and the *StorageKeyType* parameter to define the storage keys to use.</span></span>

<span data-ttu-id="29b90-108">Azt is megadhatja, hogy az *RetentionInDays* és a *TableIdentifier* paramétereinek értéke megadásával meghatározza a naplózási naplók tábla adatmegőrzési listáját.</span><span class="sxs-lookup"><span data-stu-id="29b90-108">You can also define retention for the audit logs table by setting the value of the *RetentionInDays* and *TableIdentifier* parameters to define the period and the seed for the audit log table names.</span></span>
<span data-ttu-id="29b90-109">Adja meg a *EventType* paramétert annak meghatározásához, hogy milyen típusú események legyenek naplózva.</span><span class="sxs-lookup"><span data-stu-id="29b90-109">Specify the *EventType* parameter to define which event types to audit.</span></span>
<span data-ttu-id="29b90-110">A parancsmag futtatását követően a kiszolgáló házirendjét használó adatbázisok naplózása engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="29b90-110">After you run this cmdlet, auditing of the databases that use the policy of this server is enabled.</span></span>
<span data-ttu-id="29b90-111">Ha a parancsmag sikerrel jár, és a *PassThru* paramétert adja meg, a parancsmag egy olyan objektumot ad eredményül, amely leírja a jelenlegi naplózási házirendet, valamint a kiszolgálói azonosítókat.</span><span class="sxs-lookup"><span data-stu-id="29b90-111">If the cmdlet succeeds and you specify the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy, and the server identifiers.</span></span>
<span data-ttu-id="29b90-112">A kiszolgálói azonosítók közé tartozik a **ResourceGroupName** és a **kiszolgálónév**.</span><span class="sxs-lookup"><span data-stu-id="29b90-112">Server identifiers include **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="29b90-113">Példák</span><span class="sxs-lookup"><span data-stu-id="29b90-113">EXAMPLES</span></span>

### <span data-ttu-id="29b90-114">1. példa: az Azure SQL Server-kiszolgálók naplózási házirendjének beállítása táblázat-naplózás használatával</span><span class="sxs-lookup"><span data-stu-id="29b90-114">Example 1: Set the auditing policy of an Azure SQL server use Table auditing</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Table -StorageAccountName "Storage22"
```

<span data-ttu-id="29b90-115">Ez a parancs a Server01 nevű kiszolgáló naplózási házirendjét állítja be a Storage22 nevű tárolási fiók használatára.</span><span class="sxs-lookup"><span data-stu-id="29b90-115">This command sets the auditing policy of the server named Server01 to use a storage account named Storage22.</span></span>

### <span data-ttu-id="29b90-116">2. példa: az Azure SQL Server meglévő naplózási házirendjének a tárolási fiók kulcsának beállítása</span><span class="sxs-lookup"><span data-stu-id="29b90-116">Example 2: Set the storage account key of an existing auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountKey Secondary
```

<span data-ttu-id="29b90-117">Ez a parancs a másodlagos kulcs használatához a Server01 nevű kiszolgáló naplózási házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="29b90-117">This command sets the auditing policy of the server named Server01 to use the secondary key.</span></span>
<span data-ttu-id="29b90-118">A parancs nem módosítja a tárolási fiók nevét.</span><span class="sxs-lookup"><span data-stu-id="29b90-118">The command does not modify the storage account name.</span></span>

### <span data-ttu-id="29b90-119">3. példa: az Azure SQL Server naplózási házirendjének beállítása adott eseménytípus használatára</span><span class="sxs-lookup"><span data-stu-id="29b90-119">Example 3: Set the auditing policy of an Azure SQL server to use a specific event type</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventType Login_Failure
```

### <span data-ttu-id="29b90-120">Példa 4: az adatbázis naplózási házirendjének beállítása blob-naplózás használatára</span><span class="sxs-lookup"><span data-stu-id="29b90-120">Example 4: Set the auditing policy of a database to use Blob auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -RetentionInDays 8
```

<span data-ttu-id="29b90-121">Ez a parancs a Server01 nevű kiszolgáló naplózási házirendjét állítja be a Login_Failure eseménytípus használatához.</span><span class="sxs-lookup"><span data-stu-id="29b90-121">This command sets the auditing policy of the server named Server01 to use the Login_Failure event type.</span></span>
<span data-ttu-id="29b90-122">Ez a parancs nem módosítja az egyéb beállításokat.</span><span class="sxs-lookup"><span data-stu-id="29b90-122">This command does not modify any other setting.</span></span>

## <span data-ttu-id="29b90-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29b90-123">PARAMETERS</span></span>

### <span data-ttu-id="29b90-124">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="29b90-124">-AuditActionGroup</span></span>
<span data-ttu-id="29b90-125">Adjon meg egy vagy több naplózási műveleti csoportot.</span><span class="sxs-lookup"><span data-stu-id="29b90-125">Specify one or more audit action groups.</span></span> <span data-ttu-id="29b90-126">Ez a paraméter csak a blob-naplózásra érvényes.</span><span class="sxs-lookup"><span data-stu-id="29b90-126">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="29b90-127">-AuditType</span><span class="sxs-lookup"><span data-stu-id="29b90-127">-AuditType</span></span>
<span data-ttu-id="29b90-128">Adja meg a naplózási típust.</span><span class="sxs-lookup"><span data-stu-id="29b90-128">Specify the audit type.</span></span> <span data-ttu-id="29b90-129">A naplókat táblázatos tárterület vagy blob-tároló segítségével lehet írni.</span><span class="sxs-lookup"><span data-stu-id="29b90-129">Audit logs can be written to Table storage or Blob storage.</span></span> <span data-ttu-id="29b90-130">A blob-naplózás magasabb teljesítményt nyújt, és támogatja az objektum szintű naplózást.</span><span class="sxs-lookup"><span data-stu-id="29b90-130">Blob auditing provides higher performance and supports object-level auditing.</span></span>

```yaml
Type: AuditType
Parameter Sets: (All)
Aliases:
Accepted values: NotSet, Table, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29b90-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29b90-131">-DefaultProfile</span></span>
<span data-ttu-id="29b90-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="29b90-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29b90-133">-EventType</span><span class="sxs-lookup"><span data-stu-id="29b90-133">-EventType</span></span>
<span data-ttu-id="29b90-134">A naplózni kívánt esemény típusait adja meg.</span><span class="sxs-lookup"><span data-stu-id="29b90-134">Specifies the event types to audit.</span></span>
<span data-ttu-id="29b90-135">Ez a paraméter csak a tábla naplózására érvényes.</span><span class="sxs-lookup"><span data-stu-id="29b90-135">This parameter is only applicable to Table auditing.</span></span>

<span data-ttu-id="29b90-136">Több eseménytípus is megadható.</span><span class="sxs-lookup"><span data-stu-id="29b90-136">You can specify several event types.</span></span>
<span data-ttu-id="29b90-137">A mind lehetőséget megadhatja az összes eseménytípus naplózásához, vagy ha azt szeretné, hogy a program ne ellenőrizze az események naplózását.</span><span class="sxs-lookup"><span data-stu-id="29b90-137">You can specify All to audit all of the event types or None to specify that no events will be audited.</span></span>
<span data-ttu-id="29b90-138">Ha egyszerre adja meg a teljes vagy a nincs beállítást, a parancs nem működik.</span><span class="sxs-lookup"><span data-stu-id="29b90-138">If you specify All or None at the same time, the command fails.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure, StoredProcedure_Success, StoredProcedure_Failure, Login_Success, Login_Failure, TransactionManagement_Success, TransactionManagement_Failure, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29b90-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29b90-139">-PassThru</span></span>
<span data-ttu-id="29b90-140">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="29b90-140">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="29b90-141">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="29b90-141">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="29b90-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29b90-142">-ResourceGroupName</span></span>
<span data-ttu-id="29b90-143">Az adatbázist tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="29b90-143">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="29b90-144">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="29b90-144">-RetentionInDays</span></span>
<span data-ttu-id="29b90-145">A naplókban szereplő retenciós napok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="29b90-145">Specifies the number of retention days for the audit logs table.</span></span>
<span data-ttu-id="29b90-146">A nulla (0) érték azt jelzi, hogy a táblázat nem marad meg.</span><span class="sxs-lookup"><span data-stu-id="29b90-146">A value of zero (0) means that the table is not retained.</span></span>
<span data-ttu-id="29b90-147">Ez az alapértelmezett.</span><span class="sxs-lookup"><span data-stu-id="29b90-147">this is the default.</span></span>
<span data-ttu-id="29b90-148">Ha nullánál nagyobb értéket ad meg, a *TableIdentifer* paraméter értékét is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="29b90-148">If you specify a value greater than zero, you must also specify a value for the *TableIdentifer* parameter.</span></span>

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

### <span data-ttu-id="29b90-149">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="29b90-149">-ServerName</span></span>
<span data-ttu-id="29b90-150">Az adatbázist tartalmazó kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="29b90-150">Specifies the name of the server that contains the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29b90-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="29b90-151">-StorageAccountName</span></span>
<span data-ttu-id="29b90-152">Az adatbázis naplózásához használt tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="29b90-152">Specifies the name of the storage account for auditing the database.</span></span>
<span data-ttu-id="29b90-153">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="29b90-153">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="29b90-154">Ha nem adja meg ezt a paramétert, a parancsmag az adatbázis naplózási házirendjének részeként megadott tárolási fiókot használja.</span><span class="sxs-lookup"><span data-stu-id="29b90-154">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy of the database.</span></span>
<span data-ttu-id="29b90-155">Ha most először adja meg az adatbázis-naplózási házirendet, és nem adja meg ezt a paramétert, akkor a parancs nem működik.</span><span class="sxs-lookup"><span data-stu-id="29b90-155">If this is the first time a database auditing policy is defined and you do not specify this parameter, the command fails.</span></span>

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

### <span data-ttu-id="29b90-156">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="29b90-156">-StorageKeyType</span></span>
<span data-ttu-id="29b90-157">Itt adhatja meg, hogy a tárterület-hozzáférési kulcsok közül melyik használható.</span><span class="sxs-lookup"><span data-stu-id="29b90-157">Specifies which of the storage access keys to use.</span></span>
<span data-ttu-id="29b90-158">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="29b90-158">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="29b90-159">Elsődleges</span><span class="sxs-lookup"><span data-stu-id="29b90-159">Primary</span></span>
- <span data-ttu-id="29b90-160">Másodlagos</span><span class="sxs-lookup"><span data-stu-id="29b90-160">Secondary</span></span>

<span data-ttu-id="29b90-161">Az alapértelmezett érték az elsődleges.</span><span class="sxs-lookup"><span data-stu-id="29b90-161">The default value is Primary.</span></span>

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

### <span data-ttu-id="29b90-162">-TableIdentifier</span><span class="sxs-lookup"><span data-stu-id="29b90-162">-TableIdentifier</span></span>
<span data-ttu-id="29b90-163">A naplókat tartalmazó tábla nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="29b90-163">Specifies the name of the audit logs table.</span></span>
<span data-ttu-id="29b90-164">Adja meg ezt az értéket, ha a *RetentionInDays* paraméterhez nullánál nagyobb értéket ad meg.</span><span class="sxs-lookup"><span data-stu-id="29b90-164">Specify this value if you specify a value greater than zero for the *RetentionInDays* parameter.</span></span>

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

### <span data-ttu-id="29b90-165">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="29b90-165">-Confirm</span></span>
<span data-ttu-id="29b90-166">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="29b90-166">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b90-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29b90-167">-WhatIf</span></span>
<span data-ttu-id="29b90-168">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="29b90-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29b90-169">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="29b90-169">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b90-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29b90-170">CommonParameters</span></span>
<span data-ttu-id="29b90-171">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29b90-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29b90-172">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29b90-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29b90-173">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29b90-173">INPUTS</span></span>

### <span data-ttu-id="29b90-174">Nincs</span><span class="sxs-lookup"><span data-stu-id="29b90-174">None</span></span>
<span data-ttu-id="29b90-175">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="29b90-175">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="29b90-176">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29b90-176">OUTPUTS</span></span>

### <span data-ttu-id="29b90-177">Microsoft. Azure. Command. SQL. Security. Model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="29b90-177">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="29b90-178">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29b90-178">NOTES</span></span>

## <span data-ttu-id="29b90-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29b90-179">RELATED LINKS</span></span>

[<span data-ttu-id="29b90-180">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="29b90-180">Get-AzureRmSqlServerAuditingPolicy</span></span>](./Get-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="29b90-181">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="29b90-181">Use-AzureRmSqlServerAuditingPolicy</span></span>](./Use-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="29b90-182">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="29b90-182">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


