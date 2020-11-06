---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpPrefix.md
ms.openlocfilehash: 7b60c157f3e86e72461c82f34a2d23dcb5eb0b20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491893"
---
# <span data-ttu-id="8f61a-101">Set-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="8f61a-101">Set-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="8f61a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8f61a-102">SYNOPSIS</span></span>
<span data-ttu-id="8f61a-103">A címkék beállítása meglévő PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="8f61a-103">Sets the Tags for an existing PublicIpPrefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f61a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8f61a-104">SYNTAX</span></span>

```
Set-AzureRmPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f61a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8f61a-105">DESCRIPTION</span></span>
<span data-ttu-id="8f61a-106">A **set-AzureRmPublicIpPrefix** parancsmag a nyilvános IP-előtag címkéit állítja be.</span><span class="sxs-lookup"><span data-stu-id="8f61a-106">The **Set-AzureRmPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="8f61a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8f61a-107">EXAMPLES</span></span>

### <span data-ttu-id="8f61a-108">Adja meg a nyilvános IP-előtag címkéit</span><span class="sxs-lookup"><span data-stu-id="8f61a-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzureRmPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="8f61a-109">Az első parancs a meglévő nyilvános IP-előtagot kapja, a második parancs beállítja a címkék tulajdonságot, a harmadik parancs pedig frissíti a meglévő objektumot.</span><span class="sxs-lookup"><span data-stu-id="8f61a-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="8f61a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8f61a-110">PARAMETERS</span></span>

### <span data-ttu-id="8f61a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f61a-111">-AsJob</span></span>
<span data-ttu-id="8f61a-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8f61a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8f61a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f61a-113">-DefaultProfile</span></span>
<span data-ttu-id="8f61a-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f61a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f61a-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="8f61a-115">-PublicIpPrefix</span></span>
<span data-ttu-id="8f61a-116">A PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="8f61a-116">The PublicIpPrefix</span></span>

```yaml
Type: PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f61a-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8f61a-117">-Confirm</span></span>
<span data-ttu-id="8f61a-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8f61a-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f61a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f61a-119">-WhatIf</span></span>
<span data-ttu-id="8f61a-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8f61a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f61a-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8f61a-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f61a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f61a-122">CommonParameters</span></span>
<span data-ttu-id="8f61a-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8f61a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8f61a-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f61a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f61a-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f61a-125">INPUTS</span></span>

### <span data-ttu-id="8f61a-126">Microsoft. Azure. commands. Network. models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="8f61a-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="8f61a-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f61a-127">OUTPUTS</span></span>

### <span data-ttu-id="8f61a-128">Microsoft. Azure. commands. Network. models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="8f61a-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="8f61a-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8f61a-129">NOTES</span></span>

## <span data-ttu-id="8f61a-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f61a-130">RELATED LINKS</span></span>
