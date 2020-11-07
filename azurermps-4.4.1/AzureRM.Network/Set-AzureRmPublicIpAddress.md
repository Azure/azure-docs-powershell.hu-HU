---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
ms.openlocfilehash: 1460b4497909d56e2d10d03e33df71518c52b796
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672430"
---
# <span data-ttu-id="d9c8b-101">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d9c8b-101">Set-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="d9c8b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d9c8b-102">SYNOPSIS</span></span>
<span data-ttu-id="d9c8b-103">Egy nyilvános IP-cím cél állapotának beállítása.</span><span class="sxs-lookup"><span data-stu-id="d9c8b-103">Sets the goal state for a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9c8b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d9c8b-104">SYNTAX</span></span>

```
Set-AzureRmPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9c8b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d9c8b-105">DESCRIPTION</span></span>
<span data-ttu-id="d9c8b-106">A **set-AzureRmPublicIpAddress** parancsmag a nyilvános IP-cím cél állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="d9c8b-106">The **Set-AzureRmPublicIpAddress** cmdlet sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="d9c8b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d9c8b-107">EXAMPLES</span></span>

### <span data-ttu-id="d9c8b-108">1: nyilvános IP-cím kiosztási módjának módosítása</span><span class="sxs-lookup"><span data-stu-id="d9c8b-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="d9c8b-109">Az első parancs a nyilvános IP-cím erőforrást kapja a név $publicIPName az erőforráscsoport $rgName.</span><span class="sxs-lookup"><span data-stu-id="d9c8b-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="d9c8b-110">A második parancs a nyilvános IP-cím objektum kiosztási módját a "statikus" értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="d9c8b-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="d9c8b-111">Set-AzureRmPublicIPAddress parancs frissíti a nyilvános IP-cím erőforrást a frissített objektummal, és a hozzárendelési módszert "Static" értékre módosítja.</span><span class="sxs-lookup"><span data-stu-id="d9c8b-111">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="d9c8b-112">A nyilvános IP-címet azonnal kiosztja A rendszer.</span><span class="sxs-lookup"><span data-stu-id="d9c8b-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="d9c8b-113">2: nyilvános IP-cím DNS-tartománynevének módosítása</span><span class="sxs-lookup"><span data-stu-id="d9c8b-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="d9c8b-114">Az első parancs a nyilvános IP-cím erőforrást kapja a név $publicIPName az erőforráscsoport $rgName.</span><span class="sxs-lookup"><span data-stu-id="d9c8b-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="d9c8b-115">A második parancs a DomainNameLabel tulajdonságot a szükséges DNS-előtagra állítja be.</span><span class="sxs-lookup"><span data-stu-id="d9c8b-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="d9c8b-116">Set-AzureRmPublicIPAddress parancs frissíti a nyilvános IP-cím erőforrást a frissített objektummal.</span><span class="sxs-lookup"><span data-stu-id="d9c8b-116">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="d9c8b-117">A DomainNameLabel & FQDN a várt módon módosul.</span><span class="sxs-lookup"><span data-stu-id="d9c8b-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="d9c8b-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d9c8b-118">PARAMETERS</span></span>

### <span data-ttu-id="d9c8b-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d9c8b-119">-PublicIpAddress</span></span>
<span data-ttu-id="d9c8b-120">Itt adhatja meg azt a **PublicIpAddress** -objektumot, amely a nyilvános IP-címet megadó cél állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9c8b-120">Specifies a **PublicIpAddress** object that represents the goal state to which the public IP address should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9c8b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9c8b-121">-DefaultProfile</span></span>
<span data-ttu-id="d9c8b-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d9c8b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9c8b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9c8b-123">CommonParameters</span></span>
<span data-ttu-id="d9c8b-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d9c8b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9c8b-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9c8b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9c8b-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9c8b-126">INPUTS</span></span>

### <span data-ttu-id="d9c8b-127">PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d9c8b-127">PSPublicIpAddress</span></span>
<span data-ttu-id="d9c8b-128">A ' PublicIpAddress ' paraméter az "PSPublicIpAddress" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="d9c8b-128">Parameter 'PublicIpAddress' accepts value of type 'PSPublicIpAddress' from the pipeline</span></span>

## <span data-ttu-id="d9c8b-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9c8b-129">OUTPUTS</span></span>

### <span data-ttu-id="d9c8b-130">Microsoft. Azure. commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d9c8b-130">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="d9c8b-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d9c8b-131">NOTES</span></span>

## <span data-ttu-id="d9c8b-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d9c8b-132">RELATED LINKS</span></span>

[<span data-ttu-id="d9c8b-133">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d9c8b-133">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="d9c8b-134">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d9c8b-134">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="d9c8b-135">Új – AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d9c8b-135">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="d9c8b-136">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d9c8b-136">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)


