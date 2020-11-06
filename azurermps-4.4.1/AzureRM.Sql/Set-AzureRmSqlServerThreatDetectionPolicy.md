---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 7c71e9390ca28b48127a2f977e04eba645ae962f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505567"
---
# <span data-ttu-id="93b39-101">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="93b39-101">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="93b39-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="93b39-102">SYNOPSIS</span></span>
<span data-ttu-id="93b39-103">Veszélyforrás-észlelési házirendet állít be a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="93b39-103">Sets a threat detection policy on a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93b39-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="93b39-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93b39-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="93b39-105">DESCRIPTION</span></span>
<span data-ttu-id="93b39-106">A **set-AzureRmSqlServerThreatDetectionPolicy** parancsmag fenyegetés-észlelési házirendet állít be egy Azure SQL Serveren.</span><span class="sxs-lookup"><span data-stu-id="93b39-106">The **Set-AzureRmSqlServerThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL server.</span></span>
<span data-ttu-id="93b39-107">A fenyegetések észlelésének engedélyezéséhez a kiszolgálón engedélyeznie kell a naplózási házirendet.</span><span class="sxs-lookup"><span data-stu-id="93b39-107">In order to enable threat detection on a server an auditing policy must be enabled on that server.</span></span>
<span data-ttu-id="93b39-108">A parancsmag használatához adja meg a *ResourceGroupName* és a kiszolgálónév paramétert a kiszolgáló azonosítójának megadásához.</span><span class="sxs-lookup"><span data-stu-id="93b39-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="93b39-109">Példák</span><span class="sxs-lookup"><span data-stu-id="93b39-109">EXAMPLES</span></span>

### <span data-ttu-id="93b39-110">1. példa: az adatbázis veszélyforrás-észlelési házirendjének beállítása</span><span class="sxs-lookup"><span data-stu-id="93b39-110">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="93b39-111">Ez a parancs beállítja a Server01 nevű kiszolgáló veszélyforrás-észlelési házirendjét.</span><span class="sxs-lookup"><span data-stu-id="93b39-111">This command sets the threat detection policy for a server named Server01.</span></span>

## <span data-ttu-id="93b39-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="93b39-112">PARAMETERS</span></span>

### <span data-ttu-id="93b39-113">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="93b39-113">-EmailAdmins</span></span>
<span data-ttu-id="93b39-114">Azt adja meg, hogy a fenyegetés észlelése házirend a rendszergazdákat e-mailben használja-e.</span><span class="sxs-lookup"><span data-stu-id="93b39-114">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="93b39-115">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="93b39-115">-ExcludedDetectionType</span></span>
<span data-ttu-id="93b39-116">A házirendből kizárandó észlelési típusokból álló tömböt adja meg.</span><span class="sxs-lookup"><span data-stu-id="93b39-116">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="93b39-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="93b39-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="93b39-118">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="93b39-118">Sql_Injection</span></span>
- <span data-ttu-id="93b39-119">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="93b39-119">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="93b39-120">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="93b39-120">Access_Anomaly</span></span>
- <span data-ttu-id="93b39-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="93b39-121">None</span></span>

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

### <span data-ttu-id="93b39-122">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="93b39-122">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="93b39-123">A házirend által küldött e-mail-címek pontosvesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="93b39-123">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="93b39-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93b39-124">-PassThru</span></span>
<span data-ttu-id="93b39-125">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="93b39-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="93b39-126">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="93b39-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="93b39-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93b39-127">-ResourceGroupName</span></span>
<span data-ttu-id="93b39-128">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="93b39-128">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="93b39-129">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="93b39-129">-RetentionInDays</span></span>
<span data-ttu-id="93b39-130">A naplók adatmegőrzési napjainak száma</span><span class="sxs-lookup"><span data-stu-id="93b39-130">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="93b39-131">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="93b39-131">-ServerName</span></span>
<span data-ttu-id="93b39-132">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="93b39-132">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="93b39-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="93b39-133">-StorageAccountName</span></span>
<span data-ttu-id="93b39-134">A használandó tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="93b39-134">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="93b39-135">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="93b39-135">Wildcards are not permitted.</span></span> <span data-ttu-id="93b39-136">Ehhez a paraméterhez nincs szükség.</span><span class="sxs-lookup"><span data-stu-id="93b39-136">This parameter is not required.</span></span> <span data-ttu-id="93b39-137">Ha ezt a paramétert nem jeleníti meg, a parancsmag az adatbázis veszélyforrások észlelési házirendjének részeként megadott tárolási fiókot fogja használni.</span><span class="sxs-lookup"><span data-stu-id="93b39-137">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="93b39-138">Ha ez az első alkalom, hogy egy adatbázis-theat-észlelési házirend van definiálva, és ez a paraméter nem jelenik meg, a parancsmag nem fog működni.</span><span class="sxs-lookup"><span data-stu-id="93b39-138">If this is the first time a database theat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="93b39-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="93b39-139">-Confirm</span></span>
<span data-ttu-id="93b39-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="93b39-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93b39-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93b39-141">-WhatIf</span></span>
<span data-ttu-id="93b39-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="93b39-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93b39-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="93b39-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93b39-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93b39-144">-DefaultProfile</span></span>
<span data-ttu-id="93b39-145">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="93b39-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93b39-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93b39-146">CommonParameters</span></span>
<span data-ttu-id="93b39-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="93b39-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93b39-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93b39-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93b39-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="93b39-149">INPUTS</span></span>

###  
<span data-ttu-id="93b39-150">Ebben a parancsmagban nem lehet beírni a bemenetet.</span><span class="sxs-lookup"><span data-stu-id="93b39-150">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="93b39-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93b39-151">OUTPUTS</span></span>

### <span data-ttu-id="93b39-152">Microsoft. Azure. Command. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="93b39-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>
<span data-ttu-id="93b39-153">Ez a parancsmag egy **ServerThreatDetectionPolicyModel** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="93b39-153">This cmdlet returns a **ServerThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="93b39-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="93b39-154">NOTES</span></span>

## <span data-ttu-id="93b39-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93b39-155">RELATED LINKS</span></span>

[<span data-ttu-id="93b39-156">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="93b39-156">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="93b39-157">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="93b39-157">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="93b39-158">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="93b39-158">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
