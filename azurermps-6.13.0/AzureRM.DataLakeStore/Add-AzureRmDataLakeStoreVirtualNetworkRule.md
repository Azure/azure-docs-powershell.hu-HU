---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: a25125b8aa76fa8d2be99f7f80b8fea2383bdf02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499575"
---
# <span data-ttu-id="aa7ba-101">Add-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="aa7ba-101">Add-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="aa7ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa7ba-102">SYNOPSIS</span></span>
<span data-ttu-id="aa7ba-103">Virtuális hálózati szabály felvétele a megadott Data Lake Store-fiókba.</span><span class="sxs-lookup"><span data-stu-id="aa7ba-103">Adds a virtual network rule to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa7ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa7ba-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa7ba-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa7ba-105">DESCRIPTION</span></span>
<span data-ttu-id="aa7ba-106">Az **Add-AzureRmDataLakeStoreVirtualNetworkRule** parancsmag virtuális hálózati szabályt ad a megadott Data Lake Store-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="aa7ba-106">The **Add-AzureRmDataLakeStoreVirtualNetworkRule** cmdlet adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="aa7ba-107">Példák</span><span class="sxs-lookup"><span data-stu-id="aa7ba-107">EXAMPLES</span></span>

### <span data-ttu-id="aa7ba-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="aa7ba-108">Example 1</span></span>
```powershell
PS C:\> Add-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "testId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="aa7ba-109">Ezzel létrehoz egy új virtuális hálózati szabályt "myVNET" néven a "frissíteni" fiókban "testId" alhálózati azonosítóval</span><span class="sxs-lookup"><span data-stu-id="aa7ba-109">This creates a new virtual network rule called "myVNET" in account "dls" with a subnet id "testId"</span></span>

## <span data-ttu-id="aa7ba-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa7ba-110">PARAMETERS</span></span>

### <span data-ttu-id="aa7ba-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="aa7ba-111">-Account</span></span>
<span data-ttu-id="aa7ba-112">Az Data Lake Store fiók a virtuális hálózati szabály hozzáadásához</span><span class="sxs-lookup"><span data-stu-id="aa7ba-112">The Data Lake Store account to add the virtual network rule to</span></span>

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

### <span data-ttu-id="aa7ba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa7ba-113">-DefaultProfile</span></span>
<span data-ttu-id="aa7ba-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aa7ba-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa7ba-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aa7ba-115">-Name</span></span>
<span data-ttu-id="aa7ba-116">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="aa7ba-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="aa7ba-117">– NetI</span><span class="sxs-lookup"><span data-stu-id="aa7ba-117">-SubnetId</span></span>
<span data-ttu-id="aa7ba-118">A virtuális hálózat szabálya</span><span class="sxs-lookup"><span data-stu-id="aa7ba-118">The subnetId of the virtual network rule</span></span>

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

### <span data-ttu-id="aa7ba-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aa7ba-119">-Confirm</span></span>
<span data-ttu-id="aa7ba-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aa7ba-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa7ba-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa7ba-121">-WhatIf</span></span>
<span data-ttu-id="aa7ba-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aa7ba-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa7ba-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aa7ba-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa7ba-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa7ba-124">CommonParameters</span></span>
<span data-ttu-id="aa7ba-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa7ba-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa7ba-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa7ba-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa7ba-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa7ba-127">INPUTS</span></span>

### <span data-ttu-id="aa7ba-128">System. String</span><span class="sxs-lookup"><span data-stu-id="aa7ba-128">System.String</span></span>

## <span data-ttu-id="aa7ba-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa7ba-129">OUTPUTS</span></span>

### <span data-ttu-id="aa7ba-130">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="aa7ba-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="aa7ba-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa7ba-131">NOTES</span></span>

## <span data-ttu-id="aa7ba-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa7ba-132">RELATED LINKS</span></span>
