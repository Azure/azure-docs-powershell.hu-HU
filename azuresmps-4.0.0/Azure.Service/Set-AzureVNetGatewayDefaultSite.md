---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A34A2B01-A658-410E-8B68-98A6427DFC33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 345d9048ea729b6fe954d2da5e01310be42c79ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016413"
---
# <span data-ttu-id="1870a-101">Set-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="1870a-101">Set-AzureVNetGatewayDefaultSite</span></span>

## <span data-ttu-id="1870a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1870a-102">SYNOPSIS</span></span>
<span data-ttu-id="1870a-103">A kényszerített bújtatási forgalom alapértelmezett webhelyének beállítása.</span><span class="sxs-lookup"><span data-stu-id="1870a-103">Sets the default site for forced tunneling traffic.</span></span>

## <span data-ttu-id="1870a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1870a-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayDefaultSite -VNetName <String> -DefaultSite <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="1870a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1870a-105">DESCRIPTION</span></span>
<span data-ttu-id="1870a-106">A **set-AzureVNetGatewayDefaultSite** parancsmag az alapértelmezett útvonalat állítja be a helyszíni webhelyre a kényszerített bújtatási forgalom eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="1870a-106">The **Set-AzureVNetGatewayDefaultSite** cmdlet sets the default route to the on-premises site for forced tunneling traffic.</span></span>
<span data-ttu-id="1870a-107">Ez a parancs a virtuális hálózatokra vonatkozóan egy Azure virtuális magánhálózati (VPN-) átjáró útvonalát állítja be.</span><span class="sxs-lookup"><span data-stu-id="1870a-107">This command sets the route on an Azure virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="1870a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="1870a-108">EXAMPLES</span></span>

## <span data-ttu-id="1870a-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1870a-109">PARAMETERS</span></span>

### <span data-ttu-id="1870a-110">-DefaultSite</span><span class="sxs-lookup"><span data-stu-id="1870a-110">-DefaultSite</span></span>
<span data-ttu-id="1870a-111">A helyszíni helyi hálózat webhelyének nevét adja meg a kényszeres bújtatási forgalomhoz.</span><span class="sxs-lookup"><span data-stu-id="1870a-111">Specifies the name of the on-premises local network site for forced tunneling traffic.</span></span>

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

### <span data-ttu-id="1870a-112">-Profil</span><span class="sxs-lookup"><span data-stu-id="1870a-112">-Profile</span></span>
<span data-ttu-id="1870a-113">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="1870a-113">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1870a-114">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="1870a-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1870a-115">-VNetName</span><span class="sxs-lookup"><span data-stu-id="1870a-115">-VNetName</span></span>
<span data-ttu-id="1870a-116">Virtuális hálózatot ad meg.</span><span class="sxs-lookup"><span data-stu-id="1870a-116">Specifies a virtual network.</span></span>
<span data-ttu-id="1870a-117">Ez a parancsmag a VPN-átjáró alapértelmezett útvonalát állítja be a virtuális hálózat számára, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="1870a-117">This cmdlet sets the default route of the VPN gateway for forced tunneling traffic for the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="1870a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1870a-118">CommonParameters</span></span>
<span data-ttu-id="1870a-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1870a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1870a-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1870a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1870a-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1870a-121">INPUTS</span></span>

## <span data-ttu-id="1870a-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1870a-122">OUTPUTS</span></span>

## <span data-ttu-id="1870a-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1870a-123">NOTES</span></span>

## <span data-ttu-id="1870a-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1870a-124">RELATED LINKS</span></span>

[<span data-ttu-id="1870a-125">Remove-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="1870a-125">Remove-AzureVNetGatewayDefaultSite</span></span>](./Remove-AzureVNetGatewayDefaultSite.md)
