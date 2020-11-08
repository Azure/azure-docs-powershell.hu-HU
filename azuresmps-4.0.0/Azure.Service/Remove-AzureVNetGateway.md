---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 3E6EF9B8-9709-4E59-A1E5-78CDA4EAAE1B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88dcd2f4bad149396d58948d3d656defdf055104
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015490"
---
# <span data-ttu-id="99bb0-101">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="99bb0-101">Remove-AzureVNetGateway</span></span>

## <span data-ttu-id="99bb0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99bb0-102">SYNOPSIS</span></span>
<span data-ttu-id="99bb0-103">VPN-átjáró törlése</span><span class="sxs-lookup"><span data-stu-id="99bb0-103">Deletes a VPN gateway.</span></span>

## <span data-ttu-id="99bb0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99bb0-104">SYNTAX</span></span>

```
Remove-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="99bb0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="99bb0-105">DESCRIPTION</span></span>
<span data-ttu-id="99bb0-106">A **Remove-AzureVNetGateway** parancsmag egy meglévő virtuális MAGÁNHÁLÓZATI (VPN-) átjárót töröl egy virtuális hálózathoz.</span><span class="sxs-lookup"><span data-stu-id="99bb0-106">The **Remove-AzureVNetGateway** cmdlet deletes an existing virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="99bb0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="99bb0-107">EXAMPLES</span></span>

### <span data-ttu-id="99bb0-108">1. példa: virtuális hálózati átjáró eltávolítása</span><span class="sxs-lookup"><span data-stu-id="99bb0-108">Example 1: Remove a virtual network gateway</span></span>
```
PS C:\> Remove-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="99bb0-109">Ez a parancs eltávolítja a virtuális hálózati átjárót a ContosoVN07 nevű virtuális hálózatból.</span><span class="sxs-lookup"><span data-stu-id="99bb0-109">This command removes the virtual network gateway from the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="99bb0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99bb0-110">PARAMETERS</span></span>

### <span data-ttu-id="99bb0-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="99bb0-111">-Profile</span></span>
<span data-ttu-id="99bb0-112">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="99bb0-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="99bb0-113">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="99bb0-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="99bb0-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="99bb0-114">-VNetName</span></span>
<span data-ttu-id="99bb0-115">Annak a virtuális hálózatnak a meghatározása, amelyben ez a parancsmag törli a VPN-átjárót.</span><span class="sxs-lookup"><span data-stu-id="99bb0-115">Specifies the virtual network in which this cmdlet deletes the VPN gateway.</span></span>

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

### <span data-ttu-id="99bb0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99bb0-116">CommonParameters</span></span>
<span data-ttu-id="99bb0-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99bb0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99bb0-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99bb0-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99bb0-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99bb0-119">INPUTS</span></span>

## <span data-ttu-id="99bb0-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99bb0-120">OUTPUTS</span></span>

## <span data-ttu-id="99bb0-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99bb0-121">NOTES</span></span>

## <span data-ttu-id="99bb0-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99bb0-122">RELATED LINKS</span></span>

[<span data-ttu-id="99bb0-123">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="99bb0-123">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="99bb0-124">Új – AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="99bb0-124">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="99bb0-125">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="99bb0-125">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="99bb0-126">Átméretezés-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="99bb0-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="99bb0-127">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="99bb0-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


