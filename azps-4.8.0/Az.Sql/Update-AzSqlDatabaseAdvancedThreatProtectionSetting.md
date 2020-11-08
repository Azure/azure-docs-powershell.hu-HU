---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 1bd5906ac4736fc2aace122070edfebe1e59fe3f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181288"
---
# <span data-ttu-id="ebc26-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="ebc26-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="ebc26-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ebc26-102">SYNOPSIS</span></span>
<span data-ttu-id="ebc26-103">Speciális veszélyforrások elleni védelemre vonatkozó beállításokat állít be az adatbázisokban.</span><span class="sxs-lookup"><span data-stu-id="ebc26-103">Sets a advanced threat protection settings on a database.</span></span>

## <span data-ttu-id="ebc26-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ebc26-104">SYNTAX</span></span>

```
Update-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebc26-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ebc26-105">DESCRIPTION</span></span>
<span data-ttu-id="ebc26-106">Az **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** parancsmag az Azure SQL-adatbázisokban speciális veszélyforrások elleni védelemi beállításokat állít be.</span><span class="sxs-lookup"><span data-stu-id="ebc26-106">The **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL database.</span></span>
<span data-ttu-id="ebc26-107">Az adatbázis speciális veszélyforrások elleni védelmének engedélyezéséhez a naplózási beállításokat engedélyeznie kell az adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="ebc26-107">In order to enable advanced threat protection on a database an auditing settings must be enabled on that database.</span></span>
<span data-ttu-id="ebc26-108">A parancsmag használatához adja meg a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paramétert az adatbázis meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="ebc26-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="ebc26-109">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="ebc26-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ebc26-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ebc26-110">EXAMPLES</span></span>

### <span data-ttu-id="ebc26-111">1. példa: az adatbázis speciális veszélyforrásokkal kapcsolatos védelmi beállításainak megadása</span><span class="sxs-lookup"><span data-stu-id="ebc26-111">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="ebc26-112">Ez a parancs a Server01 nevű kiszolgálón a Database01 nevű adatbázis speciális veszélyforrásokkal kapcsolatos védelmi beállításait állítja be.</span><span class="sxs-lookup"><span data-stu-id="ebc26-112">This command sets the advanced threat protection settings for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="ebc26-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ebc26-113">PARAMETERS</span></span>

### <span data-ttu-id="ebc26-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ebc26-114">-DatabaseName</span></span>
<span data-ttu-id="ebc26-115">Annak az adatbázisnak a nevét adja meg, amelyben a beállítások be vannak állítva.</span><span class="sxs-lookup"><span data-stu-id="ebc26-115">Specifies the name of the database where the settings is set.</span></span>

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

### <span data-ttu-id="ebc26-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebc26-116">-DefaultProfile</span></span>
<span data-ttu-id="ebc26-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ebc26-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ebc26-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="ebc26-118">-EmailAdmins</span></span>
<span data-ttu-id="ebc26-119">Meghatározza, hogy a speciális veszélyforrások elleni védelem beállításai a rendszergazdák e-mailen keresztül kerülnek-e kapcsolatba.</span><span class="sxs-lookup"><span data-stu-id="ebc26-119">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="ebc26-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="ebc26-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="ebc26-121">A beállításokból kizárandó észlelési típusok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ebc26-121">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="ebc26-122">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ebc26-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ebc26-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="ebc26-123">Sql_Injection</span></span> 
- <span data-ttu-id="ebc26-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="ebc26-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="ebc26-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="ebc26-125">Access_Anomaly</span></span> 
- <span data-ttu-id="ebc26-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="ebc26-126">None</span></span>

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

### <span data-ttu-id="ebc26-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="ebc26-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="ebc26-128">Az e-mail-címek pontosvesszővel elválasztott listáját adja meg, amelyre a beállítások riasztásokat küldenek.</span><span class="sxs-lookup"><span data-stu-id="ebc26-128">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="ebc26-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebc26-129">-PassThru</span></span>
<span data-ttu-id="ebc26-130">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ebc26-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ebc26-131">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ebc26-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ebc26-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebc26-132">-ResourceGroupName</span></span>
<span data-ttu-id="ebc26-133">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="ebc26-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="ebc26-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="ebc26-134">-RetentionInDays</span></span>
<span data-ttu-id="ebc26-135">A naplók adatmegőrzési napjainak száma</span><span class="sxs-lookup"><span data-stu-id="ebc26-135">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="ebc26-136">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="ebc26-136">-ServerName</span></span>
<span data-ttu-id="ebc26-137">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ebc26-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="ebc26-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ebc26-138">-StorageAccountName</span></span>
<span data-ttu-id="ebc26-139">A használandó tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ebc26-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="ebc26-140">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="ebc26-140">Wildcards are not permitted.</span></span> <span data-ttu-id="ebc26-141">Ehhez a paraméterhez nincs szükség.</span><span class="sxs-lookup"><span data-stu-id="ebc26-141">This parameter is not required.</span></span> <span data-ttu-id="ebc26-142">Ha ez a paraméter nincs megadva, a parancsmag az adatbázis speciális veszélyforrások elleni védelmének részeként megadott tárolási fiókot fogja használni.</span><span class="sxs-lookup"><span data-stu-id="ebc26-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="ebc26-143">Ha ez az első alkalom, hogy az adatbázis speciális veszélyforrások elleni védelme beállítás van megadva, és ez a paraméter nem jelenik meg, a parancsmag sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="ebc26-143">If this is the first time a database advanced threat protection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="ebc26-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ebc26-144">-Confirm</span></span>
<span data-ttu-id="ebc26-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ebc26-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebc26-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebc26-146">-WhatIf</span></span>
<span data-ttu-id="ebc26-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ebc26-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebc26-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ebc26-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebc26-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebc26-149">CommonParameters</span></span>
<span data-ttu-id="ebc26-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ebc26-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebc26-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ebc26-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebc26-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebc26-152">INPUTS</span></span>

### <span data-ttu-id="ebc26-153">System. String</span><span class="sxs-lookup"><span data-stu-id="ebc26-153">System.String</span></span>

### <span data-ttu-id="ebc26-154">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ebc26-154">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ebc26-155">Microsoft. Azure. Command. SQL. ThreatDetection. Model. DetectionType []</span><span class="sxs-lookup"><span data-stu-id="ebc26-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="ebc26-156">System. null ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ebc26-156">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ebc26-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebc26-157">OUTPUTS</span></span>

### <span data-ttu-id="ebc26-158">Microsoft. Azure. Command. SQL. ThreatDetection. Model. DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="ebc26-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="ebc26-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ebc26-159">NOTES</span></span>

## <span data-ttu-id="ebc26-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ebc26-160">RELATED LINKS</span></span>

[<span data-ttu-id="ebc26-161">Get-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="ebc26-161">Get-AzSqlDatabaseThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="ebc26-162">Remove-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="ebc26-162">Remove-AzSqlDatabaseThreatDetectionsettings</span></span>](./Remove-AzSqlDatabaseThreatDetectionsettings.md)

[<span data-ttu-id="ebc26-163">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="ebc26-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


