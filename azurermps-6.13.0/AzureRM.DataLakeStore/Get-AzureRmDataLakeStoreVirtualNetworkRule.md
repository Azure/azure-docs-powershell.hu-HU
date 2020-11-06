---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 1b404a42c3d40138408d7fb6f2c13a8af91c45c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494060"
---
# <span data-ttu-id="c2795-101">Get-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c2795-101">Get-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="c2795-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c2795-102">SYNOPSIS</span></span>
<span data-ttu-id="c2795-103">A megadott virtuális hálózati szabályok beolvasása a megadott Data Lake Store áruházban.</span><span class="sxs-lookup"><span data-stu-id="c2795-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="c2795-104">Ha nincs megadva virtuális hálózati szabály, akkor a rendszer megjeleníti a fiókhoz tartozó összes virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="c2795-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2795-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c2795-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2795-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="c2795-106">DESCRIPTION</span></span>
<span data-ttu-id="c2795-107">A Get-AzureRmDataLakeStoreVirtualNetworkRule parancsmag a megadott adattó-tárolóban kapja meg a megadott virtuális hálózati szabályokat.</span><span class="sxs-lookup"><span data-stu-id="c2795-107">The Get-AzureRmDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="c2795-108">Ha nincs megadva virtuális hálózati szabály, akkor a rendszer megjeleníti a fiókhoz tartozó összes virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="c2795-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="c2795-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c2795-109">EXAMPLES</span></span>

### <span data-ttu-id="c2795-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c2795-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="c2795-111">A "myVNET" nevű virtuális hálózati szabály értékét számítja ki a "frissíteni" fiókból.</span><span class="sxs-lookup"><span data-stu-id="c2795-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="c2795-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c2795-112">PARAMETERS</span></span>

### <span data-ttu-id="c2795-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="c2795-113">-Account</span></span>
<span data-ttu-id="c2795-114">Az adattó-tároló fiók a virtuális hálózati szabály beszerzéséhez</span><span class="sxs-lookup"><span data-stu-id="c2795-114">The Data Lake Store account to get the virtual network rule from</span></span>

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

### <span data-ttu-id="c2795-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2795-115">-DefaultProfile</span></span>
<span data-ttu-id="c2795-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c2795-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2795-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c2795-117">-Name</span></span>
<span data-ttu-id="c2795-118">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="c2795-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="c2795-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2795-119">CommonParameters</span></span>
<span data-ttu-id="c2795-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c2795-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2795-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2795-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2795-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2795-122">INPUTS</span></span>

### <span data-ttu-id="c2795-123">System. String</span><span class="sxs-lookup"><span data-stu-id="c2795-123">System.String</span></span>

## <span data-ttu-id="c2795-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2795-124">OUTPUTS</span></span>

### <span data-ttu-id="c2795-125">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c2795-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="c2795-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c2795-126">NOTES</span></span>

## <span data-ttu-id="c2795-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2795-127">RELATED LINKS</span></span>
