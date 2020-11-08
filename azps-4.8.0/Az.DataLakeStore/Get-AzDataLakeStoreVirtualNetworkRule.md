---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 95e18d7e36122ed199b4a4c880b4fc918f1164f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181125"
---
# <span data-ttu-id="b86c4-101">Get-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b86c4-101">Get-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="b86c4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b86c4-102">SYNOPSIS</span></span>
<span data-ttu-id="b86c4-103">A megadott virtuális hálózati szabályok beolvasása a megadott Data Lake Store áruházban.</span><span class="sxs-lookup"><span data-stu-id="b86c4-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="b86c4-104">Ha nincs megadva virtuális hálózati szabály, akkor a rendszer megjeleníti a fiókhoz tartozó összes virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="b86c4-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="b86c4-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b86c4-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b86c4-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="b86c4-106">DESCRIPTION</span></span>
<span data-ttu-id="b86c4-107">A Get-AzDataLakeStoreVirtualNetworkRule parancsmag a megadott adattó-tárolóban kapja meg a megadott virtuális hálózati szabályokat.</span><span class="sxs-lookup"><span data-stu-id="b86c4-107">The Get-AzDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="b86c4-108">Ha nincs megadva virtuális hálózati szabály, akkor a rendszer megjeleníti a fiókhoz tartozó összes virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="b86c4-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="b86c4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b86c4-109">EXAMPLES</span></span>

### <span data-ttu-id="b86c4-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b86c4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="b86c4-111">A "myVNET" nevű virtuális hálózati szabály értékét számítja ki a "frissíteni" fiókból.</span><span class="sxs-lookup"><span data-stu-id="b86c4-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="b86c4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b86c4-112">PARAMETERS</span></span>

### <span data-ttu-id="b86c4-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="b86c4-113">-Account</span></span>
<span data-ttu-id="b86c4-114">Az adattó-tároló fiók a virtuális hálózati szabály beszerzéséhez</span><span class="sxs-lookup"><span data-stu-id="b86c4-114">The Data Lake Store account to get the virtual network rule from</span></span>

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

### <span data-ttu-id="b86c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b86c4-115">-DefaultProfile</span></span>
<span data-ttu-id="b86c4-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b86c4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b86c4-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b86c4-117">-Name</span></span>
<span data-ttu-id="b86c4-118">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="b86c4-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="b86c4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b86c4-119">CommonParameters</span></span>
<span data-ttu-id="b86c4-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b86c4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b86c4-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b86c4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b86c4-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b86c4-122">INPUTS</span></span>

### <span data-ttu-id="b86c4-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b86c4-123">System.String</span></span>

## <span data-ttu-id="b86c4-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b86c4-124">OUTPUTS</span></span>

### <span data-ttu-id="b86c4-125">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b86c4-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="b86c4-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b86c4-126">NOTES</span></span>

## <span data-ttu-id="b86c4-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b86c4-127">RELATED LINKS</span></span>
