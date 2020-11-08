---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 4cb7d3a48d1783e834b9ecdd53d86969b4e1e6cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184323"
---
# <span data-ttu-id="24021-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="24021-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="24021-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24021-102">SYNOPSIS</span></span>
<span data-ttu-id="24021-103">Nyilvános IP-cím frissítése</span><span class="sxs-lookup"><span data-stu-id="24021-103">Updates a public IP address.</span></span>

## <span data-ttu-id="24021-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24021-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24021-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="24021-105">DESCRIPTION</span></span>
<span data-ttu-id="24021-106">A **set-AzPublicIpAddress** parancsmag nyilvános IP-címet frissít.</span><span class="sxs-lookup"><span data-stu-id="24021-106">The **Set-AzPublicIpAddress** cmdlet updates a public IP address.</span></span>

## <span data-ttu-id="24021-107">Példák</span><span class="sxs-lookup"><span data-stu-id="24021-107">EXAMPLES</span></span>

### <span data-ttu-id="24021-108">1: nyilvános IP-cím kiosztási módjának módosítása</span><span class="sxs-lookup"><span data-stu-id="24021-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="24021-109">Az első parancs a nyilvános IP-cím erőforrást kapja a név $publicIPName az erőforráscsoport $rgName.</span><span class="sxs-lookup"><span data-stu-id="24021-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="24021-110">A második parancs a nyilvános IP-cím objektum kiosztási módját a "statikus" értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="24021-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="24021-111">Set-AzPublicIPAddress parancs frissíti a nyilvános IP-cím erőforrást a frissített objektummal, és a hozzárendelési módszert "Static" értékre módosítja.</span><span class="sxs-lookup"><span data-stu-id="24021-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="24021-112">A nyilvános IP-címet azonnal kiosztja A rendszer.</span><span class="sxs-lookup"><span data-stu-id="24021-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="24021-113">2: DNS-tartomány hozzáadása nyilvános IP-címről</span><span class="sxs-lookup"><span data-stu-id="24021-113">2: Add DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="24021-114">Az első parancs a nyilvános IP-cím erőforrást kapja a név $publicIPName az erőforráscsoport $rgName.</span><span class="sxs-lookup"><span data-stu-id="24021-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="24021-115">A második parancs a DomainNameLabel tulajdonságot a szükséges DNS-előtagra állítja be.</span><span class="sxs-lookup"><span data-stu-id="24021-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="24021-116">Set-AzPublicIPAddress parancs frissíti a nyilvános IP-cím erőforrást a frissített objektummal.</span><span class="sxs-lookup"><span data-stu-id="24021-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="24021-117">A DomainNameLabel & FQDN a várt módon módosul.</span><span class="sxs-lookup"><span data-stu-id="24021-117">DomainNameLabel & Fqdn are modified as expected.</span></span>
    
### <span data-ttu-id="24021-118">3: nyilvános IP-cím DNS-tartományának módosítása</span><span class="sxs-lookup"><span data-stu-id="24021-118">3: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="24021-119">Az első parancs a nyilvános IP-cím erőforrást kapja a név $publicIPName az erőforráscsoport $rgName.</span><span class="sxs-lookup"><span data-stu-id="24021-119">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="24021-120">A második parancs a DomainNameLabel tulajdonságot a szükséges DNS-előtagra állítja be.</span><span class="sxs-lookup"><span data-stu-id="24021-120">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="24021-121">Set-AzPublicIPAddress parancs frissíti a nyilvános IP-cím erőforrást a frissített objektummal.</span><span class="sxs-lookup"><span data-stu-id="24021-121">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="24021-122">A DomainNameLabel & FQDN a várt módon módosul.</span><span class="sxs-lookup"><span data-stu-id="24021-122">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="24021-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24021-123">PARAMETERS</span></span>

### <span data-ttu-id="24021-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24021-124">-AsJob</span></span>
<span data-ttu-id="24021-125">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="24021-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24021-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24021-126">-DefaultProfile</span></span>
<span data-ttu-id="24021-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="24021-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24021-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="24021-128">-PublicIpAddress</span></span>
<span data-ttu-id="24021-129">Itt adhatja meg azt a nyilvános IP-címet, amely a nyilvános IP-címet megadó államot jelöli.</span><span class="sxs-lookup"><span data-stu-id="24021-129">Specifies a public IP address object representing the state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="24021-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24021-130">CommonParameters</span></span>
<span data-ttu-id="24021-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24021-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24021-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24021-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24021-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24021-133">INPUTS</span></span>

### <span data-ttu-id="24021-134">Microsoft. Azure. commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="24021-134">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="24021-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24021-135">OUTPUTS</span></span>

### <span data-ttu-id="24021-136">Microsoft. Azure. commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="24021-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="24021-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24021-137">NOTES</span></span>

## <span data-ttu-id="24021-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24021-138">RELATED LINKS</span></span>

[<span data-ttu-id="24021-139">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="24021-139">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="24021-140">Új – AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="24021-140">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="24021-141">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="24021-141">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


