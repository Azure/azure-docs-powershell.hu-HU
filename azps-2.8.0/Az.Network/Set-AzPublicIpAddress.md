---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: cc2ef6f016047bd20beba1671129a15c3dfa06f6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838330"
---
# <span data-ttu-id="8995a-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8995a-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="8995a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8995a-102">SYNOPSIS</span></span>
<span data-ttu-id="8995a-103">Nyilvános IP-cím frissítése</span><span class="sxs-lookup"><span data-stu-id="8995a-103">Updates a public IP address.</span></span>

## <span data-ttu-id="8995a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8995a-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8995a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8995a-105">DESCRIPTION</span></span>
<span data-ttu-id="8995a-106">A **set-AzPublicIpAddress** parancsmag nyilvános IP-címet frissít.</span><span class="sxs-lookup"><span data-stu-id="8995a-106">The **Set-AzPublicIpAddress** cmdlet updates a public IP address.</span></span>

## <span data-ttu-id="8995a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8995a-107">EXAMPLES</span></span>

### <span data-ttu-id="8995a-108">1: nyilvános IP-cím kiosztási módjának módosítása</span><span class="sxs-lookup"><span data-stu-id="8995a-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="8995a-109">Az első parancs a nyilvános IP-cím erőforrást kapja a név $publicIPName az erőforráscsoport $rgName.</span><span class="sxs-lookup"><span data-stu-id="8995a-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="8995a-110">A második parancs a nyilvános IP-cím objektum kiosztási módját a "statikus" értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="8995a-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="8995a-111">Set-AzPublicIPAddress parancs frissíti a nyilvános IP-cím erőforrást a frissített objektummal, és a hozzárendelési módszert "Static" értékre módosítja.</span><span class="sxs-lookup"><span data-stu-id="8995a-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="8995a-112">A nyilvános IP-címet azonnal kiosztja A rendszer.</span><span class="sxs-lookup"><span data-stu-id="8995a-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="8995a-113">2: nyilvános IP-cím DNS-tartománynevének módosítása</span><span class="sxs-lookup"><span data-stu-id="8995a-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="8995a-114">Az első parancs a nyilvános IP-cím erőforrást kapja a név $publicIPName az erőforráscsoport $rgName.</span><span class="sxs-lookup"><span data-stu-id="8995a-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="8995a-115">A második parancs a DomainNameLabel tulajdonságot a szükséges DNS-előtagra állítja be.</span><span class="sxs-lookup"><span data-stu-id="8995a-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="8995a-116">Set-AzPublicIPAddress parancs frissíti a nyilvános IP-cím erőforrást a frissített objektummal.</span><span class="sxs-lookup"><span data-stu-id="8995a-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="8995a-117">A DomainNameLabel & FQDN a várt módon módosul.</span><span class="sxs-lookup"><span data-stu-id="8995a-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="8995a-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8995a-118">PARAMETERS</span></span>

### <span data-ttu-id="8995a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8995a-119">-AsJob</span></span>
<span data-ttu-id="8995a-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8995a-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8995a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8995a-121">-DefaultProfile</span></span>
<span data-ttu-id="8995a-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8995a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8995a-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8995a-123">-PublicIpAddress</span></span>
<span data-ttu-id="8995a-124">Itt adhatja meg azt a nyilvános IP-címet, amely a nyilvános IP-címet megadó államot jelöli.</span><span class="sxs-lookup"><span data-stu-id="8995a-124">Specifies a public IP address object representing the state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="8995a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8995a-125">CommonParameters</span></span>
<span data-ttu-id="8995a-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8995a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8995a-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8995a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8995a-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8995a-128">INPUTS</span></span>

### <span data-ttu-id="8995a-129">Microsoft. Azure. commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8995a-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="8995a-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8995a-130">OUTPUTS</span></span>

### <span data-ttu-id="8995a-131">Microsoft. Azure. commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8995a-131">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="8995a-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8995a-132">NOTES</span></span>

## <span data-ttu-id="8995a-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8995a-133">RELATED LINKS</span></span>

[<span data-ttu-id="8995a-134">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8995a-134">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="8995a-135">Új – AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8995a-135">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="8995a-136">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8995a-136">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


