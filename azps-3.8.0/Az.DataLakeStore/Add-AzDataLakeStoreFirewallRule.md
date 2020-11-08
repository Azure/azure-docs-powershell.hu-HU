---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: a13125695ab5f4c57ab2e7013d64fff376643076
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010522"
---
# <span data-ttu-id="b7ddd-101">Add-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b7ddd-101">Add-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="b7ddd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b7ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="b7ddd-103">Tűzfal-szabály felvétele a megadott Data Lake Store-fiókba.</span><span class="sxs-lookup"><span data-stu-id="b7ddd-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="b7ddd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b7ddd-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7ddd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b7ddd-105">DESCRIPTION</span></span>
<span data-ttu-id="b7ddd-106">A **Add-AzDataLakeStoreFirewallRule** parancsmag a megadott adattó-tároló fiókba felveszi a tűzfal szabályait.</span><span class="sxs-lookup"><span data-stu-id="b7ddd-106">The **Add-AzDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="b7ddd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b7ddd-107">EXAMPLES</span></span>

### <span data-ttu-id="b7ddd-108">1. példa: Új tűzfalszabály hozzáadása az adattó-tároló fiókhoz</span><span class="sxs-lookup"><span data-stu-id="b7ddd-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="b7ddd-109">Ezzel létrehoz egy új, "MyRule" nevű tűzfal-szabályt a "ContosoADL" fiókban, a 127.0.0.1-127.0.0.2 IP-tartománnyal</span><span class="sxs-lookup"><span data-stu-id="b7ddd-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="b7ddd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b7ddd-110">PARAMETERS</span></span>

### <span data-ttu-id="b7ddd-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="b7ddd-111">-Account</span></span>
<span data-ttu-id="b7ddd-112">Az adattó áruházbeli fiókja a tűzfalszabály hozzáadásához</span><span class="sxs-lookup"><span data-stu-id="b7ddd-112">The Data Lake Store account to add the firewall rule to</span></span>

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

### <span data-ttu-id="b7ddd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7ddd-113">-DefaultProfile</span></span>
<span data-ttu-id="b7ddd-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b7ddd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7ddd-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="b7ddd-115">-EndIpAddress</span></span>
<span data-ttu-id="b7ddd-116">A tűzfalszabály érvényes IP-hatókörének a vége</span><span class="sxs-lookup"><span data-stu-id="b7ddd-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="b7ddd-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b7ddd-117">-Name</span></span>
<span data-ttu-id="b7ddd-118">A hozzáadni kívánt tűzfal-szabály neve.</span><span class="sxs-lookup"><span data-stu-id="b7ddd-118">The name of the firewall rule to add.</span></span>

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

### <span data-ttu-id="b7ddd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7ddd-119">-ResourceGroupName</span></span>
<span data-ttu-id="b7ddd-120">Annak az erőforráscsoport-csoportnak a neve, amelybe a tűzfalszabály hozzáadására szolgáló fiók van.</span><span class="sxs-lookup"><span data-stu-id="b7ddd-120">Name of resource group under which the account to add the firewall rule is.</span></span>

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

### <span data-ttu-id="b7ddd-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="b7ddd-121">-StartIpAddress</span></span>
<span data-ttu-id="b7ddd-122">A tűzfalszabály érvényes IP-hatókörének kezdete</span><span class="sxs-lookup"><span data-stu-id="b7ddd-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="b7ddd-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b7ddd-123">-Confirm</span></span>
<span data-ttu-id="b7ddd-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b7ddd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7ddd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7ddd-125">-WhatIf</span></span>
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

### <span data-ttu-id="b7ddd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7ddd-126">CommonParameters</span></span>
<span data-ttu-id="b7ddd-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b7ddd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7ddd-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7ddd-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7ddd-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7ddd-129">INPUTS</span></span>

### <span data-ttu-id="b7ddd-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b7ddd-130">System.String</span></span>

## <span data-ttu-id="b7ddd-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7ddd-131">OUTPUTS</span></span>

### <span data-ttu-id="b7ddd-132">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b7ddd-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="b7ddd-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b7ddd-133">NOTES</span></span>

## <span data-ttu-id="b7ddd-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7ddd-134">RELATED LINKS</span></span>
