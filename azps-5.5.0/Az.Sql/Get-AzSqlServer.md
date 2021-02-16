---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
ms.openlocfilehash: 79577b9812f743035d90b2c4fe112dd9f2468fd2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165786"
---
# <span data-ttu-id="60439-101">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="60439-101">Get-AzSqlServer</span></span>

## <span data-ttu-id="60439-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60439-102">SYNOPSIS</span></span>
<span data-ttu-id="60439-103">Az SQL Database-kiszolgálókra vonatkozó információkat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="60439-103">Returns information about SQL Database servers.</span></span>

## <span data-ttu-id="60439-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="60439-104">SYNTAX</span></span>

```
Get-AzSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60439-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="60439-105">DESCRIPTION</span></span>
<span data-ttu-id="60439-106">A **Get-AzSqlServer** parancsmag egy vagy több Azure SQL Database-kiszolgálóról ad információkat.</span><span class="sxs-lookup"><span data-stu-id="60439-106">The **Get-AzSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="60439-107">Adja meg a kiszolgáló nevét, hogy csak az adott kiszolgáló adatait lássa.</span><span class="sxs-lookup"><span data-stu-id="60439-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="60439-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="60439-108">EXAMPLES</span></span>

### <span data-ttu-id="60439-109">1. példa: Az SQL Server összes példányának hozzárendelése erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="60439-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net
```

<span data-ttu-id="60439-110">Ez a parancs információkat kap az Erőforráscsoport01 erőforráscsoporthoz rendelt Összes Azure SQL-adatbázis-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="60439-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="60439-111">2. példa: Információ az Azure SQL-adatbázis kiszolgálóról</span><span class="sxs-lookup"><span data-stu-id="60439-111">Example 2: Get information about an Azure SQL Database server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net
```

<span data-ttu-id="60439-112">Ez a parancs információkat kap a Server01 nevű Azure SQL-adatbázis-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="60439-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="60439-113">3. példa: Az SQL Server összes példányának lekérte az előfizetésben</span><span class="sxs-lookup"><span data-stu-id="60439-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzSqlServer
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net

ResourceGroupName        : resourcegroup02
ServerName               : server03
Location                 : East US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server03.database.windows.net
```

<span data-ttu-id="60439-114">Ez a parancs információkat kap az aktuális előfizetés összes Azure SQL Database-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="60439-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

### <span data-ttu-id="60439-115">4. példa: Az SQL Server összes példányának hozzárendelése egy erőforráscsoporthoz szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="60439-115">Example 4: Get all instances of SQL Server assigned to a resource group using filtering</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "server*"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net
```

<span data-ttu-id="60439-116">Ez a parancs információt kap az Erőforráscsoport01 erőforráscsoporthoz rendelt Összes Azure SQL-adatbázis-kiszolgálóról, amelyek "kiszolgáló" kezdetekkel kezdődnek.</span><span class="sxs-lookup"><span data-stu-id="60439-116">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01 that start with "server".</span></span>

## <span data-ttu-id="60439-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60439-117">PARAMETERS</span></span>

### <span data-ttu-id="60439-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60439-118">-DefaultProfile</span></span>
<span data-ttu-id="60439-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="60439-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60439-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60439-120">-ResourceGroupName</span></span>
<span data-ttu-id="60439-121">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a kiszolgálók hozzá vannak rendelve.</span><span class="sxs-lookup"><span data-stu-id="60439-121">Specifies the name of the resource group to which servers are assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60439-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="60439-122">-ServerName</span></span>
<span data-ttu-id="60439-123">Annak a kiszolgálónak a nevét adja meg, amelybe a parancsmagot beállítja.</span><span class="sxs-lookup"><span data-stu-id="60439-123">Specifies the name of the server that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60439-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60439-124">-Confirm</span></span>
<span data-ttu-id="60439-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="60439-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60439-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60439-126">-WhatIf</span></span>
<span data-ttu-id="60439-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="60439-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60439-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="60439-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60439-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60439-129">CommonParameters</span></span>
<span data-ttu-id="60439-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60439-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60439-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60439-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60439-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="60439-132">INPUTS</span></span>

### <span data-ttu-id="60439-133">System.String</span><span class="sxs-lookup"><span data-stu-id="60439-133">System.String</span></span>

## <span data-ttu-id="60439-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60439-134">OUTPUTS</span></span>

### <span data-ttu-id="60439-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="60439-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="60439-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="60439-136">NOTES</span></span>

## <span data-ttu-id="60439-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60439-137">RELATED LINKS</span></span>

[<span data-ttu-id="60439-138">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="60439-138">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="60439-139">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="60439-139">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="60439-140">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="60439-140">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="60439-141">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="60439-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


