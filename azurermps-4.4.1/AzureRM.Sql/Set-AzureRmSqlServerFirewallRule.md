---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: c8a3e10fb2f78556112831f4310eca60e296cf48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680744"
---
# <span data-ttu-id="d979b-101">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d979b-101">Set-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="d979b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d979b-102">SYNOPSIS</span></span>
<span data-ttu-id="d979b-103">Tűzfal-szabály módosítása az Azure SQL adatbázis-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="d979b-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d979b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d979b-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d979b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d979b-105">DESCRIPTION</span></span>
<span data-ttu-id="d979b-106">A **set-AzureRmSqlServerFirewallRule** parancsmag egy Azure SQL-adatbázis-kiszolgálón módosítja a tűzfalszabályok egyikét.</span><span class="sxs-lookup"><span data-stu-id="d979b-106">The **Set-AzureRmSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="d979b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d979b-107">EXAMPLES</span></span>

### <span data-ttu-id="d979b-108">Példa 1: tűzfalszabály módosítása</span><span class="sxs-lookup"><span data-stu-id="d979b-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="d979b-109">Ez a parancs módosítja a Server01 nevű kiszolgálón a Rule01 nevű tűzfalszabályok egyikét.</span><span class="sxs-lookup"><span data-stu-id="d979b-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="d979b-110">A parancs módosítja a kezdési és a befejezési IP-címet.</span><span class="sxs-lookup"><span data-stu-id="d979b-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="d979b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d979b-111">PARAMETERS</span></span>

### <span data-ttu-id="d979b-112">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="d979b-112">-EndIpAddress</span></span>
<span data-ttu-id="d979b-113">A szabályhoz tartozó IP-címtartomány utolsó értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d979b-113">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="d979b-114">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="d979b-114">-FirewallRuleName</span></span>
<span data-ttu-id="d979b-115">Annak a tűzfal-szabálynak a neve, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="d979b-115">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d979b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d979b-116">-ResourceGroupName</span></span>
<span data-ttu-id="d979b-117">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="d979b-117">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="d979b-118">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="d979b-118">-ServerName</span></span>
<span data-ttu-id="d979b-119">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d979b-119">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="d979b-120">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="d979b-120">-StartIpAddress</span></span>
<span data-ttu-id="d979b-121">A tűzfalszabály IP-címtartomány kezdetének értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d979b-121">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="d979b-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d979b-122">-Confirm</span></span>
<span data-ttu-id="d979b-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d979b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d979b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d979b-124">-WhatIf</span></span>
<span data-ttu-id="d979b-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d979b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d979b-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d979b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d979b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d979b-127">-DefaultProfile</span></span>
<span data-ttu-id="d979b-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d979b-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d979b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d979b-129">CommonParameters</span></span>
<span data-ttu-id="d979b-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d979b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d979b-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d979b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d979b-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d979b-132">INPUTS</span></span>

## <span data-ttu-id="d979b-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d979b-133">OUTPUTS</span></span>

### <span data-ttu-id="d979b-134">Microsoft. Azure. Command. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="d979b-134">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="d979b-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d979b-135">NOTES</span></span>

## <span data-ttu-id="d979b-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d979b-136">RELATED LINKS</span></span>

[<span data-ttu-id="d979b-137">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d979b-137">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="d979b-138">Új – AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d979b-138">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="d979b-139">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d979b-139">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="d979b-140">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d979b-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


