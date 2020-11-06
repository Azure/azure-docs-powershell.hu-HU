---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 3ad3e98e6fb2ab5c6e0b04495142861ecfe9e0ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498975"
---
# <span data-ttu-id="a8af3-101">Set-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a8af3-101">Set-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="a8af3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a8af3-102">SYNOPSIS</span></span>
<span data-ttu-id="a8af3-103">A megadott tűzfalszabályok módosítása a megadott adattó-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="a8af3-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8af3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a8af3-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8af3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a8af3-105">DESCRIPTION</span></span>
<span data-ttu-id="a8af3-106">A **set-AzureRmDataLakeStoreFirewallRule** parancsmag a megadott tűzfal-szabályt módosítja a megadott adattó-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="a8af3-106">The **Set-AzureRmDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="a8af3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a8af3-107">EXAMPLES</span></span>

### <span data-ttu-id="a8af3-108">Példa 1: a tűzfalszabályok kezdési és befejezési IP-körének frissítése</span><span class="sxs-lookup"><span data-stu-id="a8af3-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="a8af3-109">A "ContosoADL" fiók "MyFirewallRule" ("") tűzfal-127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="a8af3-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="a8af3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a8af3-110">PARAMETERS</span></span>

### <span data-ttu-id="a8af3-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="a8af3-111">-Account</span></span>
<span data-ttu-id="a8af3-112">Az Data Lake Store fiók a tűzfalszabályok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="a8af3-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="a8af3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8af3-113">-DefaultProfile</span></span>
<span data-ttu-id="a8af3-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a8af3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8af3-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="a8af3-115">-EndIpAddress</span></span>
<span data-ttu-id="a8af3-116">A tűzfalszabály érvényes IP-hatókörének a vége</span><span class="sxs-lookup"><span data-stu-id="a8af3-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8af3-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a8af3-117">-Name</span></span>
<span data-ttu-id="a8af3-118">A tűzfalszabály neve.</span><span class="sxs-lookup"><span data-stu-id="a8af3-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="a8af3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8af3-119">-ResourceGroupName</span></span>
<span data-ttu-id="a8af3-120">Annak a csoportnak a nevét adja meg, amely a fiókot tartalmazza a tűzfalszabály frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="a8af3-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8af3-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="a8af3-121">-StartIpAddress</span></span>
<span data-ttu-id="a8af3-122">A tűzfalszabály érvényes IP-hatókörének kezdete</span><span class="sxs-lookup"><span data-stu-id="a8af3-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8af3-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a8af3-123">-Confirm</span></span>
<span data-ttu-id="a8af3-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a8af3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8af3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8af3-125">-WhatIf</span></span>
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

### <span data-ttu-id="a8af3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8af3-126">CommonParameters</span></span>
<span data-ttu-id="a8af3-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a8af3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8af3-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8af3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8af3-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8af3-129">INPUTS</span></span>

### <span data-ttu-id="a8af3-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="a8af3-130">None</span></span>
<span data-ttu-id="a8af3-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a8af3-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a8af3-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8af3-132">OUTPUTS</span></span>

### <span data-ttu-id="a8af3-133">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a8af3-133">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="a8af3-134">A frissített tűzfalszabály részletei.</span><span class="sxs-lookup"><span data-stu-id="a8af3-134">The details of the updated firewall rule.</span></span>

## <span data-ttu-id="a8af3-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a8af3-135">NOTES</span></span>

## <span data-ttu-id="a8af3-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8af3-136">RELATED LINKS</span></span>

