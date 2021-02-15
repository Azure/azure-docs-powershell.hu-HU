---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 91941fbef7363a56da8a8021294750cc862aab55
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161971"
---
# <span data-ttu-id="047a2-101">Set-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="047a2-101">Set-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="047a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="047a2-102">SYNOPSIS</span></span>
<span data-ttu-id="047a2-103">Frissíti a tűzfalszabályt egy Data Lake Analytics-fiókban.</span><span class="sxs-lookup"><span data-stu-id="047a2-103">Updates a firewall rule in a Data Lake Analytics account.</span></span>

## <span data-ttu-id="047a2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="047a2-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="047a2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="047a2-105">DESCRIPTION</span></span>
<span data-ttu-id="047a2-106">A **Set-AzDataLakeAnalyticsFirewallRule** parancsmag frissíti a tűzfalszabályt egy Azure Data Lake Analytics-fiókban.</span><span class="sxs-lookup"><span data-stu-id="047a2-106">The **Set-AzDataLakeAnalyticsFirewallRule** cmdlet updates a firewall rule in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="047a2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="047a2-107">EXAMPLES</span></span>

### <span data-ttu-id="047a2-108">1. példa: Tűzfalszabály frissítése</span><span class="sxs-lookup"><span data-stu-id="047a2-108">Example 1: Update a firewall rule</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="047a2-109">Ez a parancs frissíti a "ContosoAdlAcct" fiók tűzfalszabályát a következő új IP-tartományra: 127.0.0.1 - 127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="047a2-109">This command updates the firewall rule named "my firewall rule" in account "ContosoAdlAcct" to have the new IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="047a2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="047a2-110">PARAMETERS</span></span>

### <span data-ttu-id="047a2-111">-Account</span><span class="sxs-lookup"><span data-stu-id="047a2-111">-Account</span></span>
<span data-ttu-id="047a2-112">The Data Lake Analytics account to update the firewall rule in</span><span class="sxs-lookup"><span data-stu-id="047a2-112">The Data Lake Analytics account to update the firewall rule in</span></span>

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

### <span data-ttu-id="047a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="047a2-113">-DefaultProfile</span></span>
<span data-ttu-id="047a2-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="047a2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="047a2-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="047a2-115">-EndIpAddress</span></span>
<span data-ttu-id="047a2-116">A tűzfalszabály érvényes IP-tartományának vége</span><span class="sxs-lookup"><span data-stu-id="047a2-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="047a2-117">-Name</span><span class="sxs-lookup"><span data-stu-id="047a2-117">-Name</span></span>
<span data-ttu-id="047a2-118">A tűzfalszabály neve.</span><span class="sxs-lookup"><span data-stu-id="047a2-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="047a2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="047a2-119">-ResourceGroupName</span></span>
<span data-ttu-id="047a2-120">Annak az erőforráscsoportnak a neve, amely alatt be szeretnéolvasni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="047a2-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="047a2-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="047a2-121">-StartIpAddress</span></span>
<span data-ttu-id="047a2-122">A tűzfalszabály érvényes IP-tartományának kezdete</span><span class="sxs-lookup"><span data-stu-id="047a2-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="047a2-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="047a2-123">-Confirm</span></span>
<span data-ttu-id="047a2-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="047a2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="047a2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="047a2-125">-WhatIf</span></span>
<span data-ttu-id="047a2-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="047a2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="047a2-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="047a2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="047a2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="047a2-128">CommonParameters</span></span>
<span data-ttu-id="047a2-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="047a2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="047a2-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="047a2-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="047a2-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="047a2-131">INPUTS</span></span>

### <span data-ttu-id="047a2-132">System.String</span><span class="sxs-lookup"><span data-stu-id="047a2-132">System.String</span></span>

## <span data-ttu-id="047a2-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="047a2-133">OUTPUTS</span></span>

### <span data-ttu-id="047a2-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="047a2-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="047a2-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="047a2-135">NOTES</span></span>

## <span data-ttu-id="047a2-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="047a2-136">RELATED LINKS</span></span>
