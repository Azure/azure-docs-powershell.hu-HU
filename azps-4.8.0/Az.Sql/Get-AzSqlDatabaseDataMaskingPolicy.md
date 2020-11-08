---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 8fb1b8125a6fd0c42bedc00733f3a128846673e4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017574"
---
# <span data-ttu-id="e0b52-101">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="e0b52-101">Get-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="e0b52-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0b52-102">SYNOPSIS</span></span>
<span data-ttu-id="e0b52-103">Egy adatbázis adatmaszkolási házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e0b52-103">Gets the data masking policy for a database.</span></span>

## <span data-ttu-id="e0b52-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0b52-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0b52-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0b52-105">DESCRIPTION</span></span>
<span data-ttu-id="e0b52-106">A **Get-AzSqlDatabaseDataMaskingPolicy** parancsmag egy Azure SQL-adatbázis adatmaszkolási házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e0b52-106">The **Get-AzSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="e0b52-107">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paraméterrel keresse meg az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="e0b52-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="e0b52-108">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="e0b52-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="e0b52-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e0b52-109">EXAMPLES</span></span>

### <span data-ttu-id="e0b52-110">Példa 1: egy Azure SQL-adatbázis adatmaszkolási házirendjének beszerzése</span><span class="sxs-lookup"><span data-stu-id="e0b52-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="e0b52-111">Ez a parancs beolvassa az adatmaszkolási házirendet az adatbázis-Database01 az erőforráscsoport ResourceGroup01 a kiszolgálói Server01.</span><span class="sxs-lookup"><span data-stu-id="e0b52-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="e0b52-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0b52-112">PARAMETERS</span></span>

### <span data-ttu-id="e0b52-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e0b52-113">-DatabaseName</span></span>
<span data-ttu-id="e0b52-114">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0b52-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="e0b52-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0b52-115">-DefaultProfile</span></span>
<span data-ttu-id="e0b52-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e0b52-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0b52-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0b52-117">-ResourceGroupName</span></span>
<span data-ttu-id="e0b52-118">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="e0b52-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="e0b52-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="e0b52-119">-ServerName</span></span>
<span data-ttu-id="e0b52-120">Annak a kiszolgálónak a nevét adja meg, ahol az adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="e0b52-120">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="e0b52-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e0b52-121">-Confirm</span></span>
<span data-ttu-id="e0b52-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e0b52-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0b52-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0b52-123">-WhatIf</span></span>
<span data-ttu-id="e0b52-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e0b52-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0b52-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e0b52-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0b52-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0b52-126">CommonParameters</span></span>
<span data-ttu-id="e0b52-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0b52-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0b52-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e0b52-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0b52-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0b52-129">INPUTS</span></span>

### <span data-ttu-id="e0b52-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e0b52-130">System.String</span></span>

## <span data-ttu-id="e0b52-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0b52-131">OUTPUTS</span></span>

### <span data-ttu-id="e0b52-132">Microsoft. Azure. Command. SQL. DataMasking. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="e0b52-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="e0b52-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0b52-133">NOTES</span></span>

## <span data-ttu-id="e0b52-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0b52-134">RELATED LINKS</span></span>

[<span data-ttu-id="e0b52-135">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="e0b52-135">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="e0b52-136">Új – AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="e0b52-136">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="e0b52-137">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="e0b52-137">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="e0b52-138">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="e0b52-138">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="e0b52-139">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="e0b52-139">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


