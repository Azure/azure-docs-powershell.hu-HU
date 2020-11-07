---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 8d58085aa55958e6e0fc9658d814d4bc05006fd6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668747"
---
# <span data-ttu-id="fb226-101">Set-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fb226-101">Set-AzSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="fb226-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb226-102">SYNOPSIS</span></span>
<span data-ttu-id="fb226-103">Veszélyforrás-észlelési házirendet állít be a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="fb226-103">Sets a threat detection policy on a server.</span></span>

## <span data-ttu-id="fb226-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb226-104">SYNTAX</span></span>

```
Set-AzSqlServerThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb226-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb226-105">DESCRIPTION</span></span>
<span data-ttu-id="fb226-106">A **set-AzSqlServerThreatDetectionPolicy** parancsmag fenyegetés-észlelési házirendet állít be egy Azure SQL Serveren.</span><span class="sxs-lookup"><span data-stu-id="fb226-106">The **Set-AzSqlServerThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL server.</span></span>
<span data-ttu-id="fb226-107">A fenyegetések észlelésének engedélyezéséhez a kiszolgálón engedélyeznie kell a naplózási házirendet.</span><span class="sxs-lookup"><span data-stu-id="fb226-107">In order to enable threat detection on a server an auditing policy must be enabled on that server.</span></span>
<span data-ttu-id="fb226-108">A parancsmag használatához adja meg a *ResourceGroupName* és a kiszolgálónév paramétert a kiszolgáló azonosítójának megadásához.</span><span class="sxs-lookup"><span data-stu-id="fb226-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="fb226-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fb226-109">EXAMPLES</span></span>

### <span data-ttu-id="fb226-110">1. példa: az adatbázis veszélyforrás-észlelési házirendjének beállítása</span><span class="sxs-lookup"><span data-stu-id="fb226-110">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="fb226-111">Ez a parancs beállítja a Server01 nevű kiszolgáló veszélyforrás-észlelési házirendjét.</span><span class="sxs-lookup"><span data-stu-id="fb226-111">This command sets the threat detection policy for a server named Server01.</span></span>

## <span data-ttu-id="fb226-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb226-112">PARAMETERS</span></span>

### <span data-ttu-id="fb226-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb226-113">-DefaultProfile</span></span>
<span data-ttu-id="fb226-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fb226-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb226-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="fb226-115">-EmailAdmins</span></span>
<span data-ttu-id="fb226-116">Azt adja meg, hogy a fenyegetés észlelése házirend a rendszergazdákat e-mailben használja-e.</span><span class="sxs-lookup"><span data-stu-id="fb226-116">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="fb226-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="fb226-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="fb226-118">A házirendből kizárandó észlelési típusokból álló tömböt adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb226-118">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="fb226-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="fb226-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fb226-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="fb226-120">Sql_Injection</span></span>
- <span data-ttu-id="fb226-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="fb226-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="fb226-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="fb226-122">Access_Anomaly</span></span>
- <span data-ttu-id="fb226-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="fb226-123">None</span></span>

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

### <span data-ttu-id="fb226-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="fb226-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="fb226-125">A házirend által küldött e-mail-címek pontosvesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb226-125">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="fb226-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb226-126">-PassThru</span></span>
<span data-ttu-id="fb226-127">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="fb226-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fb226-128">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="fb226-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fb226-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb226-129">-ResourceGroupName</span></span>
<span data-ttu-id="fb226-130">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="fb226-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="fb226-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="fb226-131">-RetentionInDays</span></span>
<span data-ttu-id="fb226-132">A naplók adatmegőrzési napjainak száma</span><span class="sxs-lookup"><span data-stu-id="fb226-132">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="fb226-133">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="fb226-133">-ServerName</span></span>
<span data-ttu-id="fb226-134">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb226-134">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="fb226-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fb226-135">-StorageAccountName</span></span>
<span data-ttu-id="fb226-136">A használandó tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb226-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="fb226-137">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="fb226-137">Wildcards are not permitted.</span></span> <span data-ttu-id="fb226-138">Ehhez a paraméterhez nincs szükség.</span><span class="sxs-lookup"><span data-stu-id="fb226-138">This parameter is not required.</span></span> <span data-ttu-id="fb226-139">Ha ezt a paramétert nem jeleníti meg, a parancsmag az adatbázis veszélyforrások észlelési házirendjének részeként megadott tárolási fiókot fogja használni.</span><span class="sxs-lookup"><span data-stu-id="fb226-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="fb226-140">Ha ez az első alkalom, hogy egy adatbázis-theat-észlelési házirend van definiálva, és ez a paraméter nem jelenik meg, a parancsmag nem fog működni.</span><span class="sxs-lookup"><span data-stu-id="fb226-140">If this is the first time a database theat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="fb226-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fb226-141">-Confirm</span></span>
<span data-ttu-id="fb226-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fb226-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb226-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb226-143">-WhatIf</span></span>
<span data-ttu-id="fb226-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fb226-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb226-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fb226-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb226-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb226-146">CommonParameters</span></span>
<span data-ttu-id="fb226-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb226-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb226-148">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fb226-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb226-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb226-149">INPUTS</span></span>

### <span data-ttu-id="fb226-150">System. String</span><span class="sxs-lookup"><span data-stu-id="fb226-150">System.String</span></span>

### <span data-ttu-id="fb226-151">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fb226-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fb226-152">Microsoft. Azure. Command. SQL. ThreatDetection. Model. DetectionType []</span><span class="sxs-lookup"><span data-stu-id="fb226-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="fb226-153">System. null ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fb226-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="fb226-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb226-154">OUTPUTS</span></span>

### <span data-ttu-id="fb226-155">Microsoft. Azure. Command. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="fb226-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="fb226-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb226-156">NOTES</span></span>

## <span data-ttu-id="fb226-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb226-157">RELATED LINKS</span></span>

[<span data-ttu-id="fb226-158">Get-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fb226-158">Get-AzSqlServerThreatDetectionPolicy</span></span>](./Get-AzSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="fb226-159">Remove-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fb226-159">Remove-AzSqlServerThreatDetectionPolicy</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="fb226-160">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="fb226-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
