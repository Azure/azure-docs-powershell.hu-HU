---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: c1e4c3f748df4808fe570e95150450d3b3987d00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503783"
---
# <span data-ttu-id="da029-101">Add-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="da029-101">Add-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="da029-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da029-102">SYNOPSIS</span></span>
<span data-ttu-id="da029-103">Tűzfal-szabály felvétele a megadott Data Lake Store-fiókba.</span><span class="sxs-lookup"><span data-stu-id="da029-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da029-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da029-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da029-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="da029-105">DESCRIPTION</span></span>
<span data-ttu-id="da029-106">A **Add-AzureRmDataLakeStoreFirewallRule** parancsmag a megadott adattó-tároló fiókba felveszi a tűzfal szabályait.</span><span class="sxs-lookup"><span data-stu-id="da029-106">The **Add-AzureRmDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="da029-107">Példák</span><span class="sxs-lookup"><span data-stu-id="da029-107">EXAMPLES</span></span>

### <span data-ttu-id="da029-108">1. példa: Új tűzfalszabály hozzáadása az adattó-tároló fiókhoz</span><span class="sxs-lookup"><span data-stu-id="da029-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="da029-109">Ezzel létrehoz egy új, "MyRule" nevű tűzfal-szabályt a "ContosoADL" fiókban, a 127.0.0.1-127.0.0.2 IP-tartománnyal</span><span class="sxs-lookup"><span data-stu-id="da029-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="da029-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da029-110">PARAMETERS</span></span>

### <span data-ttu-id="da029-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="da029-111">-Account</span></span>
<span data-ttu-id="da029-112">Az adattó áruházbeli fiókja a tűzfalszabály hozzáadásához</span><span class="sxs-lookup"><span data-stu-id="da029-112">The Data Lake Store account to add the firewall rule to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da029-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da029-113">-DefaultProfile</span></span>
<span data-ttu-id="da029-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="da029-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da029-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="da029-115">-EndIpAddress</span></span>
<span data-ttu-id="da029-116">A tűzfalszabály érvényes IP-hatókörének a vége</span><span class="sxs-lookup"><span data-stu-id="da029-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da029-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="da029-117">-Name</span></span>
<span data-ttu-id="da029-118">A hozzáadni kívánt tűzfal-szabály neve.</span><span class="sxs-lookup"><span data-stu-id="da029-118">The name of the firewall rule to add.</span></span>

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

### <span data-ttu-id="da029-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da029-119">-ResourceGroupName</span></span>
<span data-ttu-id="da029-120">Annak az erőforráscsoport-csoportnak a neve, amelybe a tűzfalszabály hozzáadására szolgáló fiók van.</span><span class="sxs-lookup"><span data-stu-id="da029-120">Name of resource group under which the account to add the firewall rule is.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da029-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="da029-121">-StartIpAddress</span></span>
<span data-ttu-id="da029-122">A tűzfalszabály érvényes IP-hatókörének kezdete</span><span class="sxs-lookup"><span data-stu-id="da029-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da029-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="da029-123">-Confirm</span></span>
<span data-ttu-id="da029-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="da029-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da029-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da029-125">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da029-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da029-126">CommonParameters</span></span>
<span data-ttu-id="da029-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da029-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da029-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da029-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da029-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da029-129">INPUTS</span></span>

### <span data-ttu-id="da029-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="da029-130">None</span></span>
<span data-ttu-id="da029-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="da029-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="da029-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da029-132">OUTPUTS</span></span>

### <span data-ttu-id="da029-133">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="da029-133">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="da029-134">A hozzáadott tűzfalszabály.</span><span class="sxs-lookup"><span data-stu-id="da029-134">The firewall rule that was added.</span></span>

## <span data-ttu-id="da029-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da029-135">NOTES</span></span>

## <span data-ttu-id="da029-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da029-136">RELATED LINKS</span></span>

