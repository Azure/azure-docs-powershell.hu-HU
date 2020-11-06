---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 746a9a9908865047d5b904b5b47b71ca9c30fbd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494608"
---
# <span data-ttu-id="e285c-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e285c-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="e285c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e285c-102">SYNOPSIS</span></span>
<span data-ttu-id="e285c-103">Veszélyforrás-észlelési házirendet állít be egy adatbázison.</span><span class="sxs-lookup"><span data-stu-id="e285c-103">Sets a threat detection policy on a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e285c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e285c-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e285c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e285c-105">DESCRIPTION</span></span>
<span data-ttu-id="e285c-106">A **set-AzureRmSqlDatabaseThreatDetectionPolicy** parancsmag fenyegetés-észlelési házirendet állít be egy Azure SQL-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="e285c-106">The **Set-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL database.</span></span>
<span data-ttu-id="e285c-107">Ha engedélyezni szeretné a fenyegetések észlelését egy adatbázisban, a naplózási házirendet engedélyeznie kell az adott adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="e285c-107">In order to enable threat detection on a database an auditing policy must be enabled on that database.</span></span>

<span data-ttu-id="e285c-108">A parancsmag használatához adja meg a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paramétert az adatbázis meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="e285c-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>

<span data-ttu-id="e285c-109">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="e285c-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="e285c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e285c-110">EXAMPLES</span></span>

### <span data-ttu-id="e285c-111">1. példa: az adatbázis veszélyforrás-észlelési házirendjének beállítása</span><span class="sxs-lookup"><span data-stu-id="e285c-111">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="e285c-112">Ez a parancs beállítja a Database01 nevű adatbázis veszélyforrások észlelési házirendjét a Server01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="e285c-112">This command sets the threat detection policy for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="e285c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e285c-113">PARAMETERS</span></span>

### <span data-ttu-id="e285c-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e285c-114">-DatabaseName</span></span>
<span data-ttu-id="e285c-115">Annak az adatbázisnak a nevét adja meg, amelyben a házirend van beállítva.</span><span class="sxs-lookup"><span data-stu-id="e285c-115">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="e285c-116">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="e285c-116">-EmailAdmins</span></span>
<span data-ttu-id="e285c-117">Azt adja meg, hogy a fenyegetés észlelése házirend a rendszergazdákat e-mailben használja-e.</span><span class="sxs-lookup"><span data-stu-id="e285c-117">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="e285c-118">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="e285c-118">-ExcludedDetectionType</span></span>
<span data-ttu-id="e285c-119">A házirendből kizárandó észlelési típusokból álló tömböt adja meg.</span><span class="sxs-lookup"><span data-stu-id="e285c-119">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="e285c-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e285c-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e285c-121">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="e285c-121">Sql_Injection</span></span> 
- <span data-ttu-id="e285c-122">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="e285c-122">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="e285c-123">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="e285c-123">Access_Anomaly</span></span> 
- <span data-ttu-id="e285c-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="e285c-124">None</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]
Parameter Sets: (All)
Aliases: 
Accepted values: Sql_Injection, Sql_Injection_Vulnerability, Access_Anomaly, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e285c-125">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="e285c-125">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="e285c-126">A házirend által küldött e-mail-címek pontosvesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e285c-126">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="e285c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e285c-127">-PassThru</span></span>
<span data-ttu-id="e285c-128">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="e285c-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e285c-129">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="e285c-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e285c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e285c-130">-ResourceGroupName</span></span>
<span data-ttu-id="e285c-131">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="e285c-131">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e285c-132">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e285c-132">-RetentionInDays</span></span>
<span data-ttu-id="e285c-133">A naplók adatmegőrzési napjainak száma</span><span class="sxs-lookup"><span data-stu-id="e285c-133">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="e285c-134">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="e285c-134">-ServerName</span></span>
<span data-ttu-id="e285c-135">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e285c-135">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="e285c-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e285c-136">-StorageAccountName</span></span>
<span data-ttu-id="e285c-137">A használandó tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e285c-137">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="e285c-138">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="e285c-138">Wildcards are not permitted.</span></span> <span data-ttu-id="e285c-139">Ehhez a paraméterhez nincs szükség.</span><span class="sxs-lookup"><span data-stu-id="e285c-139">This parameter is not required.</span></span> <span data-ttu-id="e285c-140">Ha ezt a paramétert nem jeleníti meg, a parancsmag az adatbázis veszélyforrások észlelési házirendjének részeként megadott tárolási fiókot fogja használni.</span><span class="sxs-lookup"><span data-stu-id="e285c-140">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="e285c-141">Ha ez az első alkalom, hogy egy adatbázis-veszélyforrás észlelési házirend van definiálva, és a paraméter nincs megadva, a parancsmag sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="e285c-141">If this is the first time a database threat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="e285c-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e285c-142">-Confirm</span></span>
<span data-ttu-id="e285c-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e285c-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e285c-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e285c-144">-WhatIf</span></span>
<span data-ttu-id="e285c-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e285c-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e285c-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e285c-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e285c-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e285c-147">-DefaultProfile</span></span>
<span data-ttu-id="e285c-148">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e285c-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e285c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e285c-149">CommonParameters</span></span>
<span data-ttu-id="e285c-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e285c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e285c-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e285c-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e285c-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e285c-152">INPUTS</span></span>

###  
<span data-ttu-id="e285c-153">Ebben a parancsmagban nem lehet beírni a bemenetet.</span><span class="sxs-lookup"><span data-stu-id="e285c-153">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="e285c-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e285c-154">OUTPUTS</span></span>

### <span data-ttu-id="e285c-155">Microsoft. Azure. Command. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="e285c-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="e285c-156">Ez a parancsmag egy **Model. DatabaseThreatDetectionPolicyModel** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="e285c-156">This cmdlet returns a **Model.DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="e285c-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e285c-157">NOTES</span></span>

## <span data-ttu-id="e285c-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e285c-158">RELATED LINKS</span></span>

[<span data-ttu-id="e285c-159">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e285c-159">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="e285c-160">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e285c-160">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="e285c-161">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="e285c-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


