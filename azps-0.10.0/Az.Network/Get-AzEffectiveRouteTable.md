---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: 37c9827f2af970c0c376c31f4d67ba7723e02e99
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841678"
---
# <span data-ttu-id="385a3-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="385a3-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="385a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="385a3-102">SYNOPSIS</span></span>
<span data-ttu-id="385a3-103">Beilleszti egy hálózati kapcsolat tényleges útválasztási táblázatát.</span><span class="sxs-lookup"><span data-stu-id="385a3-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="385a3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="385a3-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="385a3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="385a3-105">DESCRIPTION</span></span>
<span data-ttu-id="385a3-106">A **Get-AzEffectiveRouteTable** parancsmag a hálózati felületen alkalmazott tényleges útválasztási táblázatot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="385a3-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="385a3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="385a3-107">EXAMPLES</span></span>

### <span data-ttu-id="385a3-108">Példa 1: a tényleges Route-táblázat beszerzése hálózati felületen</span><span class="sxs-lookup"><span data-stu-id="385a3-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="385a3-109">Ez a parancs a MyResourceGroup nevű erőforráscsoport MyNetworkInterface nevű hálózati kapcsolattal társított tényleges útvonali táblát kapja.</span><span class="sxs-lookup"><span data-stu-id="385a3-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="385a3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="385a3-110">PARAMETERS</span></span>

### <span data-ttu-id="385a3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="385a3-111">-AsJob</span></span>
<span data-ttu-id="385a3-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="385a3-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="385a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="385a3-113">-DefaultProfile</span></span>
<span data-ttu-id="385a3-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="385a3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="385a3-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="385a3-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="385a3-116">Megadhatja egy hálózati kapcsolat nevét.</span><span class="sxs-lookup"><span data-stu-id="385a3-116">Specified the name of a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="385a3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="385a3-117">-ResourceGroupName</span></span>
<span data-ttu-id="385a3-118">Egy hálózati kapcsolat erőforráscsoport-adatcsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="385a3-118">Specifies the resource group of a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="385a3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="385a3-119">CommonParameters</span></span>
<span data-ttu-id="385a3-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="385a3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="385a3-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="385a3-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="385a3-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="385a3-122">INPUTS</span></span>

## <span data-ttu-id="385a3-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="385a3-123">OUTPUTS</span></span>

### <span data-ttu-id="385a3-124">Microsoft. Azure. commands. Network. models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="385a3-124">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="385a3-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="385a3-125">NOTES</span></span>

## <span data-ttu-id="385a3-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="385a3-126">RELATED LINKS</span></span>

[<span data-ttu-id="385a3-127">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="385a3-127">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)


