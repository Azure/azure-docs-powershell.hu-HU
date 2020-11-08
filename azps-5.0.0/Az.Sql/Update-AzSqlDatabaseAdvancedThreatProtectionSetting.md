---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 1bd5906ac4736fc2aace122070edfebe1e59fe3f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186956"
---
# <span data-ttu-id="0e3ba-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="0e3ba-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="0e3ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0e3ba-102">SYNOPSIS</span></span>
<span data-ttu-id="0e3ba-103">Speciális veszélyforrások elleni védelemre vonatkozó beállításokat állít be az adatbázisokban.</span><span class="sxs-lookup"><span data-stu-id="0e3ba-103">Sets a advanced threat protection settings on a database.</span></span>

## <span data-ttu-id="0e3ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0e3ba-104">SYNTAX</span></span>

```
Update-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e3ba-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0e3ba-105">DESCRIPTION</span></span>
<span data-ttu-id="0e3ba-106">Az **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** parancsmag az Azure SQL-adatbázisokban speciális veszélyforrások elleni védelemi beállításokat állít be.</span><span class="sxs-lookup"><span data-stu-id="0e3ba-106">The **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL database.</span></span>
<span data-ttu-id="0e3ba-107">Az adatbázis speciális veszélyforrások elleni védelmének engedélyezéséhez a naplózási beállításokat engedélyeznie kell az adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="0e3ba-107">In order to enable advanced threat protection on a database an auditing settings must be enabled on that database.</span></span>
<span data-ttu-id="0e3ba-108">A parancsmag használatához adja meg a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paramétert az adatbázis meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="0e3ba-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="0e3ba-109">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="0e3ba-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="0e3ba-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0e3ba-110">EXAMPLES</span></span>

### <span data-ttu-id="0e3ba-111">1. példa: az adatbázis speciális veszélyforrásokkal kapcsolatos védelmi beállításainak megadása</span><span class="sxs-lookup"><span data-stu-id="0e3ba-111">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="0e3ba-112">Ez a parancs a Server01 nevű kiszolgálón a Database01 nevű adatbázis speciális veszélyforrásokkal kapcsolatos védelmi beállításait állítja be.</span><span class="sxs-lookup"><span data-stu-id="0e3ba-112">This command sets the advanced threat protection settings for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="0e3ba-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0e3ba-113">PARAMETERS</span></span>

### <span data-ttu-id="0e3ba-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0e3ba-114">-DatabaseName</span></span>
<span data-ttu-id="0e3ba-115">Annak az adatbázisnak a nevét adja meg, amelyben a beállítások be vannak állítva.</span><span class="sxs-lookup"><span data-stu-id="0e3ba-115">Specifies the name of the database where the settings is set.</span></span>

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

### <span data-ttu-id="0e3ba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e3ba-116">-DefaultProfile</span></span>
<span data-ttu-id="0e3ba-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0e3ba-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e3ba-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="0e3ba-118">-EmailAdmins</span></span>
<span data-ttu-id="0e3ba-119">Meghatározza, hogy a speciális veszélyforrások elleni védelem beállításai a rendszergazdák e-mailen keresztül kerülnek-e kapcsolatba.</span><span class="sxs-lookup"><span data-stu-id="0e3ba-119">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="0e3ba-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="0e3ba-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="0e3ba-121">A beállításokból kizárandó észlelési típusok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e3ba-121">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="0e3ba-122">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0e3ba-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0e3ba-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="0e3ba-123">Sql_Injection</span></span> 
- <span data-ttu-id="0e3ba-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="0e3ba-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="0e3ba-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="0e3ba-125">Access_Anomaly</span></span> 
- <span data-ttu-id="0e3ba-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="0e3ba-126">None</span></span>

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

### <span data-ttu-id="0e3ba-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="0e3ba-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="0e3ba-128">Az e-mail-címek pontosvesszővel elválasztott listáját adja meg, amelyre a beállítások riasztásokat küldenek.</span><span class="sxs-lookup"><span data-stu-id="0e3ba-128">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="0e3ba-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e3ba-129">-PassThru</span></span>
<span data-ttu-id="0e3ba-130">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="0e3ba-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0e3ba-131">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="0e3ba-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0e3ba-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e3ba-132">-ResourceGroupName</span></span>
<span data-ttu-id="0e3ba-133">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="0e3ba-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="0e3ba-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="0e3ba-134">-RetentionInDays</span></span>
<span data-ttu-id="0e3ba-135">A naplók adatmegőrzési napjainak száma</span><span class="sxs-lookup"><span data-stu-id="0e3ba-135">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="0e3ba-136">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="0e3ba-136">-ServerName</span></span>
<span data-ttu-id="0e3ba-137">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e3ba-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="0e3ba-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0e3ba-138">-StorageAccountName</span></span>
<span data-ttu-id="0e3ba-139">A használandó tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e3ba-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="0e3ba-140">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="0e3ba-140">Wildcards are not permitted.</span></span> <span data-ttu-id="0e3ba-141">Ehhez a paraméterhez nincs szükség.</span><span class="sxs-lookup"><span data-stu-id="0e3ba-141">This parameter is not required.</span></span> <span data-ttu-id="0e3ba-142">Ha ez a paraméter nincs megadva, a parancsmag az adatbázis speciális veszélyforrások elleni védelmének részeként megadott tárolási fiókot fogja használni.</span><span class="sxs-lookup"><span data-stu-id="0e3ba-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="0e3ba-143">Ha ez az első alkalom, hogy az adatbázis speciális veszélyforrások elleni védelme beállítás van megadva, és ez a paraméter nem jelenik meg, a parancsmag sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="0e3ba-143">If this is the first time a database advanced threat protection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="0e3ba-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0e3ba-144">-Confirm</span></span>
<span data-ttu-id="0e3ba-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0e3ba-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e3ba-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e3ba-146">-WhatIf</span></span>
<span data-ttu-id="0e3ba-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0e3ba-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e3ba-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0e3ba-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e3ba-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e3ba-149">CommonParameters</span></span>
<span data-ttu-id="0e3ba-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0e3ba-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e3ba-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0e3ba-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e3ba-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e3ba-152">INPUTS</span></span>

### <span data-ttu-id="0e3ba-153">System. String</span><span class="sxs-lookup"><span data-stu-id="0e3ba-153">System.String</span></span>

### <span data-ttu-id="0e3ba-154">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0e3ba-154">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0e3ba-155">Microsoft. Azure. Command. SQL. ThreatDetection. Model. DetectionType []</span><span class="sxs-lookup"><span data-stu-id="0e3ba-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="0e3ba-156">System. null ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0e3ba-156">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="0e3ba-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e3ba-157">OUTPUTS</span></span>

### <span data-ttu-id="0e3ba-158">Microsoft. Azure. Command. SQL. ThreatDetection. Model. DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="0e3ba-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="0e3ba-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0e3ba-159">NOTES</span></span>

## <span data-ttu-id="0e3ba-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e3ba-160">RELATED LINKS</span></span>

[<span data-ttu-id="0e3ba-161">Get-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="0e3ba-161">Get-AzSqlDatabaseThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="0e3ba-162">Remove-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="0e3ba-162">Remove-AzSqlDatabaseThreatDetectionsettings</span></span>](./Remove-AzSqlDatabaseThreatDetectionsettings.md)

[<span data-ttu-id="0e3ba-163">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="0e3ba-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


