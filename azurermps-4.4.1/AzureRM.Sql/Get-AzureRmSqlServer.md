---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
ms.openlocfilehash: f2d687ce10edf56fc424c03873c733971f70e546
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501591"
---
# <span data-ttu-id="5cab8-101">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="5cab8-101">Get-AzureRmSqlServer</span></span>

## <span data-ttu-id="5cab8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5cab8-102">SYNOPSIS</span></span>
<span data-ttu-id="5cab8-103">SQL-adatbázis-kiszolgálókról ad információt.</span><span class="sxs-lookup"><span data-stu-id="5cab8-103">Returns information about SQL Database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cab8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5cab8-104">SYNTAX</span></span>

```
Get-AzureRmSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cab8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5cab8-105">DESCRIPTION</span></span>
<span data-ttu-id="5cab8-106">A **Get-AzureRmSqlServer** parancsmag információt ad egy vagy több Azure SQL-adatbázis-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="5cab8-106">The **Get-AzureRmSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="5cab8-107">Adja meg a kiszolgáló nevét, hogy csak az adott kiszolgáló adatait lássa.</span><span class="sxs-lookup"><span data-stu-id="5cab8-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="5cab8-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5cab8-108">EXAMPLES</span></span>

### <span data-ttu-id="5cab8-109">Példa 1: az összes SQL Server-példány beolvasása egy erőforráscsoport számára</span><span class="sxs-lookup"><span data-stu-id="5cab8-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLoginSqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     : 

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="5cab8-110">Ez a parancs információkat kap az erőforráscsoport ResourceGroup01 hozzárendelt összes Azure SQL-adatbázis-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="5cab8-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="5cab8-111">2. példa: információk beszerzése Azure SQL-adatbázis-kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="5cab8-111">Example 2: Get information about an Azure SQL Database server</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="5cab8-112">Ez a parancs a Server01 nevű Azure SQL adatbázis-kiszolgálóról kap információkat.</span><span class="sxs-lookup"><span data-stu-id="5cab8-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="5cab8-113">Példa 3: az SQL Server összes példányának beszerzése az előfizetésbe</span><span class="sxs-lookup"><span data-stu-id="5cab8-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmSqlServer
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     : 

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     : 

ResourceGroupName        : resourcegroup02
ServerName               : server03
Location                 : East US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="5cab8-114">Ez a parancs információt kap az összes Azure SQL adatbázis-kiszolgálóról az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="5cab8-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

## <span data-ttu-id="5cab8-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5cab8-115">PARAMETERS</span></span>

### <span data-ttu-id="5cab8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cab8-116">-ResourceGroupName</span></span>
<span data-ttu-id="5cab8-117">Annak az erőforráscsoportnak a neve, amelybe a kiszolgálók vannak rendelve.</span><span class="sxs-lookup"><span data-stu-id="5cab8-117">Specifies the name of the resource group to which servers are assigned.</span></span>

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

### <span data-ttu-id="5cab8-118">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="5cab8-118">-ServerName</span></span>
<span data-ttu-id="5cab8-119">Itt adhatja meg annak a kiszolgálónak a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="5cab8-119">Specifies the name of the server that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5cab8-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5cab8-120">-Confirm</span></span>
<span data-ttu-id="5cab8-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5cab8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cab8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cab8-122">-WhatIf</span></span>
<span data-ttu-id="5cab8-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5cab8-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cab8-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5cab8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cab8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cab8-125">-DefaultProfile</span></span>
<span data-ttu-id="5cab8-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5cab8-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cab8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cab8-127">CommonParameters</span></span>
<span data-ttu-id="5cab8-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5cab8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cab8-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cab8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cab8-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5cab8-130">INPUTS</span></span>

## <span data-ttu-id="5cab8-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5cab8-131">OUTPUTS</span></span>

### <span data-ttu-id="5cab8-132">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="5cab8-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="5cab8-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5cab8-133">NOTES</span></span>

## <span data-ttu-id="5cab8-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5cab8-134">RELATED LINKS</span></span>

[<span data-ttu-id="5cab8-135">Új – AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="5cab8-135">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="5cab8-136">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="5cab8-136">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="5cab8-137">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="5cab8-137">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="5cab8-138">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="5cab8-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


