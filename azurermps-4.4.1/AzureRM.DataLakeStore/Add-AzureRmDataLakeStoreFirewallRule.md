---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 45784bdcb684c1bd98ef1891042ad3ff6a172381
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679468"
---
# <span data-ttu-id="343df-101">Add-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="343df-101">Add-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="343df-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="343df-102">SYNOPSIS</span></span>
<span data-ttu-id="343df-103">Tűzfal-szabály felvétele a megadott Data Lake Store-fiókba.</span><span class="sxs-lookup"><span data-stu-id="343df-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="343df-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="343df-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="343df-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="343df-105">DESCRIPTION</span></span>
<span data-ttu-id="343df-106">A **Add-AzureRmDataLakeStoreFirewallRule** parancsmag a megadott adattó-tároló fiókba felveszi a tűzfal szabályait.</span><span class="sxs-lookup"><span data-stu-id="343df-106">The **Add-AzureRmDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="343df-107">Példák</span><span class="sxs-lookup"><span data-stu-id="343df-107">EXAMPLES</span></span>

### <span data-ttu-id="343df-108">1. példa: Új tűzfalszabály hozzáadása az adattó-tároló fiókhoz</span><span class="sxs-lookup"><span data-stu-id="343df-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="343df-109">Ezzel létrehoz egy új, "MyRule" nevű tűzfal-szabályt a "ContosoADL" fiókban, a 127.0.0.1-127.0.0.2 IP-tartománnyal</span><span class="sxs-lookup"><span data-stu-id="343df-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="343df-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="343df-110">PARAMETERS</span></span>

### <span data-ttu-id="343df-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="343df-111">-Account</span></span>
<span data-ttu-id="343df-112">Az adattó áruházbeli fiókja a tűzfalszabály hozzáadásához</span><span class="sxs-lookup"><span data-stu-id="343df-112">The Data Lake Store account to add the firewall rule to</span></span>

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

### <span data-ttu-id="343df-113">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="343df-113">-EndIpAddress</span></span>
<span data-ttu-id="343df-114">A tűzfalszabály érvényes IP-hatókörének a vége</span><span class="sxs-lookup"><span data-stu-id="343df-114">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="343df-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="343df-115">-Name</span></span>
<span data-ttu-id="343df-116">A hozzáadni kívánt tűzfal-szabály neve.</span><span class="sxs-lookup"><span data-stu-id="343df-116">The name of the firewall rule to add.</span></span>

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

### <span data-ttu-id="343df-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="343df-117">-ResourceGroupName</span></span>
<span data-ttu-id="343df-118">Annak az erőforráscsoport-csoportnak a neve, amelybe a tűzfalszabály hozzáadására szolgáló fiók van.</span><span class="sxs-lookup"><span data-stu-id="343df-118">Name of resource group under which the account to add the firewall rule is.</span></span>

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

### <span data-ttu-id="343df-119">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="343df-119">-StartIpAddress</span></span>
<span data-ttu-id="343df-120">A tűzfalszabály érvényes IP-hatókörének kezdete</span><span class="sxs-lookup"><span data-stu-id="343df-120">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="343df-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="343df-121">-Confirm</span></span>
<span data-ttu-id="343df-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="343df-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="343df-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="343df-123">-WhatIf</span></span>
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

### <span data-ttu-id="343df-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="343df-124">-DefaultProfile</span></span>
<span data-ttu-id="343df-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="343df-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="343df-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="343df-126">CommonParameters</span></span>
<span data-ttu-id="343df-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="343df-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="343df-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="343df-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="343df-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="343df-129">INPUTS</span></span>

## <span data-ttu-id="343df-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="343df-130">OUTPUTS</span></span>

### <span data-ttu-id="343df-131">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="343df-131">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="343df-132">A hozzáadott tűzfalszabály.</span><span class="sxs-lookup"><span data-stu-id="343df-132">The firewall rule that was added.</span></span>

## <span data-ttu-id="343df-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="343df-133">NOTES</span></span>

## <span data-ttu-id="343df-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="343df-134">RELATED LINKS</span></span>

