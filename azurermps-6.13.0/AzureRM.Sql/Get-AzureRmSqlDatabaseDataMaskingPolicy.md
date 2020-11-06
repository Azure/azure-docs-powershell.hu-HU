---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 6b787e3347c20e011193d0b3968e036d53f62226
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499368"
---
# <span data-ttu-id="d5583-101">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="d5583-101">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="d5583-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5583-102">SYNOPSIS</span></span>
<span data-ttu-id="d5583-103">Egy adatbázis adatmaszkolási házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d5583-103">Gets the data masking policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5583-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5583-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d5583-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d5583-105">DESCRIPTION</span></span>
<span data-ttu-id="d5583-106">A **Get-AzureRmSqlDatabaseDataMaskingPolicy** parancsmag egy Azure SQL-adatbázis adatmaszkolási házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d5583-106">The **Get-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="d5583-107">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paraméterrel keresse meg az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="d5583-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="d5583-108">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="d5583-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="d5583-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d5583-109">EXAMPLES</span></span>

### <span data-ttu-id="d5583-110">Példa 1: egy Azure SQL-adatbázis adatmaszkolási házirendjének beszerzése</span><span class="sxs-lookup"><span data-stu-id="d5583-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="d5583-111">Ez a parancs beolvassa az adatmaszkolási házirendet az adatbázis-Database01 az erőforráscsoport ResourceGroup01 a kiszolgálói Server01.</span><span class="sxs-lookup"><span data-stu-id="d5583-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="d5583-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5583-112">PARAMETERS</span></span>

### <span data-ttu-id="d5583-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d5583-113">-DatabaseName</span></span>
<span data-ttu-id="d5583-114">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5583-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="d5583-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5583-115">-DefaultProfile</span></span>
<span data-ttu-id="d5583-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d5583-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5583-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5583-117">-ResourceGroupName</span></span>
<span data-ttu-id="d5583-118">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="d5583-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="d5583-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="d5583-119">-ServerName</span></span>
<span data-ttu-id="d5583-120">Annak a kiszolgálónak a nevét adja meg, ahol az adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="d5583-120">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="d5583-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d5583-121">-Confirm</span></span>
<span data-ttu-id="d5583-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d5583-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5583-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5583-123">-WhatIf</span></span>
<span data-ttu-id="d5583-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d5583-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5583-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d5583-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5583-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5583-126">CommonParameters</span></span>
<span data-ttu-id="d5583-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5583-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5583-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5583-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5583-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5583-129">INPUTS</span></span>

### <span data-ttu-id="d5583-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d5583-130">System.String</span></span>

## <span data-ttu-id="d5583-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5583-131">OUTPUTS</span></span>

### <span data-ttu-id="d5583-132">Microsoft. Azure. Command. SQL. DataMasking. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d5583-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="d5583-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5583-133">NOTES</span></span>

## <span data-ttu-id="d5583-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5583-134">RELATED LINKS</span></span>

[<span data-ttu-id="d5583-135">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="d5583-135">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="d5583-136">Új – AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="d5583-136">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="d5583-137">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="d5583-137">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="d5583-138">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="d5583-138">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="d5583-139">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="d5583-139">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)


