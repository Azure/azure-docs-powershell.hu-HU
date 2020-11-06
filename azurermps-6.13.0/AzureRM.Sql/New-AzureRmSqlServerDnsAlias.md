---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 3ce18369645705f78722f7505c8dd1e46f2514b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492717"
---
# <span data-ttu-id="9934a-101">New-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="9934a-101">New-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="9934a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9934a-102">SYNOPSIS</span></span>
<span data-ttu-id="9934a-103">A parancs létrehoz egy új Azure SQL Server DNS-aliast.</span><span class="sxs-lookup"><span data-stu-id="9934a-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9934a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9934a-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9934a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9934a-105">DESCRIPTION</span></span>
<span data-ttu-id="9934a-106">Új Azure SQL Server DNS-Alias létrehozása, amely a megadott kiszolgálón van mutatva.</span><span class="sxs-lookup"><span data-stu-id="9934a-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="9934a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9934a-107">EXAMPLES</span></span>

### <span data-ttu-id="9934a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9934a-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzureRmSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="9934a-109">Ez a parancs Azure SQL Server DNS-aliast hoz létre a kiszolgáló kiszolgálónév nevű aliasName.</span><span class="sxs-lookup"><span data-stu-id="9934a-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="9934a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9934a-110">PARAMETERS</span></span>

### <span data-ttu-id="9934a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9934a-111">-AsJob</span></span>
<span data-ttu-id="9934a-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9934a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9934a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9934a-113">-DefaultProfile</span></span>
<span data-ttu-id="9934a-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9934a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9934a-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9934a-115">-Name</span></span>
<span data-ttu-id="9934a-116">Az Azure SQL Server DNS-aliasának neve.</span><span class="sxs-lookup"><span data-stu-id="9934a-116">The Azure Sql Server Dns Alias name.</span></span>

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

### <span data-ttu-id="9934a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9934a-117">-ResourceGroupName</span></span>
<span data-ttu-id="9934a-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9934a-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="9934a-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="9934a-119">-ServerName</span></span>
<span data-ttu-id="9934a-120">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="9934a-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="9934a-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9934a-121">-Confirm</span></span>
<span data-ttu-id="9934a-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9934a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9934a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9934a-123">-WhatIf</span></span>
<span data-ttu-id="9934a-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9934a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9934a-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9934a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9934a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9934a-126">CommonParameters</span></span>
<span data-ttu-id="9934a-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9934a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9934a-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9934a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9934a-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9934a-129">INPUTS</span></span>

### <span data-ttu-id="9934a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9934a-130">System.String</span></span>

## <span data-ttu-id="9934a-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9934a-131">OUTPUTS</span></span>

### <span data-ttu-id="9934a-132">Microsoft. Azure. Command. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="9934a-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="9934a-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9934a-133">NOTES</span></span>

## <span data-ttu-id="9934a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9934a-134">RELATED LINKS</span></span>
