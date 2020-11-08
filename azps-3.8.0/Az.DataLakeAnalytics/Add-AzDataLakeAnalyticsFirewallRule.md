---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/add-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: d9e6dd2e3fedff0d97919e04ca4f8b61536e2075
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94015043"
---
# <span data-ttu-id="be058-101">Add-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="be058-101">Add-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="be058-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="be058-102">SYNOPSIS</span></span>
<span data-ttu-id="be058-103">Tűzfal-szabályt ad hozzá az adattó-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="be058-103">Adds a firewall rule to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="be058-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="be058-104">SYNTAX</span></span>

```
Add-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be058-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="be058-105">DESCRIPTION</span></span>
<span data-ttu-id="be058-106">Az **Add-AzDataLakeAnalyticsFirewallRule** parancsmag tűzfal-szabályt ad az Azure Data Lake-tó Analytics-fiókjához.</span><span class="sxs-lookup"><span data-stu-id="be058-106">The **Add-AzDataLakeAnalyticsFirewallRule** cmdlet adds a firewall rule to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="be058-107">Példák</span><span class="sxs-lookup"><span data-stu-id="be058-107">EXAMPLES</span></span>

### <span data-ttu-id="be058-108">1. példa: tűzfalszabály hozzáadása</span><span class="sxs-lookup"><span data-stu-id="be058-108">Example 1: Add a firewall rule</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="be058-109">Ez a parancs hozzáadja a "My Firewall Rule" nevű tűzfal-szabályt a "ContosoAdlAcct" fiókból az IP-tartománnyal: 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="be058-109">This command adds the firewall rule named "my firewall rule" from account "ContosoAdlAcct" with the IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="be058-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="be058-110">PARAMETERS</span></span>

### <span data-ttu-id="be058-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="be058-111">-Account</span></span>
<span data-ttu-id="be058-112">Az Data Lake Analytics-fiók a tűzfalszabály hozzáadásához</span><span class="sxs-lookup"><span data-stu-id="be058-112">The Data Lake Analytics account to add the firewall rule to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be058-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be058-113">-DefaultProfile</span></span>
<span data-ttu-id="be058-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="be058-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be058-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="be058-115">-EndIpAddress</span></span>
<span data-ttu-id="be058-116">A tűzfalszabály érvényes IP-hatókörének a vége</span><span class="sxs-lookup"><span data-stu-id="be058-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be058-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="be058-117">-Name</span></span>
<span data-ttu-id="be058-118">A tűzfalszabály neve.</span><span class="sxs-lookup"><span data-stu-id="be058-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="be058-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be058-119">-ResourceGroupName</span></span>
<span data-ttu-id="be058-120">Annak az erőforráscsoport-csoportnak a neve, amelybe be szeretné olvasni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="be058-120">Name of resource group under which want to retrieve the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be058-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="be058-121">-StartIpAddress</span></span>
<span data-ttu-id="be058-122">A tűzfalszabály érvényes IP-hatókörének kezdete</span><span class="sxs-lookup"><span data-stu-id="be058-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be058-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="be058-123">-Confirm</span></span>
<span data-ttu-id="be058-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="be058-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be058-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be058-125">-WhatIf</span></span>
<span data-ttu-id="be058-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="be058-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be058-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="be058-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be058-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be058-128">CommonParameters</span></span>
<span data-ttu-id="be058-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="be058-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be058-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be058-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be058-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="be058-131">INPUTS</span></span>

### <span data-ttu-id="be058-132">System. String</span><span class="sxs-lookup"><span data-stu-id="be058-132">System.String</span></span>

## <span data-ttu-id="be058-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="be058-133">OUTPUTS</span></span>

### <span data-ttu-id="be058-134">Microsoft. Azure. Command. DataLakeAnalytics. models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="be058-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="be058-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="be058-135">NOTES</span></span>

## <span data-ttu-id="be058-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="be058-136">RELATED LINKS</span></span>
