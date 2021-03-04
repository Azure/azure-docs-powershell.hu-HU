---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: ec5ac8ab949b95fba3f82ea795dadcecfac360ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931185"
---
# <span data-ttu-id="cccf9-101">Get-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="cccf9-101">Get-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="cccf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cccf9-102">SYNOPSIS</span></span>
<span data-ttu-id="cccf9-103">A megadott virtuális hálózati szabályokat kapja meg a megadott Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="cccf9-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="cccf9-104">Ha nincs megadva virtuális hálózati szabály, akkor felsorolja a fiók összes virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="cccf9-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="cccf9-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cccf9-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cccf9-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cccf9-106">DESCRIPTION</span></span>
<span data-ttu-id="cccf9-107">A Get-AzDataLakeStoreVirtualNetworkRule parancsmag megkapja a megadott virtuális hálózati szabályokat a megadott Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="cccf9-107">The Get-AzDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="cccf9-108">Ha nincs megadva virtuális hálózati szabály, akkor felsorolja a fiók összes virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="cccf9-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="cccf9-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cccf9-109">EXAMPLES</span></span>

### <span data-ttu-id="cccf9-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="cccf9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="cccf9-111">Visszaadja a "myVNET" nevű virtuális hálózatszabályt a "dls" fiókból.</span><span class="sxs-lookup"><span data-stu-id="cccf9-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="cccf9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cccf9-112">PARAMETERS</span></span>

### <span data-ttu-id="cccf9-113">-Account</span><span class="sxs-lookup"><span data-stu-id="cccf9-113">-Account</span></span>
<span data-ttu-id="cccf9-114">The Data Lake Store account to get the virtual network rule from</span><span class="sxs-lookup"><span data-stu-id="cccf9-114">The Data Lake Store account to get the virtual network rule from</span></span>

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

### <span data-ttu-id="cccf9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cccf9-115">-DefaultProfile</span></span>
<span data-ttu-id="cccf9-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cccf9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cccf9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cccf9-117">-Name</span></span>
<span data-ttu-id="cccf9-118">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="cccf9-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="cccf9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cccf9-119">CommonParameters</span></span>
<span data-ttu-id="cccf9-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cccf9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cccf9-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cccf9-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cccf9-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cccf9-122">INPUTS</span></span>

### <span data-ttu-id="cccf9-123">System.String</span><span class="sxs-lookup"><span data-stu-id="cccf9-123">System.String</span></span>

## <span data-ttu-id="cccf9-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cccf9-124">OUTPUTS</span></span>

### <span data-ttu-id="cccf9-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="cccf9-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="cccf9-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cccf9-126">NOTES</span></span>

## <span data-ttu-id="cccf9-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cccf9-127">RELATED LINKS</span></span>
