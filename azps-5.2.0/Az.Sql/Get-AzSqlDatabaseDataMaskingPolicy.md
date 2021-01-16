---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 8fb1b8125a6fd0c42bedc00733f3a128846673e4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368534"
---
# <span data-ttu-id="f9a22-101">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="f9a22-101">Get-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="f9a22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9a22-102">SYNOPSIS</span></span>
<span data-ttu-id="f9a22-103">Beveszi egy adatbázis adatmaszkolási házirendjeit.</span><span class="sxs-lookup"><span data-stu-id="f9a22-103">Gets the data masking policy for a database.</span></span>

## <span data-ttu-id="f9a22-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f9a22-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9a22-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f9a22-105">DESCRIPTION</span></span>
<span data-ttu-id="f9a22-106">A **Get-AzSqlDatabaseDataMaskingPolicy** parancsmag egy Azure SQL-adatbázis adatmaszkolási házirendjéhez jut.</span><span class="sxs-lookup"><span data-stu-id="f9a22-106">The **Get-AzSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="f9a22-107">A parancsmagot a *ResourceGroupName,* *a ServerName* és a *DatabaseName* paraméter használatával azonosíthatja az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="f9a22-107">To use this cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="f9a22-108">Ezt a parancsmagot az Azure SQL Server Stretch Database szolgáltatása is támogatja.</span><span class="sxs-lookup"><span data-stu-id="f9a22-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="f9a22-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f9a22-109">EXAMPLES</span></span>

### <span data-ttu-id="f9a22-110">1. példa: Azure SQL-adatbázis adatmaszkolási házirendének lekérte</span><span class="sxs-lookup"><span data-stu-id="f9a22-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="f9a22-111">Ez a parancs az adatbázis Adatbázis01 adatmaszkolási házirendjeit a kiszolgáló01 ResourceGroup01 erőforráscsoportjának adatbázisából kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f9a22-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="f9a22-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9a22-112">PARAMETERS</span></span>

### <span data-ttu-id="f9a22-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f9a22-113">-DatabaseName</span></span>
<span data-ttu-id="f9a22-114">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9a22-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="f9a22-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9a22-115">-DefaultProfile</span></span>
<span data-ttu-id="f9a22-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f9a22-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9a22-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9a22-117">-ResourceGroupName</span></span>
<span data-ttu-id="f9a22-118">Annak az erőforráscsoportnak a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="f9a22-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="f9a22-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f9a22-119">-ServerName</span></span>
<span data-ttu-id="f9a22-120">Annak a kiszolgálónak a neve, ahol az adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="f9a22-120">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="f9a22-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9a22-121">-Confirm</span></span>
<span data-ttu-id="f9a22-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f9a22-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9a22-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9a22-123">-WhatIf</span></span>
<span data-ttu-id="f9a22-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f9a22-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9a22-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f9a22-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9a22-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9a22-126">CommonParameters</span></span>
<span data-ttu-id="f9a22-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9a22-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9a22-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9a22-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9a22-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f9a22-129">INPUTS</span></span>

### <span data-ttu-id="f9a22-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f9a22-130">System.String</span></span>

## <span data-ttu-id="f9a22-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9a22-131">OUTPUTS</span></span>

### <span data-ttu-id="f9a22-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="f9a22-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="f9a22-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f9a22-133">NOTES</span></span>

## <span data-ttu-id="f9a22-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9a22-134">RELATED LINKS</span></span>

[<span data-ttu-id="f9a22-135">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="f9a22-135">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="f9a22-136">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="f9a22-136">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="f9a22-137">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="f9a22-137">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="f9a22-138">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="f9a22-138">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="f9a22-139">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="f9a22-139">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


