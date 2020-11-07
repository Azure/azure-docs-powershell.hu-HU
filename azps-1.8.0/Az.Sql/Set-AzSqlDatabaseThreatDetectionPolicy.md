---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 231d38105851a5af7d32535d85827ce70e69caa5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668784"
---
# <span data-ttu-id="773f6-101">Set-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="773f6-101">Set-AzSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="773f6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="773f6-102">SYNOPSIS</span></span>
<span data-ttu-id="773f6-103">Veszélyforrás-észlelési házirendet állít be egy adatbázison.</span><span class="sxs-lookup"><span data-stu-id="773f6-103">Sets a threat detection policy on a database.</span></span>

## <span data-ttu-id="773f6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="773f6-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="773f6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="773f6-105">DESCRIPTION</span></span>
<span data-ttu-id="773f6-106">A **set-AzSqlDatabaseThreatDetectionPolicy** parancsmag fenyegetés-észlelési házirendet állít be egy Azure SQL-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="773f6-106">The **Set-AzSqlDatabaseThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL database.</span></span>
<span data-ttu-id="773f6-107">Ha engedélyezni szeretné a fenyegetések észlelését egy adatbázisban, a naplózási házirendet engedélyeznie kell az adott adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="773f6-107">In order to enable threat detection on a database an auditing policy must be enabled on that database.</span></span>
<span data-ttu-id="773f6-108">A parancsmag használatához adja meg a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paramétert az adatbázis meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="773f6-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="773f6-109">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="773f6-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="773f6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="773f6-110">EXAMPLES</span></span>

### <span data-ttu-id="773f6-111">1. példa: az adatbázis veszélyforrás-észlelési házirendjének beállítása</span><span class="sxs-lookup"><span data-stu-id="773f6-111">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="773f6-112">Ez a parancs beállítja a Database01 nevű adatbázis veszélyforrások észlelési házirendjét a Server01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="773f6-112">This command sets the threat detection policy for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="773f6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="773f6-113">PARAMETERS</span></span>

### <span data-ttu-id="773f6-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="773f6-114">-DatabaseName</span></span>
<span data-ttu-id="773f6-115">Annak az adatbázisnak a nevét adja meg, amelyben a házirend van beállítva.</span><span class="sxs-lookup"><span data-stu-id="773f6-115">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="773f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="773f6-116">-DefaultProfile</span></span>
<span data-ttu-id="773f6-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="773f6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="773f6-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="773f6-118">-EmailAdmins</span></span>
<span data-ttu-id="773f6-119">Azt adja meg, hogy a fenyegetés észlelése házirend a rendszergazdákat e-mailben használja-e.</span><span class="sxs-lookup"><span data-stu-id="773f6-119">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="773f6-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="773f6-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="773f6-121">A házirendből kizárandó észlelési típusokból álló tömböt adja meg.</span><span class="sxs-lookup"><span data-stu-id="773f6-121">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="773f6-122">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="773f6-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="773f6-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="773f6-123">Sql_Injection</span></span> 
- <span data-ttu-id="773f6-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="773f6-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="773f6-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="773f6-125">Access_Anomaly</span></span> 
- <span data-ttu-id="773f6-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="773f6-126">None</span></span>

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

### <span data-ttu-id="773f6-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="773f6-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="773f6-128">A házirend által küldött e-mail-címek pontosvesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="773f6-128">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="773f6-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="773f6-129">-PassThru</span></span>
<span data-ttu-id="773f6-130">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="773f6-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="773f6-131">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="773f6-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="773f6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="773f6-132">-ResourceGroupName</span></span>
<span data-ttu-id="773f6-133">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="773f6-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="773f6-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="773f6-134">-RetentionInDays</span></span>
<span data-ttu-id="773f6-135">A naplók adatmegőrzési napjainak száma</span><span class="sxs-lookup"><span data-stu-id="773f6-135">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="773f6-136">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="773f6-136">-ServerName</span></span>
<span data-ttu-id="773f6-137">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="773f6-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="773f6-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="773f6-138">-StorageAccountName</span></span>
<span data-ttu-id="773f6-139">A használandó tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="773f6-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="773f6-140">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="773f6-140">Wildcards are not permitted.</span></span> <span data-ttu-id="773f6-141">Ehhez a paraméterhez nincs szükség.</span><span class="sxs-lookup"><span data-stu-id="773f6-141">This parameter is not required.</span></span> <span data-ttu-id="773f6-142">Ha ezt a paramétert nem jeleníti meg, a parancsmag az adatbázis veszélyforrások észlelési házirendjének részeként megadott tárolási fiókot fogja használni.</span><span class="sxs-lookup"><span data-stu-id="773f6-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="773f6-143">Ha ez az első alkalom, hogy egy adatbázis-veszélyforrás észlelési házirend van definiálva, és a paraméter nincs megadva, a parancsmag sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="773f6-143">If this is the first time a database threat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="773f6-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="773f6-144">-Confirm</span></span>
<span data-ttu-id="773f6-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="773f6-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="773f6-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="773f6-146">-WhatIf</span></span>
<span data-ttu-id="773f6-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="773f6-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="773f6-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="773f6-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="773f6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="773f6-149">CommonParameters</span></span>
<span data-ttu-id="773f6-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="773f6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="773f6-151">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="773f6-151">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="773f6-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="773f6-152">INPUTS</span></span>

### <span data-ttu-id="773f6-153">System. String</span><span class="sxs-lookup"><span data-stu-id="773f6-153">System.String</span></span>

### <span data-ttu-id="773f6-154">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="773f6-154">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="773f6-155">Microsoft. Azure. Command. SQL. ThreatDetection. Model. DetectionType []</span><span class="sxs-lookup"><span data-stu-id="773f6-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="773f6-156">System. null ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="773f6-156">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="773f6-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="773f6-157">OUTPUTS</span></span>

### <span data-ttu-id="773f6-158">Microsoft. Azure. Command. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="773f6-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="773f6-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="773f6-159">NOTES</span></span>

## <span data-ttu-id="773f6-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="773f6-160">RELATED LINKS</span></span>

[<span data-ttu-id="773f6-161">Get-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="773f6-161">Get-AzSqlDatabaseThreatDetectionPolicy</span></span>](./Get-AzSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="773f6-162">Remove-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="773f6-162">Remove-AzSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="773f6-163">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="773f6-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


