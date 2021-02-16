---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: baa3e3d4b272bccab5fe33b9af05edc9ed254236
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406706"
---
# <span data-ttu-id="35d47-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="35d47-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="35d47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35d47-102">SYNOPSIS</span></span>
<span data-ttu-id="35d47-103">Speciális veszélyforrás-védelmi beállításokat ad meg az adatbázisokban.</span><span class="sxs-lookup"><span data-stu-id="35d47-103">Sets a advanced threat protection settings on a database.</span></span>

## <span data-ttu-id="35d47-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="35d47-104">SYNTAX</span></span>

```
Update-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35d47-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="35d47-105">DESCRIPTION</span></span>
<span data-ttu-id="35d47-106">Az **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** parancsmag speciális veszélyforrás-védelmi beállításokat állít be egy Azure SQL-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="35d47-106">The **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL database.</span></span>
<span data-ttu-id="35d47-107">A komplex veszélyforrások elleni védelem adatbázison való speciális védelméhez engedélyezni kell az adatbázis naplózási beállításait.</span><span class="sxs-lookup"><span data-stu-id="35d47-107">In order to enable advanced threat protection on a database an auditing settings must be enabled on that database.</span></span>
<span data-ttu-id="35d47-108">A parancsmagot a *ResourceGroupName,* *a ServerName* és a *DatabaseName* paraméter megadásával azonosíthatja az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="35d47-108">To use this cmdlet, specify the *ResourceGroupName*, *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="35d47-109">Ezt a parancsmagot az Azure SQL Server Stretch Database szolgáltatása is támogatja.</span><span class="sxs-lookup"><span data-stu-id="35d47-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="35d47-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="35d47-110">EXAMPLES</span></span>

### <span data-ttu-id="35d47-111">1. példa: Az adatbázisok komplex veszélyforrások elleni védelmi beállításainak megadása</span><span class="sxs-lookup"><span data-stu-id="35d47-111">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="35d47-112">Ez a parancs a Database01 nevű adatbázis komplex veszélyforrás-védelmi beállításait állítja be a Server01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="35d47-112">This command sets the advanced threat protection settings for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="35d47-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35d47-113">PARAMETERS</span></span>

### <span data-ttu-id="35d47-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="35d47-114">-DatabaseName</span></span>
<span data-ttu-id="35d47-115">Annak az adatbázisnak a nevét adja meg, amelyben a beállítások meg vannak állítva.</span><span class="sxs-lookup"><span data-stu-id="35d47-115">Specifies the name of the database where the settings is set.</span></span>

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

### <span data-ttu-id="35d47-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35d47-116">-DefaultProfile</span></span>
<span data-ttu-id="35d47-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="35d47-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35d47-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="35d47-118">-EmailAdmins</span></span>
<span data-ttu-id="35d47-119">Azt adja meg, hogy a komplex veszélyforrások elleni védelem speciális beállításai e-mailben lépnek-e a rendszergazdákhoz.</span><span class="sxs-lookup"><span data-stu-id="35d47-119">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="35d47-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="35d47-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="35d47-121">A beállításokból kizárandó észlelési típusok tömbje.</span><span class="sxs-lookup"><span data-stu-id="35d47-121">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="35d47-122">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="35d47-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="35d47-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="35d47-123">Sql_Injection</span></span>
- <span data-ttu-id="35d47-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="35d47-124">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="35d47-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="35d47-125">Access_Anomaly</span></span>
- <span data-ttu-id="35d47-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="35d47-126">None</span></span>

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

### <span data-ttu-id="35d47-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="35d47-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="35d47-128">Pontosvesszővel elválasztott listát ad meg azokról az e-mail-címekről, amelyekre a beállítások riasztásokat küld.</span><span class="sxs-lookup"><span data-stu-id="35d47-128">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="35d47-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35d47-129">-PassThru</span></span>
<span data-ttu-id="35d47-130">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="35d47-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="35d47-131">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="35d47-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="35d47-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35d47-132">-ResourceGroupName</span></span>
<span data-ttu-id="35d47-133">Annak az erőforráscsoportnak a neve, amelyhez a kiszolgáló hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="35d47-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="35d47-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="35d47-134">-RetentionInDays</span></span>
<span data-ttu-id="35d47-135">A naplók adatmegőrzési napjainak száma</span><span class="sxs-lookup"><span data-stu-id="35d47-135">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="35d47-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="35d47-136">-ServerName</span></span>
<span data-ttu-id="35d47-137">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="35d47-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="35d47-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="35d47-138">-StorageAccountName</span></span>
<span data-ttu-id="35d47-139">A használni használt tárfiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="35d47-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="35d47-140">A helyettesítő karakterek használata nem engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="35d47-140">Wildcards are not permitted.</span></span> <span data-ttu-id="35d47-141">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="35d47-141">This parameter is not required.</span></span> <span data-ttu-id="35d47-142">Ha ez a paraméter nincs megadva, a parancsmag az adatbázis komplex veszélyforrás-védelmi beállításainak részeként korábban definiált tárfiókot fogja használni.</span><span class="sxs-lookup"><span data-stu-id="35d47-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="35d47-143">Ha első alkalommal határoz meg komplex veszélyforrások elleni védelemre vonatkozó adatbázis-beállításokat, és ez a paraméter nincs megadva, a parancsmag nem fog működni.</span><span class="sxs-lookup"><span data-stu-id="35d47-143">If this is the first time a database advanced threat protection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="35d47-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35d47-144">-Confirm</span></span>
<span data-ttu-id="35d47-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="35d47-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35d47-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35d47-146">-WhatIf</span></span>
<span data-ttu-id="35d47-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="35d47-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35d47-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="35d47-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35d47-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35d47-149">CommonParameters</span></span>
<span data-ttu-id="35d47-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35d47-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35d47-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35d47-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35d47-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35d47-152">INPUTS</span></span>

### <span data-ttu-id="35d47-153">System.String</span><span class="sxs-lookup"><span data-stu-id="35d47-153">System.String</span></span>

### <span data-ttu-id="35d47-154">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="35d47-154">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="35d47-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span><span class="sxs-lookup"><span data-stu-id="35d47-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="35d47-156">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="35d47-156">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="35d47-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35d47-157">OUTPUTS</span></span>

### <span data-ttu-id="35d47-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="35d47-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="35d47-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="35d47-159">NOTES</span></span>

## <span data-ttu-id="35d47-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35d47-160">RELATED LINKS</span></span>

[<span data-ttu-id="35d47-161">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="35d47-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
