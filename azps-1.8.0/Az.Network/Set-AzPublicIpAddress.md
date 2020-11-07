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
ms.locfileid: "93669981"
---
# <span data-ttu-id="fdb5c-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fdb5c-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="fdb5c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fdb5c-102">SYNOPSIS</span></span>
<span data-ttu-id="fdb5c-103">Nyilvános IP-cím frissítése</span><span class="sxs-lookup"><span data-stu-id="fdb5c-103">Updates a public IP address.</span></span>

## <span data-ttu-id="fdb5c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fdb5c-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fdb5c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fdb5c-105">DESCRIPTION</span></span>
<span data-ttu-id="fdb5c-106">A **set-AzPublicIpAddress** parancsmag nyilvános IP-címet frissít.</span><span class="sxs-lookup"><span data-stu-id="fdb5c-106">The **Set-AzPublicIpAddress** cmdlet updates a public IP address.</span></span>

## <span data-ttu-id="fdb5c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fdb5c-107">EXAMPLES</span></span>

### <span data-ttu-id="fdb5c-108">1: nyilvános IP-cím kiosztási módjának módosítása</span><span class="sxs-lookup"><span data-stu-id="fdb5c-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="fdb5c-109">Az első parancs a nyilvános IP-cím erőforrást kapja a név $publicIPName az erőforráscsoport $rgName.</span><span class="sxs-lookup"><span data-stu-id="fdb5c-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="fdb5c-110">A második parancs a nyilvános IP-cím objektum kiosztási módját a "statikus" értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="fdb5c-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="fdb5c-111">Set-AzPublicIPAddress parancs frissíti a nyilvános IP-cím erőforrást a frissített objektummal, és a hozzárendelési módszert "Static" értékre módosítja.</span><span class="sxs-lookup"><span data-stu-id="fdb5c-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="fdb5c-112">A nyilvános IP-címet azonnal kiosztja A rendszer.</span><span class="sxs-lookup"><span data-stu-id="fdb5c-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="fdb5c-113">2: nyilvános IP-cím DNS-tartománynevének módosítása</span><span class="sxs-lookup"><span data-stu-id="fdb5c-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="fdb5c-114">Az első parancs a nyilvános IP-cím erőforrást kapja a név $publicIPName az erőforráscsoport $rgName.</span><span class="sxs-lookup"><span data-stu-id="fdb5c-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="fdb5c-115">A második parancs a DomainNameLabel tulajdonságot a szükséges DNS-előtagra állítja be.</span><span class="sxs-lookup"><span data-stu-id="fdb5c-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="fdb5c-116">Set-AzPublicIPAddress parancs frissíti a nyilvános IP-cím erőforrást a frissített objektummal.</span><span class="sxs-lookup"><span data-stu-id="fdb5c-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="fdb5c-117">A DomainNameLabel & FQDN a várt módon módosul.</span><span class="sxs-lookup"><span data-stu-id="fdb5c-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="fdb5c-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fdb5c-118">PARAMETERS</span></span>

### <span data-ttu-id="fdb5c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fdb5c-119">-AsJob</span></span>
<span data-ttu-id="fdb5c-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fdb5c-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fdb5c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdb5c-121">-DefaultProfile</span></span>
<span data-ttu-id="fdb5c-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fdb5c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdb5c-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fdb5c-123">-PublicIpAddress</span></span>
<span data-ttu-id="fdb5c-124">Itt adhatja meg azt a nyilvános IP-címet, amely a nyilvános IP-címet megadó államot jelöli.</span><span class="sxs-lookup"><span data-stu-id="fdb5c-124">Specifies a public IP address object representing the state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="fdb5c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdb5c-125">CommonParameters</span></span>
<span data-ttu-id="fdb5c-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fdb5c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdb5c-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdb5c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdb5c-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdb5c-128">INPUTS</span></span>

### <span data-ttu-id="fdb5c-129">Microsoft. Azure. commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fdb5c-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="fdb5c-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdb5c-130">OUTPUTS</span></span>

### <span data-ttu-id="fdb5c-131">Microsoft. Azure. commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fdb5c-131">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="fdb5c-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fdb5c-132">NOTES</span></span>

## <span data-ttu-id="fdb5c-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fdb5c-133">RELATED LINKS</span></span>

[<span data-ttu-id="fdb5c-134">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fdb5c-134">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="fdb5c-135">Új – AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fdb5c-135">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="fdb5c-136">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fdb5c-136">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


