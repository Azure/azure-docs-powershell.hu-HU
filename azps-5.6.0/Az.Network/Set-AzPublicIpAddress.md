---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 33712b9813d6c23ed72097597d94a22bf7644992
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938561"
---
# <span data-ttu-id="f6b29-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f6b29-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="f6b29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6b29-102">SYNOPSIS</span></span>
<span data-ttu-id="f6b29-103">Nyilvános IP-cím frissítése.</span><span class="sxs-lookup"><span data-stu-id="f6b29-103">Updates a public IP address.</span></span>

## <span data-ttu-id="f6b29-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f6b29-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6b29-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f6b29-105">DESCRIPTION</span></span>
<span data-ttu-id="f6b29-106">A **Set-AzPublicIpAddress** parancsmag frissíti a nyilvános IP-címet.</span><span class="sxs-lookup"><span data-stu-id="f6b29-106">The **Set-AzPublicIpAddress** cmdlet updates a public IP address.</span></span>

## <span data-ttu-id="f6b29-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f6b29-107">EXAMPLES</span></span>

### <span data-ttu-id="f6b29-108">1: Nyilvános IP-cím kiosztási módszerének módosítása</span><span class="sxs-lookup"><span data-stu-id="f6b29-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="f6b29-109">Az első parancs a nyilvános IP-cím erőforrást kapja meg, $publicIPName az erőforráscsoportban $rgName.</span><span class="sxs-lookup"><span data-stu-id="f6b29-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="f6b29-110">A második parancs a nyilvános IP-címobjektum kiosztási módját "Statikusra" állítja.</span><span class="sxs-lookup"><span data-stu-id="f6b29-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="f6b29-111">Set-AzPublicIPAddress parancs frissíti a nyilvános IP-címforrást a frissített objektummal, és "Statikus" módra módosítja a terhelési módot.</span><span class="sxs-lookup"><span data-stu-id="f6b29-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="f6b29-112">A nyilvános IP-címeket a rendszer azonnal kiosztja.</span><span class="sxs-lookup"><span data-stu-id="f6b29-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="f6b29-113">2: NYILVÁNOS IP-cím DNS-tartománycímkéinek hozzáadása</span><span class="sxs-lookup"><span data-stu-id="f6b29-113">2: Add DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="f6b29-114">Az első parancs a nyilvános IP-cím erőforrást kapja meg, $publicIPName az erőforráscsoportban $rgName.</span><span class="sxs-lookup"><span data-stu-id="f6b29-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="f6b29-115">A második parancs a DomainNameLabel tulajdonságot a szükséges DNS-előtagra állítja.</span><span class="sxs-lookup"><span data-stu-id="f6b29-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="f6b29-116">Set-AzPublicIPAddress parancs frissíti a nyilvános IP-cím erőforrást a frissített objektummal.</span><span class="sxs-lookup"><span data-stu-id="f6b29-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="f6b29-117">A DomainNameLabel & Fqdn a várt módon módosul.</span><span class="sxs-lookup"><span data-stu-id="f6b29-117">DomainNameLabel & Fqdn are modified as expected.</span></span>
    
### <span data-ttu-id="f6b29-118">3: Nyilvános IP-cím DNS-tartománycímkéinek módosítása</span><span class="sxs-lookup"><span data-stu-id="f6b29-118">3: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="f6b29-119">Az első parancs a nyilvános IP-cím erőforrást kapja meg, $publicIPName az erőforráscsoportban $rgName.</span><span class="sxs-lookup"><span data-stu-id="f6b29-119">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="f6b29-120">A második parancs a DomainNameLabel tulajdonságot a szükséges DNS-előtagra állítja.</span><span class="sxs-lookup"><span data-stu-id="f6b29-120">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="f6b29-121">Set-AzPublicIPAddress parancs frissíti a nyilvános IP-cím erőforrást a frissített objektummal.</span><span class="sxs-lookup"><span data-stu-id="f6b29-121">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="f6b29-122">A DomainNameLabel & Fqdn a várt módon módosul.</span><span class="sxs-lookup"><span data-stu-id="f6b29-122">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="f6b29-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6b29-123">PARAMETERS</span></span>

### <span data-ttu-id="f6b29-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6b29-124">-AsJob</span></span>
<span data-ttu-id="f6b29-125">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f6b29-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f6b29-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6b29-126">-DefaultProfile</span></span>
<span data-ttu-id="f6b29-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6b29-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6b29-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f6b29-128">-PublicIpAddress</span></span>
<span data-ttu-id="f6b29-129">Egy olyan nyilvános IP-címobjektumot ad meg, amely azt az állapotot képviseli, amelyben a nyilvános IP-címet be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="f6b29-129">Specifies a public IP address object representing the state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="f6b29-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6b29-130">CommonParameters</span></span>
<span data-ttu-id="f6b29-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6b29-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6b29-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6b29-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6b29-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f6b29-133">INPUTS</span></span>

### <span data-ttu-id="f6b29-134">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f6b29-134">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="f6b29-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6b29-135">OUTPUTS</span></span>

### <span data-ttu-id="f6b29-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f6b29-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="f6b29-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f6b29-137">NOTES</span></span>

## <span data-ttu-id="f6b29-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6b29-138">RELATED LINKS</span></span>

[<span data-ttu-id="f6b29-139">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f6b29-139">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="f6b29-140">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f6b29-140">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="f6b29-141">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f6b29-141">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


