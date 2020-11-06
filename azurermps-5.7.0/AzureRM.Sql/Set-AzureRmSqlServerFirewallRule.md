---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: e0957e7c68a2332cbd50bbc42d703c41bb277b75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492988"
---
# <span data-ttu-id="b0228-101">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b0228-101">Set-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="b0228-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b0228-102">SYNOPSIS</span></span>
<span data-ttu-id="b0228-103">Tűzfal-szabály módosítása az Azure SQL adatbázis-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="b0228-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0228-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b0228-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0228-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b0228-105">DESCRIPTION</span></span>
<span data-ttu-id="b0228-106">A **set-AzureRmSqlServerFirewallRule** parancsmag egy Azure SQL-adatbázis-kiszolgálón módosítja a tűzfalszabályok egyikét.</span><span class="sxs-lookup"><span data-stu-id="b0228-106">The **Set-AzureRmSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="b0228-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b0228-107">EXAMPLES</span></span>

### <span data-ttu-id="b0228-108">Példa 1: tűzfalszabály módosítása</span><span class="sxs-lookup"><span data-stu-id="b0228-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="b0228-109">Ez a parancs módosítja a Server01 nevű kiszolgálón a Rule01 nevű tűzfalszabályok egyikét.</span><span class="sxs-lookup"><span data-stu-id="b0228-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="b0228-110">A parancs módosítja a kezdési és a befejezési IP-címet.</span><span class="sxs-lookup"><span data-stu-id="b0228-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="b0228-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b0228-111">PARAMETERS</span></span>

### <span data-ttu-id="b0228-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0228-112">-DefaultProfile</span></span>
<span data-ttu-id="b0228-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b0228-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0228-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="b0228-114">-EndIpAddress</span></span>
<span data-ttu-id="b0228-115">A szabályhoz tartozó IP-címtartomány utolsó értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b0228-115">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="b0228-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="b0228-116">-FirewallRuleName</span></span>
<span data-ttu-id="b0228-117">Annak a tűzfal-szabálynak a neve, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="b0228-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0228-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0228-118">-ResourceGroupName</span></span>
<span data-ttu-id="b0228-119">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="b0228-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="b0228-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="b0228-120">-ServerName</span></span>
<span data-ttu-id="b0228-121">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b0228-121">Specifies the name of the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0228-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="b0228-122">-StartIpAddress</span></span>
<span data-ttu-id="b0228-123">A tűzfalszabály IP-címtartomány kezdetének értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b0228-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="b0228-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b0228-124">-Confirm</span></span>
<span data-ttu-id="b0228-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b0228-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0228-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0228-126">-WhatIf</span></span>
<span data-ttu-id="b0228-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b0228-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0228-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b0228-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0228-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0228-129">CommonParameters</span></span>
<span data-ttu-id="b0228-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b0228-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0228-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0228-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0228-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0228-132">INPUTS</span></span>

### <span data-ttu-id="b0228-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="b0228-133">None</span></span>
<span data-ttu-id="b0228-134">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="b0228-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b0228-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0228-135">OUTPUTS</span></span>

### <span data-ttu-id="b0228-136">Microsoft. Azure. Command. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="b0228-136">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="b0228-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b0228-137">NOTES</span></span>

## <span data-ttu-id="b0228-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0228-138">RELATED LINKS</span></span>

[<span data-ttu-id="b0228-139">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b0228-139">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="b0228-140">Új – AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b0228-140">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="b0228-141">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b0228-141">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="b0228-142">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="b0228-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


