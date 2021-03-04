---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/add-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: ed5d4514603ccefeefa4e99d9458434ffeb17cba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925010"
---
# <span data-ttu-id="f19e3-101">Add-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f19e3-101">Add-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="f19e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f19e3-102">SYNOPSIS</span></span>
<span data-ttu-id="f19e3-103">Tűzfalszabály hozzáadása Data Lake Analytics-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="f19e3-103">Adds a firewall rule to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="f19e3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f19e3-104">SYNTAX</span></span>

```
Add-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f19e3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f19e3-105">DESCRIPTION</span></span>
<span data-ttu-id="f19e3-106">Az **Add-AzDataLakeAnalyticsFirewallRule parancsmag** tűzfalszabályt ad egy Azure Data Lake Analytics-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="f19e3-106">The **Add-AzDataLakeAnalyticsFirewallRule** cmdlet adds a firewall rule to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="f19e3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f19e3-107">EXAMPLES</span></span>

### <span data-ttu-id="f19e3-108">1. példa: Tűzfalszabály hozzáadása</span><span class="sxs-lookup"><span data-stu-id="f19e3-108">Example 1: Add a firewall rule</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="f19e3-109">Ez a parancs hozzáadja a "saját tűzfalszabály" nevű tűzfalszabályt a "ContosoAdlAcct" fiókból a következő IP-tartomán belül: 127.0.0.1 - 127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="f19e3-109">This command adds the firewall rule named "my firewall rule" from account "ContosoAdlAcct" with the IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="f19e3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f19e3-110">PARAMETERS</span></span>

### <span data-ttu-id="f19e3-111">-Account</span><span class="sxs-lookup"><span data-stu-id="f19e3-111">-Account</span></span>
<span data-ttu-id="f19e3-112">The Data Lake Analytics account to add the firewall rule to</span><span class="sxs-lookup"><span data-stu-id="f19e3-112">The Data Lake Analytics account to add the firewall rule to</span></span>

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

### <span data-ttu-id="f19e3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f19e3-113">-DefaultProfile</span></span>
<span data-ttu-id="f19e3-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f19e3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f19e3-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="f19e3-115">-EndIpAddress</span></span>
<span data-ttu-id="f19e3-116">A tűzfalszabály érvényes IP-tartományának vége</span><span class="sxs-lookup"><span data-stu-id="f19e3-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="f19e3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f19e3-117">-Name</span></span>
<span data-ttu-id="f19e3-118">A tűzfalszabály neve.</span><span class="sxs-lookup"><span data-stu-id="f19e3-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="f19e3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f19e3-119">-ResourceGroupName</span></span>
<span data-ttu-id="f19e3-120">Annak az erőforráscsoportnak a neve, amely alatt be szeretnéolvasni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="f19e3-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="f19e3-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="f19e3-121">-StartIpAddress</span></span>
<span data-ttu-id="f19e3-122">A tűzfalszabály érvényes IP-tartományának kezdete</span><span class="sxs-lookup"><span data-stu-id="f19e3-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="f19e3-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f19e3-123">-Confirm</span></span>
<span data-ttu-id="f19e3-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f19e3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f19e3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f19e3-125">-WhatIf</span></span>
<span data-ttu-id="f19e3-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f19e3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f19e3-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f19e3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f19e3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f19e3-128">CommonParameters</span></span>
<span data-ttu-id="f19e3-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f19e3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f19e3-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f19e3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f19e3-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f19e3-131">INPUTS</span></span>

### <span data-ttu-id="f19e3-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f19e3-132">System.String</span></span>

## <span data-ttu-id="f19e3-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f19e3-133">OUTPUTS</span></span>

### <span data-ttu-id="f19e3-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f19e3-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="f19e3-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f19e3-135">NOTES</span></span>

## <span data-ttu-id="f19e3-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f19e3-136">RELATED LINKS</span></span>
