---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: aa70b94614f8a0826a5d1563439afa8cb9ef6d95
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502324"
---
# <span data-ttu-id="ef960-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ef960-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="ef960-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef960-102">SYNOPSIS</span></span>
<span data-ttu-id="ef960-103">Veszélyforrás-észlelési házirendet állít be egy adatbázison.</span><span class="sxs-lookup"><span data-stu-id="ef960-103">Sets a threat detection policy on a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef960-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef960-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef960-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef960-105">DESCRIPTION</span></span>
<span data-ttu-id="ef960-106">A **set-AzureRmSqlDatabaseThreatDetectionPolicy** parancsmag fenyegetés-észlelési házirendet állít be egy Azure SQL-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="ef960-106">The **Set-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL database.</span></span>
<span data-ttu-id="ef960-107">Ha engedélyezni szeretné a fenyegetések észlelését egy adatbázisban, a naplózási házirendet engedélyeznie kell az adott adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="ef960-107">In order to enable threat detection on a database an auditing policy must be enabled on that database.</span></span>

<span data-ttu-id="ef960-108">A parancsmag használatához adja meg a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paramétert az adatbázis meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="ef960-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>

<span data-ttu-id="ef960-109">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="ef960-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ef960-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ef960-110">EXAMPLES</span></span>

### <span data-ttu-id="ef960-111">1. példa: az adatbázis veszélyforrás-észlelési házirendjének beállítása</span><span class="sxs-lookup"><span data-stu-id="ef960-111">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="ef960-112">Ez a parancs beállítja a Database01 nevű adatbázis veszélyforrások észlelési házirendjét a Server01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="ef960-112">This command sets the threat detection policy for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="ef960-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef960-113">PARAMETERS</span></span>

### <span data-ttu-id="ef960-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ef960-114">-DatabaseName</span></span>
<span data-ttu-id="ef960-115">Annak az adatbázisnak a nevét adja meg, amelyben a házirend van beállítva.</span><span class="sxs-lookup"><span data-stu-id="ef960-115">Specifies the name of the database where the policy is set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef960-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef960-116">-DefaultProfile</span></span>
<span data-ttu-id="ef960-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ef960-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef960-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="ef960-118">-EmailAdmins</span></span>
<span data-ttu-id="ef960-119">Azt adja meg, hogy a fenyegetés észlelése házirend a rendszergazdákat e-mailben használja-e.</span><span class="sxs-lookup"><span data-stu-id="ef960-119">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef960-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="ef960-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="ef960-121">A házirendből kizárandó észlelési típusokból álló tömböt adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef960-121">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="ef960-122">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ef960-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ef960-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="ef960-123">Sql_Injection</span></span> 
- <span data-ttu-id="ef960-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="ef960-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="ef960-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="ef960-125">Access_Anomaly</span></span> 
- <span data-ttu-id="ef960-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="ef960-126">None</span></span>

```yaml
Type: DetectionType[]
Parameter Sets: (All)
Aliases:
Accepted values: Sql_Injection, Sql_Injection_Vulnerability, Access_Anomaly, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef960-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="ef960-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="ef960-128">A házirend által küldött e-mail-címek pontosvesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef960-128">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="ef960-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef960-129">-PassThru</span></span>
<span data-ttu-id="ef960-130">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ef960-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ef960-131">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ef960-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ef960-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef960-132">-ResourceGroupName</span></span>
<span data-ttu-id="ef960-133">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="ef960-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="ef960-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="ef960-134">-RetentionInDays</span></span>
<span data-ttu-id="ef960-135">A naplók adatmegőrzési napjainak száma</span><span class="sxs-lookup"><span data-stu-id="ef960-135">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="ef960-136">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="ef960-136">-ServerName</span></span>
<span data-ttu-id="ef960-137">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef960-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="ef960-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ef960-138">-StorageAccountName</span></span>
<span data-ttu-id="ef960-139">A használandó tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef960-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="ef960-140">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="ef960-140">Wildcards are not permitted.</span></span> <span data-ttu-id="ef960-141">Ehhez a paraméterhez nincs szükség.</span><span class="sxs-lookup"><span data-stu-id="ef960-141">This parameter is not required.</span></span> <span data-ttu-id="ef960-142">Ha ezt a paramétert nem jeleníti meg, a parancsmag az adatbázis veszélyforrások észlelési házirendjének részeként megadott tárolási fiókot fogja használni.</span><span class="sxs-lookup"><span data-stu-id="ef960-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="ef960-143">Ha ez az első alkalom, hogy egy adatbázis-veszélyforrás észlelési házirend van definiálva, és a paraméter nincs megadva, a parancsmag sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="ef960-143">If this is the first time a database threat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="ef960-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ef960-144">-Confirm</span></span>
<span data-ttu-id="ef960-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ef960-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef960-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef960-146">-WhatIf</span></span>
<span data-ttu-id="ef960-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ef960-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef960-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ef960-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef960-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef960-149">CommonParameters</span></span>
<span data-ttu-id="ef960-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef960-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef960-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef960-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef960-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef960-152">INPUTS</span></span>

###  
<span data-ttu-id="ef960-153">Ebben a parancsmagban nem lehet beírni a bemenetet.</span><span class="sxs-lookup"><span data-stu-id="ef960-153">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="ef960-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef960-154">OUTPUTS</span></span>

### <span data-ttu-id="ef960-155">Microsoft. Azure. Command. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="ef960-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="ef960-156">Ez a parancsmag egy **Model. DatabaseThreatDetectionPolicyModel** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="ef960-156">This cmdlet returns a **Model.DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="ef960-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef960-157">NOTES</span></span>

## <span data-ttu-id="ef960-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef960-158">RELATED LINKS</span></span>

[<span data-ttu-id="ef960-159">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ef960-159">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="ef960-160">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ef960-160">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="ef960-161">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="ef960-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


