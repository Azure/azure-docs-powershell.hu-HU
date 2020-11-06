---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 40ce06b21be7312598978bbd56b10e4e33915ece
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492987"
---
# <span data-ttu-id="7d23d-101">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7d23d-101">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="7d23d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7d23d-102">SYNOPSIS</span></span>
<span data-ttu-id="7d23d-103">Veszélyforrás-észlelési házirendet állít be a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="7d23d-103">Sets a threat detection policy on a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d23d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7d23d-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d23d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7d23d-105">DESCRIPTION</span></span>
<span data-ttu-id="7d23d-106">A **set-AzureRmSqlServerThreatDetectionPolicy** parancsmag fenyegetés-észlelési házirendet állít be egy Azure SQL Serveren.</span><span class="sxs-lookup"><span data-stu-id="7d23d-106">The **Set-AzureRmSqlServerThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL server.</span></span>
<span data-ttu-id="7d23d-107">A fenyegetések észlelésének engedélyezéséhez a kiszolgálón engedélyeznie kell a naplózási házirendet.</span><span class="sxs-lookup"><span data-stu-id="7d23d-107">In order to enable threat detection on a server an auditing policy must be enabled on that server.</span></span>
<span data-ttu-id="7d23d-108">A parancsmag használatához adja meg a *ResourceGroupName* és a kiszolgálónév paramétert a kiszolgáló azonosítójának megadásához.</span><span class="sxs-lookup"><span data-stu-id="7d23d-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="7d23d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7d23d-109">EXAMPLES</span></span>

### <span data-ttu-id="7d23d-110">1. példa: az adatbázis veszélyforrás-észlelési házirendjének beállítása</span><span class="sxs-lookup"><span data-stu-id="7d23d-110">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="7d23d-111">Ez a parancs beállítja a Server01 nevű kiszolgáló veszélyforrás-észlelési házirendjét.</span><span class="sxs-lookup"><span data-stu-id="7d23d-111">This command sets the threat detection policy for a server named Server01.</span></span>

## <span data-ttu-id="7d23d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7d23d-112">PARAMETERS</span></span>

### <span data-ttu-id="7d23d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d23d-113">-DefaultProfile</span></span>
<span data-ttu-id="7d23d-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7d23d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d23d-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="7d23d-115">-EmailAdmins</span></span>
<span data-ttu-id="7d23d-116">Azt adja meg, hogy a fenyegetés észlelése házirend a rendszergazdákat e-mailben használja-e.</span><span class="sxs-lookup"><span data-stu-id="7d23d-116">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="7d23d-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="7d23d-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="7d23d-118">A házirendből kizárandó észlelési típusokból álló tömböt adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d23d-118">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="7d23d-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7d23d-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7d23d-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="7d23d-120">Sql_Injection</span></span>
- <span data-ttu-id="7d23d-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="7d23d-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="7d23d-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="7d23d-122">Access_Anomaly</span></span>
- <span data-ttu-id="7d23d-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="7d23d-123">None</span></span>

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

### <span data-ttu-id="7d23d-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="7d23d-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="7d23d-125">A házirend által küldött e-mail-címek pontosvesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d23d-125">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="7d23d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d23d-126">-PassThru</span></span>
<span data-ttu-id="7d23d-127">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="7d23d-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7d23d-128">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="7d23d-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7d23d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d23d-129">-ResourceGroupName</span></span>
<span data-ttu-id="7d23d-130">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="7d23d-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="7d23d-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="7d23d-131">-RetentionInDays</span></span>
<span data-ttu-id="7d23d-132">A naplók adatmegőrzési napjainak száma</span><span class="sxs-lookup"><span data-stu-id="7d23d-132">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="7d23d-133">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="7d23d-133">-ServerName</span></span>
<span data-ttu-id="7d23d-134">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d23d-134">Specifies the name of the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d23d-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7d23d-135">-StorageAccountName</span></span>
<span data-ttu-id="7d23d-136">A használandó tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d23d-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="7d23d-137">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="7d23d-137">Wildcards are not permitted.</span></span> <span data-ttu-id="7d23d-138">Ehhez a paraméterhez nincs szükség.</span><span class="sxs-lookup"><span data-stu-id="7d23d-138">This parameter is not required.</span></span> <span data-ttu-id="7d23d-139">Ha ezt a paramétert nem jeleníti meg, a parancsmag az adatbázis veszélyforrások észlelési házirendjének részeként megadott tárolási fiókot fogja használni.</span><span class="sxs-lookup"><span data-stu-id="7d23d-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="7d23d-140">Ha ez az első alkalom, hogy egy adatbázis-theat-észlelési házirend van definiálva, és ez a paraméter nem jelenik meg, a parancsmag nem fog működni.</span><span class="sxs-lookup"><span data-stu-id="7d23d-140">If this is the first time a database theat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="7d23d-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7d23d-141">-Confirm</span></span>
<span data-ttu-id="7d23d-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7d23d-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d23d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d23d-143">-WhatIf</span></span>
<span data-ttu-id="7d23d-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7d23d-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d23d-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7d23d-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d23d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d23d-146">CommonParameters</span></span>
<span data-ttu-id="7d23d-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7d23d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d23d-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d23d-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d23d-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d23d-149">INPUTS</span></span>

###  
<span data-ttu-id="7d23d-150">Ebben a parancsmagban nem lehet beírni a bemenetet.</span><span class="sxs-lookup"><span data-stu-id="7d23d-150">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="7d23d-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d23d-151">OUTPUTS</span></span>

### <span data-ttu-id="7d23d-152">Microsoft. Azure. Command. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="7d23d-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>
<span data-ttu-id="7d23d-153">Ez a parancsmag egy **ServerThreatDetectionPolicyModel** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="7d23d-153">This cmdlet returns a **ServerThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="7d23d-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7d23d-154">NOTES</span></span>

## <span data-ttu-id="7d23d-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d23d-155">RELATED LINKS</span></span>

[<span data-ttu-id="7d23d-156">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7d23d-156">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="7d23d-157">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7d23d-157">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="7d23d-158">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="7d23d-158">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
