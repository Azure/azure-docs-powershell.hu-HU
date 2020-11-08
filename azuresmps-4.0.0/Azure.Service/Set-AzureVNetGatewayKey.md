---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 1AB168AA-F466-4C7C-9AD7-0BC7AEEBC932
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8daca2a335f063264fb2e6734948cc1353946e8a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015810"
---
# <span data-ttu-id="84ba3-101">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="84ba3-101">Set-AzureVNetGatewayKey</span></span>

## <span data-ttu-id="84ba3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="84ba3-102">SYNOPSIS</span></span>
<span data-ttu-id="84ba3-103">Az Azure VPN-átjáró és egy helyi hálózati webhely közötti kapcsolathoz tartozó előmegosztott kulcs beállítása.</span><span class="sxs-lookup"><span data-stu-id="84ba3-103">Sets the pre-shared key for the connection between an Azure VPN gateway and a local network site.</span></span>

## <span data-ttu-id="84ba3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="84ba3-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayKey -VNetName <String> -LocalNetworkSiteName <String> -SharedKey <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="84ba3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="84ba3-105">DESCRIPTION</span></span>
<span data-ttu-id="84ba3-106">A **set-AzureVNetGatewayKey** parancsmag az Azure virtual private Network (VPN) átjáró és a helyszíni helyi hálózat webhelye közötti kapcsolat előmegosztott kulcsát állítja be.</span><span class="sxs-lookup"><span data-stu-id="84ba3-106">The **Set-AzureVNetGatewayKey** cmdlet sets the pre-shared key for the connection between an Azure virtual private network (VPN) gateway and an on-premises local network site.</span></span>
<span data-ttu-id="84ba3-107">A kulcsnak egyenlőnek kell lennie a helyi hálózati webhely átjáróján beállított kulccsal.</span><span class="sxs-lookup"><span data-stu-id="84ba3-107">The key must be equal to the key configured on the gateway of the local network site.</span></span>
<span data-ttu-id="84ba3-108">Ha a billentyűk nem egyeznek meg, a kapcsolat nem hozható létre.</span><span class="sxs-lookup"><span data-stu-id="84ba3-108">If the keys do not match, a connection cannot establish.</span></span>

## <span data-ttu-id="84ba3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="84ba3-109">EXAMPLES</span></span>

## <span data-ttu-id="84ba3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="84ba3-110">PARAMETERS</span></span>

### <span data-ttu-id="84ba3-111">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="84ba3-111">-LocalNetworkSiteName</span></span>
<span data-ttu-id="84ba3-112">Annak a helyi hálózati webhelynek a neve, amely a virtuális hálózati átjáróhoz csatlakozik.</span><span class="sxs-lookup"><span data-stu-id="84ba3-112">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

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

### <span data-ttu-id="84ba3-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="84ba3-113">-Profile</span></span>
<span data-ttu-id="84ba3-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="84ba3-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="84ba3-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="84ba3-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="84ba3-116">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="84ba3-116">-SharedKey</span></span>
<span data-ttu-id="84ba3-117">A VPN-átjáróhoz hozzárendelni kívánt megosztott kulcsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="84ba3-117">Specifies the shared key to assign to the VPN gateway.</span></span>
<span data-ttu-id="84ba3-118">Az értéknek a 128 karakternél nem hosszabb alfa-numerikus karakterláncnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="84ba3-118">The value must be an alpha-numerical string no longer than 128 characters.</span></span>

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

### <span data-ttu-id="84ba3-119">-VNetName</span><span class="sxs-lookup"><span data-stu-id="84ba3-119">-VNetName</span></span>
<span data-ttu-id="84ba3-120">Annak a virtuális hálózatnak a megadása, amelynek a parancsmagja a kapcsolat megosztott kulcsát állítja be.</span><span class="sxs-lookup"><span data-stu-id="84ba3-120">Specifies the virtual network for which this cmdlet sets the shared key for the connection.</span></span>

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

### <span data-ttu-id="84ba3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84ba3-121">CommonParameters</span></span>
<span data-ttu-id="84ba3-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="84ba3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84ba3-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84ba3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84ba3-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="84ba3-124">INPUTS</span></span>

## <span data-ttu-id="84ba3-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84ba3-125">OUTPUTS</span></span>

## <span data-ttu-id="84ba3-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="84ba3-126">NOTES</span></span>

## <span data-ttu-id="84ba3-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84ba3-127">RELATED LINKS</span></span>

[<span data-ttu-id="84ba3-128">Get-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="84ba3-128">Get-AzureVNetGatewayKey</span></span>](./Get-AzureVNetGatewayKey.md)


