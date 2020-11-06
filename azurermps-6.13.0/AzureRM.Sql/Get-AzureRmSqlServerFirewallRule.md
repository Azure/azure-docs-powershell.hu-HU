---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 5e32e136d293c7b5eb8017592cf1ac4e01c60b01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495607"
---
# <span data-ttu-id="1404a-101">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1404a-101">Get-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="1404a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1404a-102">SYNOPSIS</span></span>
<span data-ttu-id="1404a-103">Tűzfal-szabályokat kap egy SQL-adatbázis-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="1404a-103">Gets firewall rules for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1404a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1404a-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1404a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1404a-105">DESCRIPTION</span></span>
<span data-ttu-id="1404a-106">A **Get-AzureRmSqlServerFirewallRule** parancsmag tűzfal-szabályokat kap az Azure SQL-adatbázis-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="1404a-106">The **Get-AzureRmSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="1404a-107">Ha megadhatja a tűzfalszabály nevét, ez a parancsmag információt kap az adott tűzfalszabály-szabályról.</span><span class="sxs-lookup"><span data-stu-id="1404a-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="1404a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="1404a-108">EXAMPLES</span></span>

### <span data-ttu-id="1404a-109">Példa 1: a kiszolgáló összes szabályának lekérése</span><span class="sxs-lookup"><span data-stu-id="1404a-109">Example 1: Get all rules for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : AllowAllWindowsAzureIps

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule01
```

<span data-ttu-id="1404a-110">Ez a parancs beolvassa a Server01 nevű kiszolgáló összes tűzfal-szabályát.</span><span class="sxs-lookup"><span data-stu-id="1404a-110">This command gets all the firewall rules for the server named Server01.</span></span>

## <span data-ttu-id="1404a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1404a-111">PARAMETERS</span></span>

### <span data-ttu-id="1404a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1404a-112">-DefaultProfile</span></span>
<span data-ttu-id="1404a-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1404a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1404a-114">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="1404a-114">-FirewallRuleName</span></span>
<span data-ttu-id="1404a-115">A tűzfalszabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1404a-115">Specifies the name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1404a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1404a-116">-ResourceGroupName</span></span>
<span data-ttu-id="1404a-117">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az SQL-kiszolgáló van rendelve.</span><span class="sxs-lookup"><span data-stu-id="1404a-117">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="1404a-118">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="1404a-118">-ServerName</span></span>
<span data-ttu-id="1404a-119">Az SQL-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1404a-119">Specifies the name of the SQL Server.</span></span>

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

### <span data-ttu-id="1404a-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1404a-120">-Confirm</span></span>
<span data-ttu-id="1404a-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1404a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1404a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1404a-122">-WhatIf</span></span>
<span data-ttu-id="1404a-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1404a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1404a-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1404a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1404a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1404a-125">CommonParameters</span></span>
<span data-ttu-id="1404a-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1404a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1404a-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1404a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1404a-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1404a-128">INPUTS</span></span>

### <span data-ttu-id="1404a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1404a-129">System.String</span></span>

## <span data-ttu-id="1404a-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1404a-130">OUTPUTS</span></span>

### <span data-ttu-id="1404a-131">Microsoft. Azure. Command. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="1404a-131">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="1404a-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1404a-132">NOTES</span></span>

## <span data-ttu-id="1404a-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1404a-133">RELATED LINKS</span></span>

[<span data-ttu-id="1404a-134">Új – AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1404a-134">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="1404a-135">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1404a-135">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="1404a-136">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1404a-136">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="1404a-137">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="1404a-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


