---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 897911a4f13b2453d0e814828000309ad8865ba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498724"
---
# <span data-ttu-id="03404-101">New-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="03404-101">New-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="03404-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="03404-102">SYNOPSIS</span></span>
<span data-ttu-id="03404-103">A parancs létrehoz egy új Azure SQL Server DNS-aliast.</span><span class="sxs-lookup"><span data-stu-id="03404-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03404-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="03404-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03404-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="03404-105">DESCRIPTION</span></span>
<span data-ttu-id="03404-106">Új Azure SQL Server DNS-Alias létrehozása, amely a megadott kiszolgálón van mutatva.</span><span class="sxs-lookup"><span data-stu-id="03404-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="03404-107">Példák</span><span class="sxs-lookup"><span data-stu-id="03404-107">EXAMPLES</span></span>

### <span data-ttu-id="03404-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="03404-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzureRmSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="03404-109">Ez a parancs Azure SQL Server DNS-aliast hoz létre a kiszolgáló kiszolgálónév nevű aliasName.</span><span class="sxs-lookup"><span data-stu-id="03404-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="03404-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="03404-110">PARAMETERS</span></span>

### <span data-ttu-id="03404-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03404-111">-AsJob</span></span>
<span data-ttu-id="03404-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="03404-112">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03404-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03404-113">-DefaultProfile</span></span>
<span data-ttu-id="03404-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03404-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03404-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="03404-115">-Name</span></span>
<span data-ttu-id="03404-116">Az Azure SQL Server DNS-aliasának neve.</span><span class="sxs-lookup"><span data-stu-id="03404-116">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03404-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03404-117">-ResourceGroupName</span></span>
<span data-ttu-id="03404-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="03404-118">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03404-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="03404-119">-ServerName</span></span>
<span data-ttu-id="03404-120">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="03404-120">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03404-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="03404-121">-Confirm</span></span>
<span data-ttu-id="03404-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="03404-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03404-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03404-123">-WhatIf</span></span>
<span data-ttu-id="03404-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="03404-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03404-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="03404-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03404-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03404-126">CommonParameters</span></span>
<span data-ttu-id="03404-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="03404-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03404-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03404-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03404-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="03404-129">INPUTS</span></span>

### <span data-ttu-id="03404-130">System. String</span><span class="sxs-lookup"><span data-stu-id="03404-130">System.String</span></span>

## <span data-ttu-id="03404-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03404-131">OUTPUTS</span></span>

### <span data-ttu-id="03404-132">Microsoft. Azure. Command. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="03404-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="03404-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="03404-133">NOTES</span></span>

## <span data-ttu-id="03404-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03404-134">RELATED LINKS</span></span>
