---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: d4a167871e452cb12533e38793fae463ba6f8dc8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846637"
---
# <span data-ttu-id="968ed-101">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="968ed-101">Set-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="968ed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="968ed-102">SYNOPSIS</span></span>
<span data-ttu-id="968ed-103">Adatmaszkolás beállítása egy adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="968ed-103">Sets data masking for a database.</span></span>

## <span data-ttu-id="968ed-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="968ed-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedUsers <String>] [-DataMaskingState <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="968ed-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="968ed-105">DESCRIPTION</span></span>
<span data-ttu-id="968ed-106">A **set-AzSqlDatabaseDataMaskingPolicy** parancsmag az Azure SQL-adatbázisok adatmaszkolási házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="968ed-106">The **Set-AzSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="968ed-107">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paraméterrel keresse meg az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="968ed-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="968ed-108">Beállíthatja, hogy az adatmaszkolási műveletek engedélyezve vagy Letiltva legyenek a *DataMaskingState* paraméterben.</span><span class="sxs-lookup"><span data-stu-id="968ed-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>
<span data-ttu-id="968ed-109">Ha a parancsmag sikerrel jár, és a *PassThru* paramétert használja, a program az adatbázis-azonosítók mellett az aktuális adatmaszkolási házirendet leíró objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="968ed-109">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="968ed-110">Az adatbázis-azonosítók közé tartoznak a következők: a **ResourceGroupName** , a **kiszolgálónév** és a **databasename**.</span><span class="sxs-lookup"><span data-stu-id="968ed-110">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="968ed-111">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="968ed-111">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="968ed-112">Példák</span><span class="sxs-lookup"><span data-stu-id="968ed-112">EXAMPLES</span></span>

### <span data-ttu-id="968ed-113">Példa 1: adatbázis adatmaszkolási házirendjének beállítása</span><span class="sxs-lookup"><span data-stu-id="968ed-113">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="968ed-114">Ez a parancs beállítja a database01 nevű adatbázis adatmaszkolási házirendjét a server01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="968ed-114">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="968ed-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="968ed-115">PARAMETERS</span></span>

### <span data-ttu-id="968ed-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="968ed-116">-DatabaseName</span></span>
<span data-ttu-id="968ed-117">Annak az adatbázisnak a nevét adja meg, amelyben a házirend van beállítva.</span><span class="sxs-lookup"><span data-stu-id="968ed-117">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="968ed-118">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="968ed-118">-DataMaskingState</span></span>
<span data-ttu-id="968ed-119">Megadja, hogy az adatmaszkolási művelet engedélyezve vagy Letiltva van-e.</span><span class="sxs-lookup"><span data-stu-id="968ed-119">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="968ed-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="968ed-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="968ed-121">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="968ed-121">Enabled</span></span>
- <span data-ttu-id="968ed-122">Letiltva: az alapértelmezett érték engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="968ed-122">Disabled The default value is Enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="968ed-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="968ed-123">-DefaultProfile</span></span>
<span data-ttu-id="968ed-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="968ed-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="968ed-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="968ed-125">-PassThru</span></span>
<span data-ttu-id="968ed-126">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="968ed-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="968ed-127">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="968ed-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="968ed-128">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="968ed-128">-PrivilegedUsers</span></span>
<span data-ttu-id="968ed-129">A Kiemelt felhasználói azonosítók pontosvesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="968ed-129">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="968ed-130">Ezek a felhasználók jogosultak a maszkolási adatmaszkolási szolgáltatás megtekintésére.</span><span class="sxs-lookup"><span data-stu-id="968ed-130">These users are allowed to view the masking data.</span></span>

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

### <span data-ttu-id="968ed-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="968ed-131">-ResourceGroupName</span></span>
<span data-ttu-id="968ed-132">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="968ed-132">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="968ed-133">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="968ed-133">-ServerName</span></span>
<span data-ttu-id="968ed-134">Az adatbázist működtető kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="968ed-134">Specifies the name of the server hosting the database.</span></span>

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

### <span data-ttu-id="968ed-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="968ed-135">-Confirm</span></span>
<span data-ttu-id="968ed-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="968ed-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="968ed-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="968ed-137">-WhatIf</span></span>
<span data-ttu-id="968ed-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="968ed-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="968ed-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="968ed-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="968ed-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="968ed-140">CommonParameters</span></span>
<span data-ttu-id="968ed-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="968ed-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="968ed-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="968ed-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="968ed-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="968ed-143">INPUTS</span></span>

### <span data-ttu-id="968ed-144">System. String</span><span class="sxs-lookup"><span data-stu-id="968ed-144">System.String</span></span>

## <span data-ttu-id="968ed-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="968ed-145">OUTPUTS</span></span>

### <span data-ttu-id="968ed-146">Microsoft. Azure. Command. SQL. DataMasking. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="968ed-146">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="968ed-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="968ed-147">NOTES</span></span>

## <span data-ttu-id="968ed-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="968ed-148">RELATED LINKS</span></span>

[<span data-ttu-id="968ed-149">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="968ed-149">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="968ed-150">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="968ed-150">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="968ed-151">Új – AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="968ed-151">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="968ed-152">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="968ed-152">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="968ed-153">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="968ed-153">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="968ed-154">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="968ed-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


