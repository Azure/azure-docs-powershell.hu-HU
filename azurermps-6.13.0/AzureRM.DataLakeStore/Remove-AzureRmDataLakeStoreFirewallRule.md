---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 7e762ed090b0076c5cc8d0b359cf8883ae26265d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491947"
---
# <span data-ttu-id="6e866-101">Remove-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6e866-101">Remove-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="6e866-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6e866-102">SYNOPSIS</span></span>
<span data-ttu-id="6e866-103">A megadott tűzfalszabályok eltávolítása a megadott Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="6e866-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e866-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6e866-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e866-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6e866-105">DESCRIPTION</span></span>
<span data-ttu-id="6e866-106">A **Remove-AzureRmDataLakeStoreFirewallRule** parancsmag eltávolítja a megadott tűzfalszabályok a megadott Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="6e866-106">The **Remove-AzureRmDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="6e866-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6e866-107">EXAMPLES</span></span>

### <span data-ttu-id="6e866-108">1. példa: tűzfalszabály eltávolítása egy fiókból</span><span class="sxs-lookup"><span data-stu-id="6e866-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="6e866-109">A "MyFirewallRule" "ContosoADL" fiókból eltávolított tűzfalszabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6e866-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="6e866-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6e866-110">PARAMETERS</span></span>

### <span data-ttu-id="6e866-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="6e866-111">-Account</span></span>
<span data-ttu-id="6e866-112">Az Data Lake Store fiók a tűzfalszabályok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="6e866-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="6e866-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e866-113">-DefaultProfile</span></span>
<span data-ttu-id="6e866-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6e866-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e866-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6e866-115">-Name</span></span>
<span data-ttu-id="6e866-116">A törlendő tűzfal-szabály neve.</span><span class="sxs-lookup"><span data-stu-id="6e866-116">The name of the firewall rule to delete.</span></span>

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

### <span data-ttu-id="6e866-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e866-117">-PassThru</span></span>
<span data-ttu-id="6e866-118">A törlési művelet eredményét jelző logikai választ adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="6e866-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="6e866-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e866-119">-ResourceGroupName</span></span>
<span data-ttu-id="6e866-120">Annak a csoportnak a nevét adja meg, amely tartalmazza azt a fiókot, amelyből el szeretné távolítani a tűzfal szabályát.</span><span class="sxs-lookup"><span data-stu-id="6e866-120">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

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

### <span data-ttu-id="6e866-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6e866-121">-Confirm</span></span>
<span data-ttu-id="6e866-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6e866-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e866-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e866-123">-WhatIf</span></span>
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

### <span data-ttu-id="6e866-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e866-124">CommonParameters</span></span>
<span data-ttu-id="6e866-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6e866-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e866-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e866-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e866-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e866-127">INPUTS</span></span>

### <span data-ttu-id="6e866-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6e866-128">System.String</span></span>

### <span data-ttu-id="6e866-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6e866-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6e866-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e866-130">OUTPUTS</span></span>

### <span data-ttu-id="6e866-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6e866-131">System.Boolean</span></span>

## <span data-ttu-id="6e866-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6e866-132">NOTES</span></span>

## <span data-ttu-id="6e866-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e866-133">RELATED LINKS</span></span>
