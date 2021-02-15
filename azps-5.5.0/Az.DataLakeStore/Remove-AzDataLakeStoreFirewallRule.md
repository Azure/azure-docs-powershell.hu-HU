---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: e583379f9541c056943081b804a84ecd7bee7bf5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204350"
---
# <span data-ttu-id="821d7-101">Remove-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="821d7-101">Remove-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="821d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="821d7-102">SYNOPSIS</span></span>
<span data-ttu-id="821d7-103">A megadott tűzfalszabály eltávolítása a megadott Data Lake Store-ból.</span><span class="sxs-lookup"><span data-stu-id="821d7-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="821d7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="821d7-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="821d7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="821d7-105">DESCRIPTION</span></span>
<span data-ttu-id="821d7-106">A **Remove-AzDataLakeStoreFirewallRule** parancsmag eltávolítja a megadott tűzfalszabályt a megadott Data Lake Store-ból.</span><span class="sxs-lookup"><span data-stu-id="821d7-106">The **Remove-AzDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="821d7-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="821d7-107">EXAMPLES</span></span>

### <span data-ttu-id="821d7-108">1. példa: Tűzfalszabály eltávolítása fiókból</span><span class="sxs-lookup"><span data-stu-id="821d7-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="821d7-109">Eltávolítja a "MyFirewallRule" tűzfalszabályt a "ContosoADL" fiókból</span><span class="sxs-lookup"><span data-stu-id="821d7-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="821d7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="821d7-110">PARAMETERS</span></span>

### <span data-ttu-id="821d7-111">-Account</span><span class="sxs-lookup"><span data-stu-id="821d7-111">-Account</span></span>
<span data-ttu-id="821d7-112">The Data Lake Store account to update the firewall rule in</span><span class="sxs-lookup"><span data-stu-id="821d7-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="821d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="821d7-113">-DefaultProfile</span></span>
<span data-ttu-id="821d7-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="821d7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="821d7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="821d7-115">-Name</span></span>
<span data-ttu-id="821d7-116">A törölni kívánt tűzfalszabály neve.</span><span class="sxs-lookup"><span data-stu-id="821d7-116">The name of the firewall rule to delete.</span></span>

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

### <span data-ttu-id="821d7-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="821d7-117">-PassThru</span></span>
<span data-ttu-id="821d7-118">Azt jelzi, hogy a törlési művelet eredményét jelző logikai választ kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="821d7-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="821d7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="821d7-119">-ResourceGroupName</span></span>
<span data-ttu-id="821d7-120">Annak az erőforráscsoportnak a nevét adja meg, amely azt a fiókot tartalmazza, amelyből el szeretné távolítani a tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="821d7-120">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="821d7-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="821d7-121">-Confirm</span></span>
<span data-ttu-id="821d7-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="821d7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="821d7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="821d7-123">-WhatIf</span></span>
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

### <span data-ttu-id="821d7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="821d7-124">CommonParameters</span></span>
<span data-ttu-id="821d7-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="821d7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="821d7-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="821d7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="821d7-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="821d7-127">INPUTS</span></span>

### <span data-ttu-id="821d7-128">System.String</span><span class="sxs-lookup"><span data-stu-id="821d7-128">System.String</span></span>

### <span data-ttu-id="821d7-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="821d7-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="821d7-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="821d7-130">OUTPUTS</span></span>

### <span data-ttu-id="821d7-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="821d7-131">System.Boolean</span></span>

## <span data-ttu-id="821d7-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="821d7-132">NOTES</span></span>

## <span data-ttu-id="821d7-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="821d7-133">RELATED LINKS</span></span>
