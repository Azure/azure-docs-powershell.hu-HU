---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 1c649a63e8ba57a3d2e9f9af28e0ce4b12ca9a0d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297716"
---
# <span data-ttu-id="c08dd-101">Set-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c08dd-101">Set-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="c08dd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c08dd-102">SYNOPSIS</span></span>
<span data-ttu-id="c08dd-103">Módosítja a megadott virtuális hálózati szabályt a megadott adattó-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="c08dd-103">Modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="c08dd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c08dd-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c08dd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c08dd-105">DESCRIPTION</span></span>
<span data-ttu-id="c08dd-106">A **set-AzDataLakeStoreVirtualNetworkRule** parancsmag a megadott Data Lake Store-ban módosítja a megadott virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="c08dd-106">The **Set-AzDataLakeStoreVirtualNetworkRule** cmdlet modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="c08dd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c08dd-107">EXAMPLES</span></span>

### <span data-ttu-id="c08dd-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c08dd-108">Example 1</span></span>
```powershell
PS C:\> Set-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "updatedId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/updatedId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="c08dd-109">A virtuális hálózati szabály "myVNET" alhálózati azonosítójának frissítése a "frissíteni" fiókból "updatedId"-ra</span><span class="sxs-lookup"><span data-stu-id="c08dd-109">Updates the subnet id of virtual network rule "myVNET" in account "dls" to "updatedId"</span></span>

## <span data-ttu-id="c08dd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c08dd-110">PARAMETERS</span></span>

### <span data-ttu-id="c08dd-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="c08dd-111">-Account</span></span>
<span data-ttu-id="c08dd-112">Az Data Lake Store fiók a virtuális hálózati szabály frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="c08dd-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="c08dd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c08dd-113">-DefaultProfile</span></span>
<span data-ttu-id="c08dd-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c08dd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c08dd-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c08dd-115">-Name</span></span>
<span data-ttu-id="c08dd-116">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="c08dd-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="c08dd-117">– NetI</span><span class="sxs-lookup"><span data-stu-id="c08dd-117">-SubnetId</span></span>
<span data-ttu-id="c08dd-118">A virtuális hálózati szabály érvényes IP-hatókörének kezdete</span><span class="sxs-lookup"><span data-stu-id="c08dd-118">The start of the valid ip range for the virtual network rule</span></span>

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

### <span data-ttu-id="c08dd-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c08dd-119">-Confirm</span></span>
<span data-ttu-id="c08dd-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c08dd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c08dd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c08dd-121">-WhatIf</span></span>
<span data-ttu-id="c08dd-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c08dd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c08dd-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c08dd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c08dd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c08dd-124">CommonParameters</span></span>
<span data-ttu-id="c08dd-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c08dd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c08dd-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c08dd-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c08dd-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c08dd-127">INPUTS</span></span>

### <span data-ttu-id="c08dd-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c08dd-128">System.String</span></span>

## <span data-ttu-id="c08dd-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c08dd-129">OUTPUTS</span></span>

### <span data-ttu-id="c08dd-130">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c08dd-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="c08dd-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c08dd-131">NOTES</span></span>

## <span data-ttu-id="c08dd-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c08dd-132">RELATED LINKS</span></span>
