---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 3ec370f0e4865ed5695e4f0890f99b50709e9ad8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846445"
---
# <span data-ttu-id="ac300-101">Update-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="ac300-101">Update-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="ac300-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ac300-102">SYNOPSIS</span></span>
<span data-ttu-id="ac300-103">Speciális veszélyforrások elleni védelemre vonatkozó beállításokat állít be a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="ac300-103">Sets a advanced threat protection settings on a server.</span></span>

## <span data-ttu-id="ac300-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ac300-104">SYNTAX</span></span>

```
Update-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac300-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ac300-105">DESCRIPTION</span></span>
<span data-ttu-id="ac300-106">Az **Update-AzSqlServerAdvancedThreatProtectionSetting** parancsmag egy Azure SQL Server-kiszolgálón az Advanced Threat Protection beállításait állítja be.</span><span class="sxs-lookup"><span data-stu-id="ac300-106">The **Update-AzSqlServerAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL server.</span></span>
<span data-ttu-id="ac300-107">A kiszolgálón futó speciális veszélyforrások elleni védelem engedélyezéséhez a naplózási beállításokat engedélyeznie kell a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="ac300-107">In order to enable advanced threat protection on a server an auditing settings must be enabled on that server.</span></span>
<span data-ttu-id="ac300-108">A parancsmag használatához adja meg a *ResourceGroupName* és a kiszolgálónév paramétert a kiszolgáló azonosítójának megadásához.</span><span class="sxs-lookup"><span data-stu-id="ac300-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="ac300-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ac300-109">EXAMPLES</span></span>

### <span data-ttu-id="ac300-110">1. példa: az adatbázis speciális veszélyforrásokkal kapcsolatos védelmi beállításainak megadása</span><span class="sxs-lookup"><span data-stu-id="ac300-110">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="ac300-111">Ez a parancs beállítja a Server01 nevű kiszolgáló speciális veszélyforrások elleni védelmét.</span><span class="sxs-lookup"><span data-stu-id="ac300-111">This command sets the advanced threat protection settings for a server named Server01.</span></span>

## <span data-ttu-id="ac300-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ac300-112">PARAMETERS</span></span>

### <span data-ttu-id="ac300-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac300-113">-DefaultProfile</span></span>
<span data-ttu-id="ac300-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ac300-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac300-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="ac300-115">-EmailAdmins</span></span>
<span data-ttu-id="ac300-116">Meghatározza, hogy a speciális veszélyforrások elleni védelem beállításai a rendszergazdák e-mailen keresztül kerülnek-e kapcsolatba.</span><span class="sxs-lookup"><span data-stu-id="ac300-116">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="ac300-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="ac300-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="ac300-118">A beállításokból kizárandó észlelési típusok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ac300-118">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="ac300-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ac300-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ac300-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="ac300-120">Sql_Injection</span></span>
- <span data-ttu-id="ac300-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="ac300-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="ac300-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="ac300-122">Access_Anomaly</span></span>
- <span data-ttu-id="ac300-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="ac300-123">None</span></span>

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

### <span data-ttu-id="ac300-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="ac300-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="ac300-125">Az e-mail-címek pontosvesszővel elválasztott listáját adja meg, amelyre a beállítások riasztásokat küldenek.</span><span class="sxs-lookup"><span data-stu-id="ac300-125">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="ac300-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac300-126">-PassThru</span></span>
<span data-ttu-id="ac300-127">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ac300-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ac300-128">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ac300-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ac300-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac300-129">-ResourceGroupName</span></span>
<span data-ttu-id="ac300-130">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="ac300-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="ac300-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="ac300-131">-RetentionInDays</span></span>
<span data-ttu-id="ac300-132">A naplók adatmegőrzési napjainak száma</span><span class="sxs-lookup"><span data-stu-id="ac300-132">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="ac300-133">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="ac300-133">-ServerName</span></span>
<span data-ttu-id="ac300-134">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ac300-134">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="ac300-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ac300-135">-StorageAccountName</span></span>
<span data-ttu-id="ac300-136">A használandó tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ac300-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="ac300-137">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="ac300-137">Wildcards are not permitted.</span></span> <span data-ttu-id="ac300-138">Ehhez a paraméterhez nincs szükség.</span><span class="sxs-lookup"><span data-stu-id="ac300-138">This parameter is not required.</span></span> <span data-ttu-id="ac300-139">Ha ez a paraméter nincs megadva, a parancsmag az adatbázis speciális veszélyforrások elleni védelmének részeként megadott tárolási fiókot fogja használni.</span><span class="sxs-lookup"><span data-stu-id="ac300-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="ac300-140">Ha ez az első alkalom, hogy az adatbázis-fenyegetések észlelési beállításai meg vannak adva, és ez a paraméter nincs megadva, a parancsmag sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="ac300-140">If this is the first time a database threat detection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="ac300-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ac300-141">-Confirm</span></span>
<span data-ttu-id="ac300-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ac300-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac300-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac300-143">-WhatIf</span></span>
<span data-ttu-id="ac300-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ac300-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac300-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ac300-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac300-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac300-146">CommonParameters</span></span>
<span data-ttu-id="ac300-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ac300-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac300-148">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ac300-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac300-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac300-149">INPUTS</span></span>

### <span data-ttu-id="ac300-150">System. String</span><span class="sxs-lookup"><span data-stu-id="ac300-150">System.String</span></span>

### <span data-ttu-id="ac300-151">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ac300-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ac300-152">Microsoft. Azure. Command. SQL. ThreatDetection. Model. DetectionType []</span><span class="sxs-lookup"><span data-stu-id="ac300-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="ac300-153">System. null ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ac300-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ac300-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac300-154">OUTPUTS</span></span>

### <span data-ttu-id="ac300-155">Microsoft. Azure. Command. SQL. ThreatDetection. Model. ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="ac300-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="ac300-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ac300-156">NOTES</span></span>

## <span data-ttu-id="ac300-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac300-157">RELATED LINKS</span></span>

[<span data-ttu-id="ac300-158">Get-AzSqlServerThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="ac300-158">Get-AzSqlServerThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="ac300-159">Remove-AzSqlServerThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="ac300-159">Remove-AzSqlServerThreatDetectionsettings</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="ac300-160">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="ac300-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
