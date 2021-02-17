---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 49b484c17b595a8f676a089f8627b70a1f34c471
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399498"
---
# <span data-ttu-id="d3d08-101">Set-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d3d08-101">Set-AzSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="d3d08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3d08-102">SYNOPSIS</span></span>
<span data-ttu-id="d3d08-103">Veszélyforrás-észlelési házirendet állít be egy kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="d3d08-103">Sets a threat detection policy on a server.</span></span>

## <span data-ttu-id="d3d08-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d3d08-104">SYNTAX</span></span>

```
Set-AzSqlServerThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3d08-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d3d08-105">DESCRIPTION</span></span>
<span data-ttu-id="d3d08-106">A **Set-AzSqlServerThreatDetectionPolicy parancsmag** egy Azure SQL-kiszolgálón veszélyforrás-észlelési házirendet állít be.</span><span class="sxs-lookup"><span data-stu-id="d3d08-106">The **Set-AzSqlServerThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL server.</span></span>
<span data-ttu-id="d3d08-107">Ha engedélyezni szeretné a veszélyforrás-észlelést egy kiszolgálón, a kiszolgálón engedélyezni kell egy naplózási házirendet.</span><span class="sxs-lookup"><span data-stu-id="d3d08-107">In order to enable threat detection on a server an auditing policy must be enabled on that server.</span></span>
<span data-ttu-id="d3d08-108">A parancsmagot a *ResourceGroupName* és a ServerName paraméter megadásával azonosíthatja a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="d3d08-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="d3d08-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d3d08-109">EXAMPLES</span></span>

### <span data-ttu-id="d3d08-110">1. példa: Adatbázis veszélyforrás-észlelési házirendének beállítása</span><span class="sxs-lookup"><span data-stu-id="d3d08-110">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="d3d08-111">Ez a parancs beállítja a veszélyforrás-észlelési házirendet egy Server01 nevű kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="d3d08-111">This command sets the threat detection policy for a server named Server01.</span></span>

## <span data-ttu-id="d3d08-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3d08-112">PARAMETERS</span></span>

### <span data-ttu-id="d3d08-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3d08-113">-DefaultProfile</span></span>
<span data-ttu-id="d3d08-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d3d08-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3d08-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="d3d08-115">-EmailAdmins</span></span>
<span data-ttu-id="d3d08-116">Azt adja meg, hogy a veszélyforrás-észlelési házirend e-mail használatával kapcsolatba lép-e a rendszergazdákval.</span><span class="sxs-lookup"><span data-stu-id="d3d08-116">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="d3d08-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="d3d08-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="d3d08-118">A házirendből kizárandó észlelési típusok tömbje.</span><span class="sxs-lookup"><span data-stu-id="d3d08-118">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="d3d08-119">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="d3d08-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d3d08-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="d3d08-120">Sql_Injection</span></span>
- <span data-ttu-id="d3d08-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="d3d08-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="d3d08-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="d3d08-122">Access_Anomaly</span></span>
- <span data-ttu-id="d3d08-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="d3d08-123">None</span></span>

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

### <span data-ttu-id="d3d08-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="d3d08-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="d3d08-125">Pontosvesszővel elválasztott listát ad meg azokról az e-mail-címekről, amelyekre a házirend riasztásokat küld.</span><span class="sxs-lookup"><span data-stu-id="d3d08-125">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="d3d08-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3d08-126">-PassThru</span></span>
<span data-ttu-id="d3d08-127">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="d3d08-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d3d08-128">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="d3d08-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d3d08-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3d08-129">-ResourceGroupName</span></span>
<span data-ttu-id="d3d08-130">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="d3d08-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="d3d08-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="d3d08-131">-RetentionInDays</span></span>
<span data-ttu-id="d3d08-132">A naplók adatmegőrzési napjainak száma</span><span class="sxs-lookup"><span data-stu-id="d3d08-132">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="d3d08-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d3d08-133">-ServerName</span></span>
<span data-ttu-id="d3d08-134">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d3d08-134">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="d3d08-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d3d08-135">-StorageAccountName</span></span>
<span data-ttu-id="d3d08-136">A használni használt tárfiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d3d08-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="d3d08-137">A helyettesítő karakterek használata nem engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="d3d08-137">Wildcards are not permitted.</span></span> <span data-ttu-id="d3d08-138">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="d3d08-138">This parameter is not required.</span></span> <span data-ttu-id="d3d08-139">Ha ez a paraméter nincs megadva, a parancsmag az adatbázis veszélyforrás-észlelési házirend részeként korábban definiált tárfiókot fogja használni.</span><span class="sxs-lookup"><span data-stu-id="d3d08-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="d3d08-140">Ha első alkalommal határoz meg adatbázis-észlelési házirendet, és ez a paraméter nincs megadva, a parancsmag nem fog működni.</span><span class="sxs-lookup"><span data-stu-id="d3d08-140">If this is the first time a database theat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="d3d08-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3d08-141">-Confirm</span></span>
<span data-ttu-id="d3d08-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d3d08-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3d08-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3d08-143">-WhatIf</span></span>
<span data-ttu-id="d3d08-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d3d08-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3d08-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d3d08-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3d08-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3d08-146">CommonParameters</span></span>
<span data-ttu-id="d3d08-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3d08-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3d08-148">További információt a [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3d08-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3d08-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3d08-149">INPUTS</span></span>

### <span data-ttu-id="d3d08-150">System.String</span><span class="sxs-lookup"><span data-stu-id="d3d08-150">System.String</span></span>

### <span data-ttu-id="d3d08-151">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d3d08-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d3d08-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span><span class="sxs-lookup"><span data-stu-id="d3d08-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="d3d08-153">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d3d08-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d3d08-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3d08-154">OUTPUTS</span></span>

### <span data-ttu-id="d3d08-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d3d08-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="d3d08-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d3d08-156">NOTES</span></span>

## <span data-ttu-id="d3d08-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3d08-157">RELATED LINKS</span></span>

[<span data-ttu-id="d3d08-158">Get-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d3d08-158">Get-AzSqlServerThreatDetectionPolicy</span></span>](./Get-AzSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="d3d08-159">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d3d08-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
