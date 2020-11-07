---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 13ab762b7f5ed8457bc8975687c3a45315be969b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680472"
---
# <span data-ttu-id="ffd7f-101">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="ffd7f-101">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="ffd7f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ffd7f-102">SYNOPSIS</span></span>
<span data-ttu-id="ffd7f-103">Egy adatbázis adatmaszkolási házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ffd7f-103">Gets the data masking policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffd7f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ffd7f-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ffd7f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ffd7f-105">DESCRIPTION</span></span>
<span data-ttu-id="ffd7f-106">A **Get-AzureRmSqlDatabaseDataMaskingPolicy** parancsmag egy Azure SQL-adatbázis adatmaszkolási házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ffd7f-106">The **Get-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="ffd7f-107">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paraméterrel keresse meg az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="ffd7f-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

<span data-ttu-id="ffd7f-108">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="ffd7f-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ffd7f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ffd7f-109">EXAMPLES</span></span>

### <span data-ttu-id="ffd7f-110">Példa 1: egy Azure SQL-adatbázis adatmaszkolási házirendjének beszerzése</span><span class="sxs-lookup"><span data-stu-id="ffd7f-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="ffd7f-111">Ez a parancs beolvassa az adatmaszkolási házirendet az adatbázis-Database01 az erőforráscsoport ResourceGroup01 a kiszolgálói Server01.</span><span class="sxs-lookup"><span data-stu-id="ffd7f-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="ffd7f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ffd7f-112">PARAMETERS</span></span>

### <span data-ttu-id="ffd7f-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ffd7f-113">-DatabaseName</span></span>
<span data-ttu-id="ffd7f-114">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ffd7f-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="ffd7f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffd7f-115">-ResourceGroupName</span></span>
<span data-ttu-id="ffd7f-116">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="ffd7f-116">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="ffd7f-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="ffd7f-117">-ServerName</span></span>
<span data-ttu-id="ffd7f-118">Annak a kiszolgálónak a nevét adja meg, ahol az adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="ffd7f-118">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="ffd7f-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ffd7f-119">-Confirm</span></span>
<span data-ttu-id="ffd7f-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ffd7f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffd7f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffd7f-121">-WhatIf</span></span>
<span data-ttu-id="ffd7f-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ffd7f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffd7f-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ffd7f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffd7f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffd7f-124">-DefaultProfile</span></span>
<span data-ttu-id="ffd7f-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ffd7f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffd7f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffd7f-126">CommonParameters</span></span>
<span data-ttu-id="ffd7f-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ffd7f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffd7f-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffd7f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffd7f-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffd7f-129">INPUTS</span></span>

## <span data-ttu-id="ffd7f-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffd7f-130">OUTPUTS</span></span>

### <span data-ttu-id="ffd7f-131">Microsoft. Azure. Command. SQL. Security. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="ffd7f-131">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="ffd7f-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ffd7f-132">NOTES</span></span>

## <span data-ttu-id="ffd7f-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ffd7f-133">RELATED LINKS</span></span>

[<span data-ttu-id="ffd7f-134">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ffd7f-134">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ffd7f-135">Új – AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ffd7f-135">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ffd7f-136">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ffd7f-136">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ffd7f-137">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="ffd7f-137">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="ffd7f-138">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ffd7f-138">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)


