---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 8480037bf4b756a03a40ad1c1dff01ab1d28ac69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499119"
---
# <span data-ttu-id="de3ad-101">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="de3ad-101">Set-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="de3ad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="de3ad-102">SYNOPSIS</span></span>
<span data-ttu-id="de3ad-103">Az Azure SQL Server-kiszolgálók naplózási beállításainak módosítása</span><span class="sxs-lookup"><span data-stu-id="de3ad-103">Changes the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de3ad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="de3ad-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de3ad-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="de3ad-105">DESCRIPTION</span></span>
<span data-ttu-id="de3ad-106">A **set-AzureRmSqlServerAuditing** parancsmag az Azure SQL Server-kiszolgálók naplózási beállításait módosítja.</span><span class="sxs-lookup"><span data-stu-id="de3ad-106">The **Set-AzureRmSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="de3ad-107">A parancsmag használatához a *ResourceGroupName* és a *kiszolgálónév* paraméterrel keresse meg a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="de3ad-107">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="de3ad-108">Adja meg a *StorageAccountName* paramétert a naplók tárolási fiókjának a megadásához, illetve a *StorageKeyType* paramétert a tárolási kulcsok meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="de3ad-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="de3ad-109">A házirend engedélyezéséhez vagy letiltásához használja az *állami* paramétert.</span><span class="sxs-lookup"><span data-stu-id="de3ad-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="de3ad-110">A naplók adatmegőrzését úgy is megadhatja, hogy az *RetentionInDays* paraméter értékét adja meg a naplók időszakának meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="de3ad-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="de3ad-111">A parancsmag sikeres futtatását követően a megadott Azure SQL-kiszolgálón megadott Azure SQL-adatbázisok naplózása engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="de3ad-111">After the cmdlet runs successfully, auditing of the Azure SQL databases that are defined in the specified Azure SQL server is enabled.</span></span>
<span data-ttu-id="de3ad-112">Ha a parancsmag sikerrel jár, és a *PassThru* paramétert használja, a kiszolgálói azonosítók mellett egy olyan objektumot ad eredményül, amely leírja az aktuális blob-naplózási házirendet.</span><span class="sxs-lookup"><span data-stu-id="de3ad-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the server identifiers.</span></span>
<span data-ttu-id="de3ad-113">A kiszolgálói azonosítók tartalmazzák, de nem korlátozódnak a **ResourceGroupName** és a **kiszolgáló_neve** -ra.</span><span class="sxs-lookup"><span data-stu-id="de3ad-113">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="de3ad-114">Példák</span><span class="sxs-lookup"><span data-stu-id="de3ad-114">EXAMPLES</span></span>

### <span data-ttu-id="de3ad-115">1. példa: az Azure SQL Server-kiszolgálók naplózási házirendjének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="de3ad-115">Example 1: Enable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="de3ad-116">2. példa: az Azure SQL Server-kiszolgálók naplózási házirendjének letiltása</span><span class="sxs-lookup"><span data-stu-id="de3ad-116">Example 2: Disable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

## <span data-ttu-id="de3ad-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="de3ad-117">PARAMETERS</span></span>

### <span data-ttu-id="de3ad-118">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="de3ad-118">-AuditActionGroup</span></span>
<span data-ttu-id="de3ad-119">A naplózási műveletek csoportjának készlete</span><span class="sxs-lookup"><span data-stu-id="de3ad-119">The set of the audit action groups</span></span>

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

### <span data-ttu-id="de3ad-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de3ad-120">-PassThru</span></span>
<span data-ttu-id="de3ad-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="de3ad-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="de3ad-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de3ad-122">-ResourceGroupName</span></span>
<span data-ttu-id="de3ad-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="de3ad-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="de3ad-124">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="de3ad-124">-RetentionInDays</span></span>
<span data-ttu-id="de3ad-125">A naplók adatmegőrzési napjainak száma</span><span class="sxs-lookup"><span data-stu-id="de3ad-125">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="de3ad-126">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="de3ad-126">-ServerName</span></span>
<span data-ttu-id="de3ad-127">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="de3ad-127">SQL server name.</span></span>

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

### <span data-ttu-id="de3ad-128">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="de3ad-128">-State</span></span>
<span data-ttu-id="de3ad-129">A naplózási házirend állapota</span><span class="sxs-lookup"><span data-stu-id="de3ad-129">The state of the auditing policy</span></span>

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

### <span data-ttu-id="de3ad-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="de3ad-130">-StorageAccountName</span></span>
<span data-ttu-id="de3ad-131">A tárolási fiók neve</span><span class="sxs-lookup"><span data-stu-id="de3ad-131">The name of the storage account</span></span>

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

### <span data-ttu-id="de3ad-132">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="de3ad-132">-StorageKeyType</span></span>
<span data-ttu-id="de3ad-133">A tárolási kulcs típusa</span><span class="sxs-lookup"><span data-stu-id="de3ad-133">The type of the storage key</span></span>

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

### <span data-ttu-id="de3ad-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="de3ad-134">-Confirm</span></span>
<span data-ttu-id="de3ad-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="de3ad-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de3ad-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de3ad-136">-WhatIf</span></span>
<span data-ttu-id="de3ad-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="de3ad-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de3ad-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="de3ad-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de3ad-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de3ad-139">-DefaultProfile</span></span>
<span data-ttu-id="de3ad-140">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de3ad-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de3ad-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de3ad-141">CommonParameters</span></span>
<span data-ttu-id="de3ad-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="de3ad-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de3ad-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de3ad-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de3ad-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="de3ad-144">INPUTS</span></span>

## <span data-ttu-id="de3ad-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de3ad-145">OUTPUTS</span></span>

### <span data-ttu-id="de3ad-146">Microsoft. Azure. Command. SQL. Security. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="de3ad-146">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="de3ad-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="de3ad-147">NOTES</span></span>

## <span data-ttu-id="de3ad-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de3ad-148">RELATED LINKS</span></span>

