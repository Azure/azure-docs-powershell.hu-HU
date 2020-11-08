---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
ms.openlocfilehash: 79577b9812f743035d90b2c4fe112dd9f2468fd2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195149"
---
# <span data-ttu-id="a1797-101">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="a1797-101">Get-AzSqlServer</span></span>

## <span data-ttu-id="a1797-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a1797-102">SYNOPSIS</span></span>
<span data-ttu-id="a1797-103">SQL-adatbázis-kiszolgálókról ad információt.</span><span class="sxs-lookup"><span data-stu-id="a1797-103">Returns information about SQL Database servers.</span></span>

## <span data-ttu-id="a1797-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a1797-104">SYNTAX</span></span>

```
Get-AzSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1797-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a1797-105">DESCRIPTION</span></span>
<span data-ttu-id="a1797-106">A **Get-AzSqlServer** parancsmag információt ad egy vagy több Azure SQL-adatbázis-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="a1797-106">The **Get-AzSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="a1797-107">Adja meg a kiszolgáló nevét, hogy csak az adott kiszolgáló adatait lássa.</span><span class="sxs-lookup"><span data-stu-id="a1797-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="a1797-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a1797-108">EXAMPLES</span></span>

### <span data-ttu-id="a1797-109">Példa 1: az összes SQL Server-példány beolvasása egy erőforráscsoport számára</span><span class="sxs-lookup"><span data-stu-id="a1797-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
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

<span data-ttu-id="a1797-110">Ez a parancs információkat kap az erőforráscsoport ResourceGroup01 hozzárendelt összes Azure SQL-adatbázis-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="a1797-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="a1797-111">2. példa: információk beszerzése Azure SQL-adatbázis-kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="a1797-111">Example 2: Get information about an Azure SQL Database server</span></span>
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

<span data-ttu-id="a1797-112">Ez a parancs a Server01 nevű Azure SQL adatbázis-kiszolgálóról kap információkat.</span><span class="sxs-lookup"><span data-stu-id="a1797-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="a1797-113">Példa 3: az SQL Server összes példányának beszerzése az előfizetésbe</span><span class="sxs-lookup"><span data-stu-id="a1797-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
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

<span data-ttu-id="a1797-114">Ez a parancs információt kap az összes Azure SQL adatbázis-kiszolgálóról az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="a1797-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

### <span data-ttu-id="a1797-115">Példa 4: az összes SQL Server-példány beolvasása egy erőforráscsoport használatával szűréssel</span><span class="sxs-lookup"><span data-stu-id="a1797-115">Example 4: Get all instances of SQL Server assigned to a resource group using filtering</span></span>
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

<span data-ttu-id="a1797-116">Ez a parancs információt kap a "kiszolgálóval" kezdődő erőforráscsoport-ResourceGroup01 társított összes Azure SQL-adatbázis-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="a1797-116">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01 that start with "server".</span></span>

## <span data-ttu-id="a1797-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a1797-117">PARAMETERS</span></span>

### <span data-ttu-id="a1797-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1797-118">-DefaultProfile</span></span>
<span data-ttu-id="a1797-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a1797-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1797-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1797-120">-ResourceGroupName</span></span>
<span data-ttu-id="a1797-121">Annak az erőforráscsoportnak a neve, amelybe a kiszolgálók vannak rendelve.</span><span class="sxs-lookup"><span data-stu-id="a1797-121">Specifies the name of the resource group to which servers are assigned.</span></span>

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

### <span data-ttu-id="a1797-122">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="a1797-122">-ServerName</span></span>
<span data-ttu-id="a1797-123">Itt adhatja meg annak a kiszolgálónak a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="a1797-123">Specifies the name of the server that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a1797-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a1797-124">-Confirm</span></span>
<span data-ttu-id="a1797-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a1797-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1797-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1797-126">-WhatIf</span></span>
<span data-ttu-id="a1797-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a1797-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1797-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a1797-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1797-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1797-129">CommonParameters</span></span>
<span data-ttu-id="a1797-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a1797-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1797-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a1797-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1797-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1797-132">INPUTS</span></span>

### <span data-ttu-id="a1797-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a1797-133">System.String</span></span>

## <span data-ttu-id="a1797-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1797-134">OUTPUTS</span></span>

### <span data-ttu-id="a1797-135">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="a1797-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="a1797-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a1797-136">NOTES</span></span>

## <span data-ttu-id="a1797-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1797-137">RELATED LINKS</span></span>

[<span data-ttu-id="a1797-138">Új – AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="a1797-138">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="a1797-139">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="a1797-139">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="a1797-140">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="a1797-140">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="a1797-141">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="a1797-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


