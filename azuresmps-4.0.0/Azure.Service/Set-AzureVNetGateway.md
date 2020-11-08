---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 70899AAC-BF64-4FFA-9DAF-92E859D0B271
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3b30172f947c1c8bf39a8be84039d9166d6ea290
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016414"
---
# <span data-ttu-id="0f4c5-101">Set-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="0f4c5-101">Set-AzureVNetGateway</span></span>

## <span data-ttu-id="0f4c5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f4c5-102">SYNOPSIS</span></span>
<span data-ttu-id="0f4c5-103">Engedélyezi vagy letiltja az Azure virtuális hálózat VPN-átjáróját.</span><span class="sxs-lookup"><span data-stu-id="0f4c5-103">Enables or disables a VPN gateway for an Azure virtual network.</span></span>

## <span data-ttu-id="0f4c5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f4c5-104">SYNTAX</span></span>

### <span data-ttu-id="0f4c5-105">Connect (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0f4c5-105">Connect (Default)</span></span>
```
Set-AzureVNetGateway [-Connect] -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="0f4c5-106">Leválasztása</span><span class="sxs-lookup"><span data-stu-id="0f4c5-106">Disconnect</span></span>
```
Set-AzureVNetGateway [-Disconnect] -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0f4c5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f4c5-107">DESCRIPTION</span></span>
<span data-ttu-id="0f4c5-108">A **set-AzureVNetGateway** parancsmag engedélyezi vagy letiltja a virtuális MAGÁNHÁLÓZATI (VPN) átjárót egy Azure virtuális hálózathoz.</span><span class="sxs-lookup"><span data-stu-id="0f4c5-108">The **Set-AzureVNetGateway** cmdlet enables or disables a virtual private network (VPN) gateway for an Azure virtual network.</span></span>
<span data-ttu-id="0f4c5-109">A virtuális hálózati átjáró a virtuális hálózathoz való csatlakozáshoz szükséges virtuális MAGÁNHÁLÓZATI végpont.</span><span class="sxs-lookup"><span data-stu-id="0f4c5-109">A virtual network gateway is a VPN endpoint for connecting to a virtual network.</span></span>
<span data-ttu-id="0f4c5-110">Adja meg a *Connect* vagy a *Disconnect* paramétert a VPN-kapcsolat engedélyezéséhez vagy letiltásához egy helyszíni helyi hálózati webhely és egy virtuális hálózat között.</span><span class="sxs-lookup"><span data-stu-id="0f4c5-110">Specify the *Connect* or *Disconnect* parameter to enable or disable the VPN connection between an on-premises local network site and a virtual network.</span></span>

## <span data-ttu-id="0f4c5-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0f4c5-111">EXAMPLES</span></span>

### <span data-ttu-id="0f4c5-112">1. példa: virtuális hálózati átjáró engedélyezése virtuális hálózatokhoz</span><span class="sxs-lookup"><span data-stu-id="0f4c5-112">Example 1: Enable a virtual network gateway for a virtual network</span></span>
```
PS C:\> Set-AzureVNetGateway -Connect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

<span data-ttu-id="0f4c5-113">Ez a parancs engedélyezi a virtuális hálózati átjárót a ContosoProdNet nevű Azure virtuális hálózat és a ContosoBranchOffice nevű helyi hálózati webhely VPN-eszköze között.</span><span class="sxs-lookup"><span data-stu-id="0f4c5-113">This command enables the virtual network gateway between the Azure virtual network named ContosoProdNet and the VPN device for the local network site named ContosoBranchOffice.</span></span>

### <span data-ttu-id="0f4c5-114">2. példa: virtuális hálózati átjáró letiltása virtuális hálózat esetén</span><span class="sxs-lookup"><span data-stu-id="0f4c5-114">Example 2: Disable a virtual network gateway for a virtual network</span></span>
```
PS C:\> Set-AzureVNetGateway -Disconnect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

<span data-ttu-id="0f4c5-115">Ez a parancs letiltja a virtuális hálózati átjárót a ContosoProdNet nevű Azure virtuális hálózat és a ContosoBranchOffice nevű helyi hálózati webhely VPN-eszköze között.</span><span class="sxs-lookup"><span data-stu-id="0f4c5-115">This command disables the virtual network gateway between the Azure virtual network named ContosoProdNet and the VPN device for the local network site named ContosoBranchOffice.</span></span>

## <span data-ttu-id="0f4c5-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f4c5-116">PARAMETERS</span></span>

### <span data-ttu-id="0f4c5-117">-Connect</span><span class="sxs-lookup"><span data-stu-id="0f4c5-117">-Connect</span></span>
<span data-ttu-id="0f4c5-118">Azt jelzi, hogy ez a parancsmag lehetővé teszi a virtuális hálózat és a helyi hálózati webhely közötti VPN-kapcsolat használatát.</span><span class="sxs-lookup"><span data-stu-id="0f4c5-118">Indicates that this cmdlet enables the VPN connection between a virtual network and a local network site.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Connect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f4c5-119">-Disconnect</span><span class="sxs-lookup"><span data-stu-id="0f4c5-119">-Disconnect</span></span>
<span data-ttu-id="0f4c5-120">Jelzi, hogy ez a parancsmag letiltja a virtuális hálózat és a helyi hálózati webhely közötti VPN-kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="0f4c5-120">Indicates that this cmdlet disables the VPN connection between a virtual network and a local network site.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disconnect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f4c5-121">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="0f4c5-121">-LocalNetworkSiteName</span></span>
<span data-ttu-id="0f4c5-122">Annak a helyszíni helyi hálózati webhelynek a neve, amelyhez ez a parancsmag engedélyezi vagy letiltja a VPN-kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="0f4c5-122">Specifies the name of the on-premises local network site for which this cmdlet enables or disables the VPN connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f4c5-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="0f4c5-123">-Profile</span></span>
<span data-ttu-id="0f4c5-124">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="0f4c5-124">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="0f4c5-125">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="0f4c5-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f4c5-126">-VNetName</span><span class="sxs-lookup"><span data-stu-id="0f4c5-126">-VNetName</span></span>
<span data-ttu-id="0f4c5-127">Annak a virtuális hálózatnak a megadása, amelyhez ez a parancsmag engedélyezi vagy letiltja a VPN-kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="0f4c5-127">Specifies the virtual network for which this cmdlet enables or disables the VPN connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f4c5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f4c5-128">CommonParameters</span></span>
<span data-ttu-id="0f4c5-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0f4c5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f4c5-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f4c5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f4c5-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f4c5-131">INPUTS</span></span>

## <span data-ttu-id="0f4c5-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f4c5-132">OUTPUTS</span></span>

## <span data-ttu-id="0f4c5-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f4c5-133">NOTES</span></span>

## <span data-ttu-id="0f4c5-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f4c5-134">RELATED LINKS</span></span>

[<span data-ttu-id="0f4c5-135">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="0f4c5-135">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="0f4c5-136">Új – AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="0f4c5-136">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="0f4c5-137">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="0f4c5-137">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="0f4c5-138">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="0f4c5-138">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="0f4c5-139">Átméretezés-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="0f4c5-139">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)


