---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
ms.openlocfilehash: 66f8c3acc178a922868177200e6d4f1f8f50931f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847389"
---
# <span data-ttu-id="2d87d-101">New-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="2d87d-101">New-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="2d87d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2d87d-102">SYNOPSIS</span></span>
<span data-ttu-id="2d87d-103">A parancs létrehoz egy új Azure SQL Server DNS-aliast.</span><span class="sxs-lookup"><span data-stu-id="2d87d-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="2d87d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2d87d-104">SYNTAX</span></span>

```
New-AzSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d87d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2d87d-105">DESCRIPTION</span></span>
<span data-ttu-id="2d87d-106">Új Azure SQL Server DNS-Alias létrehozása, amely a megadott kiszolgálón van mutatva.</span><span class="sxs-lookup"><span data-stu-id="2d87d-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="2d87d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2d87d-107">EXAMPLES</span></span>

### <span data-ttu-id="2d87d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2d87d-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="2d87d-109">Ez a parancs Azure SQL Server DNS-aliast hoz létre a kiszolgáló kiszolgálónév nevű aliasName.</span><span class="sxs-lookup"><span data-stu-id="2d87d-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="2d87d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2d87d-110">PARAMETERS</span></span>

### <span data-ttu-id="2d87d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d87d-111">-AsJob</span></span>
<span data-ttu-id="2d87d-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2d87d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d87d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d87d-113">-DefaultProfile</span></span>
<span data-ttu-id="2d87d-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2d87d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d87d-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2d87d-115">-Name</span></span>
<span data-ttu-id="2d87d-116">Az Azure SQL Server DNS-aliasának neve.</span><span class="sxs-lookup"><span data-stu-id="2d87d-116">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d87d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d87d-117">-ResourceGroupName</span></span>
<span data-ttu-id="2d87d-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2d87d-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="2d87d-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="2d87d-119">-ServerName</span></span>
<span data-ttu-id="2d87d-120">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="2d87d-120">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d87d-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2d87d-121">-Confirm</span></span>
<span data-ttu-id="2d87d-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2d87d-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d87d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d87d-123">-WhatIf</span></span>
<span data-ttu-id="2d87d-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2d87d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d87d-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2d87d-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d87d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d87d-126">CommonParameters</span></span>
<span data-ttu-id="2d87d-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2d87d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d87d-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2d87d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d87d-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d87d-129">INPUTS</span></span>

### <span data-ttu-id="2d87d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2d87d-130">System.String</span></span>

## <span data-ttu-id="2d87d-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d87d-131">OUTPUTS</span></span>

### <span data-ttu-id="2d87d-132">Microsoft. Azure. Command. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="2d87d-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="2d87d-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2d87d-133">NOTES</span></span>

## <span data-ttu-id="2d87d-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d87d-134">RELATED LINKS</span></span>