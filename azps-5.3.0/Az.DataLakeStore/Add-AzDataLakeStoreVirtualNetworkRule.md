---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 8fbb586e1829cd40302ab290c2d671c67666b7e3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465851"
---
# <span data-ttu-id="dffca-101">Add-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="dffca-101">Add-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="dffca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dffca-102">SYNOPSIS</span></span>
<span data-ttu-id="dffca-103">Virtuális hálózati szabályt ad hozzá a megadott Data Lake Store-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="dffca-103">Adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="dffca-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dffca-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dffca-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dffca-105">DESCRIPTION</span></span>
<span data-ttu-id="dffca-106">Az **Add-AzDataLakeStoreVirtualNetworkRule** parancsmag hozzáad egy virtuális hálózati szabályt a megadott Data Lake Store-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="dffca-106">The **Add-AzDataLakeStoreVirtualNetworkRule** cmdlet adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="dffca-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dffca-107">EXAMPLES</span></span>

### <span data-ttu-id="dffca-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="dffca-108">Example 1</span></span>
```powershell
PS C:\> Add-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "testId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="dffca-109">Ez létrehoz egy "myVNET" nevű új virtuális hálózati szabályt a "dls" fiókban a "testId" alhálózati azonosítóval</span><span class="sxs-lookup"><span data-stu-id="dffca-109">This creates a new virtual network rule called "myVNET" in account "dls" with a subnet id "testId"</span></span>

## <span data-ttu-id="dffca-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dffca-110">PARAMETERS</span></span>

### <span data-ttu-id="dffca-111">-Account</span><span class="sxs-lookup"><span data-stu-id="dffca-111">-Account</span></span>
<span data-ttu-id="dffca-112">The Data Lake Store account to add the virtual network rule to</span><span class="sxs-lookup"><span data-stu-id="dffca-112">The Data Lake Store account to add the virtual network rule to</span></span>

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

### <span data-ttu-id="dffca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dffca-113">-DefaultProfile</span></span>
<span data-ttu-id="dffca-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dffca-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dffca-115">-Name</span><span class="sxs-lookup"><span data-stu-id="dffca-115">-Name</span></span>
<span data-ttu-id="dffca-116">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="dffca-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="dffca-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="dffca-117">-SubnetId</span></span>
<span data-ttu-id="dffca-118">A virtuális hálózati szabály alhálózatiazonosítója</span><span class="sxs-lookup"><span data-stu-id="dffca-118">The subnetId of the virtual network rule</span></span>

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

### <span data-ttu-id="dffca-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dffca-119">-Confirm</span></span>
<span data-ttu-id="dffca-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="dffca-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dffca-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dffca-121">-WhatIf</span></span>
<span data-ttu-id="dffca-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="dffca-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dffca-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dffca-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dffca-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dffca-124">CommonParameters</span></span>
<span data-ttu-id="dffca-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dffca-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dffca-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dffca-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dffca-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dffca-127">INPUTS</span></span>

### <span data-ttu-id="dffca-128">System.String</span><span class="sxs-lookup"><span data-stu-id="dffca-128">System.String</span></span>

## <span data-ttu-id="dffca-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dffca-129">OUTPUTS</span></span>

### <span data-ttu-id="dffca-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="dffca-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="dffca-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dffca-131">NOTES</span></span>

## <span data-ttu-id="dffca-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dffca-132">RELATED LINKS</span></span>
