---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 67260128-D57B-4587-BB61-2475703ABA66
online version: ''
schema: 2.0.0
ms.openlocfilehash: 38aca36799c57dd5a135af99e4b99ab713d2b1ca
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015489"
---
# <span data-ttu-id="86a11-101">Remove-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="86a11-101">Remove-AzureVNetGatewayDefaultSite</span></span>

## <span data-ttu-id="86a11-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86a11-102">SYNOPSIS</span></span>
<span data-ttu-id="86a11-103">Eltávolítja az alapértelmezett útvonalat a kényszerített bújtatási forgalomhoz.</span><span class="sxs-lookup"><span data-stu-id="86a11-103">Removes the default route for forced tunneling traffic.</span></span>

## <span data-ttu-id="86a11-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86a11-104">SYNTAX</span></span>

```
Remove-AzureVNetGatewayDefaultSite -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="86a11-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="86a11-105">DESCRIPTION</span></span>
<span data-ttu-id="86a11-106">A **Remove-AzureVNetGatewayDefaultSite** parancsmag eltávolítja az alapértelmezett útvonalat a helyszíni webhelyre a kényszerített bújtatási forgalomhoz.</span><span class="sxs-lookup"><span data-stu-id="86a11-106">The **Remove-AzureVNetGatewayDefaultSite** cmdlet removes the default route to the on-premises site for forced tunneling traffic.</span></span>
<span data-ttu-id="86a11-107">Ez a parancsmag eltávolítja egy virtuális hálózat Azure virtuális magánhálózati (VPN) átjárójának útvonalát.</span><span class="sxs-lookup"><span data-stu-id="86a11-107">This cmdlet removes the route from an Azure virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="86a11-108">Példák</span><span class="sxs-lookup"><span data-stu-id="86a11-108">EXAMPLES</span></span>

### <span data-ttu-id="86a11-109">1. példa: az útvonal eltávolítása az alapértelmezett webhelyre</span><span class="sxs-lookup"><span data-stu-id="86a11-109">Example 1: Remove a route to the default site</span></span>
```
PS C:\> Remove-AzureVNetGatewayDefaultSite -VnetName "ContosoVNet01"
```

<span data-ttu-id="86a11-110">Ez a parancs eltávolítja az alapértelmezett webhelynek az ContosoVNet01 nevű virtuális hálózat virtuális magánhálózaton található útvonalát.</span><span class="sxs-lookup"><span data-stu-id="86a11-110">This command removes the route to the default site from the VPN of the virtual network named ContosoVNet01.</span></span>

## <span data-ttu-id="86a11-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86a11-111">PARAMETERS</span></span>

### <span data-ttu-id="86a11-112">-Profil</span><span class="sxs-lookup"><span data-stu-id="86a11-112">-Profile</span></span>
<span data-ttu-id="86a11-113">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="86a11-113">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="86a11-114">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="86a11-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="86a11-115">-VNetName</span><span class="sxs-lookup"><span data-stu-id="86a11-115">-VNetName</span></span>
<span data-ttu-id="86a11-116">Virtuális hálózatot ad meg.</span><span class="sxs-lookup"><span data-stu-id="86a11-116">Specifies a virtual network.</span></span>
<span data-ttu-id="86a11-117">Ez a parancsmag eltávolítja a virtuális hálózat VPN-átjárójának alapértelmezett útvonalát, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="86a11-117">This cmdlet removes the default route from the VPN gateway for the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="86a11-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86a11-118">CommonParameters</span></span>
<span data-ttu-id="86a11-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86a11-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86a11-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86a11-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86a11-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86a11-121">INPUTS</span></span>

## <span data-ttu-id="86a11-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86a11-122">OUTPUTS</span></span>

## <span data-ttu-id="86a11-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86a11-123">NOTES</span></span>

## <span data-ttu-id="86a11-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86a11-124">RELATED LINKS</span></span>

[<span data-ttu-id="86a11-125">Set-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="86a11-125">Set-AzureVNetGatewayDefaultSite</span></span>](./Set-AzureVNetGatewayDefaultSite.md)
