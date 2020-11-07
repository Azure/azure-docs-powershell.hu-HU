---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 079ff61475405407fc2f6864d9fda43b1a5fc4cc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666840"
---
# <span data-ttu-id="322bb-101">Get-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="322bb-101">Get-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="322bb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="322bb-102">SYNOPSIS</span></span>
<span data-ttu-id="322bb-103">A megadott virtuális hálózati szabályok beolvasása a megadott Data Lake Store áruházban.</span><span class="sxs-lookup"><span data-stu-id="322bb-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="322bb-104">Ha nincs megadva virtuális hálózati szabály, akkor a rendszer megjeleníti a fiókhoz tartozó összes virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="322bb-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="322bb-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="322bb-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="322bb-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="322bb-106">DESCRIPTION</span></span>
<span data-ttu-id="322bb-107">A Get-AzDataLakeStoreVirtualNetworkRule parancsmag a megadott adattó-tárolóban kapja meg a megadott virtuális hálózati szabályokat.</span><span class="sxs-lookup"><span data-stu-id="322bb-107">The Get-AzDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="322bb-108">Ha nincs megadva virtuális hálózati szabály, akkor a rendszer megjeleníti a fiókhoz tartozó összes virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="322bb-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="322bb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="322bb-109">EXAMPLES</span></span>

### <span data-ttu-id="322bb-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="322bb-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="322bb-111">A "myVNET" nevű virtuális hálózati szabály értékét számítja ki a "frissíteni" fiókból.</span><span class="sxs-lookup"><span data-stu-id="322bb-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="322bb-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="322bb-112">PARAMETERS</span></span>

### <span data-ttu-id="322bb-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="322bb-113">-Account</span></span>
<span data-ttu-id="322bb-114">Az adattó-tároló fiók a virtuális hálózati szabály beszerzéséhez</span><span class="sxs-lookup"><span data-stu-id="322bb-114">The Data Lake Store account to get the virtual network rule from</span></span>

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

### <span data-ttu-id="322bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="322bb-115">-DefaultProfile</span></span>
<span data-ttu-id="322bb-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="322bb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="322bb-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="322bb-117">-Name</span></span>
<span data-ttu-id="322bb-118">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="322bb-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="322bb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="322bb-119">CommonParameters</span></span>
<span data-ttu-id="322bb-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="322bb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="322bb-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="322bb-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="322bb-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="322bb-122">INPUTS</span></span>

### <span data-ttu-id="322bb-123">System. String</span><span class="sxs-lookup"><span data-stu-id="322bb-123">System.String</span></span>

## <span data-ttu-id="322bb-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="322bb-124">OUTPUTS</span></span>

### <span data-ttu-id="322bb-125">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="322bb-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="322bb-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="322bb-126">NOTES</span></span>

## <span data-ttu-id="322bb-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="322bb-127">RELATED LINKS</span></span>
