---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 95e18d7e36122ed199b4a4c880b4fc918f1164f5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347969"
---
# <span data-ttu-id="e9df2-101">Get-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e9df2-101">Get-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="e9df2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9df2-102">SYNOPSIS</span></span>
<span data-ttu-id="e9df2-103">A megadott virtuális hálózati szabályokat kapja meg a megadott Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="e9df2-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="e9df2-104">Ha nincs megadva virtuális hálózati szabály, akkor felsorolja a fiók összes virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="e9df2-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="e9df2-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e9df2-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9df2-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e9df2-106">DESCRIPTION</span></span>
<span data-ttu-id="e9df2-107">A Get-AzDataLakeStoreVirtualNetworkRule parancsmag megkapja a megadott virtuális hálózati szabályokat a megadott Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="e9df2-107">The Get-AzDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="e9df2-108">Ha nincs megadva virtuális hálózati szabály, akkor felsorolja a fiók összes virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="e9df2-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="e9df2-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e9df2-109">EXAMPLES</span></span>

### <span data-ttu-id="e9df2-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="e9df2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="e9df2-111">Visszaadja a "myVNET" nevű virtuális hálózatszabályt a "dls" fiókból.</span><span class="sxs-lookup"><span data-stu-id="e9df2-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="e9df2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9df2-112">PARAMETERS</span></span>

### <span data-ttu-id="e9df2-113">-Account</span><span class="sxs-lookup"><span data-stu-id="e9df2-113">-Account</span></span>
<span data-ttu-id="e9df2-114">The Data Lake Store account to get the virtual network rule from</span><span class="sxs-lookup"><span data-stu-id="e9df2-114">The Data Lake Store account to get the virtual network rule from</span></span>

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

### <span data-ttu-id="e9df2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9df2-115">-DefaultProfile</span></span>
<span data-ttu-id="e9df2-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e9df2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9df2-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e9df2-117">-Name</span></span>
<span data-ttu-id="e9df2-118">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="e9df2-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="e9df2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9df2-119">CommonParameters</span></span>
<span data-ttu-id="e9df2-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9df2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9df2-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9df2-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9df2-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9df2-122">INPUTS</span></span>

### <span data-ttu-id="e9df2-123">System.String</span><span class="sxs-lookup"><span data-stu-id="e9df2-123">System.String</span></span>

## <span data-ttu-id="e9df2-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9df2-124">OUTPUTS</span></span>

### <span data-ttu-id="e9df2-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e9df2-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="e9df2-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e9df2-126">NOTES</span></span>

## <span data-ttu-id="e9df2-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9df2-127">RELATED LINKS</span></span>
