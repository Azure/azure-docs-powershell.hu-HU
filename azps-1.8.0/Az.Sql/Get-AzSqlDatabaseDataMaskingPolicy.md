---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: b604f0c154b24f8d50e6b341b1f39f8592981793
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669039"
---
# <span data-ttu-id="c77ed-101">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="c77ed-101">Get-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="c77ed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c77ed-102">SYNOPSIS</span></span>
<span data-ttu-id="c77ed-103">Egy adatbázis adatmaszkolási házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c77ed-103">Gets the data masking policy for a database.</span></span>

## <span data-ttu-id="c77ed-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c77ed-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c77ed-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c77ed-105">DESCRIPTION</span></span>
<span data-ttu-id="c77ed-106">A **Get-AzSqlDatabaseDataMaskingPolicy** parancsmag egy Azure SQL-adatbázis adatmaszkolási házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c77ed-106">The **Get-AzSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="c77ed-107">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paraméterrel keresse meg az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="c77ed-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="c77ed-108">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="c77ed-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c77ed-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c77ed-109">EXAMPLES</span></span>

### <span data-ttu-id="c77ed-110">Példa 1: egy Azure SQL-adatbázis adatmaszkolási házirendjének beszerzése</span><span class="sxs-lookup"><span data-stu-id="c77ed-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="c77ed-111">Ez a parancs beolvassa az adatmaszkolási házirendet az adatbázis-Database01 az erőforráscsoport ResourceGroup01 a kiszolgálói Server01.</span><span class="sxs-lookup"><span data-stu-id="c77ed-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="c77ed-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c77ed-112">PARAMETERS</span></span>

### <span data-ttu-id="c77ed-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c77ed-113">-DatabaseName</span></span>
<span data-ttu-id="c77ed-114">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c77ed-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="c77ed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c77ed-115">-DefaultProfile</span></span>
<span data-ttu-id="c77ed-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c77ed-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c77ed-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c77ed-117">-ResourceGroupName</span></span>
<span data-ttu-id="c77ed-118">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="c77ed-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="c77ed-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="c77ed-119">-ServerName</span></span>
<span data-ttu-id="c77ed-120">Annak a kiszolgálónak a nevét adja meg, ahol az adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="c77ed-120">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="c77ed-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c77ed-121">-Confirm</span></span>
<span data-ttu-id="c77ed-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c77ed-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c77ed-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c77ed-123">-WhatIf</span></span>
<span data-ttu-id="c77ed-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c77ed-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c77ed-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c77ed-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c77ed-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c77ed-126">CommonParameters</span></span>
<span data-ttu-id="c77ed-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c77ed-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c77ed-128">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c77ed-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c77ed-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c77ed-129">INPUTS</span></span>

### <span data-ttu-id="c77ed-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c77ed-130">System.String</span></span>

## <span data-ttu-id="c77ed-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c77ed-131">OUTPUTS</span></span>

### <span data-ttu-id="c77ed-132">Microsoft. Azure. Command. SQL. DataMasking. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c77ed-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="c77ed-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c77ed-133">NOTES</span></span>

## <span data-ttu-id="c77ed-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c77ed-134">RELATED LINKS</span></span>

[<span data-ttu-id="c77ed-135">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="c77ed-135">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="c77ed-136">Új – AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="c77ed-136">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="c77ed-137">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="c77ed-137">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="c77ed-138">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="c77ed-138">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="c77ed-139">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="c77ed-139">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


