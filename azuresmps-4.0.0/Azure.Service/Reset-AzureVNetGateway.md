---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: B4102F33-979B-4649-99F4-96A295EAE43C
online version: ''
schema: 2.0.0
ms.openlocfilehash: ddb0ac79f5164fb5c953dd1cf1efeff8391d30fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015465"
---
# <span data-ttu-id="4b2f9-101">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="4b2f9-101">Reset-AzureVNetGateway</span></span>

## <span data-ttu-id="4b2f9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4b2f9-102">SYNOPSIS</span></span>
<span data-ttu-id="4b2f9-103">Virtuális hálózat VPN-átjárójának alaphelyzetbe állítása.</span><span class="sxs-lookup"><span data-stu-id="4b2f9-103">Resets a virtual network VPN gateway.</span></span>

## <span data-ttu-id="4b2f9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4b2f9-104">SYNTAX</span></span>

```
Reset-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4b2f9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4b2f9-105">DESCRIPTION</span></span>
<span data-ttu-id="4b2f9-106">A **reset-AzureVNetGateway** parancsmag visszaállítja a virtuális MAGÁNHÁLÓZAT (VPN) virtuális hálózati átjáróját, és újraindul.</span><span class="sxs-lookup"><span data-stu-id="4b2f9-106">The **Reset-AzureVNetGateway** cmdlet resets and restarts a virtual private network (VPN) virtual network gateway.</span></span>

## <span data-ttu-id="4b2f9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4b2f9-107">EXAMPLES</span></span>

### <span data-ttu-id="4b2f9-108">1. példa: virtuális hálózati átjáró alaphelyzetbe állítása</span><span class="sxs-lookup"><span data-stu-id="4b2f9-108">Example 1: Reset a virtual network gateway</span></span>
```
PS C:\> Reset-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="4b2f9-109">Ez a parancs visszaállítja a virtuális hálózati átjárót a ContosoVN07 nevű virtuális hálózatból.</span><span class="sxs-lookup"><span data-stu-id="4b2f9-109">This command resets the virtual network gateway from the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="4b2f9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4b2f9-110">PARAMETERS</span></span>

### <span data-ttu-id="4b2f9-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="4b2f9-111">-Profile</span></span>
<span data-ttu-id="4b2f9-112">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="4b2f9-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="4b2f9-113">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="4b2f9-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4b2f9-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="4b2f9-114">-VNetName</span></span>
<span data-ttu-id="4b2f9-115">Annak a virtuális hálózatnak a virtuális hálózata, amely az adott parancsmag alaphelyzetbe állítását tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4b2f9-115">Specifies the virtual network that contains the virtual network gateway that this cmdlet resets.</span></span>

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

### <span data-ttu-id="4b2f9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b2f9-116">CommonParameters</span></span>
<span data-ttu-id="4b2f9-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4b2f9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b2f9-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b2f9-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b2f9-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b2f9-119">INPUTS</span></span>

## <span data-ttu-id="4b2f9-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b2f9-120">OUTPUTS</span></span>

## <span data-ttu-id="4b2f9-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4b2f9-121">NOTES</span></span>

## <span data-ttu-id="4b2f9-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4b2f9-122">RELATED LINKS</span></span>

[<span data-ttu-id="4b2f9-123">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="4b2f9-123">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="4b2f9-124">Új – AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="4b2f9-124">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="4b2f9-125">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="4b2f9-125">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="4b2f9-126">Átméretezés-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="4b2f9-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="4b2f9-127">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="4b2f9-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


