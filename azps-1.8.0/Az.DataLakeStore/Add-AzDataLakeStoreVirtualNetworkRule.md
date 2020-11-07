---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 4fccc705951ba944afdf13bf75d581e7c76d593f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671077"
---
# <span data-ttu-id="eab84-101">Add-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="eab84-101">Add-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="eab84-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eab84-102">SYNOPSIS</span></span>
<span data-ttu-id="eab84-103">Virtuális hálózati szabály felvétele a megadott Data Lake Store-fiókba.</span><span class="sxs-lookup"><span data-stu-id="eab84-103">Adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="eab84-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eab84-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eab84-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="eab84-105">DESCRIPTION</span></span>
<span data-ttu-id="eab84-106">Az **Add-AzDataLakeStoreVirtualNetworkRule** parancsmag virtuális hálózati szabályt ad a megadott Data Lake Store-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="eab84-106">The **Add-AzDataLakeStoreVirtualNetworkRule** cmdlet adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="eab84-107">Példák</span><span class="sxs-lookup"><span data-stu-id="eab84-107">EXAMPLES</span></span>

### <span data-ttu-id="eab84-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="eab84-108">Example 1</span></span>
```powershell
PS C:\> Add-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "testId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="eab84-109">Ezzel létrehoz egy új virtuális hálózati szabályt "myVNET" néven a "frissíteni" fiókban "testId" alhálózati azonosítóval</span><span class="sxs-lookup"><span data-stu-id="eab84-109">This creates a new virtual network rule called "myVNET" in account "dls" with a subnet id "testId"</span></span>

## <span data-ttu-id="eab84-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eab84-110">PARAMETERS</span></span>

### <span data-ttu-id="eab84-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="eab84-111">-Account</span></span>
<span data-ttu-id="eab84-112">Az Data Lake Store fiók a virtuális hálózati szabály hozzáadásához</span><span class="sxs-lookup"><span data-stu-id="eab84-112">The Data Lake Store account to add the virtual network rule to</span></span>

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

### <span data-ttu-id="eab84-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eab84-113">-DefaultProfile</span></span>
<span data-ttu-id="eab84-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eab84-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eab84-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eab84-115">-Name</span></span>
<span data-ttu-id="eab84-116">A virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="eab84-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="eab84-117">– NetI</span><span class="sxs-lookup"><span data-stu-id="eab84-117">-SubnetId</span></span>
<span data-ttu-id="eab84-118">A virtuális hálózat szabálya</span><span class="sxs-lookup"><span data-stu-id="eab84-118">The subnetId of the virtual network rule</span></span>

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

### <span data-ttu-id="eab84-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eab84-119">-Confirm</span></span>
<span data-ttu-id="eab84-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eab84-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eab84-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eab84-121">-WhatIf</span></span>
<span data-ttu-id="eab84-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eab84-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eab84-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eab84-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eab84-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eab84-124">CommonParameters</span></span>
<span data-ttu-id="eab84-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eab84-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eab84-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eab84-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eab84-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eab84-127">INPUTS</span></span>

### <span data-ttu-id="eab84-128">System. String</span><span class="sxs-lookup"><span data-stu-id="eab84-128">System.String</span></span>

## <span data-ttu-id="eab84-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eab84-129">OUTPUTS</span></span>

### <span data-ttu-id="eab84-130">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="eab84-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="eab84-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eab84-131">NOTES</span></span>

## <span data-ttu-id="eab84-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eab84-132">RELATED LINKS</span></span>
