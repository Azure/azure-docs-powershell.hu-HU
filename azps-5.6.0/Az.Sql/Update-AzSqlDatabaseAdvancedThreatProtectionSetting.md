---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/powershell/module/az.sql/Update-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 9677f45e772cbcb48190f5792df97e96051180c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939314"
---
# <span data-ttu-id="5a925-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="5a925-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="5a925-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a925-102">SYNOPSIS</span></span>
<span data-ttu-id="5a925-103">Speciális veszélyforrás-védelmi beállításokat ad meg az adatbázisokban.</span><span class="sxs-lookup"><span data-stu-id="5a925-103">Sets a advanced threat protection settings on a database.</span></span>

## <span data-ttu-id="5a925-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5a925-104">SYNTAX</span></span>

```
Update-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a925-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5a925-105">DESCRIPTION</span></span>
<span data-ttu-id="5a925-106">Az **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** parancsmag speciális veszélyforrás-védelmi beállításokat állít be egy Azure SQL-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="5a925-106">The **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL database.</span></span>
<span data-ttu-id="5a925-107">A komplex veszélyforrások elleni védelem speciális védelméhez engedélyezni kell az adatbázisban a naplózási beállításokat.</span><span class="sxs-lookup"><span data-stu-id="5a925-107">In order to enable advanced threat protection on a database an auditing settings must be enabled on that database.</span></span>
<span data-ttu-id="5a925-108">A parancsmagot a *ResourceGroupName,* *a ServerName* és a *DatabaseName* paraméter megadásával azonosíthatja az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="5a925-108">To use this cmdlet, specify the *ResourceGroupName*, *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="5a925-109">Ezt a parancsmagot az Azure SQL Server Stretch Database szolgáltatása is támogatja.</span><span class="sxs-lookup"><span data-stu-id="5a925-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="5a925-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5a925-110">EXAMPLES</span></span>

### <span data-ttu-id="5a925-111">1. példa: Az adatbázisok komplex veszélyforrások elleni védelmi beállításainak megadása</span><span class="sxs-lookup"><span data-stu-id="5a925-111">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="5a925-112">Ez a parancs beállítja egy Database01 nevű adatbázis komplex veszélyforrás-védelmi beállításait a Server01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="5a925-112">This command sets the advanced threat protection settings for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="5a925-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a925-113">PARAMETERS</span></span>

### <span data-ttu-id="5a925-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5a925-114">-DatabaseName</span></span>
<span data-ttu-id="5a925-115">Annak az adatbázisnak a nevét adja meg, amelyben a beállítások meg vannak állítva.</span><span class="sxs-lookup"><span data-stu-id="5a925-115">Specifies the name of the database where the settings is set.</span></span>

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

### <span data-ttu-id="5a925-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a925-116">-DefaultProfile</span></span>
<span data-ttu-id="5a925-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5a925-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a925-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="5a925-118">-EmailAdmins</span></span>
<span data-ttu-id="5a925-119">Azt adja meg, hogy a komplex veszélyforrások elleni védelem speciális beállításai e-mailben lépnek-e kapcsolatba a rendszergazdákval.</span><span class="sxs-lookup"><span data-stu-id="5a925-119">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="5a925-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="5a925-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="5a925-121">A beállításokból kizárandó észlelési típusok tömbje.</span><span class="sxs-lookup"><span data-stu-id="5a925-121">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="5a925-122">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="5a925-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5a925-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="5a925-123">Sql_Injection</span></span> 
- <span data-ttu-id="5a925-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="5a925-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="5a925-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="5a925-125">Access_Anomaly</span></span> 
- <span data-ttu-id="5a925-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="5a925-126">None</span></span>

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

### <span data-ttu-id="5a925-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="5a925-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="5a925-128">Pontosvesszővel elválasztott listát ad meg azokról az e-mail-címekről, amelyekre a beállítások riasztásokat küld.</span><span class="sxs-lookup"><span data-stu-id="5a925-128">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="5a925-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a925-129">-PassThru</span></span>
<span data-ttu-id="5a925-130">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="5a925-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5a925-131">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="5a925-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5a925-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a925-132">-ResourceGroupName</span></span>
<span data-ttu-id="5a925-133">Annak az erőforráscsoportnak a neve, amelyhez a kiszolgáló hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="5a925-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="5a925-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="5a925-134">-RetentionInDays</span></span>
<span data-ttu-id="5a925-135">A naplók adatmegőrzési napjainak száma</span><span class="sxs-lookup"><span data-stu-id="5a925-135">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="5a925-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5a925-136">-ServerName</span></span>
<span data-ttu-id="5a925-137">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a925-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="5a925-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5a925-138">-StorageAccountName</span></span>
<span data-ttu-id="5a925-139">A használni használt tárfiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a925-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="5a925-140">A helyettesítő karakterek használata nem engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="5a925-140">Wildcards are not permitted.</span></span> <span data-ttu-id="5a925-141">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5a925-141">This parameter is not required.</span></span> <span data-ttu-id="5a925-142">Ha ez a paraméter nincs megadva, a parancsmag az adatbázis komplex veszélyforrás-védelmi beállításainak részeként korábban definiált tárfiókot fogja használni.</span><span class="sxs-lookup"><span data-stu-id="5a925-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="5a925-143">Ha első alkalommal határoz meg komplex veszélyforrások elleni védelemre vonatkozó adatbázis-beállításokat, és ez a paraméter nincs megadva, a parancsmag nem fog működni.</span><span class="sxs-lookup"><span data-stu-id="5a925-143">If this is the first time a database advanced threat protection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="5a925-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a925-144">-Confirm</span></span>
<span data-ttu-id="5a925-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5a925-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a925-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a925-146">-WhatIf</span></span>
<span data-ttu-id="5a925-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5a925-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a925-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5a925-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a925-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a925-149">CommonParameters</span></span>
<span data-ttu-id="5a925-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a925-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a925-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a925-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a925-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a925-152">INPUTS</span></span>

### <span data-ttu-id="5a925-153">System.String</span><span class="sxs-lookup"><span data-stu-id="5a925-153">System.String</span></span>

### <span data-ttu-id="5a925-154">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5a925-154">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5a925-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span><span class="sxs-lookup"><span data-stu-id="5a925-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="5a925-156">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5a925-156">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5a925-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a925-157">OUTPUTS</span></span>

### <span data-ttu-id="5a925-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="5a925-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="5a925-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5a925-159">NOTES</span></span>

## <span data-ttu-id="5a925-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a925-160">RELATED LINKS</span></span>

[<span data-ttu-id="5a925-161">Get-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="5a925-161">Get-AzSqlDatabaseThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="5a925-162">Remove-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="5a925-162">Remove-AzSqlDatabaseThreatDetectionsettings</span></span>](./Remove-AzSqlDatabaseThreatDetectionsettings.md)

[<span data-ttu-id="5a925-163">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="5a925-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


