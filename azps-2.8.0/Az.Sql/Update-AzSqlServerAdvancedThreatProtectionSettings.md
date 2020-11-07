---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlServerAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSettings.md
ms.openlocfilehash: 16fa9df22141b62f8a5b7ff3b6cad3ca05b1d406
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839563"
---
# <span data-ttu-id="efe06-101">Update-AzSqlServerAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="efe06-101">Update-AzSqlServerAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="efe06-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="efe06-102">SYNOPSIS</span></span>
<span data-ttu-id="efe06-103">Speciális veszélyforrások elleni védelemre vonatkozó beállításokat állít be a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="efe06-103">Sets a advanced threat protection settings on a server.</span></span>

## <span data-ttu-id="efe06-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="efe06-104">SYNTAX</span></span>

```
Update-AzSqlServerAdvancedThreatProtectionSettings [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efe06-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="efe06-105">DESCRIPTION</span></span>
<span data-ttu-id="efe06-106">Az **Update-AzSqlServerAdvancedThreatProtectionSettings** parancsmag egy Azure SQL Server-kiszolgálón az Advanced Threat Protection beállításait állítja be.</span><span class="sxs-lookup"><span data-stu-id="efe06-106">The **Update-AzSqlServerAdvancedThreatProtectionSettings** cmdlet sets a advanced threat protection settings on an Azure SQL server.</span></span>
<span data-ttu-id="efe06-107">A kiszolgálón futó speciális veszélyforrások elleni védelem engedélyezéséhez a naplózási beállításokat engedélyeznie kell a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="efe06-107">In order to enable advanced threat protection on a server an auditing settings must be enabled on that server.</span></span>
<span data-ttu-id="efe06-108">A parancsmag használatához adja meg a *ResourceGroupName* és a kiszolgálónév paramétert a kiszolgáló azonosítójának megadásához.</span><span class="sxs-lookup"><span data-stu-id="efe06-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="efe06-109">Példák</span><span class="sxs-lookup"><span data-stu-id="efe06-109">EXAMPLES</span></span>

### <span data-ttu-id="efe06-110">1. példa: az adatbázis speciális veszélyforrásokkal kapcsolatos védelmi beállításainak megadása</span><span class="sxs-lookup"><span data-stu-id="efe06-110">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="efe06-111">Ez a parancs beállítja a Server01 nevű kiszolgáló speciális veszélyforrások elleni védelmét.</span><span class="sxs-lookup"><span data-stu-id="efe06-111">This command sets the advanced threat protection settings for a server named Server01.</span></span>

## <span data-ttu-id="efe06-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="efe06-112">PARAMETERS</span></span>

### <span data-ttu-id="efe06-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efe06-113">-DefaultProfile</span></span>
<span data-ttu-id="efe06-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="efe06-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="efe06-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="efe06-115">-EmailAdmins</span></span>
<span data-ttu-id="efe06-116">Meghatározza, hogy a speciális veszélyforrások elleni védelem beállításai a rendszergazdák e-mailen keresztül kerülnek-e kapcsolatba.</span><span class="sxs-lookup"><span data-stu-id="efe06-116">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="efe06-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="efe06-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="efe06-118">A beállításokból kizárandó észlelési típusok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="efe06-118">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="efe06-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="efe06-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="efe06-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="efe06-120">Sql_Injection</span></span>
- <span data-ttu-id="efe06-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="efe06-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="efe06-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="efe06-122">Access_Anomaly</span></span>
- <span data-ttu-id="efe06-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="efe06-123">None</span></span>

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

### <span data-ttu-id="efe06-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="efe06-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="efe06-125">Az e-mail-címek pontosvesszővel elválasztott listáját adja meg, amelyre a beállítások riasztásokat küldenek.</span><span class="sxs-lookup"><span data-stu-id="efe06-125">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="efe06-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="efe06-126">-PassThru</span></span>
<span data-ttu-id="efe06-127">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="efe06-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="efe06-128">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="efe06-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="efe06-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efe06-129">-ResourceGroupName</span></span>
<span data-ttu-id="efe06-130">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="efe06-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="efe06-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="efe06-131">-RetentionInDays</span></span>
<span data-ttu-id="efe06-132">A naplók adatmegőrzési napjainak száma</span><span class="sxs-lookup"><span data-stu-id="efe06-132">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="efe06-133">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="efe06-133">-ServerName</span></span>
<span data-ttu-id="efe06-134">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="efe06-134">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efe06-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="efe06-135">-StorageAccountName</span></span>
<span data-ttu-id="efe06-136">A használandó tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="efe06-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="efe06-137">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="efe06-137">Wildcards are not permitted.</span></span> <span data-ttu-id="efe06-138">Ehhez a paraméterhez nincs szükség.</span><span class="sxs-lookup"><span data-stu-id="efe06-138">This parameter is not required.</span></span> <span data-ttu-id="efe06-139">Ha ez a paraméter nincs megadva, a parancsmag az adatbázis speciális veszélyforrások elleni védelmének részeként megadott tárolási fiókot fogja használni.</span><span class="sxs-lookup"><span data-stu-id="efe06-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="efe06-140">Ha ez az első alkalom, hogy az adatbázis-fenyegetések észlelési beállításai meg vannak adva, és ez a paraméter nincs megadva, a parancsmag sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="efe06-140">If this is the first time a database threat detection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="efe06-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="efe06-141">-Confirm</span></span>
<span data-ttu-id="efe06-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="efe06-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efe06-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efe06-143">-WhatIf</span></span>
<span data-ttu-id="efe06-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="efe06-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efe06-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="efe06-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efe06-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efe06-146">CommonParameters</span></span>
<span data-ttu-id="efe06-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="efe06-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efe06-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efe06-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efe06-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="efe06-149">INPUTS</span></span>

### <span data-ttu-id="efe06-150">System. String</span><span class="sxs-lookup"><span data-stu-id="efe06-150">System.String</span></span>

### <span data-ttu-id="efe06-151">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="efe06-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="efe06-152">Microsoft. Azure. Command. SQL. ThreatDetection. Model. DetectionType []</span><span class="sxs-lookup"><span data-stu-id="efe06-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="efe06-153">System. null ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="efe06-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="efe06-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="efe06-154">OUTPUTS</span></span>

### <span data-ttu-id="efe06-155">Microsoft. Azure. Command. SQL. ThreatDetection. Model. ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="efe06-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="efe06-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="efe06-156">NOTES</span></span>

## <span data-ttu-id="efe06-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="efe06-157">RELATED LINKS</span></span>

[<span data-ttu-id="efe06-158">Get-AzSqlServerThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="efe06-158">Get-AzSqlServerThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="efe06-159">Remove-AzSqlServerThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="efe06-159">Remove-AzSqlServerThreatDetectionsettings</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="efe06-160">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="efe06-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
