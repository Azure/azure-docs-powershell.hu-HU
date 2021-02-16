---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: d4a167871e452cb12533e38793fae463ba6f8dc8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143995"
---
# <span data-ttu-id="cb269-101">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="cb269-101">Set-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="cb269-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb269-102">SYNOPSIS</span></span>
<span data-ttu-id="cb269-103">Beállítja egy adatbázis adatmaszkolását.</span><span class="sxs-lookup"><span data-stu-id="cb269-103">Sets data masking for a database.</span></span>

## <span data-ttu-id="cb269-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cb269-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedUsers <String>] [-DataMaskingState <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb269-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cb269-105">DESCRIPTION</span></span>
<span data-ttu-id="cb269-106">A **Set-AzSqlDatabaseDataMaskingPolicy** parancsmag beállítja egy Azure SQL-adatbázis adatmaszkolási házirendjeit.</span><span class="sxs-lookup"><span data-stu-id="cb269-106">The **Set-AzSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="cb269-107">A parancsmagot a *ResourceGroupName,* *a ServerName* és a *DatabaseName* paraméter használatával azonosíthatja az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="cb269-107">To use this cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="cb269-108">A *DataMaskingState* paraméterrel megadhatja, hogy az adatmaszkolási műveletek engedélyezettek vagy le vannak-e tiltva.</span><span class="sxs-lookup"><span data-stu-id="cb269-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>
<span data-ttu-id="cb269-109">Ha a parancsmag sikeres, és *a PassThru* paramétert használja, az adatbázis-azonosítók mellett az aktuális adatmaszkolási házirendet leíró objektumot is visszaad.</span><span class="sxs-lookup"><span data-stu-id="cb269-109">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="cb269-110">Az adatbázis-azonosítók közé tartozik többek között a **ResourceGroupName, a** **ServerName** és a **DatabaseName.**</span><span class="sxs-lookup"><span data-stu-id="cb269-110">Database identifiers include, but are not limited to, **ResourceGroupName**, **ServerName**, and **DatabaseName**.</span></span>
<span data-ttu-id="cb269-111">Ezt a parancsmagot az Azure SQL Server Stretch Database szolgáltatása is támogatja.</span><span class="sxs-lookup"><span data-stu-id="cb269-111">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="cb269-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cb269-112">EXAMPLES</span></span>

### <span data-ttu-id="cb269-113">1. példa: Adatbázis adatmaszkolási házirendének beállítása</span><span class="sxs-lookup"><span data-stu-id="cb269-113">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="cb269-114">Ez a parancs beállítja egy adatbázis01 nevű adatbázis adatmaszkolási házirendét a kiszolgáló01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="cb269-114">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="cb269-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb269-115">PARAMETERS</span></span>

### <span data-ttu-id="cb269-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cb269-116">-DatabaseName</span></span>
<span data-ttu-id="cb269-117">Annak az adatbázisnak a nevét adja meg, amelyben a házirend be van állítva.</span><span class="sxs-lookup"><span data-stu-id="cb269-117">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="cb269-118">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="cb269-118">-DataMaskingState</span></span>
<span data-ttu-id="cb269-119">Azt adja meg, hogy engedélyezve vagy letiltva van-e az adatmaszkolási művelet.</span><span class="sxs-lookup"><span data-stu-id="cb269-119">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="cb269-120">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="cb269-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cb269-121">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="cb269-121">Enabled</span></span>
- <span data-ttu-id="cb269-122">Letiltva: Az alapértelmezett érték Engedélyezve.</span><span class="sxs-lookup"><span data-stu-id="cb269-122">Disabled The default value is Enabled.</span></span>

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

### <span data-ttu-id="cb269-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb269-123">-DefaultProfile</span></span>
<span data-ttu-id="cb269-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cb269-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb269-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb269-125">-PassThru</span></span>
<span data-ttu-id="cb269-126">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="cb269-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cb269-127">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="cb269-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cb269-128">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="cb269-128">-PrivilegedUsers</span></span>
<span data-ttu-id="cb269-129">A jogosultsággal rendelkező felhasználói azonosítók pontosvesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb269-129">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="cb269-130">Ezek a felhasználók megtekinthetik a maszkolási adatokat.</span><span class="sxs-lookup"><span data-stu-id="cb269-130">These users are allowed to view the masking data.</span></span>

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

### <span data-ttu-id="cb269-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb269-131">-ResourceGroupName</span></span>
<span data-ttu-id="cb269-132">Annak az erőforráscsoportnak a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="cb269-132">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="cb269-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cb269-133">-ServerName</span></span>
<span data-ttu-id="cb269-134">Az adatbázist üzemeltető kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="cb269-134">Specifies the name of the server hosting the database.</span></span>

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

### <span data-ttu-id="cb269-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb269-135">-Confirm</span></span>
<span data-ttu-id="cb269-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cb269-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb269-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb269-137">-WhatIf</span></span>
<span data-ttu-id="cb269-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cb269-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb269-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cb269-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb269-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb269-140">CommonParameters</span></span>
<span data-ttu-id="cb269-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb269-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb269-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb269-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb269-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb269-143">INPUTS</span></span>

### <span data-ttu-id="cb269-144">System.String</span><span class="sxs-lookup"><span data-stu-id="cb269-144">System.String</span></span>

## <span data-ttu-id="cb269-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb269-145">OUTPUTS</span></span>

### <span data-ttu-id="cb269-146">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="cb269-146">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="cb269-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cb269-147">NOTES</span></span>

## <span data-ttu-id="cb269-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb269-148">RELATED LINKS</span></span>

[<span data-ttu-id="cb269-149">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="cb269-149">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="cb269-150">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="cb269-150">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="cb269-151">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="cb269-151">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="cb269-152">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="cb269-152">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="cb269-153">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="cb269-153">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="cb269-154">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="cb269-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


