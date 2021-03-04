---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 31e4f1be594735d8ea7afbe9abc5f6ccb21ada1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921297"
---
# <span data-ttu-id="4b465-101">Remove-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4b465-101">Remove-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="4b465-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b465-102">SYNOPSIS</span></span>
<span data-ttu-id="4b465-103">Eltávolít egy tűzfalszabályt egy Data Lake Analytics-fiókból.</span><span class="sxs-lookup"><span data-stu-id="4b465-103">Removes a firewall rule from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="4b465-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4b465-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4b465-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4b465-105">DESCRIPTION</span></span>
<span data-ttu-id="4b465-106">A **Remove-AzDataLakeAnalyticsFirewallRule** parancsmag eltávolít egy tűzfalszabályt egy Azure Data Lake Analytics-fiókból.</span><span class="sxs-lookup"><span data-stu-id="4b465-106">The **Remove-AzDataLakeAnalyticsFirewallRule** cmdlet removes a firewall rule from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="4b465-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4b465-107">EXAMPLES</span></span>

### <span data-ttu-id="4b465-108">1. példa: Tűzfalszabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4b465-108">Example 1: Remove a firewall rule</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="4b465-109">Ez a parancs eltávolítja a "saját tűzfalszabály" nevű tűzfalszabályt a "ContosoAdlAcct" fiókból.</span><span class="sxs-lookup"><span data-stu-id="4b465-109">This command removes the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="4b465-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b465-110">PARAMETERS</span></span>

### <span data-ttu-id="4b465-111">-Account</span><span class="sxs-lookup"><span data-stu-id="4b465-111">-Account</span></span>
<span data-ttu-id="4b465-112">The Data Lake Analytics account to remove the firewall rule from</span><span class="sxs-lookup"><span data-stu-id="4b465-112">The Data Lake Analytics account to remove the firewall rule from</span></span>

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

### <span data-ttu-id="4b465-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b465-113">-DefaultProfile</span></span>
<span data-ttu-id="4b465-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4b465-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b465-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4b465-115">-Name</span></span>
<span data-ttu-id="4b465-116">A tűzfalszabály neve.</span><span class="sxs-lookup"><span data-stu-id="4b465-116">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b465-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b465-117">-PassThru</span></span>
<span data-ttu-id="4b465-118">Azt jelzi, hogy a törlési művelet eredményét jelző logikai választ kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="4b465-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b465-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b465-119">-ResourceGroupName</span></span>
<span data-ttu-id="4b465-120">Annak az erőforráscsoportnak a neve, amely alatt be szeretnéolvasni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="4b465-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="4b465-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b465-121">-Confirm</span></span>
<span data-ttu-id="4b465-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4b465-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b465-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b465-123">-WhatIf</span></span>
<span data-ttu-id="4b465-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4b465-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b465-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4b465-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b465-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b465-126">CommonParameters</span></span>
<span data-ttu-id="4b465-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b465-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b465-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b465-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b465-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4b465-129">INPUTS</span></span>

### <span data-ttu-id="4b465-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4b465-130">System.String</span></span>

### <span data-ttu-id="4b465-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4b465-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4b465-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b465-132">OUTPUTS</span></span>

### <span data-ttu-id="4b465-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4b465-133">System.Boolean</span></span>

## <span data-ttu-id="4b465-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4b465-134">NOTES</span></span>

## <span data-ttu-id="4b465-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4b465-135">RELATED LINKS</span></span>
