---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
ms.openlocfilehash: f42e378bb0bb5202f9f955dea1b844e343a0e037
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497823"
---
# <span data-ttu-id="53047-101">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="53047-101">Get-AzureRmEffectiveRouteTable</span></span>

## <span data-ttu-id="53047-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="53047-102">SYNOPSIS</span></span>
<span data-ttu-id="53047-103">Beilleszti egy hálózati kapcsolat tényleges útválasztási táblázatát.</span><span class="sxs-lookup"><span data-stu-id="53047-103">Gets the effective route table of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53047-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="53047-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53047-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="53047-105">DESCRIPTION</span></span>
<span data-ttu-id="53047-106">A **Get-AzureRmEffectiveRouteTable** parancsmag a hálózati felületen alkalmazott tényleges útválasztási táblázatot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="53047-106">The **Get-AzureRmEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="53047-107">Példák</span><span class="sxs-lookup"><span data-stu-id="53047-107">EXAMPLES</span></span>

### <span data-ttu-id="53047-108">Példa 1: a tényleges Route-táblázat beszerzése hálózati felületen</span><span class="sxs-lookup"><span data-stu-id="53047-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="53047-109">Ez a parancs a MyResourceGroup nevű erőforráscsoport MyNetworkInterface nevű hálózati kapcsolattal társított tényleges útvonali táblát kapja.</span><span class="sxs-lookup"><span data-stu-id="53047-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="53047-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="53047-110">PARAMETERS</span></span>

### <span data-ttu-id="53047-111">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="53047-111">-NetworkInterfaceName</span></span>
<span data-ttu-id="53047-112">Megadhatja egy hálózati kapcsolat nevét.</span><span class="sxs-lookup"><span data-stu-id="53047-112">Specified the name of a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53047-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53047-113">-ResourceGroupName</span></span>
<span data-ttu-id="53047-114">Egy hálózati kapcsolat erőforráscsoport-adatcsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="53047-114">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="53047-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53047-115">-DefaultProfile</span></span>
<span data-ttu-id="53047-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="53047-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53047-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53047-117">CommonParameters</span></span>
<span data-ttu-id="53047-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="53047-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53047-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53047-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53047-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="53047-120">INPUTS</span></span>

## <span data-ttu-id="53047-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53047-121">OUTPUTS</span></span>

### <span data-ttu-id="53047-122">Microsoft. Azure. commands. Network. models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="53047-122">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="53047-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="53047-123">NOTES</span></span>

## <span data-ttu-id="53047-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53047-124">RELATED LINKS</span></span>

[<span data-ttu-id="53047-125">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="53047-125">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>](./Get-AzureRmEffectiveNetworkSecurityGroup.md)


