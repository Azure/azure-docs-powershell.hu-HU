---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
ms.openlocfilehash: 4244f8c97090009272933d73a64323e4af5dfbbf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194517"
---
# <span data-ttu-id="3c4ce-101">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3c4ce-101">Set-AzPublicIpPrefix</span></span>

## <span data-ttu-id="3c4ce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3c4ce-102">SYNOPSIS</span></span>
<span data-ttu-id="3c4ce-103">A címkék beállítása meglévő PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3c4ce-103">Sets the Tags for an existing PublicIpPrefix</span></span>

## <span data-ttu-id="3c4ce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3c4ce-104">SYNTAX</span></span>

```
Set-AzPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c4ce-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3c4ce-105">DESCRIPTION</span></span>
<span data-ttu-id="3c4ce-106">A **set-AzPublicIpPrefix** parancsmag a nyilvános IP-előtag címkéit állítja be.</span><span class="sxs-lookup"><span data-stu-id="3c4ce-106">The **Set-AzPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="3c4ce-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3c4ce-107">EXAMPLES</span></span>

### <span data-ttu-id="3c4ce-108">Adja meg a nyilvános IP-előtag címkéit</span><span class="sxs-lookup"><span data-stu-id="3c4ce-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="3c4ce-109">Az első parancs a meglévő nyilvános IP-előtagot kapja, a második parancs beállítja a címkék tulajdonságot, a harmadik parancs pedig frissíti a meglévő objektumot.</span><span class="sxs-lookup"><span data-stu-id="3c4ce-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="3c4ce-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3c4ce-110">PARAMETERS</span></span>

### <span data-ttu-id="3c4ce-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c4ce-111">-AsJob</span></span>
<span data-ttu-id="3c4ce-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3c4ce-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c4ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c4ce-113">-DefaultProfile</span></span>
<span data-ttu-id="3c4ce-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3c4ce-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c4ce-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3c4ce-115">-PublicIpPrefix</span></span>
<span data-ttu-id="3c4ce-116">A PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3c4ce-116">The PublicIpPrefix</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c4ce-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3c4ce-117">-Confirm</span></span>
<span data-ttu-id="3c4ce-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3c4ce-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c4ce-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c4ce-119">-WhatIf</span></span>
<span data-ttu-id="3c4ce-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3c4ce-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c4ce-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3c4ce-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c4ce-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c4ce-122">CommonParameters</span></span>
<span data-ttu-id="3c4ce-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3c4ce-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c4ce-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c4ce-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c4ce-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c4ce-125">INPUTS</span></span>

### <span data-ttu-id="3c4ce-126">Microsoft. Azure. commands. Network. models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3c4ce-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="3c4ce-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c4ce-127">OUTPUTS</span></span>

### <span data-ttu-id="3c4ce-128">Microsoft. Azure. commands. Network. models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3c4ce-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="3c4ce-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3c4ce-129">NOTES</span></span>

## <span data-ttu-id="3c4ce-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c4ce-130">RELATED LINKS</span></span>

[<span data-ttu-id="3c4ce-131">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3c4ce-131">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="3c4ce-132">Új – AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3c4ce-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="3c4ce-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3c4ce-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)