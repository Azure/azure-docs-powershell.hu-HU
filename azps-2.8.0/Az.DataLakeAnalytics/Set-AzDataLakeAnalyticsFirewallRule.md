---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 8d69a3297f23fdc9e4095a695ee790ae2476a136
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666885"
---
# <span data-ttu-id="8e2a4-101">Set-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8e2a4-101">Set-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="8e2a4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e2a4-102">SYNOPSIS</span></span>
<span data-ttu-id="8e2a4-103">Tűzfal szabályait frissíti az adattó-adatkezelési fiókban.</span><span class="sxs-lookup"><span data-stu-id="8e2a4-103">Updates a firewall rule in a Data Lake Analytics account.</span></span>

## <span data-ttu-id="8e2a4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e2a4-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e2a4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e2a4-105">DESCRIPTION</span></span>
<span data-ttu-id="8e2a4-106">A **set-AzDataLakeAnalyticsFirewallRule** parancsmag az Azure Data Lake Analytics-fiókban frissíti a tűzfalszabályok egyikét.</span><span class="sxs-lookup"><span data-stu-id="8e2a4-106">The **Set-AzDataLakeAnalyticsFirewallRule** cmdlet updates a firewall rule in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="8e2a4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8e2a4-107">EXAMPLES</span></span>

### <span data-ttu-id="8e2a4-108">Példa 1: tűzfalszabály frissítése</span><span class="sxs-lookup"><span data-stu-id="8e2a4-108">Example 1: Update a firewall rule</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="8e2a4-109">Ez a parancs frissíti a "saját tűzfalszabály" nevű tűzfal-szabályt a "ContosoAdlAcct" fiókban, hogy az új IP-sor legyen: 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="8e2a4-109">This command updates the firewall rule named "my firewall rule" in account "ContosoAdlAcct" to have the new IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="8e2a4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e2a4-110">PARAMETERS</span></span>

### <span data-ttu-id="8e2a4-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="8e2a4-111">-Account</span></span>
<span data-ttu-id="8e2a4-112">Az Data Lake Analytics-fiók a tűzfalszabályok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="8e2a4-112">The Data Lake Analytics account to update the firewall rule in</span></span>

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

### <span data-ttu-id="8e2a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e2a4-113">-DefaultProfile</span></span>
<span data-ttu-id="8e2a4-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8e2a4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e2a4-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="8e2a4-115">-EndIpAddress</span></span>
<span data-ttu-id="8e2a4-116">A tűzfalszabály érvényes IP-hatókörének a vége</span><span class="sxs-lookup"><span data-stu-id="8e2a4-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e2a4-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8e2a4-117">-Name</span></span>
<span data-ttu-id="8e2a4-118">A tűzfalszabály neve.</span><span class="sxs-lookup"><span data-stu-id="8e2a4-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="8e2a4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e2a4-119">-ResourceGroupName</span></span>
<span data-ttu-id="8e2a4-120">Annak az erőforráscsoport-csoportnak a neve, amelybe be szeretné olvasni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="8e2a4-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="8e2a4-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="8e2a4-121">-StartIpAddress</span></span>
<span data-ttu-id="8e2a4-122">A tűzfalszabály érvényes IP-hatókörének kezdete</span><span class="sxs-lookup"><span data-stu-id="8e2a4-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e2a4-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8e2a4-123">-Confirm</span></span>
<span data-ttu-id="8e2a4-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8e2a4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e2a4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e2a4-125">-WhatIf</span></span>
<span data-ttu-id="8e2a4-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8e2a4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e2a4-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8e2a4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e2a4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e2a4-128">CommonParameters</span></span>
<span data-ttu-id="8e2a4-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e2a4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e2a4-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e2a4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e2a4-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e2a4-131">INPUTS</span></span>

### <span data-ttu-id="8e2a4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8e2a4-132">System.String</span></span>

## <span data-ttu-id="8e2a4-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e2a4-133">OUTPUTS</span></span>

### <span data-ttu-id="8e2a4-134">Microsoft. Azure. Command. DataLakeAnalytics. models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8e2a4-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="8e2a4-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e2a4-135">NOTES</span></span>

## <span data-ttu-id="8e2a4-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e2a4-136">RELATED LINKS</span></span>
