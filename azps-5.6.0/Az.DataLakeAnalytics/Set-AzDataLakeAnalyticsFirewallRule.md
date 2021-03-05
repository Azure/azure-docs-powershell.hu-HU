---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 9fbb2064a7b7869af450ad267f73c6dc2e2b9a9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010630"
---
# <span data-ttu-id="572be-101">Set-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="572be-101">Set-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="572be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="572be-102">SYNOPSIS</span></span>
<span data-ttu-id="572be-103">Frissíti a tűzfalszabályt egy Data Lake Analytics-fiókban.</span><span class="sxs-lookup"><span data-stu-id="572be-103">Updates a firewall rule in a Data Lake Analytics account.</span></span>

## <span data-ttu-id="572be-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="572be-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="572be-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="572be-105">DESCRIPTION</span></span>
<span data-ttu-id="572be-106">A **Set-AzDataLakeAnalyticsFirewallRule** parancsmag frissíti a tűzfalszabályt egy Azure Data Lake Analytics-fiókban.</span><span class="sxs-lookup"><span data-stu-id="572be-106">The **Set-AzDataLakeAnalyticsFirewallRule** cmdlet updates a firewall rule in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="572be-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="572be-107">EXAMPLES</span></span>

### <span data-ttu-id="572be-108">1. példa: Tűzfalszabály frissítése</span><span class="sxs-lookup"><span data-stu-id="572be-108">Example 1: Update a firewall rule</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="572be-109">Ez a parancs frissíti a "ContosoAdlAcct" fiók tűzfalszabályát a következő új IP-tartományra: 127.0.0.1 - 127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="572be-109">This command updates the firewall rule named "my firewall rule" in account "ContosoAdlAcct" to have the new IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="572be-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="572be-110">PARAMETERS</span></span>

### <span data-ttu-id="572be-111">-Account</span><span class="sxs-lookup"><span data-stu-id="572be-111">-Account</span></span>
<span data-ttu-id="572be-112">The Data Lake Analytics account to update the firewall rule in</span><span class="sxs-lookup"><span data-stu-id="572be-112">The Data Lake Analytics account to update the firewall rule in</span></span>

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

### <span data-ttu-id="572be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="572be-113">-DefaultProfile</span></span>
<span data-ttu-id="572be-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="572be-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="572be-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="572be-115">-EndIpAddress</span></span>
<span data-ttu-id="572be-116">A tűzfalszabály érvényes IP-tartományának vége</span><span class="sxs-lookup"><span data-stu-id="572be-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="572be-117">-Name</span><span class="sxs-lookup"><span data-stu-id="572be-117">-Name</span></span>
<span data-ttu-id="572be-118">A tűzfalszabály neve.</span><span class="sxs-lookup"><span data-stu-id="572be-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="572be-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="572be-119">-ResourceGroupName</span></span>
<span data-ttu-id="572be-120">Annak az erőforráscsoportnak a neve, amely alatt be szeretnéolvasni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="572be-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="572be-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="572be-121">-StartIpAddress</span></span>
<span data-ttu-id="572be-122">A tűzfalszabály érvényes IP-tartományának kezdete</span><span class="sxs-lookup"><span data-stu-id="572be-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="572be-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="572be-123">-Confirm</span></span>
<span data-ttu-id="572be-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="572be-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="572be-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="572be-125">-WhatIf</span></span>
<span data-ttu-id="572be-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="572be-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="572be-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="572be-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="572be-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="572be-128">CommonParameters</span></span>
<span data-ttu-id="572be-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="572be-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="572be-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="572be-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="572be-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="572be-131">INPUTS</span></span>

### <span data-ttu-id="572be-132">System.String</span><span class="sxs-lookup"><span data-stu-id="572be-132">System.String</span></span>

## <span data-ttu-id="572be-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="572be-133">OUTPUTS</span></span>

### <span data-ttu-id="572be-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="572be-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="572be-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="572be-135">NOTES</span></span>

## <span data-ttu-id="572be-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="572be-136">RELATED LINKS</span></span>
