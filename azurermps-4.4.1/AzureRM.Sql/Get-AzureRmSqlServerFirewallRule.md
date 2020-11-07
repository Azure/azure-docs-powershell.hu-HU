---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 27715ee03871c08c53380861e2cd54d843b2ba51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679314"
---
# <span data-ttu-id="385db-101">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="385db-101">Get-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="385db-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="385db-102">SYNOPSIS</span></span>
<span data-ttu-id="385db-103">Tűzfal-szabályokat kap egy SQL-adatbázis-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="385db-103">Gets firewall rules for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="385db-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="385db-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="385db-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="385db-105">DESCRIPTION</span></span>
<span data-ttu-id="385db-106">A **Get-AzureRmSqlServerFirewallRule** parancsmag tűzfal-szabályokat kap az Azure SQL-adatbázis-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="385db-106">The **Get-AzureRmSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="385db-107">Ha megadhatja a tűzfalszabály nevét, ez a parancsmag információt kap az adott tűzfalszabály-szabályról.</span><span class="sxs-lookup"><span data-stu-id="385db-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="385db-108">Példák</span><span class="sxs-lookup"><span data-stu-id="385db-108">EXAMPLES</span></span>

### <span data-ttu-id="385db-109">Példa 1: a kiszolgáló összes szabályának lekérése</span><span class="sxs-lookup"><span data-stu-id="385db-109">Example 1: Get all rules for a server</span></span>
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

<span data-ttu-id="385db-110">Ez a parancs beolvassa a Server01 nevű kiszolgáló összes tűzfal-szabályát.</span><span class="sxs-lookup"><span data-stu-id="385db-110">This command gets all the firewall rules for the server named Server01.</span></span>

## <span data-ttu-id="385db-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="385db-111">PARAMETERS</span></span>

### <span data-ttu-id="385db-112">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="385db-112">-FirewallRuleName</span></span>
<span data-ttu-id="385db-113">A tűzfalszabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="385db-113">Specifies the name of the firewall rule.</span></span>

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

### <span data-ttu-id="385db-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="385db-114">-ResourceGroupName</span></span>
<span data-ttu-id="385db-115">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az SQL-kiszolgáló van rendelve.</span><span class="sxs-lookup"><span data-stu-id="385db-115">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="385db-116">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="385db-116">-ServerName</span></span>
<span data-ttu-id="385db-117">Az SQL-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="385db-117">Specifies the name of the SQL Server.</span></span>

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

### <span data-ttu-id="385db-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="385db-118">-Confirm</span></span>
<span data-ttu-id="385db-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="385db-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="385db-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="385db-120">-WhatIf</span></span>
<span data-ttu-id="385db-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="385db-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="385db-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="385db-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="385db-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="385db-123">-DefaultProfile</span></span>
<span data-ttu-id="385db-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="385db-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="385db-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="385db-125">CommonParameters</span></span>
<span data-ttu-id="385db-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="385db-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="385db-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="385db-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="385db-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="385db-128">INPUTS</span></span>

## <span data-ttu-id="385db-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="385db-129">OUTPUTS</span></span>

### <span data-ttu-id="385db-130">Microsoft. Azure. Command. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="385db-130">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="385db-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="385db-131">NOTES</span></span>

## <span data-ttu-id="385db-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="385db-132">RELATED LINKS</span></span>

[<span data-ttu-id="385db-133">Új – AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="385db-133">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="385db-134">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="385db-134">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="385db-135">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="385db-135">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="385db-136">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="385db-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


